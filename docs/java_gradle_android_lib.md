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

The generated code uses a few Gradle dependencies e.g., Jackson, Volley,
and Apache HttpClient. The reference to these dependencies is already
added in the build.gradle file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Android Studio click on ``` Open an Existing Android Project ```.

![Importing SDK into Android Studio - Step 1](https://apidocs.io/illustration/android?step=import1&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

* Browse to locate the folder containing the source code. Select the location of the SMASH gradle project and click ``` Ok ```.

![Importing SDK into Android Studio - Step 2](https://apidocs.io/illustration/android?step=import2&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

* Upon successful import, the project can be built by clicking on ``` Build > Make Project ``` or  pressing ``` Ctrl + F9 ```.

![Importing SDK into Android Studio - Step 3](https://apidocs.io/illustration/android?step=import3&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

## How to Use

The following section explains how to use the SMASH library in a new project.

### 1. Starting a new project 

For starting a new project, click on ``` Create New Android Studio Project ```.

![Add a new project in Android Studio - Step 1](https://apidocs.io/illustration/android?step=createNewProject0&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Here, configure the new project by adding the name, domain and location of the sample application followed by clicking ``` Next ```.

![Create a new Android Studio Project - Step 2](https://apidocs.io/illustration/android?step=createNewProject1&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Following this, select the `Phone and Tablet` option as shown in the illustration below and click `Next`.

![Create a new Android Studio Project - Step 3](https://apidocs.io/illustration/android?step=createNewProject2&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

In the following step, choose ``` Empty Activity ``` as the activity type and click ``` Next ```.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject3&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

In this step, provide an ``` Activity Name ``` and ``` Layout Name ``` and click ``` Finish ```.  This would take you to the newly created project.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject4&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

### 2. Add reference of the library project

In order to add a dependency to this sample application, click on the android button shown in the project explorer on the left side as shown in the picture. Click on ``` Project ``` in the drop down that emerges.  

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/android?step=testProject0&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Right click the sample application in the project explorer and click on ``` New > Module ```  as shown in the picture.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/android?step=testProject1&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Choose ``` Import Gradle Project ``` and click ``` Next ```.

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/android?step=testProject2&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Click on ``` Finish ``` which would take you back to the sample application with the refernced SDK. 

![Adding dependency to the client library - Step 4](https://apidocs.io/illustration/android?step=testProject3&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

In the following step naigate to the ``` SampleApplication >  app > build.gradle ``` file and add the following line ```compile project(path: ':SMASH')``` to the dependencies section as shown in the illustration below.

![Adding dependency to the client library - Step 5](https://apidocs.io/illustration/android?step=testProject4&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Finally, press ``` Sync Now ``` in the warning visible as shown in the picture below.

![Adding dependency to the client library - Step 6](https://apidocs.io/illustration/android?step=testProject5&workspaceFolder=SMASH&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

### 3. Write sample code

Once the ``` SampleApplication ``` is created, a file named ``` SampleApplication > app > src > main > java > MainActivity ``` will be visible in the *Project Explorer* with an ``` onCreate ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Android Studio, for running the tests do the following:

1. Right click on *SampleApplication > SMASH > androidTest > java)* from the project explorer.
2. Select "Run All Tests" or use "Ctrl + Shift + F10" to run the Tests.

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| basicAuthUserName | The username to use with basic authentication |
| basicAuthPassword | The password to use with basic authentication |



API client can be initialized as following. The `appContext` being passed is the Android application [`Context`](https://developer.android.com/reference/android/content/Context.html).

```java
// Configuration parameters and credentials
String basicAuthUserName = "basicAuthUserName"; // The username to use with basic authentication
String basicAuthPassword = "basicAuthPassword"; // The password to use with basic authentication

SMASH.Configuration.initialize(appContext);
SMASHClient client = new SMASHClient(basicAuthUserName, basicAuthPassword);
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
        final String key,
        final String uid,
        final String name,
        final String origin,
        final String time,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSLIR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| name |  ``` Required ```  | TODO: Add a parameter description |
| origin |  ``` Required ```  | TODO: Add a parameter description |
| time |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String name = "name";
String origin = "origin";
String time = "time";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
advancedLogging.loggingInfoAsync(key, uid, name, origin, time, contentType, new APICallBack<HttpsApiRestShApiSLIR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSLIR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="logging_setup_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.AdvancedLogging.loggingSetupAsync") loggingSetupAsync

> WAF Log Setup


```java
void loggingSetupAsync(
        final String key,
        final String uid,
        final String name,
        final String origin,
        final boolean activate,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSLR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| name |  ``` Required ```  | TODO: Add a parameter description |
| origin |  ``` Required ```  | TODO: Add a parameter description |
| activate |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String name = "name";
String origin = "origin";
boolean activate = false;
String contentType = "Content-Type";
// Invoking the API call with sample inputs
advancedLogging.loggingSetupAsync(key, uid, name, origin, activate, contentType, new APICallBack<HttpsApiRestShApiSLR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSLR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="logging_info_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.AdvancedLogging.loggingInfoAsync") loggingInfoAsync

> WAF Log Info


```java
void loggingInfoAsync(
        final HttpsApiRestShApiSLI body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSLIR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiSLI body = new HttpsApiRestShApiSLI();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    advancedLogging.loggingInfoAsync(body, contentType, new APICallBack<HttpsApiRestShApiSLIR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSLIR response) {
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


### <a name="logging_setup_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.AdvancedLogging.loggingSetupAsync") loggingSetupAsync

> WAF Log Setup


```java
void loggingSetupAsync(
        final HttpsApiRestShApiSL body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSLR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiSL body = new HttpsApiRestShApiSL();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    advancedLogging.loggingSetupAsync(body, contentType, new APICallBack<HttpsApiRestShApiSLR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSLR response) {
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
        final String key,
        final String uid,
        final String data,
        final String method,
        final int bit,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSER> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| data |  ``` Required ```  | TODO: Add a parameter description |
| method |  ``` Required ```  | TODO: Add a parameter description |
| bit |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String data = "data";
String method = "method";
int bit = 33;
String contentType = "Content-Type";
// Invoking the API call with sample inputs
encryption.dataAndFileEncryptionAsync(key, uid, data, method, bit, contentType, new APICallBack<HttpsApiRestShApiSER>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSER response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="data_and_file_encryption_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.Encryption.dataAndFileEncryptionAsync") dataAndFileEncryptionAsync

> Data and File Encryption API


```java
void dataAndFileEncryptionAsync(
        final HttpsApiRestShApiSE body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSER> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiSE body = new HttpsApiRestShApiSE();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    encryption.dataAndFileEncryptionAsync(body, contentType, new APICallBack<HttpsApiRestShApiSER>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSER response) {
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
        final String key,
        final String uid,
        final String cname,
        final String file,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSCPushR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| cname |  ``` Required ```  | TODO: Add a parameter description |
| file |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String cname = "cname";
String file = "file";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
cDN.cDNPushZoneAsync(key, uid, cname, file, contentType, new APICallBack<HttpsApiRestShApiSCPushR>() {
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
        final String key,
        final String uid,
        final String origin,
        final String cname,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSCPullR> callBack)
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
String key = "key";
String uid = "uid";
String origin = "origin";
String cname = "cname";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
cDN.cDNPullZoneAsync(key, uid, origin, cname, contentType, new APICallBack<HttpsApiRestShApiSCPullR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSCPullR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="c_dn_push_zone_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CDN.cDNPushZoneAsync") cDNPushZoneAsync

> CDN Push Zone API


```java
void cDNPushZoneAsync(
        final HttpsApiRestShApiSCPush body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSCPushR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiSCPush body = new HttpsApiRestShApiSCPush();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    cDN.cDNPushZoneAsync(body, contentType, new APICallBack<HttpsApiRestShApiSCPushR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSCPushR response) {
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


### <a name="c_dn_pull_zone_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CDN.cDNPullZoneAsync") cDNPullZoneAsync

> CDN Pull Zone API


```java
void cDNPullZoneAsync(
        final HttpsApiRestShApiSCPull body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSCPullR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiSCPull body = new HttpsApiRestShApiSCPull();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    cDN.cDNPullZoneAsync(body, contentType, new APICallBack<HttpsApiRestShApiSCPullR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSCPullR response) {
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
        final String key,
        final String uid,
        final String domain,
        final String records,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSDCR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| domain |  ``` Required ```  | TODO: Add a parameter description |
| records |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String domain = "domain";
String records = "records";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
dNS.dNSConfigurationAsync(key, uid, domain, records, contentType, new APICallBack<HttpsApiRestShApiSDCR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSDCR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="d_ns_configuration_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DNS.dNSConfigurationAsync") dNSConfigurationAsync

> DNS Configuration API


```java
void dNSConfigurationAsync(
        final HttpsApiRestShApiSDC body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSDCR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiSDC body = new HttpsApiRestShApiSDC();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    dNS.dNSConfigurationAsync(body, contentType, new APICallBack<HttpsApiRestShApiSDCR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSDCR response) {
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


### <a name="d_ns_creation_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DNS.dNSCreationAsync") dNSCreationAsync

> DNS Creation API


```java
void dNSCreationAsync(
        final String key,
        final String uid,
        final String domain,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSDAR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| domain |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String domain = "domain";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
dNS.dNSCreationAsync(key, uid, domain, contentType, new APICallBack<HttpsApiRestShApiSDAR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSDAR response) {
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
        final HttpsApiRestShApiSDA body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSDAR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiSDA body = new HttpsApiRestShApiSDA();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    dNS.dNSCreationAsync(body, contentType, new APICallBack<HttpsApiRestShApiSDAR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSDAR response) {
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
        final String key,
        final String uid,
        final String app,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSOR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| app |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String app = "app";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
codeObfuscation.obfuscationAndAntiTamperingAsync(key, uid, app, contentType, new APICallBack<HttpsApiRestShApiSOR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSOR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="obfuscation_and_anti_tampering_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CodeObfuscation.obfuscationAndAntiTamperingAsync") obfuscationAndAntiTamperingAsync

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```java
void obfuscationAndAntiTamperingAsync(
        final HttpsApiRestShApiSO body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSOR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiSO body = new HttpsApiRestShApiSO();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    codeObfuscation.obfuscationAndAntiTamperingAsync(body, contentType, new APICallBack<HttpsApiRestShApiSOR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSOR response) {
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
        final String key,
        final String uid,
        final String app,
        final String domain,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSHR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| app |  ``` Required ```  | TODO: Add a parameter description |
| domain |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String app = "app";
String domain = "domain";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
hosting.hostingSetupAsync(key, uid, app, domain, contentType, new APICallBack<HttpsApiRestShApiSHR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSHR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="hosting_setup_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.Hosting.hostingSetupAsync") hostingSetupAsync

> Node.JS and Static Web APP Hosting


```java
void hostingSetupAsync(
        final HttpsApiRestShApiSH body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiSHR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiSH body = new HttpsApiRestShApiSH();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    hosting.hostingSetupAsync(body, contentType, new APICallBack<HttpsApiRestShApiSHR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSHR response) {
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
        final String key,
        final String uid,
        final String image,
        final String transform,
        final String contentType,
        final APICallBack<HttpsApiRestShApiIR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| image |  ``` Required ```  | TODO: Add a parameter description |
| transform |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String image = "image";
String transform = "transform";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
imageManipulationAndModerationAPI.imageManipulationAsync(key, uid, image, transform, contentType, new APICallBack<HttpsApiRestShApiIR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiIR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="image_manipulation_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.ImageManipulationAndModerationAPI.imageManipulationAsync") imageManipulationAsync

> Image Manipulation API


```java
void imageManipulationAsync(
        final HttpsApiRestShApiI body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiIR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiI body = new HttpsApiRestShApiI();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    imageManipulationAndModerationAPI.imageManipulationAsync(body, contentType, new APICallBack<HttpsApiRestShApiIR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiIR response) {
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
        final String key,
        final String uid,
        final String user,
        final String a,
        final String sa,
        final String c,
        final String s,
        final int z,
        final String contentType,
        final APICallBack<HttpsApiRestShApiVAR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| a |  ``` Required ```  | TODO: Add a parameter description |
| sa |  ``` Required ```  | TODO: Add a parameter description |
| c |  ``` Required ```  | TODO: Add a parameter description |
| s |  ``` Required ```  | TODO: Add a parameter description |
| z |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String user = "user";
String a = "a";
String sa = "sa";
String c = "c";
String s = "s";
int z = 124;
String contentType = "Content-Type";
// Invoking the API call with sample inputs
verification.userAddressVerificationAsync(key, uid, user, a, sa, c, s, z, contentType, new APICallBack<HttpsApiRestShApiVAR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiVAR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="user_address_verification_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.Verification.userAddressVerificationAsync") userAddressVerificationAsync

> User Address Verification API


```java
void userAddressVerificationAsync(
        final HttpsApiRestShApiVA body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiVAR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiVA body = new HttpsApiRestShApiVA();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    verification.userAddressVerificationAsync(body, contentType, new APICallBack<HttpsApiRestShApiVAR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiVAR response) {
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


### <a name="user_verification_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.Verification.userVerificationAsync") userVerificationAsync

> User Verification API


```java
void userVerificationAsync(
        final String key,
        final String uid,
        final String user,
        final String code,
        final String contentType,
        final APICallBack<HttpsApiRestShApiVUR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| code |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String user = "user";
String code = "code";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
verification.userVerificationAsync(key, uid, user, code, contentType, new APICallBack<HttpsApiRestShApiVUR>() {
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
        final HttpsApiRestShApiVU body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiVUR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiVU body = new HttpsApiRestShApiVU();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    verification.userVerificationAsync(body, contentType, new APICallBack<HttpsApiRestShApiVUR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiVUR response) {
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


### <a name="cellphone_verification_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.Verification.cellphoneVerificationAsync") cellphoneVerificationAsync

> Verification API


```java
void cellphoneVerificationAsync(
        final String key,
        final String uid,
        final String to,
        final String contentType,
        final APICallBack<HttpsApiRestShApiVR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String to = "to";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
verification.cellphoneVerificationAsync(key, uid, to, contentType, new APICallBack<HttpsApiRestShApiVR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiVR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="cellphone_verification_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.Verification.cellphoneVerificationAsync") cellphoneVerificationAsync

> Verification API


```java
void cellphoneVerificationAsync(
        final HttpsApiRestShApiV body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiVR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiV body = new HttpsApiRestShApiV();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    verification.cellphoneVerificationAsync(body, contentType, new APICallBack<HttpsApiRestShApiVR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiVR response) {
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
        final String key,
        final String uid,
        final String user,
        final String code,
        final String contentType,
        final APICallBack<HttpsApiRestShApi2faTR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| code |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String user = "user";
String code = "code";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
twoFactorAuthenticationAPI.m2FATokenResponseAsync(key, uid, user, code, contentType, new APICallBack<HttpsApiRestShApi2faTR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApi2faTR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="m2_fa_token_response_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.TwoFactorAuthenticationAPI.m2FATokenResponseAsync") m2FATokenResponseAsync

> Two Factor Authentication Token Reply


```java
void m2FATokenResponseAsync(
        final HttpsApiRestShApi2faT body,
        final String contentType,
        final APICallBack<HttpsApiRestShApi2faTR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApi2faT body = new HttpsApiRestShApi2faT();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    twoFactorAuthenticationAPI.m2FATokenResponseAsync(body, contentType, new APICallBack<HttpsApiRestShApi2faTR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApi2faTR response) {
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


### <a name="two_factor_authentication_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.TwoFactorAuthenticationAPI.twoFactorAuthenticationAsync") twoFactorAuthenticationAsync

> Two Factor Authentication API


```java
void twoFactorAuthenticationAsync(
        final String key,
        final String uid,
        final String to,
        final String contentType,
        final APICallBack<HttpsApiRestShApi2faR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String to = "to";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
twoFactorAuthenticationAPI.twoFactorAuthenticationAsync(key, uid, to, contentType, new APICallBack<HttpsApiRestShApi2faR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApi2faR response) {
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
        final HttpsApiRestShApi2fa body,
        final String contentType,
        final APICallBack<HttpsApiRestShApi2faR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApi2fa body = new HttpsApiRestShApi2fa();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    twoFactorAuthenticationAPI.twoFactorAuthenticationAsync(body, contentType, new APICallBack<HttpsApiRestShApi2faR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApi2faR response) {
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
        final String key,
        final String uid,
        final String user,
        final String apiuid,
        final String contentType,
        final APICallBack<HttpsApiRestShApiUIR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| apiuid |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String user = "user";
String apiuid = "apiuid";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
userManagement.getUserInfoAsync(key, uid, user, apiuid, contentType, new APICallBack<HttpsApiRestShApiUIR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiUIR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="get_user_info_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagement.getUserInfoAsync") getUserInfoAsync

> Get User Info API


```java
void getUserInfoAsync(
        final HttpsApiRestShApiUI body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiUIR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiUI body = new HttpsApiRestShApiUI();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    userManagement.getUserInfoAsync(body, contentType, new APICallBack<HttpsApiRestShApiUIR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiUIR response) {
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


### <a name="update_user_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagement.updateUserAsync") updateUserAsync

> Update User API


```java
void updateUserAsync(
        final String key,
        final String uid,
        final String user,
        final String apiuid,
        final String avatar,
        final String customInput,
        final String contentType,
        final APICallBack<HttpsApiRestShApiUUR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| apiuid |  ``` Required ```  | TODO: Add a parameter description |
| avatar |  ``` Required ```  | TODO: Add a parameter description |
| customInput |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String user = "user";
String apiuid = "apiuid";
String avatar = "avatar";
String customInput = "custom input";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
userManagement.updateUserAsync(key, uid, user, apiuid, avatar, customInput, contentType, new APICallBack<HttpsApiRestShApiUUR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiUUR response) {
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
        final HttpsApiRestShApiUU body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiUUR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiUU body = new HttpsApiRestShApiUU();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    userManagement.updateUserAsync(body, contentType, new APICallBack<HttpsApiRestShApiUUR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiUUR response) {
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


### <a name="delete_user_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagement.deleteUserAsync") deleteUserAsync

> Delete User API


```java
void deleteUserAsync(
        final String api,
        final String uid,
        final String user,
        final String apiuid,
        final String contentType,
        final APICallBack<HttpsApiRestShApiUDR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| api |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| apiuid |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String api = "api";
String uid = "uid";
String user = "user";
String apiuid = "apiuid";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
userManagement.deleteUserAsync(api, uid, user, apiuid, contentType, new APICallBack<HttpsApiRestShApiUDR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiUDR response) {
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
        final HttpsApiRestShApiUD body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiUDR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiUD body = new HttpsApiRestShApiUD();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    userManagement.deleteUserAsync(body, contentType, new APICallBack<HttpsApiRestShApiUDR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiUDR response) {
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
        final String key,
        final String uid,
        final String user,
        final String password,
        final String name,
        final String email,
        final int phone,
        final int countrycode,
        final String address,
        final String contentType,
        final APICallBack<HttpsApiRestShApiAURR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| password |  ``` Required ```  | TODO: Add a parameter description |
| name |  ``` Required ```  | TODO: Add a parameter description |
| email |  ``` Required ```  | TODO: Add a parameter description |
| phone |  ``` Required ```  | TODO: Add a parameter description |
| countrycode |  ``` Required ```  | TODO: Add a parameter description |
| address |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String user = "user";
String password = "password";
String name = "name";
String email = "email";
int phone = 83;
int countrycode = 83;
String address = "address";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
loginAndRegistration.userRegistrationAsync(key, uid, user, password, name, email, phone, countrycode, address, contentType, new APICallBack<HttpsApiRestShApiAURR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiAURR response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="user_registration_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.LoginAndRegistration.userRegistrationAsync") userRegistrationAsync

> User Registration API


```java
void userRegistrationAsync(
        final HttpsApiRestShApiAUR body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiAURR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiAUR body = new HttpsApiRestShApiAUR();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    loginAndRegistration.userRegistrationAsync(body, contentType, new APICallBack<HttpsApiRestShApiAURR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiAURR response) {
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


### <a name="user_authentication_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.LoginAndRegistration.userAuthenticationAsync") userAuthenticationAsync

> User Authentication API


```java
void userAuthenticationAsync(
        final String key,
        final String uid,
        final String user,
        final String password,
        final String contentType,
        final APICallBack<HttpsApiRestShApiAULR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| password |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String key = "key";
String uid = "uid";
String user = "user";
String password = "password";
String contentType = "Content-Type";
// Invoking the API call with sample inputs
loginAndRegistration.userAuthenticationAsync(key, uid, user, password, contentType, new APICallBack<HttpsApiRestShApiAULR>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiAULR response) {
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
        final HttpsApiRestShApiAUL body,
        final String contentType,
        final APICallBack<HttpsApiRestShApiAULR> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    HttpsApiRestShApiAUL body = new HttpsApiRestShApiAUL();
    String contentType = "Content-Type";
    // Invoking the API call with sample inputs
    loginAndRegistration.userAuthenticationAsync(body, contentType, new APICallBack<HttpsApiRestShApiAULR>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiAULR response) {
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



