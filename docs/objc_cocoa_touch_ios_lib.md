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


The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```PodFile``` file that comes with the SDK. 
To resolve these dependencies, we use the Cocoapods package manager.
Visit https://guides.cocoapods.org/using/getting-started.html to setup Cocoapods on your system.
Open command prompt and type ```pod --version```. This should display the current version of Cocoapods installed if the installation was successful.

Using command line, navigate to the directory containing the generated files (including ```PodFile```) for the SDK. 
Run the command ```pod install```. This should install all the required dependencies and create the ```pods``` directory in your project directory.

![Installing dependencies using Cocoapods](https://apidocs.io/illustration/objc?step=AddDependencies&workspaceFolder=SMASH-ObjC&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Open the project workspace using the (SMASH.xcworkspace) file. Invoke the build process using `Command(⌘)+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Xcode](https://apidocs.io/illustration/objc?step=BuildSDK&workspaceFolder=SMASH-ObjC&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)


## How to Use

The generated code is a Cocoa Touch Static Library which can be used in any iOS project. The support for these generated libraries go all the way back to iOS 6.

The following section explains how to use the SMASH library in a new iOS project.     
### 1. Starting a new project
To start a new project, left-click on the ```Create a new Xcode project```.
![Create Test Project - Step 1](https://apidocs.io/illustration/objc?step=Test1&workspaceFolder=SMASH-ObjC&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Next, choose **Single View Application** and click ```Next```.
![Create Test Project - Step 2](https://apidocs.io/illustration/objc?step=Test2&workspaceFolder=SMASH-ObjC&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Provide **Test-Project** as the product name click ```Next```.
![Create Test Project - Step 3](https://apidocs.io/illustration/objc?step=Test3&workspaceFolder=SMASH-ObjC&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Choose the desired location of your project folder and click ```Create```.
![Create Test Project - Step 4](https://apidocs.io/illustration/objc?step=Test4&workspaceFolder=SMASH-ObjC&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

### 2. Adding the static library dependency
To add this dependency open a terminal and navigate to your project folder. Next, input ```pod init``` and press enter.
![Add dependency - Step 1](https://apidocs.io/illustration/objc?step=Add0&workspaceFolder=SMASH-ObjC&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Next, open the newly created ```PodFile``` in your favourite text editor. Add the following line : pod 'SMASH', :path => 'Vendor/SMASH'
![Add dependency - Step 2](https://apidocs.io/illustration/objc?step=Add1&workspaceFolder=SMASH-ObjC&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)

Execute `pod install` from terminal to install the dependecy in your project. This would add the dependency to the newly created test project.
![Add dependency - Step 3](https://apidocs.io/illustration/objc?step=Add2&workspaceFolder=SMASH-ObjC&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)


## How to Test

Unit tests in this SDK can be run using Xcode. 

First build the SDK as shown in the steps above and naivgate to the project directory and open the SMASH.xcworkspace file.

Go to the test explorer in Xcode as shown in the picture below and click on `run tests` from the menu. 
![Run tests](https://apidocs.io/illustration/objc?step=RunTests&workspaceFolder=SMASH-ObjC&workspaceName=SMASH&projectName=SMASH&rootNamespace=SMASH)


## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| key | Your API Key |
| uid | Your User ID |



Configuration variables can be set as following.
```Objc
// Configuration parameters and credentials
Configuration_Key = "API"; // Your API Key
Configuration_Uid = "UID"; // Your User ID

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

## <a name="advanced_logging_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AdvancedLoggingController") AdvancedLoggingController

### Get singleton instance
```objc
AdvancedLogging* advancedLogging = [[AdvancedLogging alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_sli_async_with_get_https_api_rest_sh_api_sli_input"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSLIAsyncWithGetHttpsApiRestShApiSLIInput") getHttpsApiRestShApiSLIAsyncWithGetHttpsApiRestShApiSLIInput

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```objc
function getHttpsApiRestShApiSLIAsyncWithGetHttpsApiRestShApiSLIInput:(GetHttpsApiRestShApiSLIInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSLI) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiSLIInput *input = [[GetHttpsApiRestShApiSLIInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.name = @"name";
    input.origin = @"origin";
    input.time = @"time";
    input.contentType = @"Content-Type";

    [self.advancedLogging getHttpsApiRestShApiSLIAsyncWithGetHttpsApiRestShApiSLIInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSLIRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_sl_async_with_get_https_api_rest_sh_api_sl_input"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSLAsyncWithGetHttpsApiRestShApiSLInput") getHttpsApiRestShApiSLAsyncWithGetHttpsApiRestShApiSLInput

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```objc
function getHttpsApiRestShApiSLAsyncWithGetHttpsApiRestShApiSLInput:(GetHttpsApiRestShApiSLInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSL) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiSLInput *input = [[GetHttpsApiRestShApiSLInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.name = @"name";
    input.origin = @"origin";
    input.activate = true;
    input.contentType = @"Content-Type";

    [self.advancedLogging getHttpsApiRestShApiSLAsyncWithGetHttpsApiRestShApiSLInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSLRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_sli_async_with_create_https_api_rest_sh_api_sli_input"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSLIAsyncWithCreateHttpsApiRestShApiSLIInput") createHttpsApiRestShApiSLIAsyncWithCreateHttpsApiRestShApiSLIInput

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```objc
function createHttpsApiRestShApiSLIAsyncWithCreateHttpsApiRestShApiSLIInput:(CreateHttpsApiRestShApiSLIInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSLI) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSLIInput *input = [[CreateHttpsApiRestShApiSLIInput alloc]init];
    input.body = [[HttpsApiRestShApiSLIModel alloc]init];
    input.contentType = @"Content-Type";

    [self.advancedLogging createHttpsApiRestShApiSLIAsyncWithCreateHttpsApiRestShApiSLIInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSLIRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_sl_async_with_create_https_api_rest_sh_api_sl_input"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSLAsyncWithCreateHttpsApiRestShApiSLInput") createHttpsApiRestShApiSLAsyncWithCreateHttpsApiRestShApiSLInput

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```objc
function createHttpsApiRestShApiSLAsyncWithCreateHttpsApiRestShApiSLInput:(CreateHttpsApiRestShApiSLInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSL) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSLInput *input = [[CreateHttpsApiRestShApiSLInput alloc]init];
    input.body = [[HttpsApiRestShApiSLModel alloc]init];
    input.contentType = @"Content-Type";

    [self.advancedLogging createHttpsApiRestShApiSLAsyncWithCreateHttpsApiRestShApiSLInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSLRModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection_controller"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtectionController") WAFDDOSProtectionController

### Get singleton instance
```objc
WAFDDOSProtection* wAFDDOSProtection = [[WAFDDOSProtection alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_swc_async_with_get_https_api_rest_sh_api_swc_input"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSWCAsyncWithGetHttpsApiRestShApiSWCInput") getHttpsApiRestShApiSWCAsyncWithGetHttpsApiRestShApiSWCInput

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function getHttpsApiRestShApiSWCAsyncWithGetHttpsApiRestShApiSWCInput:(GetHttpsApiRestShApiSWCInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSWC) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiSWCInput *input = [[GetHttpsApiRestShApiSWCInput alloc]init];
    input.key = @"API";
    input.uid = @"UID";
    input.name = @"origin-name";
    input.origin = @"origin.yourdomain.tld";
    input.rule = @"header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does";
    input.contentType = @"application/json";

    [self.wAFDDOSProtection getHttpsApiRestShApiSWCAsyncWithGetHttpsApiRestShApiSWCInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSWCRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_sw_async_with_get_https_api_rest_sh_api_sw_input"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSWAsyncWithGetHttpsApiRestShApiSWInput") getHttpsApiRestShApiSWAsyncWithGetHttpsApiRestShApiSWInput

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function getHttpsApiRestShApiSWAsyncWithGetHttpsApiRestShApiSWInput:(GetHttpsApiRestShApiSWInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSW) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiSWInput *input = [[GetHttpsApiRestShApiSWInput alloc]init];
    input.key = @"API";
    input.uid = @"UID";
    input.origin = @"origin.yourdomain.tld";
    input.cname = @"yourdomain.tld,www.yourdomain.tld";
    input.contentType = @"application/json";

    [self.wAFDDOSProtection getHttpsApiRestShApiSWAsyncWithGetHttpsApiRestShApiSWInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSWRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_swc_async_with_create_https_api_rest_sh_api_swc_input"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSWCAsyncWithCreateHttpsApiRestShApiSWCInput") createHttpsApiRestShApiSWCAsyncWithCreateHttpsApiRestShApiSWCInput

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function createHttpsApiRestShApiSWCAsyncWithCreateHttpsApiRestShApiSWCInput:(CreateHttpsApiRestShApiSWCInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSWC) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSWCInput *input = [[CreateHttpsApiRestShApiSWCInput alloc]init];
    input.body = (HttpsApiRestShApiSWCModel*) [APIHelper jsonDeserialize: @"{
  \"key\": \"YOUR API KEY\",
  \"uid\": \"YOUR USER ID\",
  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",
  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",
  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"
}"
                toClass: HttpsApiRestShApiSWCModel.class];
    input.contentType = @"application/json";

    [self.wAFDDOSProtection createHttpsApiRestShApiSWCAsyncWithCreateHttpsApiRestShApiSWCInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSWCRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_sw_async_with_create_https_api_rest_sh_api_sw_input"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSWAsyncWithCreateHttpsApiRestShApiSWInput") createHttpsApiRestShApiSWAsyncWithCreateHttpsApiRestShApiSWInput

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function createHttpsApiRestShApiSWAsyncWithCreateHttpsApiRestShApiSWInput:(CreateHttpsApiRestShApiSWInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSW) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSWInput *input = [[CreateHttpsApiRestShApiSWInput alloc]init];
    input.body = (HttpsApiRestShApiSWModel*) [APIHelper jsonDeserialize: @"{
  \"key\": \"YOUR API KEY\",
  \"uid\": \"YOUR USER ID\",
  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",
  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"
}"
                toClass: HttpsApiRestShApiSWModel.class];
    input.contentType = @"application/json";

    [self.wAFDDOSProtection createHttpsApiRestShApiSWAsyncWithCreateHttpsApiRestShApiSWInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSWRModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EncryptionController") EncryptionController

### Get singleton instance
```objc
Encryption* encryption = [[Encryption alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_se_async_with_get_https_api_rest_sh_api_se_input"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.getHttpsApiRestShApiSEAsyncWithGetHttpsApiRestShApiSEInput") getHttpsApiRestShApiSEAsyncWithGetHttpsApiRestShApiSEInput

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```objc
function getHttpsApiRestShApiSEAsyncWithGetHttpsApiRestShApiSEInput:(GetHttpsApiRestShApiSEInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSE) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiSEInput *input = [[GetHttpsApiRestShApiSEInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.data = @"data";
    input.method = @"method";
    input.bit = 148;
    input.contentType = @"Content-Type";

    [self.encryption getHttpsApiRestShApiSEAsyncWithGetHttpsApiRestShApiSEInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSERModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_se_async_with_create_https_api_rest_sh_api_se_input"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.createHttpsApiRestShApiSEAsyncWithCreateHttpsApiRestShApiSEInput") createHttpsApiRestShApiSEAsyncWithCreateHttpsApiRestShApiSEInput

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```objc
function createHttpsApiRestShApiSEAsyncWithCreateHttpsApiRestShApiSEInput:(CreateHttpsApiRestShApiSEInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSE) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSEInput *input = [[CreateHttpsApiRestShApiSEInput alloc]init];
    input.body = [[HttpsApiRestShApiSEModel alloc]init];
    input.contentType = @"Content-Type";

    [self.encryption createHttpsApiRestShApiSEAsyncWithCreateHttpsApiRestShApiSEInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSERModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CDNController") CDNController

### Get singleton instance
```objc
CDN* cDN = [[CDN alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_sc_push_async_with_get_https_api_rest_sh_api_sc_push_input"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiSCPushAsyncWithGetHttpsApiRestShApiSCPushInput") getHttpsApiRestShApiSCPushAsyncWithGetHttpsApiRestShApiSCPushInput

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```objc
function getHttpsApiRestShApiSCPushAsyncWithGetHttpsApiRestShApiSCPushInput:(GetHttpsApiRestShApiSCPushInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSCPush) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiSCPushInput *input = [[GetHttpsApiRestShApiSCPushInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.cname = @"cname";
    input.file = @"file";
    input.contentType = @"Content-Type";

    [self.cDN getHttpsApiRestShApiSCPushAsyncWithGetHttpsApiRestShApiSCPushInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSCPushRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_sc_pull_async_with_get_https_api_rest_sh_api_sc_pull_input"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiSCPullAsyncWithGetHttpsApiRestShApiSCPullInput") getHttpsApiRestShApiSCPullAsyncWithGetHttpsApiRestShApiSCPullInput

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```objc
function getHttpsApiRestShApiSCPullAsyncWithGetHttpsApiRestShApiSCPullInput:(GetHttpsApiRestShApiSCPullInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSCPull) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiSCPullInput *input = [[GetHttpsApiRestShApiSCPullInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.origin = @"origin";
    input.cname = @"cname";
    input.contentType = @"Content-Type";

    [self.cDN getHttpsApiRestShApiSCPullAsyncWithGetHttpsApiRestShApiSCPullInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSCPullRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_sc_push_async_with_create_https_api_rest_sh_api_sc_push_input"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiSCPushAsyncWithCreateHttpsApiRestShApiSCPushInput") createHttpsApiRestShApiSCPushAsyncWithCreateHttpsApiRestShApiSCPushInput

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```objc
function createHttpsApiRestShApiSCPushAsyncWithCreateHttpsApiRestShApiSCPushInput:(CreateHttpsApiRestShApiSCPushInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSCPush) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSCPushInput *input = [[CreateHttpsApiRestShApiSCPushInput alloc]init];
    input.body = [[HttpsApiRestShApiSCPushModel alloc]init];
    input.contentType = @"Content-Type";

    [self.cDN createHttpsApiRestShApiSCPushAsyncWithCreateHttpsApiRestShApiSCPushInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSCPushRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_sc_pull_async_with_create_https_api_rest_sh_api_sc_pull_input"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiSCPullAsyncWithCreateHttpsApiRestShApiSCPullInput") createHttpsApiRestShApiSCPullAsyncWithCreateHttpsApiRestShApiSCPullInput

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```objc
function createHttpsApiRestShApiSCPullAsyncWithCreateHttpsApiRestShApiSCPullInput:(CreateHttpsApiRestShApiSCPullInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSCPull) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSCPullInput *input = [[CreateHttpsApiRestShApiSCPullInput alloc]init];
    input.body = [[HttpsApiRestShApiSCPullModel alloc]init];
    input.contentType = @"Content-Type";

    [self.cDN createHttpsApiRestShApiSCPullAsyncWithCreateHttpsApiRestShApiSCPullInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSCPullRModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DNSController") DNSController

### Get singleton instance
```objc
DNS* dNS = [[DNS alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_sdc_async_with_get_https_api_rest_sh_api_sdc_input"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiSDCAsyncWithGetHttpsApiRestShApiSDCInput") getHttpsApiRestShApiSDCAsyncWithGetHttpsApiRestShApiSDCInput

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```objc
function getHttpsApiRestShApiSDCAsyncWithGetHttpsApiRestShApiSDCInput:(GetHttpsApiRestShApiSDCInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSDC) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiSDCInput *input = [[GetHttpsApiRestShApiSDCInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.domain = @"domain";
    input.records = @"records";
    input.contentType = @"Content-Type";

    [self.dNS getHttpsApiRestShApiSDCAsyncWithGetHttpsApiRestShApiSDCInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSDCRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_sdc_async_with_create_https_api_rest_sh_api_sdc_input"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiSDCAsyncWithCreateHttpsApiRestShApiSDCInput") createHttpsApiRestShApiSDCAsyncWithCreateHttpsApiRestShApiSDCInput

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```objc
function createHttpsApiRestShApiSDCAsyncWithCreateHttpsApiRestShApiSDCInput:(CreateHttpsApiRestShApiSDCInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSDC) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSDCInput *input = [[CreateHttpsApiRestShApiSDCInput alloc]init];
    input.body = [[HttpsApiRestShApiSDCModel alloc]init];
    input.contentType = @"Content-Type";

    [self.dNS createHttpsApiRestShApiSDCAsyncWithCreateHttpsApiRestShApiSDCInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSDCRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_sda_async_with_get_https_api_rest_sh_api_sda_input"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiSDAAsyncWithGetHttpsApiRestShApiSDAInput") getHttpsApiRestShApiSDAAsyncWithGetHttpsApiRestShApiSDAInput

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```objc
function getHttpsApiRestShApiSDAAsyncWithGetHttpsApiRestShApiSDAInput:(GetHttpsApiRestShApiSDAInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSDA) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| domain |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiSDAInput *input = [[GetHttpsApiRestShApiSDAInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.domain = @"domain";
    input.contentType = @"Content-Type";

    [self.dNS getHttpsApiRestShApiSDAAsyncWithGetHttpsApiRestShApiSDAInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSDARModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_sda_async_with_create_https_api_rest_sh_api_sda_input"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiSDAAsyncWithCreateHttpsApiRestShApiSDAInput") createHttpsApiRestShApiSDAAsyncWithCreateHttpsApiRestShApiSDAInput

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```objc
function createHttpsApiRestShApiSDAAsyncWithCreateHttpsApiRestShApiSDAInput:(CreateHttpsApiRestShApiSDAInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSDA) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSDAInput *input = [[CreateHttpsApiRestShApiSDAInput alloc]init];
    input.body = [[HttpsApiRestShApiSDAModel alloc]init];
    input.contentType = @"Content-Type";

    [self.dNS createHttpsApiRestShApiSDAAsyncWithCreateHttpsApiRestShApiSDAInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSDARModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscationController") CodeObfuscationController

### Get singleton instance
```objc
CodeObfuscation* codeObfuscation = [[CodeObfuscation alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_so_async_with_get_https_api_rest_sh_api_so_input"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.getHttpsApiRestShApiSOAsyncWithGetHttpsApiRestShApiSOInput") getHttpsApiRestShApiSOAsyncWithGetHttpsApiRestShApiSOInput

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```objc
function getHttpsApiRestShApiSOAsyncWithGetHttpsApiRestShApiSOInput:(GetHttpsApiRestShApiSOInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSO) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| app |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiSOInput *input = [[GetHttpsApiRestShApiSOInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.app = @"app";
    input.contentType = @"Content-Type";

    [self.codeObfuscation getHttpsApiRestShApiSOAsyncWithGetHttpsApiRestShApiSOInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSORModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_so_async_with_create_https_api_rest_sh_api_so_input"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.createHttpsApiRestShApiSOAsyncWithCreateHttpsApiRestShApiSOInput") createHttpsApiRestShApiSOAsyncWithCreateHttpsApiRestShApiSOInput

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```objc
function createHttpsApiRestShApiSOAsyncWithCreateHttpsApiRestShApiSOInput:(CreateHttpsApiRestShApiSOInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSO) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSOInput *input = [[CreateHttpsApiRestShApiSOInput alloc]init];
    input.body = [[HttpsApiRestShApiSOModel alloc]init];
    input.contentType = @"Content-Type";

    [self.codeObfuscation createHttpsApiRestShApiSOAsyncWithCreateHttpsApiRestShApiSOInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSORModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting_controller"></a>![Class: ](https://apidocs.io/img/class.png ".HostingController") HostingController

### Get singleton instance
```objc
Hosting* hosting = [[Hosting alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_sh_async_with_get_https_api_rest_sh_api_sh_input"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.getHttpsApiRestShApiSHAsyncWithGetHttpsApiRestShApiSHInput") getHttpsApiRestShApiSHAsyncWithGetHttpsApiRestShApiSHInput

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```objc
function getHttpsApiRestShApiSHAsyncWithGetHttpsApiRestShApiSHInput:(GetHttpsApiRestShApiSHInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSH) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiSHInput *input = [[GetHttpsApiRestShApiSHInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.app = @"app";
    input.domain = @"domain";
    input.contentType = @"Content-Type";

    [self.hosting getHttpsApiRestShApiSHAsyncWithGetHttpsApiRestShApiSHInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSHRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_sh_async_with_create_https_api_rest_sh_api_sh_input"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.createHttpsApiRestShApiSHAsyncWithCreateHttpsApiRestShApiSHInput") createHttpsApiRestShApiSHAsyncWithCreateHttpsApiRestShApiSHInput

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```objc
function createHttpsApiRestShApiSHAsyncWithCreateHttpsApiRestShApiSHInput:(CreateHttpsApiRestShApiSHInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSH) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSHInput *input = [[CreateHttpsApiRestShApiSHInput alloc]init];
    input.body = [[HttpsApiRestShApiSHModel alloc]init];
    input.contentType = @"Content-Type";

    [self.hosting createHttpsApiRestShApiSHAsyncWithCreateHttpsApiRestShApiSHInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSHRModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPIController") DataManipulationConversionSortingAndCompressionAPIController

### Get singleton instance
```objc
DataManipulationConversionSortingAndCompressionAPI* dataManipulationConversionSortingAndCompressionAPI = [[DataManipulationConversionSortingAndCompressionAPI alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_d_async_with_get_https_api_rest_sh_api_d_input"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.getHttpsApiRestShApiDAsyncWithGetHttpsApiRestShApiDInput") getHttpsApiRestShApiDAsyncWithGetHttpsApiRestShApiDInput

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function getHttpsApiRestShApiDAsyncWithGetHttpsApiRestShApiDInput:(GetHttpsApiRestShApiDInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiD) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiDInput *input = [[GetHttpsApiRestShApiDInput alloc]init];
    input.key = @"API";
    input.uid = @"UID";
    input.user = @"UID";
    input.apiuid = @"apiUID";
    input.data = @"https://static.yourcdn.com/data.file";
    input.contentType = @"application/json";

    [self.dataManipulationConversionSortingAndCompressionAPI getHttpsApiRestShApiDAsyncWithGetHttpsApiRestShApiDInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiDRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_d_async_with_create_https_api_rest_sh_api_d_input"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.createHttpsApiRestShApiDAsyncWithCreateHttpsApiRestShApiDInput") createHttpsApiRestShApiDAsyncWithCreateHttpsApiRestShApiDInput

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function createHttpsApiRestShApiDAsyncWithCreateHttpsApiRestShApiDInput:(CreateHttpsApiRestShApiDInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiD) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiDInput *input = [[CreateHttpsApiRestShApiDInput alloc]init];
    input.body = (HttpsApiRestShApiDModel*) [APIHelper jsonDeserialize: @"{
  \"key\": \"YOUR API KEY\",
  \"uid\": \"YOUR USER ID\",
  \"user\": \"USERS EMAIL OR USERNAME\",
  \"apiuid\": \"USERS API SIDE USER ID\",
  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",
  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",
  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",
  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",
  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"
}"
                toClass: HttpsApiRestShApiDModel.class];
    input.contentType = @"application/json";

    [self.dataManipulationConversionSortingAndCompressionAPI createHttpsApiRestShApiDAsyncWithCreateHttpsApiRestShApiDInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiDRModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPIController") ImageManipulationAndModerationAPIController

### Get singleton instance
```objc
ImageManipulationAndModerationAPI* imageManipulationAndModerationAPI = [[ImageManipulationAndModerationAPI alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_i_async_with_get_https_api_rest_sh_api_i_input"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.getHttpsApiRestShApiIAsyncWithGetHttpsApiRestShApiIInput") getHttpsApiRestShApiIAsyncWithGetHttpsApiRestShApiIInput

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```objc
function getHttpsApiRestShApiIAsyncWithGetHttpsApiRestShApiIInput:(GetHttpsApiRestShApiIInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiI) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiIInput *input = [[GetHttpsApiRestShApiIInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.image = @"image";
    input.transform = @"transform";
    input.contentType = @"Content-Type";

    [self.imageManipulationAndModerationAPI getHttpsApiRestShApiIAsyncWithGetHttpsApiRestShApiIInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiIRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_i_async_with_create_https_api_rest_sh_api_i_input"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.createHttpsApiRestShApiIAsyncWithCreateHttpsApiRestShApiIInput") createHttpsApiRestShApiIAsyncWithCreateHttpsApiRestShApiIInput

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```objc
function createHttpsApiRestShApiIAsyncWithCreateHttpsApiRestShApiIInput:(CreateHttpsApiRestShApiIInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiI) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiIInput *input = [[CreateHttpsApiRestShApiIInput alloc]init];
    input.body = [[HttpsApiRestShApiIModel alloc]init];
    input.contentType = @"Content-Type";

    [self.imageManipulationAndModerationAPI createHttpsApiRestShApiIAsyncWithCreateHttpsApiRestShApiIInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiIRModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VerificationController") VerificationController

### Get singleton instance
```objc
Verification* verification = [[Verification alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_va_async_with_get_https_api_rest_sh_api_va_input"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVAAsyncWithGetHttpsApiRestShApiVAInput") getHttpsApiRestShApiVAAsyncWithGetHttpsApiRestShApiVAInput

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```objc
function getHttpsApiRestShApiVAAsyncWithGetHttpsApiRestShApiVAInput:(GetHttpsApiRestShApiVAInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiVA) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiVAInput *input = [[GetHttpsApiRestShApiVAInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.a = @"a";
    input.sa = @"sa";
    input.c = @"c";
    input.s = @"s";
    input.z = 148;
    input.contentType = @"Content-Type";

    [self.verification getHttpsApiRestShApiVAAsyncWithGetHttpsApiRestShApiVAInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVARModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_va_async_with_create_https_api_rest_sh_api_va_input"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVAAsyncWithCreateHttpsApiRestShApiVAInput") createHttpsApiRestShApiVAAsyncWithCreateHttpsApiRestShApiVAInput

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```objc
function createHttpsApiRestShApiVAAsyncWithCreateHttpsApiRestShApiVAInput:(CreateHttpsApiRestShApiVAInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiVA) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiVAInput *input = [[CreateHttpsApiRestShApiVAInput alloc]init];
    input.body = [[HttpsApiRestShApiVAModel alloc]init];
    input.contentType = @"Content-Type";

    [self.verification createHttpsApiRestShApiVAAsyncWithCreateHttpsApiRestShApiVAInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVARModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_vu_async_with_get_https_api_rest_sh_api_vu_input"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVUAsyncWithGetHttpsApiRestShApiVUInput") getHttpsApiRestShApiVUAsyncWithGetHttpsApiRestShApiVUInput

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```objc
function getHttpsApiRestShApiVUAsyncWithGetHttpsApiRestShApiVUInput:(GetHttpsApiRestShApiVUInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiVU) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiVUInput *input = [[GetHttpsApiRestShApiVUInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.code = @"code";
    input.contentType = @"Content-Type";

    [self.verification getHttpsApiRestShApiVUAsyncWithGetHttpsApiRestShApiVUInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVURModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_vu_async_with_create_https_api_rest_sh_api_vu_input"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVUAsyncWithCreateHttpsApiRestShApiVUInput") createHttpsApiRestShApiVUAsyncWithCreateHttpsApiRestShApiVUInput

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```objc
function createHttpsApiRestShApiVUAsyncWithCreateHttpsApiRestShApiVUInput:(CreateHttpsApiRestShApiVUInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiVU) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiVUInput *input = [[CreateHttpsApiRestShApiVUInput alloc]init];
    input.body = [[HttpsApiRestShApiVUModel alloc]init];
    input.contentType = @"Content-Type";

    [self.verification createHttpsApiRestShApiVUAsyncWithCreateHttpsApiRestShApiVUInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVURModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_v_async_with_get_https_api_rest_sh_api_v_input"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVAsyncWithGetHttpsApiRestShApiVInput") getHttpsApiRestShApiVAsyncWithGetHttpsApiRestShApiVInput

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```objc
function getHttpsApiRestShApiVAsyncWithGetHttpsApiRestShApiVInput:(GetHttpsApiRestShApiVInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiV) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiVInput *input = [[GetHttpsApiRestShApiVInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.to = @"to";
    input.contentType = @"Content-Type";

    [self.verification getHttpsApiRestShApiVAsyncWithGetHttpsApiRestShApiVInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_v_async_with_create_https_api_rest_sh_api_v_input"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVAsyncWithCreateHttpsApiRestShApiVInput") createHttpsApiRestShApiVAsyncWithCreateHttpsApiRestShApiVInput

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```objc
function createHttpsApiRestShApiVAsyncWithCreateHttpsApiRestShApiVInput:(CreateHttpsApiRestShApiVInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiV) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiVInput *input = [[CreateHttpsApiRestShApiVInput alloc]init];
    input.body = [[HttpsApiRestShApiVModel alloc]init];
    input.contentType = @"Content-Type";

    [self.verification createHttpsApiRestShApiVAsyncWithCreateHttpsApiRestShApiVInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVRModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPIController") TwoFactorAuthenticationAPIController

### Get singleton instance
```objc
TwoFactorAuthenticationAPI* twoFactorAuthenticationAPI = [[TwoFactorAuthenticationAPI alloc]init] ;
```

### <a name="get_https_api_rest_sh_api2fa_t_async_with_get_https_api_rest_sh_api2fa_t_input"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2faTAsyncWithGetHttpsApiRestShApi2faTInput") getHttpsApiRestShApi2faTAsyncWithGetHttpsApiRestShApi2faTInput

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```objc
function getHttpsApiRestShApi2faTAsyncWithGetHttpsApiRestShApi2faTInput:(GetHttpsApiRestShApi2faTInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApi2faT) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApi2faTInput *input = [[GetHttpsApiRestShApi2faTInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.code = @"code";
    input.contentType = @"Content-Type";

    [self.twoFactorAuthenticationAPI getHttpsApiRestShApi2faTAsyncWithGetHttpsApiRestShApi2faTInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faTRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api2fa_t_async_with_create_https_api_rest_sh_api2fa_t_input"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2faTAsyncWithCreateHttpsApiRestShApi2faTInput") createHttpsApiRestShApi2faTAsyncWithCreateHttpsApiRestShApi2faTInput

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```objc
function createHttpsApiRestShApi2faTAsyncWithCreateHttpsApiRestShApi2faTInput:(CreateHttpsApiRestShApi2faTInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApi2faT) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApi2faTInput *input = [[CreateHttpsApiRestShApi2faTInput alloc]init];
    input.body = [[HttpsApiRestShApi2faTModel alloc]init];
    input.contentType = @"Content-Type";

    [self.twoFactorAuthenticationAPI createHttpsApiRestShApi2faTAsyncWithCreateHttpsApiRestShApi2faTInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faTRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api2fa_async_with_get_https_api_rest_sh_api2fa_input"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2faAsyncWithGetHttpsApiRestShApi2faInput") getHttpsApiRestShApi2faAsyncWithGetHttpsApiRestShApi2faInput

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```objc
function getHttpsApiRestShApi2faAsyncWithGetHttpsApiRestShApi2faInput:(GetHttpsApiRestShApi2faInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApi2fa) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    GetHttpsApiRestShApi2faInput *input = [[GetHttpsApiRestShApi2faInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.to = @"to";
    input.contentType = @"Content-Type";

    [self.twoFactorAuthenticationAPI getHttpsApiRestShApi2faAsyncWithGetHttpsApiRestShApi2faInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api2fa_async_with_create_https_api_rest_sh_api2fa_input"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2faAsyncWithCreateHttpsApiRestShApi2faInput") createHttpsApiRestShApi2faAsyncWithCreateHttpsApiRestShApi2faInput

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```objc
function createHttpsApiRestShApi2faAsyncWithCreateHttpsApiRestShApi2faInput:(CreateHttpsApiRestShApi2faInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApi2fa) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApi2faInput *input = [[CreateHttpsApiRestShApi2faInput alloc]init];
    input.body = [[HttpsApiRestShApi2faModel alloc]init];
    input.contentType = @"Content-Type";

    [self.twoFactorAuthenticationAPI createHttpsApiRestShApi2faAsyncWithCreateHttpsApiRestShApi2faInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faRModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagementController") UserManagementController

### Get singleton instance
```objc
UserManagement* userManagement = [[UserManagement alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_ui_async_with_get_https_api_rest_sh_api_ui_input"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUIAsyncWithGetHttpsApiRestShApiUIInput") getHttpsApiRestShApiUIAsyncWithGetHttpsApiRestShApiUIInput

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```objc
function getHttpsApiRestShApiUIAsyncWithGetHttpsApiRestShApiUIInput:(GetHttpsApiRestShApiUIInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiUI) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiUIInput *input = [[GetHttpsApiRestShApiUIInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.apiuid = @"apiuid";
    input.contentType = @"Content-Type";

    [self.userManagement getHttpsApiRestShApiUIAsyncWithGetHttpsApiRestShApiUIInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUIRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_ui_async_with_create_https_api_rest_sh_api_ui_input"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUIAsyncWithCreateHttpsApiRestShApiUIInput") createHttpsApiRestShApiUIAsyncWithCreateHttpsApiRestShApiUIInput

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```objc
function createHttpsApiRestShApiUIAsyncWithCreateHttpsApiRestShApiUIInput:(CreateHttpsApiRestShApiUIInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiUI) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiUIInput *input = [[CreateHttpsApiRestShApiUIInput alloc]init];
    input.body = [[HttpsApiRestShApiUIModel alloc]init];
    input.contentType = @"Content-Type";

    [self.userManagement createHttpsApiRestShApiUIAsyncWithCreateHttpsApiRestShApiUIInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUIRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_uu_async_with_get_https_api_rest_sh_api_uu_input"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUUAsyncWithGetHttpsApiRestShApiUUInput") getHttpsApiRestShApiUUAsyncWithGetHttpsApiRestShApiUUInput

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```objc
function getHttpsApiRestShApiUUAsyncWithGetHttpsApiRestShApiUUInput:(GetHttpsApiRestShApiUUInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiUU) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiUUInput *input = [[GetHttpsApiRestShApiUUInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.apiuid = @"apiuid";
    input.avatar = @"avatar";
    input.customInput = @"custom input";
    input.contentType = @"Content-Type";

    [self.userManagement getHttpsApiRestShApiUUAsyncWithGetHttpsApiRestShApiUUInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUURModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_uu_async_with_create_https_api_rest_sh_api_uu_input"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUUAsyncWithCreateHttpsApiRestShApiUUInput") createHttpsApiRestShApiUUAsyncWithCreateHttpsApiRestShApiUUInput

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```objc
function createHttpsApiRestShApiUUAsyncWithCreateHttpsApiRestShApiUUInput:(CreateHttpsApiRestShApiUUInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiUU) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiUUInput *input = [[CreateHttpsApiRestShApiUUInput alloc]init];
    input.body = [[HttpsApiRestShApiUUModel alloc]init];
    input.contentType = @"Content-Type";

    [self.userManagement createHttpsApiRestShApiUUAsyncWithCreateHttpsApiRestShApiUUInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUURModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_ud_async_with_get_https_api_rest_sh_api_ud_input"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUDAsyncWithGetHttpsApiRestShApiUDInput") getHttpsApiRestShApiUDAsyncWithGetHttpsApiRestShApiUDInput

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```objc
function getHttpsApiRestShApiUDAsyncWithGetHttpsApiRestShApiUDInput:(GetHttpsApiRestShApiUDInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiUD) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiUDInput *input = [[GetHttpsApiRestShApiUDInput alloc]init];
    input.api = @"api";
    input.uid = @"uid";
    input.user = @"user";
    input.apiuid = @"apiuid";
    input.contentType = @"Content-Type";

    [self.userManagement getHttpsApiRestShApiUDAsyncWithGetHttpsApiRestShApiUDInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUDRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_ud_async_with_create_https_api_rest_sh_api_ud_input"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUDAsyncWithCreateHttpsApiRestShApiUDInput") createHttpsApiRestShApiUDAsyncWithCreateHttpsApiRestShApiUDInput

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```objc
function createHttpsApiRestShApiUDAsyncWithCreateHttpsApiRestShApiUDInput:(CreateHttpsApiRestShApiUDInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiUD) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiUDInput *input = [[CreateHttpsApiRestShApiUDInput alloc]init];
    input.body = [[HttpsApiRestShApiUDModel alloc]init];
    input.contentType = @"Content-Type";

    [self.userManagement createHttpsApiRestShApiUDAsyncWithCreateHttpsApiRestShApiUDInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUDRModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration_controller"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistrationController") LoginAndRegistrationController

### Get singleton instance
```objc
LoginAndRegistration* loginAndRegistration = [[LoginAndRegistration alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_aur_async_with_get_https_api_rest_sh_api_aur_input"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAURAsyncWithGetHttpsApiRestShApiAURInput") getHttpsApiRestShApiAURAsyncWithGetHttpsApiRestShApiAURInput

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```objc
function getHttpsApiRestShApiAURAsyncWithGetHttpsApiRestShApiAURInput:(GetHttpsApiRestShApiAURInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiAUR) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiAURInput *input = [[GetHttpsApiRestShApiAURInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.password = @"password";
    input.name = @"name";
    input.email = @"email";
    input.phone = 239;
    input.countrycode = 239;
    input.address = @"address";
    input.contentType = @"Content-Type";

    [self.loginAndRegistration getHttpsApiRestShApiAURAsyncWithGetHttpsApiRestShApiAURInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAURRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_aur_async_with_create_https_api_rest_sh_api_aur_input"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAURAsyncWithCreateHttpsApiRestShApiAURInput") createHttpsApiRestShApiAURAsyncWithCreateHttpsApiRestShApiAURInput

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```objc
function createHttpsApiRestShApiAURAsyncWithCreateHttpsApiRestShApiAURInput:(CreateHttpsApiRestShApiAURInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiAUR) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiAURInput *input = [[CreateHttpsApiRestShApiAURInput alloc]init];
    input.body = [[HttpsApiRestShApiAURModel alloc]init];
    input.contentType = @"Content-Type";

    [self.loginAndRegistration createHttpsApiRestShApiAURAsyncWithCreateHttpsApiRestShApiAURInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAURRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_aul_async_with_get_https_api_rest_sh_api_aul_input"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAULAsyncWithGetHttpsApiRestShApiAULInput") getHttpsApiRestShApiAULAsyncWithGetHttpsApiRestShApiAULInput

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```objc
function getHttpsApiRestShApiAULAsyncWithGetHttpsApiRestShApiAULInput:(GetHttpsApiRestShApiAULInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiAUL) onCompleted(input)
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

```objc
    // Parameters for the API call
    GetHttpsApiRestShApiAULInput *input = [[GetHttpsApiRestShApiAULInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.password = @"password";
    input.contentType = @"Content-Type";

    [self.loginAndRegistration getHttpsApiRestShApiAULAsyncWithGetHttpsApiRestShApiAULInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAULRModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_aul_async_with_create_https_api_rest_sh_api_aul_input"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAULAsyncWithCreateHttpsApiRestShApiAULInput") createHttpsApiRestShApiAULAsyncWithCreateHttpsApiRestShApiAULInput

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```objc
function createHttpsApiRestShApiAULAsyncWithCreateHttpsApiRestShApiAULInput:(CreateHttpsApiRestShApiAULInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiAUL) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiAULInput *input = [[CreateHttpsApiRestShApiAULInput alloc]init];
    input.body = [[HttpsApiRestShApiAULModel alloc]init];
    input.contentType = @"Content-Type";

    [self.loginAndRegistration createHttpsApiRestShApiAULAsyncWithCreateHttpsApiRestShApiAULInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAULRModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)



