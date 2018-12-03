# 对接CloudTable HBase<a name="dli_02_0137"></a>

## 准备工作<a name="section7668515315"></a>

准备API的配置如下：

```
// authorization api info
 private static String iamApiUrl = "https://{huawei_cloud_iam_domain}/v3/auth/tokens";
 private static String projectId = "your project id";
 private static String domainName = "your account";
 private static String passwd = "your password";

 // dli common info
 private static String dliApiUrl = "https://{dli_api_domain}/";
 private static String queueName = "queue_name";
 private static String dbName = "database_name";
 private static String dliTableName = "table_in_dli";

 // cloudtable info
 private static String clusterId = "your ct cluster id";
 private static String ctTableName = "table_in_ct";
```

## 操作步骤<a name="section087118111613"></a>

1.  从IAM获取Token。

    ```
    // create http client
    Client client = HttpsUtil.getClientWithoutAuth(HBaseExample.class);
    System.out.println("Getting token...");
    Response response = HttpsUtil.doPost(client, iamApiUrl, "", getIamEntity(), "Get token failed: ");
    String token = response.getHeaderString("x-subject-token");
    System.out.println("Get token: " + token);
    ```

2.  创建DLI表关联CloudTable HBase。

    ```
    private static String getCreateTableSql() {
      return
        "create table if not exists " + dliTableName + "(" +
        "  id string," +
        "  location string," +
        "  city string," +
        "  booleanf boolean," +
        "  shortf short," +
        "  intf int," +
        "  longf long," +
        "  floatf float," +
        "  doublef double)" +
        "using cloudtable options (" +
        "  \\\"ClusterId\\\"=\\\"" + clusterId + "\\\"," +
        "  \\\"TableName\\\"=\\\"" + ctTableName + "\\\"," +
        "  \\\"RowKey\\\"=\\\"id:5, location:6, city:7\\\"," +
        "  \\\"Cols\\\"=\\\"" +
        "    booleanf:CF1.booleanf," +
        "    shortf:CF1.shortf," +
        "    intf:CF1.intf," +
        "    longf:CF1.longf," +
        "    floatf:CF1.floatf," +
        "    doublef:CF1.doublef\\\"" +
        ");";
    }
    private static String getSubmitJobEntity(String sql) {
      String entity =
        "{" +
        "  \"currentdb\": \"" + dbName + "\"," +
        "  \"sql\": \"" + sql + "\"" +
        "}";
      JSONObject json = JSONObject.fromObject(entity);
      System.out.println("Get create table entity: " + json.toString());
      return json.toString();
    }
    String submitJobUrl = dliApiUrl + projectId + "/queues/" + queueName + "/jobs/submit-job";
    System.out.println("Creating table...");
    response = HttpsUtil.doPost(client, submitJobUrl, token, getSubmitJobEntity(getCreateTableSql()), "Create table failed: ");
    System.out.println("Create table success, msg: " + response.readEntity(String.class));
    ```

3.  在CloudTable HBase中插入数据。

    ```
    private static String getInsertSql() {
      return "insert into " + dliTableName + " values('huawei', 'abcdef', 'abcdefg', true, 1, 2, 3, 4, 5);";
    }
    System.out.println("Importing data...");
    response = HttpsUtil.doPost(client, submitJobUrl, token, getSubmitJobEntity(getInsertSql()), "Import data success, msg: ");
    System.out.println("Import data success, msg: " + response.readEntity(String.class));
    ```

4.  从CloudTable HBase中扫描数据。
    1.  提交扫描作业。

        ```
        private static String getScanSql() {
          return "select * from " + dliTableName + ";";
        }
        System.out.println("Submitting scan job...");
        response = HttpsUtil.doPost(client, submitJobUrl, token, getSubmitJobEntity(getScanSql()), "Submit scan job success, msg: ");
        System.out.println("Submit scan job success, msg: " + response.readEntity(String.class));
        ```

    2.  获取扫描结果。

        ```
        System.out.println("Getting scan result...");
        String jobId = getJobId(response);
        System.out.println("Get job id: " + jobId);
        String getJobResultUrl = dliApiUrl + projectId + "/jobs/" + jobId;
        response = HttpsUtil.doGet(client, getJobResultUrl, token, "Get scan result failed: ");
        System.out.println("Get scan result success, msg: " + response.readEntity(String.class));
        ```



## 完整代码<a name="section1492963121914"></a>

HBaseExample.Java

```
import javax.ws.rs.client.Client;
import javax.ws.rs.client.Entity;
import javax.ws.rs.core.MediaType;
import javax.ws.rs.core.Response;

import net.sf.json.JSONObject;

/**
 * Example for data source cloudtable-hbase in dli
 */
public class HBaseExample {

  // authorization api info
  private static String iamApiUrl = "https://{huawei_cloud_iam_domain}/v3/auth/tokens";
  private static String projectId = "your project id";
  private static String domainName = "your account";
  private static String passwd = "your password";

  // dli common info
  private static String dliApiUrl = "https://{dli_api_domain}/";
  private static String queueName = "queue_name";
  private static String dbName = "database_name";
  private static String dliTableName = "table_in_dli";

  // cloudtable info
  private static String clusterId = "your ct cluster id";
  private static String ctTableName = "table_in_ct";

  private static String getIamEntity() {
    String entity =
      "{" +
      "  \"auth\": {" +
      "    \"identity\": {" +
      "      \"password\": {" +
      "        \"user\": {" +
      "          \"password\": \"" + passwd + "\", " +
      "          \"domain\": {" +
      "            \"name\": \"" + domainName + "\"" +
      "          }, " +
      "          \"name\": \"" + domainName + "\"" +
      "        }" +
      "      }, " +
      "      \"methods\": [" +
      "        \"password\"" +
      "      ]" +
      "    }, " +
      "    \"scope\": {" +
      "      \"project\": {" +
      "        \"id\": \"" + projectId + "\"" +
      "      }" +
      "    }" +
      "  }" +
      "}";
    JSONObject json = JSONObject.fromObject(entity);
    System.out.println("Get iam entity: " + json.toString());
    return json.toString();
  }

  private static String getCreateTableSql() {
    return
      "create table if not exists " + dliTableName + "(" +
      "  id string," +
      "  location string," +
      "  city string," +
      "  booleanf boolean," +
      "  shortf short," +
      "  intf int," +
      "  longf long," +
      "  floatf float," +
      "  doublef double)" +
      "using cloudtable options (" +
      "  \\\"ClusterId\\\"=\\\"" + clusterId + "\\\"," +
      "  \\\"TableName\\\"=\\\"" + ctTableName + "\\\"," +
      "  \\\"RowKey\\\"=\\\"id:5, location:6, city:7\\\"," +
      "  \\\"Cols\\\"=\\\"" +
      "    booleanf:CF1.booleanf," +
      "    shortf:CF1.shortf," +
      "    intf:CF1.intf," +
      "    longf:CF1.longf," +
      "    floatf:CF1.floatf," +
      "    doublef:CF1.doublef\\\"" +
      ");";
  }

  private static String getInsertSql() {
    return "insert into " + dliTableName + " values('huawei', 'abcdef', 'abcdefg', true, 1, 2, 3, 4, 5);";
  }

  private static String getScanSql() {
    return "select * from " + dliTableName + ";";
  }

  private static String getSubmitJobEntity(String sql) {
    String entity =
      "{" +
      "  \"currentdb\": \"" + dbName + "\"," +
      "  \"sql\": \"" + sql + "\"" +
      "}";
    JSONObject json = JSONObject.fromObject(entity);
    System.out.println("Get create table entity: " + json.toString());
    return json.toString();
  }

  private static String getJobId(Response respose) {
    String json = respose.readEntity(String.class);
    JSONObject jsonObject = JSONObject.fromObject(json);
    return jsonObject.get("job_id").toString();
  }

  public static void main(String[] args) throws Exception {
    // create http client
    Client client = HttpsUtil.getClientWithoutAuth(HBaseExample.class);

    try {
      // 1. get token from iam
      System.out.println("Getting token...");
      Response response = HttpsUtil.doPost(
          client, iamApiUrl, "", getIamEntity(), "Get token failed: ");
      String token = response.getHeaderString("x-subject-token");
      System.out.println("Get token: " + token);

      // 2. create table relation to cloudtable hbase
      String submitJobUrl = dliApiUrl + projectId + "/queues/" + queueName + "/jobs/submit-job";
      System.out.println("Creating table...");
      response = HttpsUtil.doPost(
          client, submitJobUrl, token, getSubmitJobEntity(getCreateTableSql()), "Create table failed: ");
      System.out.println("Create table success, msg: " + response.readEntity(String.class));

      // 3. insert data into cloudtable hbase
      System.out.println("Importing data...");
      response = HttpsUtil.doPost(
          client, submitJobUrl, token, getSubmitJobEntity(getInsertSql()), "Import data success, msg: ");
      System.out.println("Import data success, msg: " + response.readEntity(String.class));

      // 4. scan data from cloudtable hbase
      // 4.1 submit scan job
      System.out.println("Submitting scan job...");
      response = HttpsUtil.doPost(
          client, submitJobUrl, token, getSubmitJobEntity(getScanSql()), "Submit scan job success, msg: ");
      System.out.println("Submit scan job success, msg: " + response.readEntity(String.class));

      // 4.2 get scan job result
      System.out.println("Getting scan result...");
      String jobId = getJobId(response);
      System.out.println("Get job id: " + jobId);
      String getJobResultUrl = dliApiUrl + projectId + "/jobs/" + jobId;
      response = HttpsUtil.doGet(client, getJobResultUrl, token, "Get scan result failed: ");
      System.out.println("Get scan result success, msg: " + response.readEntity(String.class));
    } finally {
      if (client != null) {
        client.close();
      }
    }
  }

}
```

>![](public_sys-resources/icon-note.gif) **说明：**   
>该样例代码中的结果计算为异步计算，因此，获取结果的方式需等待作业的状态为“finished”之后，才能查看到。  

HttpsUtil.Java

```
import org.glassfish.jersey.client.ClientConfig;

import javax.net.ssl.*;
import javax.ws.rs.client.Client;
import javax.ws.rs.client.ClientBuilder;
import javax.ws.rs.client.Entity;
import javax.ws.rs.core.MediaType;
import javax.ws.rs.core.Response;
import java.security.GeneralSecurityException;
import java.security.SecureRandom;
import java.security.cert.CertificateException;
import java.security.cert.X509Certificate;

/**
 * Http method
 */
public class HttpsUtil {
  /**
   * wrapper method for ssl request sending client without auth, like console access jobmanager
   */
  public static Client getClientWithoutAuth(Class<?> invokeClass) throws GeneralSecurityException {
    return getClientBuilderWithoutAuth().withConfig(new ClientConfig()).register(invokeClass).build();
  }

  private static ClientBuilder getClientBuilderWithoutAuth() throws GeneralSecurityException {
    TrustManager[] certs = new TrustManager[]{new X509TrustManager() {
      public X509Certificate[] getAcceptedIssuers() {
        return new X509Certificate[0];
      }

      public void checkServerTrusted(X509Certificate[] chain, String authType) throws CertificateException {
      }

      public void checkClientTrusted(X509Certificate[] chain, String authType) throws CertificateException {
      }
    }};

    SSLContext ctx = null;
    try {
      ctx = SSLContext.getInstance("TLSv1.2");
      ctx.init(null, certs, new SecureRandom());
    } catch (GeneralSecurityException e) {
      System.out.println("Failed to init the ssl context");
      throw new GeneralSecurityException(e);
    }

    HttpsURLConnection.setDefaultSSLSocketFactory(ctx.getSocketFactory());

    ClientBuilder clientBuilder = ClientBuilder.newBuilder();
    clientBuilder.sslContext(ctx);
    clientBuilder.hostnameVerifier(new HostnameVerifier() {

      public boolean verify(String hostname, SSLSession session) {
        return true;
      }
    });

    return clientBuilder;

  }

  public static Response doPost(
      Client client,
      String url,
      String token,
      String body,
      String errMsg) throws Exception {
    Response response = client
      .target(url)
      .request(MediaType.APPLICATION_JSON)
      .header("x-auth-token", token)
      .post(Entity.entity(body, MediaType.APPLICATION_JSON));
    response.bufferEntity();
    if (response.getStatus() / 10 != 20) {
      throw new Exception(errMsg + response.readEntity(String.class));
    }
    return response;
  }

  public static Response doGet(Client client, String url, String token, String errMsg) throws Exception {
    Response response = client
        .target(url)
        .request(MediaType.APPLICATION_JSON)
        .header("x-auth-token", token)
        .get();
    response.bufferEntity();
    if (response.getStatus() / 10 != 20) {
      throw new Exception(errMsg + response.readEntity(String.class));
    }
    return response;
  }
}
```

