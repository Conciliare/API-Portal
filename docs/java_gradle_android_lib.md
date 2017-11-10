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
| key | Your API Key |
| uid | Your User ID |



API client can be initialized as following. The `appContext` being passed is the Android application [`Context`](https://developer.android.com/reference/android/content/Context.html).

```java
// Configuration parameters and credentials
String key = "API"; // Your API Key
String uid = "UID"; // Your User ID

SMASH.Configuration.initialize(appContext);
SMASHClient client = new SMASHClient(key, uid);
```


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [AdvancedLoggingController](#advanced_logging_controller)
* [WAFDDOSProtectionController](#wafddos_protection_controller)
* [EncryptionController](#encryption_controller)
* [CDNController](#cdn_controller)
* [DNSController](#dns_controller)
* [CodeObfuscationController](#code_obfuscation_controller)
* [HostingController](#hosting_controller)
* [DataManipulationConversionSortingAndCompressionAPIController](#data_manipulation_conversion_sorting_and_compression_api_controller)
* [ImageManipulationAndModerationAPIController](#image_manipulation_and_moderation_api_controller)
* [VerificationController](#verification_controller)
* [TwoFactorAuthenticationAPIController](#two_factor_authentication_api_controller)
* [UserManagementController](#user_management_controller)
* [LoginAndRegistrationController](#login_and_registration_controller)

## <a name="advanced_logging_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.AdvancedLoggingController") AdvancedLoggingController

### Get singleton instance

The singleton instance of the ``` AdvancedLoggingController ``` class can be accessed from the API Client.

```java
AdvancedLoggingController advancedLogging = client.getAdvancedLogging();
```

### <a name="get_https_api_rest_sh_api_sli_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.AdvancedLoggingController.getHttpsApiRestShApiSLIAsync") getHttpsApiRestShApiSLIAsync

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```java
void getHttpsApiRestShApiSLIAsync(
        final GetHttpsApiRestShApiSLIInput input,
        final APICallBack<HttpsApiRestShApiSLIRModel> callBack)
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
GetHttpsApiRestShApiSLIInput collect = new GetHttpsApiRestShApiSLIInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String name = "name";
collect.setName(name);

String origin = "origin";
collect.setOrigin(origin);

String time = "time";
collect.setTime(time);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
advancedLogging.getHttpsApiRestShApiSLIAsync(collect, new APICallBack<HttpsApiRestShApiSLIRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSLIRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="get_https_api_rest_sh_api_sl_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.AdvancedLoggingController.getHttpsApiRestShApiSLAsync") getHttpsApiRestShApiSLAsync

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```java
void getHttpsApiRestShApiSLAsync(
        final GetHttpsApiRestShApiSLInput input,
        final APICallBack<HttpsApiRestShApiSLRModel> callBack)
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
GetHttpsApiRestShApiSLInput collect = new GetHttpsApiRestShApiSLInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String name = "name";
collect.setName(name);

String origin = "origin";
collect.setOrigin(origin);

boolean activate = false;
collect.setActivate(activate);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
advancedLogging.getHttpsApiRestShApiSLAsync(collect, new APICallBack<HttpsApiRestShApiSLRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSLRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_sli_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.AdvancedLoggingController.createHttpsApiRestShApiSLIAsync") createHttpsApiRestShApiSLIAsync

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```java
void createHttpsApiRestShApiSLIAsync(
        final CreateHttpsApiRestShApiSLIInput input,
        final APICallBack<HttpsApiRestShApiSLIRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSLIInput collect = new CreateHttpsApiRestShApiSLIInput();

    HttpsApiRestShApiSLIModel body = new HttpsApiRestShApiSLIModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    advancedLogging.createHttpsApiRestShApiSLIAsync(collect, new APICallBack<HttpsApiRestShApiSLIRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSLIRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="create_https_api_rest_sh_api_sl_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.AdvancedLoggingController.createHttpsApiRestShApiSLAsync") createHttpsApiRestShApiSLAsync

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```java
void createHttpsApiRestShApiSLAsync(
        final CreateHttpsApiRestShApiSLInput input,
        final APICallBack<HttpsApiRestShApiSLRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSLInput collect = new CreateHttpsApiRestShApiSLInput();

    HttpsApiRestShApiSLModel body = new HttpsApiRestShApiSLModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    advancedLogging.createHttpsApiRestShApiSLAsync(collect, new APICallBack<HttpsApiRestShApiSLRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSLRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.WAFDDOSProtectionController") WAFDDOSProtectionController

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtectionController ``` class can be accessed from the API Client.

```java
WAFDDOSProtectionController wAFDDOSProtection = client.getWAFDDOSProtection();
```

### <a name="get_https_api_rest_sh_api_swc_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.WAFDDOSProtectionController.getHttpsApiRestShApiSWCAsync") getHttpsApiRestShApiSWCAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void getHttpsApiRestShApiSWCAsync(
        final GetHttpsApiRestShApiSWCInput input,
        final APICallBack<HttpsApiRestShApiSWCRModel> callBack)
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
GetHttpsApiRestShApiSWCInput collect = new GetHttpsApiRestShApiSWCInput();

String key = "API";
collect.setKey(key);

String uid = "UID";
collect.setUid(uid);

String name = "origin-name";
collect.setName(name);

String origin = "origin.yourdomain.tld";
collect.setOrigin(origin);

String rule = "header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does";
collect.setRule(rule);

String contentType = "application/json";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
wAFDDOSProtection.getHttpsApiRestShApiSWCAsync(collect, new APICallBack<HttpsApiRestShApiSWCRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSWCRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="get_https_api_rest_sh_api_sw_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.WAFDDOSProtectionController.getHttpsApiRestShApiSWAsync") getHttpsApiRestShApiSWAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void getHttpsApiRestShApiSWAsync(
        final GetHttpsApiRestShApiSWInput input,
        final APICallBack<HttpsApiRestShApiSWRModel> callBack)
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
GetHttpsApiRestShApiSWInput collect = new GetHttpsApiRestShApiSWInput();

String key = "API";
collect.setKey(key);

String uid = "UID";
collect.setUid(uid);

String origin = "origin.yourdomain.tld";
collect.setOrigin(origin);

String cname = "yourdomain.tld,www.yourdomain.tld";
collect.setCname(cname);

String contentType = "application/json";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
wAFDDOSProtection.getHttpsApiRestShApiSWAsync(collect, new APICallBack<HttpsApiRestShApiSWRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSWRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_swc_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.WAFDDOSProtectionController.createHttpsApiRestShApiSWCAsync") createHttpsApiRestShApiSWCAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void createHttpsApiRestShApiSWCAsync(
        final CreateHttpsApiRestShApiSWCInput input,
        final APICallBack<HttpsApiRestShApiSWCRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSWCInput collect = new CreateHttpsApiRestShApiSWCInput();

    String bodyValue = "{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}";
    HttpsApiRestShApiSWCModel body = mapper.readValue(bodyValue,new TypeReference<HttpsApiRestShApiSWCModel> (){});
collect.setBody(body);

    String contentType = "application/json";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    wAFDDOSProtection.createHttpsApiRestShApiSWCAsync(collect, new APICallBack<HttpsApiRestShApiSWCRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSWCRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="create_https_api_rest_sh_api_sw_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.WAFDDOSProtectionController.createHttpsApiRestShApiSWAsync") createHttpsApiRestShApiSWAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void createHttpsApiRestShApiSWAsync(
        final CreateHttpsApiRestShApiSWInput input,
        final APICallBack<HttpsApiRestShApiSWRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSWInput collect = new CreateHttpsApiRestShApiSWInput();

    String bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}";
    HttpsApiRestShApiSWModel body = mapper.readValue(bodyValue,new TypeReference<HttpsApiRestShApiSWModel> (){});
collect.setBody(body);

    String contentType = "application/json";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    wAFDDOSProtection.createHttpsApiRestShApiSWAsync(collect, new APICallBack<HttpsApiRestShApiSWRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSWRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.EncryptionController") EncryptionController

### Get singleton instance

The singleton instance of the ``` EncryptionController ``` class can be accessed from the API Client.

```java
EncryptionController encryption = client.getEncryption();
```

### <a name="get_https_api_rest_sh_api_se_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.EncryptionController.getHttpsApiRestShApiSEAsync") getHttpsApiRestShApiSEAsync

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```java
void getHttpsApiRestShApiSEAsync(
        final GetHttpsApiRestShApiSEInput input,
        final APICallBack<HttpsApiRestShApiSERModel> callBack)
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
GetHttpsApiRestShApiSEInput collect = new GetHttpsApiRestShApiSEInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String data = "data";
collect.setData(data);

String method = "method";
collect.setMethod(method);

int bit = 35;
collect.setBit(bit);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
encryption.getHttpsApiRestShApiSEAsync(collect, new APICallBack<HttpsApiRestShApiSERModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSERModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_se_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.EncryptionController.createHttpsApiRestShApiSEAsync") createHttpsApiRestShApiSEAsync

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```java
void createHttpsApiRestShApiSEAsync(
        final CreateHttpsApiRestShApiSEInput input,
        final APICallBack<HttpsApiRestShApiSERModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSEInput collect = new CreateHttpsApiRestShApiSEInput();

    HttpsApiRestShApiSEModel body = new HttpsApiRestShApiSEModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    encryption.createHttpsApiRestShApiSEAsync(collect, new APICallBack<HttpsApiRestShApiSERModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSERModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.CDNController") CDNController

### Get singleton instance

The singleton instance of the ``` CDNController ``` class can be accessed from the API Client.

```java
CDNController cDN = client.getCDN();
```

### <a name="get_https_api_rest_sh_api_sc_push_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CDNController.getHttpsApiRestShApiSCPushAsync") getHttpsApiRestShApiSCPushAsync

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```java
void getHttpsApiRestShApiSCPushAsync(
        final GetHttpsApiRestShApiSCPushInput input,
        final APICallBack<HttpsApiRestShApiSCPushRModel> callBack)
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
GetHttpsApiRestShApiSCPushInput collect = new GetHttpsApiRestShApiSCPushInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String cname = "cname";
collect.setCname(cname);

String file = "file";
collect.setFile(file);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
cDN.getHttpsApiRestShApiSCPushAsync(collect, new APICallBack<HttpsApiRestShApiSCPushRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSCPushRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="get_https_api_rest_sh_api_sc_pull_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CDNController.getHttpsApiRestShApiSCPullAsync") getHttpsApiRestShApiSCPullAsync

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```java
void getHttpsApiRestShApiSCPullAsync(
        final GetHttpsApiRestShApiSCPullInput input,
        final APICallBack<HttpsApiRestShApiSCPullRModel> callBack)
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
GetHttpsApiRestShApiSCPullInput collect = new GetHttpsApiRestShApiSCPullInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String origin = "origin";
collect.setOrigin(origin);

String cname = "cname";
collect.setCname(cname);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
cDN.getHttpsApiRestShApiSCPullAsync(collect, new APICallBack<HttpsApiRestShApiSCPullRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSCPullRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_sc_push_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CDNController.createHttpsApiRestShApiSCPushAsync") createHttpsApiRestShApiSCPushAsync

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```java
void createHttpsApiRestShApiSCPushAsync(
        final CreateHttpsApiRestShApiSCPushInput input,
        final APICallBack<HttpsApiRestShApiSCPushRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSCPushInput collect = new CreateHttpsApiRestShApiSCPushInput();

    HttpsApiRestShApiSCPushModel body = new HttpsApiRestShApiSCPushModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    cDN.createHttpsApiRestShApiSCPushAsync(collect, new APICallBack<HttpsApiRestShApiSCPushRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSCPushRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="create_https_api_rest_sh_api_sc_pull_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CDNController.createHttpsApiRestShApiSCPullAsync") createHttpsApiRestShApiSCPullAsync

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```java
void createHttpsApiRestShApiSCPullAsync(
        final CreateHttpsApiRestShApiSCPullInput input,
        final APICallBack<HttpsApiRestShApiSCPullRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSCPullInput collect = new CreateHttpsApiRestShApiSCPullInput();

    HttpsApiRestShApiSCPullModel body = new HttpsApiRestShApiSCPullModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    cDN.createHttpsApiRestShApiSCPullAsync(collect, new APICallBack<HttpsApiRestShApiSCPullRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSCPullRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.DNSController") DNSController

### Get singleton instance

The singleton instance of the ``` DNSController ``` class can be accessed from the API Client.

```java
DNSController dNS = client.getDNS();
```

### <a name="get_https_api_rest_sh_api_sdc_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DNSController.getHttpsApiRestShApiSDCAsync") getHttpsApiRestShApiSDCAsync

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```java
void getHttpsApiRestShApiSDCAsync(
        final GetHttpsApiRestShApiSDCInput input,
        final APICallBack<HttpsApiRestShApiSDCRModel> callBack)
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
GetHttpsApiRestShApiSDCInput collect = new GetHttpsApiRestShApiSDCInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String domain = "domain";
collect.setDomain(domain);

String records = "records";
collect.setRecords(records);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
dNS.getHttpsApiRestShApiSDCAsync(collect, new APICallBack<HttpsApiRestShApiSDCRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSDCRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_sdc_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DNSController.createHttpsApiRestShApiSDCAsync") createHttpsApiRestShApiSDCAsync

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```java
void createHttpsApiRestShApiSDCAsync(
        final CreateHttpsApiRestShApiSDCInput input,
        final APICallBack<HttpsApiRestShApiSDCRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSDCInput collect = new CreateHttpsApiRestShApiSDCInput();

    HttpsApiRestShApiSDCModel body = new HttpsApiRestShApiSDCModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    dNS.createHttpsApiRestShApiSDCAsync(collect, new APICallBack<HttpsApiRestShApiSDCRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSDCRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="get_https_api_rest_sh_api_sda_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DNSController.getHttpsApiRestShApiSDAAsync") getHttpsApiRestShApiSDAAsync

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```java
void getHttpsApiRestShApiSDAAsync(
        final GetHttpsApiRestShApiSDAInput input,
        final APICallBack<HttpsApiRestShApiSDARModel> callBack)
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
GetHttpsApiRestShApiSDAInput collect = new GetHttpsApiRestShApiSDAInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String domain = "domain";
collect.setDomain(domain);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
dNS.getHttpsApiRestShApiSDAAsync(collect, new APICallBack<HttpsApiRestShApiSDARModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSDARModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_sda_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DNSController.createHttpsApiRestShApiSDAAsync") createHttpsApiRestShApiSDAAsync

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```java
void createHttpsApiRestShApiSDAAsync(
        final CreateHttpsApiRestShApiSDAInput input,
        final APICallBack<HttpsApiRestShApiSDARModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSDAInput collect = new CreateHttpsApiRestShApiSDAInput();

    HttpsApiRestShApiSDAModel body = new HttpsApiRestShApiSDAModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    dNS.createHttpsApiRestShApiSDAAsync(collect, new APICallBack<HttpsApiRestShApiSDARModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSDARModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.CodeObfuscationController") CodeObfuscationController

### Get singleton instance

The singleton instance of the ``` CodeObfuscationController ``` class can be accessed from the API Client.

```java
CodeObfuscationController codeObfuscation = client.getCodeObfuscation();
```

### <a name="get_https_api_rest_sh_api_so_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CodeObfuscationController.getHttpsApiRestShApiSOAsync") getHttpsApiRestShApiSOAsync

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```java
void getHttpsApiRestShApiSOAsync(
        final GetHttpsApiRestShApiSOInput input,
        final APICallBack<HttpsApiRestShApiSORModel> callBack)
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
GetHttpsApiRestShApiSOInput collect = new GetHttpsApiRestShApiSOInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String app = "app";
collect.setApp(app);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
codeObfuscation.getHttpsApiRestShApiSOAsync(collect, new APICallBack<HttpsApiRestShApiSORModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSORModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_so_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CodeObfuscationController.createHttpsApiRestShApiSOAsync") createHttpsApiRestShApiSOAsync

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```java
void createHttpsApiRestShApiSOAsync(
        final CreateHttpsApiRestShApiSOInput input,
        final APICallBack<HttpsApiRestShApiSORModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSOInput collect = new CreateHttpsApiRestShApiSOInput();

    HttpsApiRestShApiSOModel body = new HttpsApiRestShApiSOModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    codeObfuscation.createHttpsApiRestShApiSOAsync(collect, new APICallBack<HttpsApiRestShApiSORModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSORModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.HostingController") HostingController

### Get singleton instance

The singleton instance of the ``` HostingController ``` class can be accessed from the API Client.

```java
HostingController hosting = client.getHosting();
```

### <a name="get_https_api_rest_sh_api_sh_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.HostingController.getHttpsApiRestShApiSHAsync") getHttpsApiRestShApiSHAsync

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```java
void getHttpsApiRestShApiSHAsync(
        final GetHttpsApiRestShApiSHInput input,
        final APICallBack<HttpsApiRestShApiSHRModel> callBack)
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
GetHttpsApiRestShApiSHInput collect = new GetHttpsApiRestShApiSHInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String app = "app";
collect.setApp(app);

String domain = "domain";
collect.setDomain(domain);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
hosting.getHttpsApiRestShApiSHAsync(collect, new APICallBack<HttpsApiRestShApiSHRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSHRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_sh_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.HostingController.createHttpsApiRestShApiSHAsync") createHttpsApiRestShApiSHAsync

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```java
void createHttpsApiRestShApiSHAsync(
        final CreateHttpsApiRestShApiSHInput input,
        final APICallBack<HttpsApiRestShApiSHRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSHInput collect = new CreateHttpsApiRestShApiSHInput();

    HttpsApiRestShApiSHModel body = new HttpsApiRestShApiSHModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    hosting.createHttpsApiRestShApiSHAsync(collect, new APICallBack<HttpsApiRestShApiSHRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSHRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.DataManipulationConversionSortingAndCompressionAPIController") DataManipulationConversionSortingAndCompressionAPIController

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPIController ``` class can be accessed from the API Client.

```java
DataManipulationConversionSortingAndCompressionAPIController dataManipulationConversionSortingAndCompressionAPI = client.getDataManipulationConversionSortingAndCompressionAPI();
```

### <a name="get_https_api_rest_sh_api_d_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DataManipulationConversionSortingAndCompressionAPIController.getHttpsApiRestShApiDAsync") getHttpsApiRestShApiDAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void getHttpsApiRestShApiDAsync(
        final GetHttpsApiRestShApiDInput input,
        final APICallBack<HttpsApiRestShApiDRModel> callBack)
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
GetHttpsApiRestShApiDInput collect = new GetHttpsApiRestShApiDInput();

String key = "API";
collect.setKey(key);

String uid = "UID";
collect.setUid(uid);

String user = "UID";
collect.setUser(user);

String apiuid = "apiUID";
collect.setApiuid(apiuid);

String data = "https://static.yourcdn.com/data.file";
collect.setData(data);

String contentType = "application/json";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
dataManipulationConversionSortingAndCompressionAPI.getHttpsApiRestShApiDAsync(collect, new APICallBack<HttpsApiRestShApiDRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiDRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_d_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DataManipulationConversionSortingAndCompressionAPIController.createHttpsApiRestShApiDAsync") createHttpsApiRestShApiDAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void createHttpsApiRestShApiDAsync(
        final CreateHttpsApiRestShApiDInput input,
        final APICallBack<HttpsApiRestShApiDRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiDInput collect = new CreateHttpsApiRestShApiDInput();

    String bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}";
    HttpsApiRestShApiDModel body = mapper.readValue(bodyValue,new TypeReference<HttpsApiRestShApiDModel> (){});
collect.setBody(body);

    String contentType = "application/json";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    dataManipulationConversionSortingAndCompressionAPI.createHttpsApiRestShApiDAsync(collect, new APICallBack<HttpsApiRestShApiDRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiDRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.ImageManipulationAndModerationAPIController") ImageManipulationAndModerationAPIController

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPIController ``` class can be accessed from the API Client.

```java
ImageManipulationAndModerationAPIController imageManipulationAndModerationAPI = client.getImageManipulationAndModerationAPI();
```

### <a name="get_https_api_rest_sh_api_i_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.ImageManipulationAndModerationAPIController.getHttpsApiRestShApiIAsync") getHttpsApiRestShApiIAsync

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```java
void getHttpsApiRestShApiIAsync(
        final GetHttpsApiRestShApiIInput input,
        final APICallBack<HttpsApiRestShApiIRModel> callBack)
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
GetHttpsApiRestShApiIInput collect = new GetHttpsApiRestShApiIInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String image = "image";
collect.setImage(image);

String transform = "transform";
collect.setTransform(transform);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
imageManipulationAndModerationAPI.getHttpsApiRestShApiIAsync(collect, new APICallBack<HttpsApiRestShApiIRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiIRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_i_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.ImageManipulationAndModerationAPIController.createHttpsApiRestShApiIAsync") createHttpsApiRestShApiIAsync

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```java
void createHttpsApiRestShApiIAsync(
        final CreateHttpsApiRestShApiIInput input,
        final APICallBack<HttpsApiRestShApiIRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiIInput collect = new CreateHttpsApiRestShApiIInput();

    HttpsApiRestShApiIModel body = new HttpsApiRestShApiIModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    imageManipulationAndModerationAPI.createHttpsApiRestShApiIAsync(collect, new APICallBack<HttpsApiRestShApiIRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiIRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.VerificationController") VerificationController

### Get singleton instance

The singleton instance of the ``` VerificationController ``` class can be accessed from the API Client.

```java
VerificationController verification = client.getVerification();
```

### <a name="get_https_api_rest_sh_api_va_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.VerificationController.getHttpsApiRestShApiVAAsync") getHttpsApiRestShApiVAAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```java
void getHttpsApiRestShApiVAAsync(
        final GetHttpsApiRestShApiVAInput input,
        final APICallBack<HttpsApiRestShApiVARModel> callBack)
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
GetHttpsApiRestShApiVAInput collect = new GetHttpsApiRestShApiVAInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String user = "user";
collect.setUser(user);

String a = "a";
collect.setA(a);

String sa = "sa";
collect.setSa(sa);

String c = "c";
collect.setC(c);

String s = "s";
collect.setS(s);

int z = 248;
collect.setZ(z);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
verification.getHttpsApiRestShApiVAAsync(collect, new APICallBack<HttpsApiRestShApiVARModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiVARModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_va_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.VerificationController.createHttpsApiRestShApiVAAsync") createHttpsApiRestShApiVAAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```java
void createHttpsApiRestShApiVAAsync(
        final CreateHttpsApiRestShApiVAInput input,
        final APICallBack<HttpsApiRestShApiVARModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiVAInput collect = new CreateHttpsApiRestShApiVAInput();

    HttpsApiRestShApiVAModel body = new HttpsApiRestShApiVAModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    verification.createHttpsApiRestShApiVAAsync(collect, new APICallBack<HttpsApiRestShApiVARModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiVARModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="get_https_api_rest_sh_api_vu_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.VerificationController.getHttpsApiRestShApiVUAsync") getHttpsApiRestShApiVUAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```java
void getHttpsApiRestShApiVUAsync(
        final GetHttpsApiRestShApiVUInput input,
        final APICallBack<HttpsApiRestShApiVURModel> callBack)
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
GetHttpsApiRestShApiVUInput collect = new GetHttpsApiRestShApiVUInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String user = "user";
collect.setUser(user);

String code = "code";
collect.setCode(code);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
verification.getHttpsApiRestShApiVUAsync(collect, new APICallBack<HttpsApiRestShApiVURModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiVURModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_vu_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.VerificationController.createHttpsApiRestShApiVUAsync") createHttpsApiRestShApiVUAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```java
void createHttpsApiRestShApiVUAsync(
        final CreateHttpsApiRestShApiVUInput input,
        final APICallBack<HttpsApiRestShApiVURModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiVUInput collect = new CreateHttpsApiRestShApiVUInput();

    HttpsApiRestShApiVUModel body = new HttpsApiRestShApiVUModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    verification.createHttpsApiRestShApiVUAsync(collect, new APICallBack<HttpsApiRestShApiVURModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiVURModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="get_https_api_rest_sh_api_v_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.VerificationController.getHttpsApiRestShApiVAsync") getHttpsApiRestShApiVAsync

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```java
void getHttpsApiRestShApiVAsync(
        final GetHttpsApiRestShApiVInput input,
        final APICallBack<HttpsApiRestShApiVRModel> callBack)
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
GetHttpsApiRestShApiVInput collect = new GetHttpsApiRestShApiVInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String to = "to";
collect.setTo(to);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
verification.getHttpsApiRestShApiVAsync(collect, new APICallBack<HttpsApiRestShApiVRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiVRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_v_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.VerificationController.createHttpsApiRestShApiVAsync") createHttpsApiRestShApiVAsync

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```java
void createHttpsApiRestShApiVAsync(
        final CreateHttpsApiRestShApiVInput input,
        final APICallBack<HttpsApiRestShApiVRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiVInput collect = new CreateHttpsApiRestShApiVInput();

    HttpsApiRestShApiVModel body = new HttpsApiRestShApiVModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    verification.createHttpsApiRestShApiVAsync(collect, new APICallBack<HttpsApiRestShApiVRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiVRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.TwoFactorAuthenticationAPIController") TwoFactorAuthenticationAPIController

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPIController ``` class can be accessed from the API Client.

```java
TwoFactorAuthenticationAPIController twoFactorAuthenticationAPI = client.getTwoFactorAuthenticationAPI();
```

### <a name="get_https_api_rest_sh_api2fa_t_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2faTAsync") getHttpsApiRestShApi2faTAsync

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```java
void getHttpsApiRestShApi2faTAsync(
        final GetHttpsApiRestShApi2faTInput input,
        final APICallBack<HttpsApiRestShApi2faTRModel> callBack)
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
GetHttpsApiRestShApi2faTInput collect = new GetHttpsApiRestShApi2faTInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String user = "user";
collect.setUser(user);

String code = "code";
collect.setCode(code);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
twoFactorAuthenticationAPI.getHttpsApiRestShApi2faTAsync(collect, new APICallBack<HttpsApiRestShApi2faTRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApi2faTRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api2fa_t_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2faTAsync") createHttpsApiRestShApi2faTAsync

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```java
void createHttpsApiRestShApi2faTAsync(
        final CreateHttpsApiRestShApi2faTInput input,
        final APICallBack<HttpsApiRestShApi2faTRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApi2faTInput collect = new CreateHttpsApiRestShApi2faTInput();

    HttpsApiRestShApi2faTModel body = new HttpsApiRestShApi2faTModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    twoFactorAuthenticationAPI.createHttpsApiRestShApi2faTAsync(collect, new APICallBack<HttpsApiRestShApi2faTRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApi2faTRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="get_https_api_rest_sh_api2fa_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2faAsync") getHttpsApiRestShApi2faAsync

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```java
void getHttpsApiRestShApi2faAsync(
        final GetHttpsApiRestShApi2faInput input,
        final APICallBack<HttpsApiRestShApi2faRModel> callBack)
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
GetHttpsApiRestShApi2faInput collect = new GetHttpsApiRestShApi2faInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String to = "to";
collect.setTo(to);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
twoFactorAuthenticationAPI.getHttpsApiRestShApi2faAsync(collect, new APICallBack<HttpsApiRestShApi2faRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApi2faRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api2fa_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2faAsync") createHttpsApiRestShApi2faAsync

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```java
void createHttpsApiRestShApi2faAsync(
        final CreateHttpsApiRestShApi2faInput input,
        final APICallBack<HttpsApiRestShApi2faRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApi2faInput collect = new CreateHttpsApiRestShApi2faInput();

    HttpsApiRestShApi2faModel body = new HttpsApiRestShApi2faModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    twoFactorAuthenticationAPI.createHttpsApiRestShApi2faAsync(collect, new APICallBack<HttpsApiRestShApi2faRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApi2faRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.UserManagementController") UserManagementController

### Get singleton instance

The singleton instance of the ``` UserManagementController ``` class can be accessed from the API Client.

```java
UserManagementController userManagement = client.getUserManagement();
```

### <a name="get_https_api_rest_sh_api_ui_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagementController.getHttpsApiRestShApiUIAsync") getHttpsApiRestShApiUIAsync

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```java
void getHttpsApiRestShApiUIAsync(
        final GetHttpsApiRestShApiUIInput input,
        final APICallBack<HttpsApiRestShApiUIRModel> callBack)
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
GetHttpsApiRestShApiUIInput collect = new GetHttpsApiRestShApiUIInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String user = "user";
collect.setUser(user);

String apiuid = "apiuid";
collect.setApiuid(apiuid);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
userManagement.getHttpsApiRestShApiUIAsync(collect, new APICallBack<HttpsApiRestShApiUIRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiUIRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_ui_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagementController.createHttpsApiRestShApiUIAsync") createHttpsApiRestShApiUIAsync

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```java
void createHttpsApiRestShApiUIAsync(
        final CreateHttpsApiRestShApiUIInput input,
        final APICallBack<HttpsApiRestShApiUIRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiUIInput collect = new CreateHttpsApiRestShApiUIInput();

    HttpsApiRestShApiUIModel body = new HttpsApiRestShApiUIModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    userManagement.createHttpsApiRestShApiUIAsync(collect, new APICallBack<HttpsApiRestShApiUIRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiUIRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="get_https_api_rest_sh_api_uu_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagementController.getHttpsApiRestShApiUUAsync") getHttpsApiRestShApiUUAsync

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```java
void getHttpsApiRestShApiUUAsync(
        final GetHttpsApiRestShApiUUInput input,
        final APICallBack<HttpsApiRestShApiUURModel> callBack)
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
GetHttpsApiRestShApiUUInput collect = new GetHttpsApiRestShApiUUInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String user = "user";
collect.setUser(user);

String apiuid = "apiuid";
collect.setApiuid(apiuid);

String avatar = "avatar";
collect.setAvatar(avatar);

String customInput = "custom input";
collect.setCustomInput(customInput);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
userManagement.getHttpsApiRestShApiUUAsync(collect, new APICallBack<HttpsApiRestShApiUURModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiUURModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_uu_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagementController.createHttpsApiRestShApiUUAsync") createHttpsApiRestShApiUUAsync

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```java
void createHttpsApiRestShApiUUAsync(
        final CreateHttpsApiRestShApiUUInput input,
        final APICallBack<HttpsApiRestShApiUURModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiUUInput collect = new CreateHttpsApiRestShApiUUInput();

    HttpsApiRestShApiUUModel body = new HttpsApiRestShApiUUModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    userManagement.createHttpsApiRestShApiUUAsync(collect, new APICallBack<HttpsApiRestShApiUURModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiUURModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="get_https_api_rest_sh_api_ud_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagementController.getHttpsApiRestShApiUDAsync") getHttpsApiRestShApiUDAsync

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```java
void getHttpsApiRestShApiUDAsync(
        final GetHttpsApiRestShApiUDInput input,
        final APICallBack<HttpsApiRestShApiUDRModel> callBack)
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
GetHttpsApiRestShApiUDInput collect = new GetHttpsApiRestShApiUDInput();

String api = "api";
collect.setApi(api);

String uid = "uid";
collect.setUid(uid);

String user = "user";
collect.setUser(user);

String apiuid = "apiuid";
collect.setApiuid(apiuid);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
userManagement.getHttpsApiRestShApiUDAsync(collect, new APICallBack<HttpsApiRestShApiUDRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiUDRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_ud_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagementController.createHttpsApiRestShApiUDAsync") createHttpsApiRestShApiUDAsync

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```java
void createHttpsApiRestShApiUDAsync(
        final CreateHttpsApiRestShApiUDInput input,
        final APICallBack<HttpsApiRestShApiUDRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiUDInput collect = new CreateHttpsApiRestShApiUDInput();

    HttpsApiRestShApiUDModel body = new HttpsApiRestShApiUDModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    userManagement.createHttpsApiRestShApiUDAsync(collect, new APICallBack<HttpsApiRestShApiUDRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiUDRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.controllers.LoginAndRegistrationController") LoginAndRegistrationController

### Get singleton instance

The singleton instance of the ``` LoginAndRegistrationController ``` class can be accessed from the API Client.

```java
LoginAndRegistrationController loginAndRegistration = client.getLoginAndRegistration();
```

### <a name="get_https_api_rest_sh_api_aur_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.LoginAndRegistrationController.getHttpsApiRestShApiAURAsync") getHttpsApiRestShApiAURAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```java
void getHttpsApiRestShApiAURAsync(
        final GetHttpsApiRestShApiAURInput input,
        final APICallBack<HttpsApiRestShApiAURRModel> callBack)
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
GetHttpsApiRestShApiAURInput collect = new GetHttpsApiRestShApiAURInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String user = "user";
collect.setUser(user);

String password = "password";
collect.setPassword(password);

String name = "name";
collect.setName(name);

String email = "email";
collect.setEmail(email);

int phone = 248;
collect.setPhone(phone);

int countrycode = 248;
collect.setCountrycode(countrycode);

String address = "address";
collect.setAddress(address);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
loginAndRegistration.getHttpsApiRestShApiAURAsync(collect, new APICallBack<HttpsApiRestShApiAURRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiAURRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_aur_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.LoginAndRegistrationController.createHttpsApiRestShApiAURAsync") createHttpsApiRestShApiAURAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```java
void createHttpsApiRestShApiAURAsync(
        final CreateHttpsApiRestShApiAURInput input,
        final APICallBack<HttpsApiRestShApiAURRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiAURInput collect = new CreateHttpsApiRestShApiAURInput();

    HttpsApiRestShApiAURModel body = new HttpsApiRestShApiAURModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    loginAndRegistration.createHttpsApiRestShApiAURAsync(collect, new APICallBack<HttpsApiRestShApiAURRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiAURRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="get_https_api_rest_sh_api_aul_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.LoginAndRegistrationController.getHttpsApiRestShApiAULAsync") getHttpsApiRestShApiAULAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```java
void getHttpsApiRestShApiAULAsync(
        final GetHttpsApiRestShApiAULInput input,
        final APICallBack<HttpsApiRestShApiAULRModel> callBack)
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
GetHttpsApiRestShApiAULInput collect = new GetHttpsApiRestShApiAULInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String user = "user";
collect.setUser(user);

String password = "password";
collect.setPassword(password);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
loginAndRegistration.getHttpsApiRestShApiAULAsync(collect, new APICallBack<HttpsApiRestShApiAULRModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiAULRModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_aul_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.LoginAndRegistrationController.createHttpsApiRestShApiAULAsync") createHttpsApiRestShApiAULAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```java
void createHttpsApiRestShApiAULAsync(
        final CreateHttpsApiRestShApiAULInput input,
        final APICallBack<HttpsApiRestShApiAULRModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiAULInput collect = new CreateHttpsApiRestShApiAULInput();

    HttpsApiRestShApiAULModel body = new HttpsApiRestShApiAULModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    loginAndRegistration.createHttpsApiRestShApiAULAsync(collect, new APICallBack<HttpsApiRestShApiAULRModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiAULRModel response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    }
);
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)



