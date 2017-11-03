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

### <a name="get_https_api_rest_sh_api_security_logging_info_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.AdvancedLoggingController.getHttpsApiRestShApiSecurityLoggingInfoAsync") getHttpsApiRestShApiSecurityLoggingInfoAsync

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```java
void getHttpsApiRestShApiSecurityLoggingInfoAsync(
        final GetHttpsApiRestShApiSecurityLoggingInfoInput input,
        final APICallBack<HttpsApiRestShApiSecurityLoggingInfoResponseModel> callBack)
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
GetHttpsApiRestShApiSecurityLoggingInfoInput collect = new GetHttpsApiRestShApiSecurityLoggingInfoInput();

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
advancedLogging.getHttpsApiRestShApiSecurityLoggingInfoAsync(collect, new APICallBack<HttpsApiRestShApiSecurityLoggingInfoResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSecurityLoggingInfoResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="get_https_api_rest_sh_api_security_logging_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.AdvancedLoggingController.getHttpsApiRestShApiSecurityLoggingAsync") getHttpsApiRestShApiSecurityLoggingAsync

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```java
void getHttpsApiRestShApiSecurityLoggingAsync(
        final GetHttpsApiRestShApiSecurityLoggingInput input,
        final APICallBack<HttpsApiRestShApiSecurityLoggingResponseModel> callBack)
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
GetHttpsApiRestShApiSecurityLoggingInput collect = new GetHttpsApiRestShApiSecurityLoggingInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String name = "name";
collect.setName(name);

String origin = "origin";
collect.setOrigin(origin);

boolean activate = true;
collect.setActivate(activate);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
advancedLogging.getHttpsApiRestShApiSecurityLoggingAsync(collect, new APICallBack<HttpsApiRestShApiSecurityLoggingResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSecurityLoggingResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_security_logging_info_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.AdvancedLoggingController.createHttpsApiRestShApiSecurityLoggingInfoAsync") createHttpsApiRestShApiSecurityLoggingInfoAsync

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```java
void createHttpsApiRestShApiSecurityLoggingInfoAsync(
        final CreateHttpsApiRestShApiSecurityLoggingInfoInput input,
        final APICallBack<HttpsApiRestShApiSecurityLoggingInfoResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSecurityLoggingInfoInput collect = new CreateHttpsApiRestShApiSecurityLoggingInfoInput();

    HttpsApiRestShApiSecurityLoggingInfoRequestModel body = new HttpsApiRestShApiSecurityLoggingInfoRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    advancedLogging.createHttpsApiRestShApiSecurityLoggingInfoAsync(collect, new APICallBack<HttpsApiRestShApiSecurityLoggingInfoResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSecurityLoggingInfoResponseModel response) {
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


### <a name="create_https_api_rest_sh_api_security_logging_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.AdvancedLoggingController.createHttpsApiRestShApiSecurityLoggingAsync") createHttpsApiRestShApiSecurityLoggingAsync

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```java
void createHttpsApiRestShApiSecurityLoggingAsync(
        final CreateHttpsApiRestShApiSecurityLoggingInput input,
        final APICallBack<HttpsApiRestShApiSecurityLoggingResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSecurityLoggingInput collect = new CreateHttpsApiRestShApiSecurityLoggingInput();

    HttpsApiRestShApiSecurityLoggingRequestModel body = new HttpsApiRestShApiSecurityLoggingRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    advancedLogging.createHttpsApiRestShApiSecurityLoggingAsync(collect, new APICallBack<HttpsApiRestShApiSecurityLoggingResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSecurityLoggingResponseModel response) {
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

### <a name="get_https_api_rest_sh_api_security_waf_configure_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.WAFDDOSProtectionController.getHttpsApiRestShApiSecurityWafConfigureAsync") getHttpsApiRestShApiSecurityWafConfigureAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void getHttpsApiRestShApiSecurityWafConfigureAsync(
        final GetHttpsApiRestShApiSecurityWafConfigureInput input,
        final APICallBack<HttpsApiRestShApiSecurityWafConfigureResponseModel> callBack)
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
GetHttpsApiRestShApiSecurityWafConfigureInput collect = new GetHttpsApiRestShApiSecurityWafConfigureInput();

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
wAFDDOSProtection.getHttpsApiRestShApiSecurityWafConfigureAsync(collect, new APICallBack<HttpsApiRestShApiSecurityWafConfigureResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSecurityWafConfigureResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="get_https_api_rest_sh_api_security_waf_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.WAFDDOSProtectionController.getHttpsApiRestShApiSecurityWafAsync") getHttpsApiRestShApiSecurityWafAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void getHttpsApiRestShApiSecurityWafAsync(
        final GetHttpsApiRestShApiSecurityWafInput input,
        final APICallBack<HttpsApiRestShApiSecurityWafResponseModel> callBack)
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
GetHttpsApiRestShApiSecurityWafInput collect = new GetHttpsApiRestShApiSecurityWafInput();

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
wAFDDOSProtection.getHttpsApiRestShApiSecurityWafAsync(collect, new APICallBack<HttpsApiRestShApiSecurityWafResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSecurityWafResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_security_waf_configure_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.WAFDDOSProtectionController.createHttpsApiRestShApiSecurityWafConfigureAsync") createHttpsApiRestShApiSecurityWafConfigureAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void createHttpsApiRestShApiSecurityWafConfigureAsync(
        final CreateHttpsApiRestShApiSecurityWafConfigureInput input,
        final APICallBack<HttpsApiRestShApiSecurityWafConfigureResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSecurityWafConfigureInput collect = new CreateHttpsApiRestShApiSecurityWafConfigureInput();

    String bodyValue = "{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}";
    HttpsApiRestShApiSecurityWafConfigureRequestModel body = mapper.readValue(bodyValue,new TypeReference<HttpsApiRestShApiSecurityWafConfigureRequestModel> (){});
collect.setBody(body);

    String contentType = "application/json";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    wAFDDOSProtection.createHttpsApiRestShApiSecurityWafConfigureAsync(collect, new APICallBack<HttpsApiRestShApiSecurityWafConfigureResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSecurityWafConfigureResponseModel response) {
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


### <a name="create_https_api_rest_sh_api_security_waf_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.WAFDDOSProtectionController.createHttpsApiRestShApiSecurityWafAsync") createHttpsApiRestShApiSecurityWafAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void createHttpsApiRestShApiSecurityWafAsync(
        final CreateHttpsApiRestShApiSecurityWafInput input,
        final APICallBack<HttpsApiRestShApiSecurityWafResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSecurityWafInput collect = new CreateHttpsApiRestShApiSecurityWafInput();

    String bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}";
    HttpsApiRestShApiSecurityWafRequestModel body = mapper.readValue(bodyValue,new TypeReference<HttpsApiRestShApiSecurityWafRequestModel> (){});
collect.setBody(body);

    String contentType = "application/json";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    wAFDDOSProtection.createHttpsApiRestShApiSecurityWafAsync(collect, new APICallBack<HttpsApiRestShApiSecurityWafResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSecurityWafResponseModel response) {
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

### <a name="get_https_api_rest_sh_api_security_encryption_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.EncryptionController.getHttpsApiRestShApiSecurityEncryptionAsync") getHttpsApiRestShApiSecurityEncryptionAsync

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```java
void getHttpsApiRestShApiSecurityEncryptionAsync(
        final GetHttpsApiRestShApiSecurityEncryptionInput input,
        final APICallBack<HttpsApiRestShApiSecurityEncryptionResponseModel> callBack)
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
GetHttpsApiRestShApiSecurityEncryptionInput collect = new GetHttpsApiRestShApiSecurityEncryptionInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String data = "data";
collect.setData(data);

String method = "method";
collect.setMethod(method);

int bit = 243;
collect.setBit(bit);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
encryption.getHttpsApiRestShApiSecurityEncryptionAsync(collect, new APICallBack<HttpsApiRestShApiSecurityEncryptionResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiSecurityEncryptionResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_security_encryption_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.EncryptionController.createHttpsApiRestShApiSecurityEncryptionAsync") createHttpsApiRestShApiSecurityEncryptionAsync

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```java
void createHttpsApiRestShApiSecurityEncryptionAsync(
        final CreateHttpsApiRestShApiSecurityEncryptionInput input,
        final APICallBack<HttpsApiRestShApiSecurityEncryptionResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiSecurityEncryptionInput collect = new CreateHttpsApiRestShApiSecurityEncryptionInput();

    HttpsApiRestShApiSecurityEncryptionRequestModel body = new HttpsApiRestShApiSecurityEncryptionRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    encryption.createHttpsApiRestShApiSecurityEncryptionAsync(collect, new APICallBack<HttpsApiRestShApiSecurityEncryptionResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiSecurityEncryptionResponseModel response) {
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

### <a name="get_https_api_rest_sh_api_service_cdn_push_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CDNController.getHttpsApiRestShApiServiceCdnPushAsync") getHttpsApiRestShApiServiceCdnPushAsync

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```java
void getHttpsApiRestShApiServiceCdnPushAsync(
        final GetHttpsApiRestShApiServiceCdnPushInput input,
        final APICallBack<HttpsApiRestShApiServiceCdnPushResponseModel> callBack)
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
GetHttpsApiRestShApiServiceCdnPushInput collect = new GetHttpsApiRestShApiServiceCdnPushInput();

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
cDN.getHttpsApiRestShApiServiceCdnPushAsync(collect, new APICallBack<HttpsApiRestShApiServiceCdnPushResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiServiceCdnPushResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="get_https_api_rest_sh_api_service_cdn_pull_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CDNController.getHttpsApiRestShApiServiceCdnPullAsync") getHttpsApiRestShApiServiceCdnPullAsync

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```java
void getHttpsApiRestShApiServiceCdnPullAsync(
        final GetHttpsApiRestShApiServiceCdnPullInput input,
        final APICallBack<HttpsApiRestShApiServiceCdnPullResponseModel> callBack)
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
GetHttpsApiRestShApiServiceCdnPullInput collect = new GetHttpsApiRestShApiServiceCdnPullInput();

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
cDN.getHttpsApiRestShApiServiceCdnPullAsync(collect, new APICallBack<HttpsApiRestShApiServiceCdnPullResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiServiceCdnPullResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_service_cdn_push_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CDNController.createHttpsApiRestShApiServiceCdnPushAsync") createHttpsApiRestShApiServiceCdnPushAsync

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```java
void createHttpsApiRestShApiServiceCdnPushAsync(
        final CreateHttpsApiRestShApiServiceCdnPushInput input,
        final APICallBack<HttpsApiRestShApiServiceCdnPushResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiServiceCdnPushInput collect = new CreateHttpsApiRestShApiServiceCdnPushInput();

    HttpsApiRestShApiServiceCdnPushRequestModel body = new HttpsApiRestShApiServiceCdnPushRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    cDN.createHttpsApiRestShApiServiceCdnPushAsync(collect, new APICallBack<HttpsApiRestShApiServiceCdnPushResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiServiceCdnPushResponseModel response) {
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


### <a name="create_https_api_rest_sh_api_service_cdn_pull_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CDNController.createHttpsApiRestShApiServiceCdnPullAsync") createHttpsApiRestShApiServiceCdnPullAsync

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```java
void createHttpsApiRestShApiServiceCdnPullAsync(
        final CreateHttpsApiRestShApiServiceCdnPullInput input,
        final APICallBack<HttpsApiRestShApiServiceCdnPullResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiServiceCdnPullInput collect = new CreateHttpsApiRestShApiServiceCdnPullInput();

    HttpsApiRestShApiServiceCdnPullRequestModel body = new HttpsApiRestShApiServiceCdnPullRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    cDN.createHttpsApiRestShApiServiceCdnPullAsync(collect, new APICallBack<HttpsApiRestShApiServiceCdnPullResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiServiceCdnPullResponseModel response) {
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

### <a name="get_https_api_rest_sh_api_service_dns_configure_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DNSController.getHttpsApiRestShApiServiceDnsConfigureAsync") getHttpsApiRestShApiServiceDnsConfigureAsync

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```java
void getHttpsApiRestShApiServiceDnsConfigureAsync(
        final GetHttpsApiRestShApiServiceDnsConfigureInput input,
        final APICallBack<HttpsApiRestShApiServiceDnsConfigureResponseModel> callBack)
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
GetHttpsApiRestShApiServiceDnsConfigureInput collect = new GetHttpsApiRestShApiServiceDnsConfigureInput();

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
dNS.getHttpsApiRestShApiServiceDnsConfigureAsync(collect, new APICallBack<HttpsApiRestShApiServiceDnsConfigureResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiServiceDnsConfigureResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_service_dns_configure_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DNSController.createHttpsApiRestShApiServiceDnsConfigureAsync") createHttpsApiRestShApiServiceDnsConfigureAsync

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```java
void createHttpsApiRestShApiServiceDnsConfigureAsync(
        final CreateHttpsApiRestShApiServiceDnsConfigureInput input,
        final APICallBack<HttpsApiRestShApiServiceDnsConfigureResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiServiceDnsConfigureInput collect = new CreateHttpsApiRestShApiServiceDnsConfigureInput();

    HttpsApiRestShApiServiceDnsConfigureRequestModel body = new HttpsApiRestShApiServiceDnsConfigureRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    dNS.createHttpsApiRestShApiServiceDnsConfigureAsync(collect, new APICallBack<HttpsApiRestShApiServiceDnsConfigureResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiServiceDnsConfigureResponseModel response) {
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


### <a name="get_https_api_rest_sh_api_service_dns_add_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DNSController.getHttpsApiRestShApiServiceDnsAddAsync") getHttpsApiRestShApiServiceDnsAddAsync

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```java
void getHttpsApiRestShApiServiceDnsAddAsync(
        final GetHttpsApiRestShApiServiceDnsAddInput input,
        final APICallBack<HttpsApiRestShApiServiceDnsAddResponseModel> callBack)
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
GetHttpsApiRestShApiServiceDnsAddInput collect = new GetHttpsApiRestShApiServiceDnsAddInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String domain = "domain";
collect.setDomain(domain);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
dNS.getHttpsApiRestShApiServiceDnsAddAsync(collect, new APICallBack<HttpsApiRestShApiServiceDnsAddResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiServiceDnsAddResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_service_dns_add_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DNSController.createHttpsApiRestShApiServiceDnsAddAsync") createHttpsApiRestShApiServiceDnsAddAsync

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```java
void createHttpsApiRestShApiServiceDnsAddAsync(
        final CreateHttpsApiRestShApiServiceDnsAddInput input,
        final APICallBack<HttpsApiRestShApiServiceDnsAddResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiServiceDnsAddInput collect = new CreateHttpsApiRestShApiServiceDnsAddInput();

    HttpsApiRestShApiServiceDnsAddRequestModel body = new HttpsApiRestShApiServiceDnsAddRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    dNS.createHttpsApiRestShApiServiceDnsAddAsync(collect, new APICallBack<HttpsApiRestShApiServiceDnsAddResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiServiceDnsAddResponseModel response) {
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

### <a name="get_https_api_rest_sh_api_service_obfuscation_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CodeObfuscationController.getHttpsApiRestShApiServiceObfuscationAsync") getHttpsApiRestShApiServiceObfuscationAsync

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```java
void getHttpsApiRestShApiServiceObfuscationAsync(
        final GetHttpsApiRestShApiServiceObfuscationInput input,
        final APICallBack<HttpsApiRestShApiServiceObfuscationResponseModel> callBack)
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
GetHttpsApiRestShApiServiceObfuscationInput collect = new GetHttpsApiRestShApiServiceObfuscationInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String app = "app";
collect.setApp(app);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
codeObfuscation.getHttpsApiRestShApiServiceObfuscationAsync(collect, new APICallBack<HttpsApiRestShApiServiceObfuscationResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiServiceObfuscationResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_service_obfuscation_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.CodeObfuscationController.createHttpsApiRestShApiServiceObfuscationAsync") createHttpsApiRestShApiServiceObfuscationAsync

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```java
void createHttpsApiRestShApiServiceObfuscationAsync(
        final CreateHttpsApiRestShApiServiceObfuscationInput input,
        final APICallBack<HttpsApiRestShApiServiceObfuscationResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiServiceObfuscationInput collect = new CreateHttpsApiRestShApiServiceObfuscationInput();

    HttpsApiRestShApiServiceObfuscationRequestModel body = new HttpsApiRestShApiServiceObfuscationRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    codeObfuscation.createHttpsApiRestShApiServiceObfuscationAsync(collect, new APICallBack<HttpsApiRestShApiServiceObfuscationResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiServiceObfuscationResponseModel response) {
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

### <a name="get_https_api_rest_sh_api_service_hosting_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.HostingController.getHttpsApiRestShApiServiceHostingAsync") getHttpsApiRestShApiServiceHostingAsync

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```java
void getHttpsApiRestShApiServiceHostingAsync(
        final GetHttpsApiRestShApiServiceHostingInput input,
        final APICallBack<HttpsApiRestShApiServiceHostingResponseModel> callBack)
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
GetHttpsApiRestShApiServiceHostingInput collect = new GetHttpsApiRestShApiServiceHostingInput();

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
hosting.getHttpsApiRestShApiServiceHostingAsync(collect, new APICallBack<HttpsApiRestShApiServiceHostingResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiServiceHostingResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_service_hosting_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.HostingController.createHttpsApiRestShApiServiceHostingAsync") createHttpsApiRestShApiServiceHostingAsync

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```java
void createHttpsApiRestShApiServiceHostingAsync(
        final CreateHttpsApiRestShApiServiceHostingInput input,
        final APICallBack<HttpsApiRestShApiServiceHostingResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiServiceHostingInput collect = new CreateHttpsApiRestShApiServiceHostingInput();

    HttpsApiRestShApiServiceHostingRequestModel body = new HttpsApiRestShApiServiceHostingRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    hosting.createHttpsApiRestShApiServiceHostingAsync(collect, new APICallBack<HttpsApiRestShApiServiceHostingResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiServiceHostingResponseModel response) {
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

### <a name="get_https_api_rest_sh_api_data_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DataManipulationConversionSortingAndCompressionAPIController.getHttpsApiRestShApiDataAsync") getHttpsApiRestShApiDataAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void getHttpsApiRestShApiDataAsync(
        final GetHttpsApiRestShApiDataInput input,
        final APICallBack<HttpsApiRestShApiDataResponseModel> callBack)
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
GetHttpsApiRestShApiDataInput collect = new GetHttpsApiRestShApiDataInput();

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
dataManipulationConversionSortingAndCompressionAPI.getHttpsApiRestShApiDataAsync(collect, new APICallBack<HttpsApiRestShApiDataResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiDataResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_data_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.DataManipulationConversionSortingAndCompressionAPIController.createHttpsApiRestShApiDataAsync") createHttpsApiRestShApiDataAsync

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```java
void createHttpsApiRestShApiDataAsync(
        final CreateHttpsApiRestShApiDataInput input,
        final APICallBack<HttpsApiRestShApiDataResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiDataInput collect = new CreateHttpsApiRestShApiDataInput();

    String bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}";
    HttpsApiRestShApiDataRequestModel body = mapper.readValue(bodyValue,new TypeReference<HttpsApiRestShApiDataRequestModel> (){});
collect.setBody(body);

    String contentType = "application/json";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    dataManipulationConversionSortingAndCompressionAPI.createHttpsApiRestShApiDataAsync(collect, new APICallBack<HttpsApiRestShApiDataResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiDataResponseModel response) {
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

### <a name="get_https_api_rest_sh_api_image_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.ImageManipulationAndModerationAPIController.getHttpsApiRestShApiImageAsync") getHttpsApiRestShApiImageAsync

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```java
void getHttpsApiRestShApiImageAsync(
        final GetHttpsApiRestShApiImageInput input,
        final APICallBack<HttpsApiRestShApiImageResponseModel> callBack)
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
GetHttpsApiRestShApiImageInput collect = new GetHttpsApiRestShApiImageInput();

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
imageManipulationAndModerationAPI.getHttpsApiRestShApiImageAsync(collect, new APICallBack<HttpsApiRestShApiImageResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiImageResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_image_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.ImageManipulationAndModerationAPIController.createHttpsApiRestShApiImageAsync") createHttpsApiRestShApiImageAsync

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```java
void createHttpsApiRestShApiImageAsync(
        final CreateHttpsApiRestShApiImageInput input,
        final APICallBack<HttpsApiRestShApiImageResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiImageInput collect = new CreateHttpsApiRestShApiImageInput();

    HttpsApiRestShApiImageRequestModel body = new HttpsApiRestShApiImageRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    imageManipulationAndModerationAPI.createHttpsApiRestShApiImageAsync(collect, new APICallBack<HttpsApiRestShApiImageResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiImageResponseModel response) {
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

### <a name="get_https_api_rest_sh_api_verify_address_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.VerificationController.getHttpsApiRestShApiVerifyAddressAsync") getHttpsApiRestShApiVerifyAddressAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```java
void getHttpsApiRestShApiVerifyAddressAsync(
        final GetHttpsApiRestShApiVerifyAddressInput input,
        final APICallBack<HttpsApiRestShApiVerifyAddressResponseModel> callBack)
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
GetHttpsApiRestShApiVerifyAddressInput collect = new GetHttpsApiRestShApiVerifyAddressInput();

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

int z = 201;
collect.setZ(z);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
verification.getHttpsApiRestShApiVerifyAddressAsync(collect, new APICallBack<HttpsApiRestShApiVerifyAddressResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiVerifyAddressResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_verify_address_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.VerificationController.createHttpsApiRestShApiVerifyAddressAsync") createHttpsApiRestShApiVerifyAddressAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```java
void createHttpsApiRestShApiVerifyAddressAsync(
        final CreateHttpsApiRestShApiVerifyAddressInput input,
        final APICallBack<HttpsApiRestShApiVerifyAddressResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiVerifyAddressInput collect = new CreateHttpsApiRestShApiVerifyAddressInput();

    HttpsApiRestShApiVerifyAddressRequestModel body = new HttpsApiRestShApiVerifyAddressRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    verification.createHttpsApiRestShApiVerifyAddressAsync(collect, new APICallBack<HttpsApiRestShApiVerifyAddressResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiVerifyAddressResponseModel response) {
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


### <a name="get_https_api_rest_sh_api_verify_user_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.VerificationController.getHttpsApiRestShApiVerifyUserAsync") getHttpsApiRestShApiVerifyUserAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```java
void getHttpsApiRestShApiVerifyUserAsync(
        final GetHttpsApiRestShApiVerifyUserInput input,
        final APICallBack<HttpsApiRestShApiVerifyUserResponseModel> callBack)
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
GetHttpsApiRestShApiVerifyUserInput collect = new GetHttpsApiRestShApiVerifyUserInput();

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
verification.getHttpsApiRestShApiVerifyUserAsync(collect, new APICallBack<HttpsApiRestShApiVerifyUserResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiVerifyUserResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_verify_user_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.VerificationController.createHttpsApiRestShApiVerifyUserAsync") createHttpsApiRestShApiVerifyUserAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```java
void createHttpsApiRestShApiVerifyUserAsync(
        final CreateHttpsApiRestShApiVerifyUserInput input,
        final APICallBack<HttpsApiRestShApiVerifyUserResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiVerifyUserInput collect = new CreateHttpsApiRestShApiVerifyUserInput();

    HttpsApiRestShApiVerifyUserRequestModel body = new HttpsApiRestShApiVerifyUserRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    verification.createHttpsApiRestShApiVerifyUserAsync(collect, new APICallBack<HttpsApiRestShApiVerifyUserResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiVerifyUserResponseModel response) {
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


### <a name="get_https_api_rest_sh_api_verify_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.VerificationController.getHttpsApiRestShApiVerifyAsync") getHttpsApiRestShApiVerifyAsync

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```java
void getHttpsApiRestShApiVerifyAsync(
        final GetHttpsApiRestShApiVerifyInput input,
        final APICallBack<HttpsApiRestShApiVerifyResponseModel> callBack)
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
GetHttpsApiRestShApiVerifyInput collect = new GetHttpsApiRestShApiVerifyInput();

String key = "key";
collect.setKey(key);

String uid = "uid";
collect.setUid(uid);

String to = "to";
collect.setTo(to);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
verification.getHttpsApiRestShApiVerifyAsync(collect, new APICallBack<HttpsApiRestShApiVerifyResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiVerifyResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_verify_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.VerificationController.createHttpsApiRestShApiVerifyAsync") createHttpsApiRestShApiVerifyAsync

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```java
void createHttpsApiRestShApiVerifyAsync(
        final CreateHttpsApiRestShApiVerifyInput input,
        final APICallBack<HttpsApiRestShApiVerifyResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiVerifyInput collect = new CreateHttpsApiRestShApiVerifyInput();

    HttpsApiRestShApiVerifyRequestModel body = new HttpsApiRestShApiVerifyRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    verification.createHttpsApiRestShApiVerifyAsync(collect, new APICallBack<HttpsApiRestShApiVerifyResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiVerifyResponseModel response) {
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

### <a name="get_https_api_rest_sh_api2fa_token_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2faTokenAsync") getHttpsApiRestShApi2faTokenAsync

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```java
void getHttpsApiRestShApi2faTokenAsync(
        final GetHttpsApiRestShApi2faTokenInput input,
        final APICallBack<HttpsApiRestShApi2faTokenResponseModel> callBack)
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
GetHttpsApiRestShApi2faTokenInput collect = new GetHttpsApiRestShApi2faTokenInput();

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
twoFactorAuthenticationAPI.getHttpsApiRestShApi2faTokenAsync(collect, new APICallBack<HttpsApiRestShApi2faTokenResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApi2faTokenResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api2fa_token_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2faTokenAsync") createHttpsApiRestShApi2faTokenAsync

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```java
void createHttpsApiRestShApi2faTokenAsync(
        final CreateHttpsApiRestShApi2faTokenInput input,
        final APICallBack<HttpsApiRestShApi2faTokenResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApi2faTokenInput collect = new CreateHttpsApiRestShApi2faTokenInput();

    HttpsApiRestShApi2faTokenRequestModel body = new HttpsApiRestShApi2faTokenRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    twoFactorAuthenticationAPI.createHttpsApiRestShApi2faTokenAsync(collect, new APICallBack<HttpsApiRestShApi2faTokenResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApi2faTokenResponseModel response) {
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
        final APICallBack<HttpsApiRestShApi2faResponseModel> callBack)
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
twoFactorAuthenticationAPI.getHttpsApiRestShApi2faAsync(collect, new APICallBack<HttpsApiRestShApi2faResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApi2faResponseModel response) {
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
        final APICallBack<HttpsApiRestShApi2faResponseModel> callBack)
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

    HttpsApiRestShApi2faRequestModel body = new HttpsApiRestShApi2faRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    twoFactorAuthenticationAPI.createHttpsApiRestShApi2faAsync(collect, new APICallBack<HttpsApiRestShApi2faResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApi2faResponseModel response) {
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

### <a name="get_https_api_rest_sh_api_user_info_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagementController.getHttpsApiRestShApiUserInfoAsync") getHttpsApiRestShApiUserInfoAsync

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```java
void getHttpsApiRestShApiUserInfoAsync(
        final GetHttpsApiRestShApiUserInfoInput input,
        final APICallBack<HttpsApiRestShApiUserInfoResponseModel> callBack)
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
GetHttpsApiRestShApiUserInfoInput collect = new GetHttpsApiRestShApiUserInfoInput();

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
userManagement.getHttpsApiRestShApiUserInfoAsync(collect, new APICallBack<HttpsApiRestShApiUserInfoResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiUserInfoResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_user_info_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagementController.createHttpsApiRestShApiUserInfoAsync") createHttpsApiRestShApiUserInfoAsync

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```java
void createHttpsApiRestShApiUserInfoAsync(
        final CreateHttpsApiRestShApiUserInfoInput input,
        final APICallBack<HttpsApiRestShApiUserInfoResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiUserInfoInput collect = new CreateHttpsApiRestShApiUserInfoInput();

    HttpsApiRestShApiUserInfoRequestModel body = new HttpsApiRestShApiUserInfoRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    userManagement.createHttpsApiRestShApiUserInfoAsync(collect, new APICallBack<HttpsApiRestShApiUserInfoResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiUserInfoResponseModel response) {
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


### <a name="get_https_api_rest_sh_api_user_update_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagementController.getHttpsApiRestShApiUserUpdateAsync") getHttpsApiRestShApiUserUpdateAsync

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```java
void getHttpsApiRestShApiUserUpdateAsync(
        final GetHttpsApiRestShApiUserUpdateInput input,
        final APICallBack<HttpsApiRestShApiUserUpdateResponseModel> callBack)
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
GetHttpsApiRestShApiUserUpdateInput collect = new GetHttpsApiRestShApiUserUpdateInput();

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
userManagement.getHttpsApiRestShApiUserUpdateAsync(collect, new APICallBack<HttpsApiRestShApiUserUpdateResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiUserUpdateResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_user_update_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagementController.createHttpsApiRestShApiUserUpdateAsync") createHttpsApiRestShApiUserUpdateAsync

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```java
void createHttpsApiRestShApiUserUpdateAsync(
        final CreateHttpsApiRestShApiUserUpdateInput input,
        final APICallBack<HttpsApiRestShApiUserUpdateResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiUserUpdateInput collect = new CreateHttpsApiRestShApiUserUpdateInput();

    HttpsApiRestShApiUserUpdateRequestModel body = new HttpsApiRestShApiUserUpdateRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    userManagement.createHttpsApiRestShApiUserUpdateAsync(collect, new APICallBack<HttpsApiRestShApiUserUpdateResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiUserUpdateResponseModel response) {
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


### <a name="get_https_api_rest_sh_api_user_delete_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagementController.getHttpsApiRestShApiUserDeleteAsync") getHttpsApiRestShApiUserDeleteAsync

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```java
void getHttpsApiRestShApiUserDeleteAsync(
        final GetHttpsApiRestShApiUserDeleteInput input,
        final APICallBack<HttpsApiRestShApiUserDeleteResponseModel> callBack)
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
GetHttpsApiRestShApiUserDeleteInput collect = new GetHttpsApiRestShApiUserDeleteInput();

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
userManagement.getHttpsApiRestShApiUserDeleteAsync(collect, new APICallBack<HttpsApiRestShApiUserDeleteResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiUserDeleteResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_user_delete_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.UserManagementController.createHttpsApiRestShApiUserDeleteAsync") createHttpsApiRestShApiUserDeleteAsync

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```java
void createHttpsApiRestShApiUserDeleteAsync(
        final CreateHttpsApiRestShApiUserDeleteInput input,
        final APICallBack<HttpsApiRestShApiUserDeleteResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiUserDeleteInput collect = new CreateHttpsApiRestShApiUserDeleteInput();

    HttpsApiRestShApiUserDeleteRequestModel body = new HttpsApiRestShApiUserDeleteRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    userManagement.createHttpsApiRestShApiUserDeleteAsync(collect, new APICallBack<HttpsApiRestShApiUserDeleteResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiUserDeleteResponseModel response) {
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

### <a name="get_https_api_rest_sh_api_auth_user_register_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.LoginAndRegistrationController.getHttpsApiRestShApiAuthUserRegisterAsync") getHttpsApiRestShApiAuthUserRegisterAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```java
void getHttpsApiRestShApiAuthUserRegisterAsync(
        final GetHttpsApiRestShApiAuthUserRegisterInput input,
        final APICallBack<HttpsApiRestShApiAuthUserRegisterResponseModel> callBack)
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
GetHttpsApiRestShApiAuthUserRegisterInput collect = new GetHttpsApiRestShApiAuthUserRegisterInput();

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

int phone = 201;
collect.setPhone(phone);

int countrycode = 201;
collect.setCountrycode(countrycode);

String address = "address";
collect.setAddress(address);

String contentType = "Content-Type";
collect.setContentType(contentType);

// Invoking the API call with sample inputs
loginAndRegistration.getHttpsApiRestShApiAuthUserRegisterAsync(collect, new APICallBack<HttpsApiRestShApiAuthUserRegisterResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiAuthUserRegisterResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_auth_user_register_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.LoginAndRegistrationController.createHttpsApiRestShApiAuthUserRegisterAsync") createHttpsApiRestShApiAuthUserRegisterAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```java
void createHttpsApiRestShApiAuthUserRegisterAsync(
        final CreateHttpsApiRestShApiAuthUserRegisterInput input,
        final APICallBack<HttpsApiRestShApiAuthUserRegisterResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiAuthUserRegisterInput collect = new CreateHttpsApiRestShApiAuthUserRegisterInput();

    HttpsApiRestShApiAuthUserRegisterRequestModel body = new HttpsApiRestShApiAuthUserRegisterRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    loginAndRegistration.createHttpsApiRestShApiAuthUserRegisterAsync(collect, new APICallBack<HttpsApiRestShApiAuthUserRegisterResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiAuthUserRegisterResponseModel response) {
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


### <a name="get_https_api_rest_sh_api_auth_user_login_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.LoginAndRegistrationController.getHttpsApiRestShApiAuthUserLoginAsync") getHttpsApiRestShApiAuthUserLoginAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```java
void getHttpsApiRestShApiAuthUserLoginAsync(
        final GetHttpsApiRestShApiAuthUserLoginInput input,
        final APICallBack<HttpsApiRestShApiAuthUserLoginResponseModel> callBack)
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
GetHttpsApiRestShApiAuthUserLoginInput collect = new GetHttpsApiRestShApiAuthUserLoginInput();

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
loginAndRegistration.getHttpsApiRestShApiAuthUserLoginAsync(collect, new APICallBack<HttpsApiRestShApiAuthUserLoginResponseModel>() {
    public void onSuccess(HttpContext context, HttpsApiRestShApiAuthUserLoginResponseModel response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
}
);

```


### <a name="create_https_api_rest_sh_api_auth_user_login_async"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.controllers.LoginAndRegistrationController.createHttpsApiRestShApiAuthUserLoginAsync") createHttpsApiRestShApiAuthUserLoginAsync

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```java
void createHttpsApiRestShApiAuthUserLoginAsync(
        final CreateHttpsApiRestShApiAuthUserLoginInput input,
        final APICallBack<HttpsApiRestShApiAuthUserLoginResponseModel> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
CreateHttpsApiRestShApiAuthUserLoginInput collect = new CreateHttpsApiRestShApiAuthUserLoginInput();

    HttpsApiRestShApiAuthUserLoginRequestModel body = new HttpsApiRestShApiAuthUserLoginRequestModel();
collect.setBody(body);

    String contentType = "Content-Type";
collect.setContentType(contentType);

    // Invoking the API call with sample inputs
    loginAndRegistration.createHttpsApiRestShApiAuthUserLoginAsync(collect, new APICallBack<HttpsApiRestShApiAuthUserLoginResponseModel>() {
        public void onSuccess(HttpContext context, HttpsApiRestShApiAuthUserLoginResponseModel response) {
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



