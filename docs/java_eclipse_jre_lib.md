# Getting started

# Introduction
* ## Multi-use Flexible API for: 
  * **User**:
    * Login 
    * Registration
    * User Management
    * Profile Updates
    * Two Factor Authentication
     
  * **Verifcation**:
    * Identity Verification
    * Address Verifcation
    * Cell Phone Verification 

  * **Image**:
    * Manipulation
    * Compression
    * Moderation
     
  * **Data**:
    * Manipulation
    * Compression
    * Conversion
    * Sorting

  * **Services**:
    * Node Application Hosting
    * DNS Management
    * CDN (Content Delivery Network)

  * **Security**:
    * Encryption
    * Code Obfuscation
    * Platform Identification
    * WAF & DDOS Protection (Web Application Firewall)
      * Advanced Logging

# Overview

*  **API Domain: api.rest.sh, api.restful.sh**

This API supports both GET and POST API requests with a JSON or XML output.

*~ You can post to this API via a direct body response in JSON/XML, or using URL variables/requests.*

# Authentication
Be sure to include your User API KEY, and UID when sending a POST or GET request to our API.

*~ If domain restriction is enabled in your dashboard, please include your domain in the request and redirect headers for your API calls.*

# Status Codes
* ## Success Codes:
  *   **200**: Information Recieved
  *   **201**: Success, Resource Created, or Updated
  *   **202**: Proccessing

* ## Information Codes:
  *   **400**: Bad Request
  *   **401**: Incorrect Credentials
  *   **403**: Forbidden
  *   **406**: Not Acceptable Input
  *   **409**: Data Conflict
  *   **413**: Payload Too Large
  *   **415**: Un-Supported Content Type
  *   **451**: Un-Available For Legal Reasons

* ## Error Codes:
  *   **500**: Internal API Error
  *   **501**: Not Implemented
  *   **503**: API Unavailable
  *   **504**: Request Timeout
  *   **511**: Authentication Required

# Rate Pricing
* **Verification requests:** 
  * per/1000 Requests: **$50.00**

* **User requests:** 
  * per/1000 Requests: **$0.0072**

* **Image requests:** 
  * per/1000 Requests: **$11.87**

* Data requests: 
  * per/1MB: **$0.00024**

* **Service requests:** 
  * **DNS Pricing Per Month:**
    * Per Hosted Zone: **$1.00**
    * Per Traffic Flow Record: **$100.00**
    * Per 1 Million Queries: **$0.80**
    * Per 1 Million Latency Based Queries: **$1.20**
    * Per 1 Million GEO Queries: **$1.40**
    * Per Health Check: **$1.00**

  * **Hosting Per Month:**
    * Per APP: **$5.00**

  * **CDN Pricing per/1GB:**
    * North America: **$0.17**
    * Europe: **$0.17**
    * Australia: **$0.28**
    * Asia: **$0.28**
    * India: **$0.34**
    * South America: **$0.5**

* **Security requests:** 
  * **WAF and DDOS Pricing Per Month:**
    * per/1000 Web Requests: **$0.0012**
    * Per Web Access Control List: **$10.00**
    * Per Custom Domain Configuration: **$2.00**
  
  * **Encryption:**
    * per/1000 data sets: **$0.0144**
    * per/1MB per file: **$0.00048**

  * **Code Obfuscation Per Month:**
    * per/APP (300 files per app): **$102.00**

  * **Code Obfuscation Per Month:**
    * per/APP (300 files per app): **$102.00**

  * **Advanced Logging:**
    * per/1000 Log Entries: **$0.0072**

## How to Build

The generated code uses a few Maven dependencies e.g., Jackson, UniRest,
and Apache HttpClient. The reference to these dependencies is already
added in the pom.xml file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Eclipse click on ``` File -> Import ```.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/java?step=import0&workspaceFolder=SMASH-Java&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

* In the import dialog, select ``` Existing Java Project ``` and click ``` Next ```.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/java?step=import1&workspaceFolder=SMASH-Java&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

* Browse to locate the folder containing the source code. Select the detected location of the project and click ``` Finish ```.

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/java?step=import2&workspaceFolder=SMASH-Java&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

* Upon successful import, the project will be automatically built by Eclipse after automatically resolving the dependencies.

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/java?step=import3&workspaceFolder=SMASH-Java&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

## How to Use

The following section explains how to use the SMASH library in a new console project.

### 1. Starting a new project

For starting a new project, click the menu command ``` File > New > Project ```.

![Add a new project in Eclipse](https://apidocs.io/illustration/java?step=createNewProject0&workspaceFolder=SMASH-Java&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Next, choose ``` Maven > Maven Project ```and click ``` Next ```.

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/java?step=createNewProject1&workspaceFolder=SMASH-Java&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Here, make sure to use the current workspace by choosing ``` Use default Workspace location ```, as shown in the picture below and click ``` Next ```.

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/java?step=createNewProject2&workspaceFolder=SMASH-Java&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Following this, select the *quick start* project type to create a simple project with an existing class and a ``` main ``` method. To do this, choose ``` maven-archetype-quickstart ``` item from the list and click ``` Next ```.

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/java?step=createNewProject3&workspaceFolder=SMASH-Java&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

In the last step, provide a ``` Group Id ``` and ``` Artifact Id ``` as shown in the picture below and click ``` Finish ```.

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/java?step=createNewProject4&workspaceFolder=SMASH-Java&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

### 2. Add reference of the library project

The created Maven project manages its dependencies using its ``` pom.xml ``` file. In order to add a dependency on the *SMASH* client library, double click on the ``` pom.xml ``` file in the ``` Package Explorer ```. Opening the ``` pom.xml ``` file will render a graphical view on the cavas. Here, switch to the ``` Dependencies ``` tab and click the ``` Add ``` button as shown in the picture below.

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/java?step=testProject0&workspaceFolder=SMASH-Java&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Clicking the ``` Add ``` button will open a dialog where you need to specify SMASH in ``` Group Id ``` and SMASH in the ``` Artifact Id ``` fields. Once added click ``` OK ```. Save the ``` pom.xml ``` file.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?step=testProject1&workspaceFolder=SMASH-Java&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

### 3. Write sample code

Once the ``` SimpleConsoleApp ``` is created, a file named ``` App.java ``` will be visible in the *Package Explorer* with a ``` main ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?step=testProject2&workspaceFolder=SMASH-Java&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Eclipse, for running the tests do the following:

1. Select the project *SMASH* from the package explorer.
2. Select "Run -> Run as -> JUnit Test" or use "Alt + Shift + X" followed by "T" to run the Tests.

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| uid | Your user ID |
| secret | Your Private API Key |
| key | Your Public API Key |



API client can be initialized as following.

```java
// Configuration parameters and credentials
String uid = "UID"; // Your user ID
String secret = "SECRET"; // Your Private API Key
String key = "KEY"; // Your Public API Key

SMASHClient client = new SMASHClient(uid, secret, key);
```


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [AdvancedLogging](#advanced_logging)
* [WAFDDOSProtection](#wafddos_protection)
* [Encryption](#encryption)
* [CDN](#cdn)
* [DNS](#dns)
* [CodeObfuscation](#code_obfuscation)
* [Hosting](#hosting)
* [DataManipulationConversionSortingAndCompressionAPI](#data_manipulation_conversion_sorting_and_compression_api)
* [ImageManipulationAndModerationAPI](#image_manipulation_and_moderation_api)
* [Verification](#verification)
* [TwoFactorAuthenticationAPI](#two_factor_authentication_api)
* [UserManagement](#user_management)
* [LoginAndRegistration](#login_and_registration)

## <a name="advanced_logging"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.AdvancedLogging") AdvancedLogging

### Get singleton instance

The singleton instance of the ``` AdvancedLogging ``` class can be accessed from the API Client.

```java
AdvancedLogging advancedLogging = client.getAdvancedLogging();
```

### <a name="logging_info_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.AdvancedLogging.loggingInfoAsync") loggingInfoAsync

> WAF Log Info


```java
void loggingInfoAsync(
        final String name,
        final String origin,
        final String time,
        final APICallBack<HttpsApiRestShApiSLIR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| name |  ``` Required ```  | Name of your WAF zone |
| origin |  ``` Required ```  | IP Address of the Web Application |
| time |  ``` Optional ```  | Specific times or dates to lookup separated by a comma in MMDDYYHHMMSS Format ( Month Month Day Day Year Year Year Hour Hour Minute Minute Second Second [01012017120059]) |


#### Example Usage

```java
String name = "name";
String origin = "origin";
String time = "time";
// Invoking the API call with sample inputs
advancedLogging.loggingInfoAsync(name, origin, time, new APICallBack<HttpsApiRestShApiSLIR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSLIR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="logging_configuration_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.AdvancedLogging.loggingConfigurationAsync") loggingConfigurationAsync

> WAF Log Configuration


```java
void loggingConfigurationAsync(
        final String name,
        final String origin,
        final String activate,
        final APICallBack<HttpsApiRestShApiSLR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| name |  ``` Required ```  | Name of the WAF zone |
| origin |  ``` Required ```  | IP Address of the Web Application you wish to configure logging on |
| activate |  ``` Required ```  | True or False |


#### Example Usage

```java
String name = "name";
String origin = "origin";
String activate = "activate";
// Invoking the API call with sample inputs
advancedLogging.loggingConfigurationAsync(name, origin, activate, new APICallBack<HttpsApiRestShApiSLR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSLR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.WAFDDOSProtection") WAFDDOSProtection

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtection ``` class can be accessed from the API Client.

```java
WAFDDOSProtection wAFDDOSProtection = client.getWAFDDOSProtection();
```

### <a name="https_api_rest_sh_api_swc_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.WAFDDOSProtection.httpsApiRestShApiSWCAsync") httpsApiRestShApiSWCAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void httpsApiRestShApiSWCAsync(
        final String key,
        final String uid,
        final String name,
        final String origin,
        final String rule,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSWCR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| name |  ``` Required ```  | TODO: Add a parameter description |
| origin |  ``` Required ```  | TODO: Add a parameter description |
| rule |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "API";
String uid = "UID";
String name = "origin-name";
String origin = "origin.yourdomain.tld";
String rule = "header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does";
String contentType = "application/json";
// Invoking the API call with sample inputs
wAFDDOSProtection.httpsApiRestShApiSWCAsync(key, uid, name, origin, rule, contentType, new APICallBack<HttpsApiRestShApiSWCR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSWCR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="https_api_rest_sh_api_sw_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.WAFDDOSProtection.httpsApiRestShApiSWAsync") httpsApiRestShApiSWAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void httpsApiRestShApiSWAsync(
        final String key,
        final String uid,
        final String origin,
        final String cname,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSWR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| origin |  ``` Required ```  | TODO: Add a parameter description |
| cname |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "API";
String uid = "UID";
String origin = "origin.yourdomain.tld";
String cname = "yourdomain.tld,www.yourdomain.tld";
String contentType = "application/json";
// Invoking the API call with sample inputs
wAFDDOSProtection.httpsApiRestShApiSWAsync(key, uid, origin, cname, contentType, new APICallBack<HttpsApiRestShApiSWR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSWR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="https_api_rest_sh_api_swc_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.WAFDDOSProtection.httpsApiRestShApiSWCAsync") httpsApiRestShApiSWCAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void httpsApiRestShApiSWCAsync(
        final HttpsApiRestShApiSWC body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSWCR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    String bodyValue = "{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}";
    HttpsApiRestShApiSWC body = mapper.readValue(bodyValue,new TypeReference<HttpsApiRestShApiSWC> (){});
    String contentType = "application/json";
    // Invoking the API call with sample inputs
    wAFDDOSProtection.httpsApiRestShApiSWCAsync(body, contentType, new APICallBack<HttpsApiRestShApiSWCR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSWCR response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="https_api_rest_sh_api_sw_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.WAFDDOSProtection.httpsApiRestShApiSWAsync") httpsApiRestShApiSWAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void httpsApiRestShApiSWAsync(
        final HttpsApiRestShApiSW body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSWR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    String bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}";
    HttpsApiRestShApiSW body = mapper.readValue(bodyValue,new TypeReference<HttpsApiRestShApiSW> (){});
    String contentType = "application/json";
    // Invoking the API call with sample inputs
    wAFDDOSProtection.httpsApiRestShApiSWAsync(body, contentType, new APICallBack<HttpsApiRestShApiSWR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSWR response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.Encryption") Encryption

### Get singleton instance

The singleton instance of the ``` Encryption ``` class can be accessed from the API Client.

```java
Encryption encryption = client.getEncryption();
```

### <a name="data_and_file_encryption_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.Encryption.dataAndFileEncryptionAsync") dataAndFileEncryptionAsync

> Data and File Encryption API


```java
void dataAndFileEncryptionAsync(
        final String data,
        final String method,
        final int bit,
        final APICallBack<HttpsApiRestShApiSER> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Required ```  | GIT URL, file URL, direct upload of file, or data as a query string |
| method |  ``` Required ```  | Single or multiple encryption types to apply to data or files separated by a comma (DES, RSA, BLOWFISH, TWOFISH, AES, IDEA, PGP) |
| bit |  ``` Required ```  | Encryption key size (4096) |


#### Example Usage

```java
String data = "data";
String method = "method";
int bit = 121;
// Invoking the API call with sample inputs
encryption.dataAndFileEncryptionAsync(data, method, bit, new APICallBack<HttpsApiRestShApiSER>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSER response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.CDN") CDN

### Get singleton instance

The singleton instance of the ``` CDN ``` class can be accessed from the API Client.

```java
CDN cDN = client.getCDN();
```

### <a name="c_dn_push_zone_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CDN.cDNPushZoneAsync") cDNPushZoneAsync

> CDN Push Zone API


```java
void cDNPushZoneAsync(
        final String cname,
        final String file,
        final APICallBack<HttpsApiRestShApiSCPushR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| cname |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access |
| file |  ``` Required ```  | GIT URL, file URL, or direct upload of file |


#### Example Usage

```java
String cname = "cname";
String file = "file";
// Invoking the API call with sample inputs
cDN.cDNPushZoneAsync(cname, file, new APICallBack<HttpsApiRestShApiSCPushR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSCPushR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="c_dn_pull_zone_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CDN.cDNPullZoneAsync") cDNPullZoneAsync

> CDN Pull Zone API


```java
void cDNPullZoneAsync(
        final String origin,
        final String cname,
        final APICallBack<HttpsApiRestShApiSCPullR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| origin |  ``` Required ```  | Domain or domain names separated by a comma |
| cname |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access |


#### Example Usage

```java
String origin = "origin";
String cname = "cname";
// Invoking the API call with sample inputs
cDN.cDNPullZoneAsync(origin, cname, new APICallBack<HttpsApiRestShApiSCPullR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSCPullR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.DNS") DNS

### Get singleton instance

The singleton instance of the ``` DNS ``` class can be accessed from the API Client.

```java
DNS dNS = client.getDNS();
```

### <a name="d_ns_configuration_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DNS.dNSConfigurationAsync") dNSConfigurationAsync

> DNS Configuration API


```java
void dNSConfigurationAsync(
        final String domain,
        final String records,
        final APICallBack<HttpsApiRestShApiSDCR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| domain |  ``` Required ```  | Domain or domain names separated by a comma |
| records |  ``` Required ```  | Records to append to domain separated by a comma (a;www.mydomain.com;127.0.0.0,cname;mydomain.com;otherdomain.com) |


#### Example Usage

```java
String domain = "domain";
String records = "records";
// Invoking the API call with sample inputs
dNS.dNSConfigurationAsync(domain, records, new APICallBack<HttpsApiRestShApiSDCR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSDCR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="d_ns_creation_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DNS.dNSCreationAsync") dNSCreationAsync

> DNS Creation API


```java
void dNSCreationAsync(
        final String domain,
        final APICallBack<HttpsApiRestShApiSDAR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| domain |  ``` Required ```  | Domain or domain names separated by a comma |


#### Example Usage

```java
String domain = "domain";
// Invoking the API call with sample inputs
dNS.dNSCreationAsync(domain, new APICallBack<HttpsApiRestShApiSDAR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSDAR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.CodeObfuscation") CodeObfuscation

### Get singleton instance

The singleton instance of the ``` CodeObfuscation ``` class can be accessed from the API Client.

```java
CodeObfuscation codeObfuscation = client.getCodeObfuscation();
```

### <a name="obfuscation_and_anti_tampering_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CodeObfuscation.obfuscationAndAntiTamperingAsync") obfuscationAndAntiTamperingAsync

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```java
void obfuscationAndAntiTamperingAsync(
        final String app,
        final APICallBack<HttpsApiRestShApiSOR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| app |  ``` Required ```  | GIT URL or ZIP package containing your APP |


#### Example Usage

```java
String app = "app";
// Invoking the API call with sample inputs
codeObfuscation.obfuscationAndAntiTamperingAsync(app, new APICallBack<HttpsApiRestShApiSOR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSOR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.Hosting") Hosting

### Get singleton instance

The singleton instance of the ``` Hosting ``` class can be accessed from the API Client.

```java
Hosting hosting = client.getHosting();
```

### <a name="hosting_setup_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.Hosting.hostingSetupAsync") hostingSetupAsync

> Node.JS and Static Web APP Hosting


```java
void hostingSetupAsync(
        final String app,
        final String domain,
        final APICallBack<HttpsApiRestShApiSHR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| app |  ``` Required ```  | GIT URL or ZIP package containing your APP |
| domain |  ``` Required ```  | Domain or domain names separated by a comma |


#### Example Usage

```java
String app = "app";
String domain = "domain";
// Invoking the API call with sample inputs
hosting.hostingSetupAsync(app, domain, new APICallBack<HttpsApiRestShApiSHR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSHR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.DataManipulationConversionSortingAndCompressionAPI") DataManipulationConversionSortingAndCompressionAPI

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPI ``` class can be accessed from the API Client.

```java
DataManipulationConversionSortingAndCompressionAPI dataManipulationConversionSortingAndCompressionAPI = client.getDataManipulationConversionSortingAndCompressionAPI();
```

### <a name="https_api_rest_sh_api_d_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiDAsync") httpsApiRestShApiDAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void httpsApiRestShApiDAsync(
        final String key,
        final String uid,
        final String user,
        final String apiuid,
        final String data,
        final String contentType,
        final APICallBack<HttpsApiRestShApiDR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| apiuid |  ``` Required ```  | TODO: Add a parameter description |
| data |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "API";
String uid = "UID";
String user = "UID";
String apiuid = "apiUID";
String data = "https://static.yourcdn.com/data.file";
String contentType = "application/json";
// Invoking the API call with sample inputs
dataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiDAsync(key, uid, user, apiuid, data, contentType, new APICallBack<HttpsApiRestShApiDR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiDR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="https_api_rest_sh_api_d_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiDAsync") httpsApiRestShApiDAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void httpsApiRestShApiDAsync(
        final HttpsApiRestShApiD body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiDR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    String bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}";
    HttpsApiRestShApiD body = mapper.readValue(bodyValue,new TypeReference<HttpsApiRestShApiD> (){});
    String contentType = "application/json";
    // Invoking the API call with sample inputs
    dataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiDAsync(body, contentType, new APICallBack<HttpsApiRestShApiDR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiDR response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.ImageManipulationAndModerationAPI") ImageManipulationAndModerationAPI

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPI ``` class can be accessed from the API Client.

```java
ImageManipulationAndModerationAPI imageManipulationAndModerationAPI = client.getImageManipulationAndModerationAPI();
```

### <a name="image_manipulation_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.ImageManipulationAndModerationAPI.imageManipulationAsync") imageManipulationAsync

> Image Manipulation API


```java
void imageManipulationAsync(
        final String image,
        final String transform,
        final APICallBack<HttpsApiRestShApiIR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| image |  ``` Required ```  | Image URL or direct upload |
| transform |  ``` Required ```  | Transformations to perform |


#### Example Usage

```java
String image = "image";
String transform = "transform";
// Invoking the API call with sample inputs
imageManipulationAndModerationAPI.imageManipulationAsync(image, transform, new APICallBack<HttpsApiRestShApiIR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiIR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.Verification") Verification

### Get singleton instance

The singleton instance of the ``` Verification ``` class can be accessed from the API Client.

```java
Verification verification = client.getVerification();
```

### <a name="user_address_verification_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.Verification.userAddressVerificationAsync") userAddressVerificationAsync

> User Address Verification API


```java
void userAddressVerificationAsync(
        final String user,
        final String a,
        final String sa,
        final String c,
        final String s,
        final int z,
        final String address,
        final APICallBack<HttpsApiRestShApiVAR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, or Email |
| a |  ``` Required ```  | Address Line One |
| sa |  ``` Required ```  | Address Line Two |
| c |  ``` Required ```  | Address City |
| s |  ``` Required ```  | Address State or Province |
| z |  ``` Required ```  | Address Zipcode |
| address |  ``` Optional ```  | Address as a one line input separated by commas |


#### Example Usage

```java
String user = "user";
String a = "a";
String sa = "sa";
String c = "c";
String s = "s";
int z = 121;
String address = "address";
// Invoking the API call with sample inputs
verification.userAddressVerificationAsync(user, a, sa, c, s, z, address, new APICallBack<HttpsApiRestShApiVAR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiVAR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="user_verification_response_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.Verification.userVerificationResponseAsync") userVerificationResponseAsync

> Users Verification Response API


```java
void userVerificationResponseAsync(
        final String user,
        final String code,
        final APICallBack<HttpsApiRestShApiVUR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |
| code |  ``` Required ```  | Verification code entered by the user |


#### Example Usage

```java
String user = "user";
String code = "code";
// Invoking the API call with sample inputs
verification.userVerificationResponseAsync(user, code, new APICallBack<HttpsApiRestShApiVUR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiVUR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="user_verification_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.Verification.userVerificationAsync") userVerificationAsync

> User Verification API


```java
void userVerificationAsync(
        final String user,
        final APICallBack<HttpsApiRestShApiVR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |


#### Example Usage

```java
String user = "user";
// Invoking the API call with sample inputs
verification.userVerificationAsync(user, new APICallBack<HttpsApiRestShApiVR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiVR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.TwoFactorAuthenticationAPI") TwoFactorAuthenticationAPI

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPI ``` class can be accessed from the API Client.

```java
TwoFactorAuthenticationAPI twoFactorAuthenticationAPI = client.getTwoFactorAuthenticationAPI();
```

### <a name="m2_fa_token_response_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.TwoFactorAuthenticationAPI.m2FATokenResponseAsync") m2FATokenResponseAsync

> Two Factor Authentication Token Reply


```java
void m2FATokenResponseAsync(
        final String user,
        final String code,
        final APICallBack<HttpsApiRestShApi2faTR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username or Email |
| code |  ``` Required ```  | Response From User Containing 2FA Code |


#### Example Usage

```java
String user = "user";
String code = "code";
// Invoking the API call with sample inputs
twoFactorAuthenticationAPI.m2FATokenResponseAsync(user, code, new APICallBack<HttpsApiRestShApi2faTR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApi2faTR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="two_factor_authentication_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.TwoFactorAuthenticationAPI.twoFactorAuthenticationAsync") twoFactorAuthenticationAsync

> Two Factor Authentication API


```java
void twoFactorAuthenticationAsync(
        final String to,
        final APICallBack<HttpsApiRestShApi2faR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| to |  ``` Required ```  | Users UID, Username, Email, Or Cellphone number |


#### Example Usage

```java
String to = "to";
// Invoking the API call with sample inputs
twoFactorAuthenticationAPI.twoFactorAuthenticationAsync(to, new APICallBack<HttpsApiRestShApi2faR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApi2faR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.UserManagement") UserManagement

### Get singleton instance

The singleton instance of the ``` UserManagement ``` class can be accessed from the API Client.

```java
UserManagement userManagement = client.getUserManagement();
```

### <a name="get_user_info_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagement.getUserInfoAsync") getUserInfoAsync

> Get User Info API


```java
void getUserInfoAsync(
        final String user,
        final APICallBack<HttpsApiRestShApiUIR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users User ID |


#### Example Usage

```java
String user = "user";
// Invoking the API call with sample inputs
userManagement.getUserInfoAsync(user, new APICallBack<HttpsApiRestShApiUIR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiUIR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="update_user_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagement.updateUserAsync") updateUserAsync

> Update User API


```java
void updateUserAsync(
        final String user,
        final String avatar,
        final String customInput,
        Map<String, Object> queryParameters,
        final APICallBack<HttpsApiRestShApiUUR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |
| avatar |  ``` Required ```  | Avatar Image URL |
| customInput |  ``` Required ```  | Custom input variable for users profile |
| queryParameters | ``` Optional ``` | Additional optional query parameters are supported by this method |


#### Example Usage

```java
String user = "user";
String avatar = "avatar";
String customInput = "custom input";
// key-value map for optional query parameters
Map<String, Object> queryParams = new LinkedHashMap<String, Object>();
// Invoking the API call with sample inputs
userManagement.updateUserAsync(user, avatar, customInput, queryParams, new APICallBack<HttpsApiRestShApiUUR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiUUR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="delete_user_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagement.deleteUserAsync") deleteUserAsync

> Delete User API


```java
void deleteUserAsync(
        final String user,
        final APICallBack<HttpsApiRestShApiUDR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, or Email |


#### Example Usage

```java
String user = "user";
// Invoking the API call with sample inputs
userManagement.deleteUserAsync(user, new APICallBack<HttpsApiRestShApiUDR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiUDR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.LoginAndRegistration") LoginAndRegistration

### Get singleton instance

The singleton instance of the ``` LoginAndRegistration ``` class can be accessed from the API Client.

```java
LoginAndRegistration loginAndRegistration = client.getLoginAndRegistration();
```

### <a name="user_registration_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.LoginAndRegistration.userRegistrationAsync") userRegistrationAsync

> User Registration API


```java
void userRegistrationAsync(
        final String email,
        final String user,
        final String password,
        final String name,
        final Integer phone,
        final Integer countrycode,
        final String address,
        Map<String, Object> queryParameters,
        final APICallBack<HttpsApiRestShApiAURR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| email |  ``` Required ```  | Users Email |
| user |  ``` Required ```  | Users Username |
| password |  ``` Required ```  | Users Password |
| name |  ``` Optional ```  | Users Name |
| phone |  ``` Optional ```  | Users Cellphone Number |
| countrycode |  ``` Optional ```  | Users Country Code (US = 1) |
| address |  ``` Optional ```  | Users Address |
| queryParameters | ``` Optional ``` | Additional optional query parameters are supported by this method |


#### Example Usage

```java
String email = "email";
String user = "user";
String password = "password";
String name = "name";
Integer phone = 121;
Integer countrycode = 121;
String address = "address";
// key-value map for optional query parameters
Map<String, Object> queryParams = new LinkedHashMap<String, Object>();
// Invoking the API call with sample inputs
loginAndRegistration.userRegistrationAsync(email, user, password, name, phone, countrycode, address, queryParams, new APICallBack<HttpsApiRestShApiAURR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiAURR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="user_authentication_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.LoginAndRegistration.userAuthenticationAsync") userAuthenticationAsync

> User Authentication API


```java
void userAuthenticationAsync(
        final String user,
        final String password,
        final APICallBack<HttpsApiRestShApiAULR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users Username or Email |
| password |  ``` Required ```  | Users Password |


#### Example Usage

```java
String user = "user";
String password = "password";
// Invoking the API call with sample inputs
loginAndRegistration.userAuthenticationAsync(user, password, new APICallBack<HttpsApiRestShApiAULR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiAULR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)



