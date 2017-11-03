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

### <a name="get_https_api_rest_sh_api_security_logging_info_async_with_get_https_api_rest_sh_api_security_logging_info_input"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSecurityLoggingInfoAsyncWithGetHttpsApiRestShApiSecurityLoggingInfoInput") getHttpsApiRestShApiSecurityLoggingInfoAsyncWithGetHttpsApiRestShApiSecurityLoggingInfoInput

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```objc
function getHttpsApiRestShApiSecurityLoggingInfoAsyncWithGetHttpsApiRestShApiSecurityLoggingInfoInput:(GetHttpsApiRestShApiSecurityLoggingInfoInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSecurityLoggingInfo) onCompleted(input)
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
    GetHttpsApiRestShApiSecurityLoggingInfoInput *input = [[GetHttpsApiRestShApiSecurityLoggingInfoInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.name = @"name";
    input.origin = @"origin";
    input.time = @"time";
    input.contentType = @"Content-Type";

    [self.advancedLogging getHttpsApiRestShApiSecurityLoggingInfoAsyncWithGetHttpsApiRestShApiSecurityLoggingInfoInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSecurityLoggingInfoResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_security_logging_async_with_get_https_api_rest_sh_api_security_logging_input"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSecurityLoggingAsyncWithGetHttpsApiRestShApiSecurityLoggingInput") getHttpsApiRestShApiSecurityLoggingAsyncWithGetHttpsApiRestShApiSecurityLoggingInput

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```objc
function getHttpsApiRestShApiSecurityLoggingAsyncWithGetHttpsApiRestShApiSecurityLoggingInput:(GetHttpsApiRestShApiSecurityLoggingInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSecurityLogging) onCompleted(input)
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
    GetHttpsApiRestShApiSecurityLoggingInput *input = [[GetHttpsApiRestShApiSecurityLoggingInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.name = @"name";
    input.origin = @"origin";
    input.activate = false;
    input.contentType = @"Content-Type";

    [self.advancedLogging getHttpsApiRestShApiSecurityLoggingAsyncWithGetHttpsApiRestShApiSecurityLoggingInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSecurityLoggingResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_security_logging_info_async_with_create_https_api_rest_sh_api_security_logging_info_input"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSecurityLoggingInfoAsyncWithCreateHttpsApiRestShApiSecurityLoggingInfoInput") createHttpsApiRestShApiSecurityLoggingInfoAsyncWithCreateHttpsApiRestShApiSecurityLoggingInfoInput

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```objc
function createHttpsApiRestShApiSecurityLoggingInfoAsyncWithCreateHttpsApiRestShApiSecurityLoggingInfoInput:(CreateHttpsApiRestShApiSecurityLoggingInfoInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSecurityLoggingInfo) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSecurityLoggingInfoInput *input = [[CreateHttpsApiRestShApiSecurityLoggingInfoInput alloc]init];
    input.body = [[HttpsApiRestShApiSecurityLoggingInfoRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.advancedLogging createHttpsApiRestShApiSecurityLoggingInfoAsyncWithCreateHttpsApiRestShApiSecurityLoggingInfoInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSecurityLoggingInfoResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_security_logging_async_with_create_https_api_rest_sh_api_security_logging_input"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSecurityLoggingAsyncWithCreateHttpsApiRestShApiSecurityLoggingInput") createHttpsApiRestShApiSecurityLoggingAsyncWithCreateHttpsApiRestShApiSecurityLoggingInput

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```objc
function createHttpsApiRestShApiSecurityLoggingAsyncWithCreateHttpsApiRestShApiSecurityLoggingInput:(CreateHttpsApiRestShApiSecurityLoggingInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSecurityLogging) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSecurityLoggingInput *input = [[CreateHttpsApiRestShApiSecurityLoggingInput alloc]init];
    input.body = [[HttpsApiRestShApiSecurityLoggingRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.advancedLogging createHttpsApiRestShApiSecurityLoggingAsyncWithCreateHttpsApiRestShApiSecurityLoggingInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSecurityLoggingResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection_controller"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtectionController") WAFDDOSProtectionController

### Get singleton instance
```objc
WAFDDOSProtection* wAFDDOSProtection = [[WAFDDOSProtection alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_security_waf_configure_async_with_get_https_api_rest_sh_api_security_waf_configure_input"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSecurityWafConfigureAsyncWithGetHttpsApiRestShApiSecurityWafConfigureInput") getHttpsApiRestShApiSecurityWafConfigureAsyncWithGetHttpsApiRestShApiSecurityWafConfigureInput

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function getHttpsApiRestShApiSecurityWafConfigureAsyncWithGetHttpsApiRestShApiSecurityWafConfigureInput:(GetHttpsApiRestShApiSecurityWafConfigureInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSecurityWafConfigure) onCompleted(input)
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
    GetHttpsApiRestShApiSecurityWafConfigureInput *input = [[GetHttpsApiRestShApiSecurityWafConfigureInput alloc]init];
    input.key = @"API";
    input.uid = @"UID";
    input.name = @"origin-name";
    input.origin = @"origin.yourdomain.tld";
    input.rule = @"header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does";
    input.contentType = @"application/json";

    [self.wAFDDOSProtection getHttpsApiRestShApiSecurityWafConfigureAsyncWithGetHttpsApiRestShApiSecurityWafConfigureInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSecurityWafConfigureResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_security_waf_async_with_get_https_api_rest_sh_api_security_waf_input"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSecurityWafAsyncWithGetHttpsApiRestShApiSecurityWafInput") getHttpsApiRestShApiSecurityWafAsyncWithGetHttpsApiRestShApiSecurityWafInput

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function getHttpsApiRestShApiSecurityWafAsyncWithGetHttpsApiRestShApiSecurityWafInput:(GetHttpsApiRestShApiSecurityWafInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSecurityWaf) onCompleted(input)
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
    GetHttpsApiRestShApiSecurityWafInput *input = [[GetHttpsApiRestShApiSecurityWafInput alloc]init];
    input.key = @"API";
    input.uid = @"UID";
    input.origin = @"origin.yourdomain.tld";
    input.cname = @"yourdomain.tld,www.yourdomain.tld";
    input.contentType = @"application/json";

    [self.wAFDDOSProtection getHttpsApiRestShApiSecurityWafAsyncWithGetHttpsApiRestShApiSecurityWafInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSecurityWafResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_security_waf_configure_async_with_create_https_api_rest_sh_api_security_waf_configure_input"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSecurityWafConfigureAsyncWithCreateHttpsApiRestShApiSecurityWafConfigureInput") createHttpsApiRestShApiSecurityWafConfigureAsyncWithCreateHttpsApiRestShApiSecurityWafConfigureInput

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function createHttpsApiRestShApiSecurityWafConfigureAsyncWithCreateHttpsApiRestShApiSecurityWafConfigureInput:(CreateHttpsApiRestShApiSecurityWafConfigureInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSecurityWafConfigure) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSecurityWafConfigureInput *input = [[CreateHttpsApiRestShApiSecurityWafConfigureInput alloc]init];
    input.body = (HttpsApiRestShApiSecurityWafConfigureRequestModel*) [APIHelper jsonDeserialize: @"{
  \"key\": \"YOUR API KEY\",
  \"uid\": \"YOUR USER ID\",
  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",
  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",
  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"
}"
                toClass: HttpsApiRestShApiSecurityWafConfigureRequestModel.class];
    input.contentType = @"application/json";

    [self.wAFDDOSProtection createHttpsApiRestShApiSecurityWafConfigureAsyncWithCreateHttpsApiRestShApiSecurityWafConfigureInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSecurityWafConfigureResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_security_waf_async_with_create_https_api_rest_sh_api_security_waf_input"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSecurityWafAsyncWithCreateHttpsApiRestShApiSecurityWafInput") createHttpsApiRestShApiSecurityWafAsyncWithCreateHttpsApiRestShApiSecurityWafInput

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function createHttpsApiRestShApiSecurityWafAsyncWithCreateHttpsApiRestShApiSecurityWafInput:(CreateHttpsApiRestShApiSecurityWafInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSecurityWaf) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSecurityWafInput *input = [[CreateHttpsApiRestShApiSecurityWafInput alloc]init];
    input.body = (HttpsApiRestShApiSecurityWafRequestModel*) [APIHelper jsonDeserialize: @"{
  \"key\": \"YOUR API KEY\",
  \"uid\": \"YOUR USER ID\",
  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",
  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"
}"
                toClass: HttpsApiRestShApiSecurityWafRequestModel.class];
    input.contentType = @"application/json";

    [self.wAFDDOSProtection createHttpsApiRestShApiSecurityWafAsyncWithCreateHttpsApiRestShApiSecurityWafInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSecurityWafResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EncryptionController") EncryptionController

### Get singleton instance
```objc
Encryption* encryption = [[Encryption alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_security_encryption_async_with_get_https_api_rest_sh_api_security_encryption_input"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.getHttpsApiRestShApiSecurityEncryptionAsyncWithGetHttpsApiRestShApiSecurityEncryptionInput") getHttpsApiRestShApiSecurityEncryptionAsyncWithGetHttpsApiRestShApiSecurityEncryptionInput

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```objc
function getHttpsApiRestShApiSecurityEncryptionAsyncWithGetHttpsApiRestShApiSecurityEncryptionInput:(GetHttpsApiRestShApiSecurityEncryptionInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiSecurityEncryption) onCompleted(input)
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
    GetHttpsApiRestShApiSecurityEncryptionInput *input = [[GetHttpsApiRestShApiSecurityEncryptionInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.data = @"data";
    input.method = @"method";
    input.bit = 101;
    input.contentType = @"Content-Type";

    [self.encryption getHttpsApiRestShApiSecurityEncryptionAsyncWithGetHttpsApiRestShApiSecurityEncryptionInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSecurityEncryptionResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_security_encryption_async_with_create_https_api_rest_sh_api_security_encryption_input"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.createHttpsApiRestShApiSecurityEncryptionAsyncWithCreateHttpsApiRestShApiSecurityEncryptionInput") createHttpsApiRestShApiSecurityEncryptionAsyncWithCreateHttpsApiRestShApiSecurityEncryptionInput

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```objc
function createHttpsApiRestShApiSecurityEncryptionAsyncWithCreateHttpsApiRestShApiSecurityEncryptionInput:(CreateHttpsApiRestShApiSecurityEncryptionInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiSecurityEncryption) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiSecurityEncryptionInput *input = [[CreateHttpsApiRestShApiSecurityEncryptionInput alloc]init];
    input.body = [[HttpsApiRestShApiSecurityEncryptionRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.encryption createHttpsApiRestShApiSecurityEncryptionAsyncWithCreateHttpsApiRestShApiSecurityEncryptionInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSecurityEncryptionResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CDNController") CDNController

### Get singleton instance
```objc
CDN* cDN = [[CDN alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_service_cdn_push_async_with_get_https_api_rest_sh_api_service_cdn_push_input"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiServiceCdnPushAsyncWithGetHttpsApiRestShApiServiceCdnPushInput") getHttpsApiRestShApiServiceCdnPushAsyncWithGetHttpsApiRestShApiServiceCdnPushInput

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```objc
function getHttpsApiRestShApiServiceCdnPushAsyncWithGetHttpsApiRestShApiServiceCdnPushInput:(GetHttpsApiRestShApiServiceCdnPushInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiServiceCdnPush) onCompleted(input)
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
    GetHttpsApiRestShApiServiceCdnPushInput *input = [[GetHttpsApiRestShApiServiceCdnPushInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.cname = @"cname";
    input.file = @"file";
    input.contentType = @"Content-Type";

    [self.cDN getHttpsApiRestShApiServiceCdnPushAsyncWithGetHttpsApiRestShApiServiceCdnPushInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiServiceCdnPushResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_service_cdn_pull_async_with_get_https_api_rest_sh_api_service_cdn_pull_input"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiServiceCdnPullAsyncWithGetHttpsApiRestShApiServiceCdnPullInput") getHttpsApiRestShApiServiceCdnPullAsyncWithGetHttpsApiRestShApiServiceCdnPullInput

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```objc
function getHttpsApiRestShApiServiceCdnPullAsyncWithGetHttpsApiRestShApiServiceCdnPullInput:(GetHttpsApiRestShApiServiceCdnPullInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiServiceCdnPull) onCompleted(input)
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
    GetHttpsApiRestShApiServiceCdnPullInput *input = [[GetHttpsApiRestShApiServiceCdnPullInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.origin = @"origin";
    input.cname = @"cname";
    input.contentType = @"Content-Type";

    [self.cDN getHttpsApiRestShApiServiceCdnPullAsyncWithGetHttpsApiRestShApiServiceCdnPullInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiServiceCdnPullResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_service_cdn_push_async_with_create_https_api_rest_sh_api_service_cdn_push_input"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiServiceCdnPushAsyncWithCreateHttpsApiRestShApiServiceCdnPushInput") createHttpsApiRestShApiServiceCdnPushAsyncWithCreateHttpsApiRestShApiServiceCdnPushInput

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```objc
function createHttpsApiRestShApiServiceCdnPushAsyncWithCreateHttpsApiRestShApiServiceCdnPushInput:(CreateHttpsApiRestShApiServiceCdnPushInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiServiceCdnPush) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiServiceCdnPushInput *input = [[CreateHttpsApiRestShApiServiceCdnPushInput alloc]init];
    input.body = [[HttpsApiRestShApiServiceCdnPushRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.cDN createHttpsApiRestShApiServiceCdnPushAsyncWithCreateHttpsApiRestShApiServiceCdnPushInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiServiceCdnPushResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_service_cdn_pull_async_with_create_https_api_rest_sh_api_service_cdn_pull_input"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiServiceCdnPullAsyncWithCreateHttpsApiRestShApiServiceCdnPullInput") createHttpsApiRestShApiServiceCdnPullAsyncWithCreateHttpsApiRestShApiServiceCdnPullInput

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```objc
function createHttpsApiRestShApiServiceCdnPullAsyncWithCreateHttpsApiRestShApiServiceCdnPullInput:(CreateHttpsApiRestShApiServiceCdnPullInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiServiceCdnPull) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiServiceCdnPullInput *input = [[CreateHttpsApiRestShApiServiceCdnPullInput alloc]init];
    input.body = [[HttpsApiRestShApiServiceCdnPullRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.cDN createHttpsApiRestShApiServiceCdnPullAsyncWithCreateHttpsApiRestShApiServiceCdnPullInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiServiceCdnPullResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DNSController") DNSController

### Get singleton instance
```objc
DNS* dNS = [[DNS alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_service_dns_configure_async_with_get_https_api_rest_sh_api_service_dns_configure_input"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiServiceDnsConfigureAsyncWithGetHttpsApiRestShApiServiceDnsConfigureInput") getHttpsApiRestShApiServiceDnsConfigureAsyncWithGetHttpsApiRestShApiServiceDnsConfigureInput

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```objc
function getHttpsApiRestShApiServiceDnsConfigureAsyncWithGetHttpsApiRestShApiServiceDnsConfigureInput:(GetHttpsApiRestShApiServiceDnsConfigureInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiServiceDnsConfigure) onCompleted(input)
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
    GetHttpsApiRestShApiServiceDnsConfigureInput *input = [[GetHttpsApiRestShApiServiceDnsConfigureInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.domain = @"domain";
    input.records = @"records";
    input.contentType = @"Content-Type";

    [self.dNS getHttpsApiRestShApiServiceDnsConfigureAsyncWithGetHttpsApiRestShApiServiceDnsConfigureInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiServiceDnsConfigureResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_service_dns_configure_async_with_create_https_api_rest_sh_api_service_dns_configure_input"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiServiceDnsConfigureAsyncWithCreateHttpsApiRestShApiServiceDnsConfigureInput") createHttpsApiRestShApiServiceDnsConfigureAsyncWithCreateHttpsApiRestShApiServiceDnsConfigureInput

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```objc
function createHttpsApiRestShApiServiceDnsConfigureAsyncWithCreateHttpsApiRestShApiServiceDnsConfigureInput:(CreateHttpsApiRestShApiServiceDnsConfigureInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiServiceDnsConfigure) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiServiceDnsConfigureInput *input = [[CreateHttpsApiRestShApiServiceDnsConfigureInput alloc]init];
    input.body = [[HttpsApiRestShApiServiceDnsConfigureRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.dNS createHttpsApiRestShApiServiceDnsConfigureAsyncWithCreateHttpsApiRestShApiServiceDnsConfigureInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiServiceDnsConfigureResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_service_dns_add_async_with_get_https_api_rest_sh_api_service_dns_add_input"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiServiceDnsAddAsyncWithGetHttpsApiRestShApiServiceDnsAddInput") getHttpsApiRestShApiServiceDnsAddAsyncWithGetHttpsApiRestShApiServiceDnsAddInput

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```objc
function getHttpsApiRestShApiServiceDnsAddAsyncWithGetHttpsApiRestShApiServiceDnsAddInput:(GetHttpsApiRestShApiServiceDnsAddInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiServiceDnsAdd) onCompleted(input)
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
    GetHttpsApiRestShApiServiceDnsAddInput *input = [[GetHttpsApiRestShApiServiceDnsAddInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.domain = @"domain";
    input.contentType = @"Content-Type";

    [self.dNS getHttpsApiRestShApiServiceDnsAddAsyncWithGetHttpsApiRestShApiServiceDnsAddInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiServiceDnsAddResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_service_dns_add_async_with_create_https_api_rest_sh_api_service_dns_add_input"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiServiceDnsAddAsyncWithCreateHttpsApiRestShApiServiceDnsAddInput") createHttpsApiRestShApiServiceDnsAddAsyncWithCreateHttpsApiRestShApiServiceDnsAddInput

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```objc
function createHttpsApiRestShApiServiceDnsAddAsyncWithCreateHttpsApiRestShApiServiceDnsAddInput:(CreateHttpsApiRestShApiServiceDnsAddInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiServiceDnsAdd) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiServiceDnsAddInput *input = [[CreateHttpsApiRestShApiServiceDnsAddInput alloc]init];
    input.body = [[HttpsApiRestShApiServiceDnsAddRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.dNS createHttpsApiRestShApiServiceDnsAddAsyncWithCreateHttpsApiRestShApiServiceDnsAddInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiServiceDnsAddResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscationController") CodeObfuscationController

### Get singleton instance
```objc
CodeObfuscation* codeObfuscation = [[CodeObfuscation alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_service_obfuscation_async_with_get_https_api_rest_sh_api_service_obfuscation_input"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.getHttpsApiRestShApiServiceObfuscationAsyncWithGetHttpsApiRestShApiServiceObfuscationInput") getHttpsApiRestShApiServiceObfuscationAsyncWithGetHttpsApiRestShApiServiceObfuscationInput

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```objc
function getHttpsApiRestShApiServiceObfuscationAsyncWithGetHttpsApiRestShApiServiceObfuscationInput:(GetHttpsApiRestShApiServiceObfuscationInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiServiceObfuscation) onCompleted(input)
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
    GetHttpsApiRestShApiServiceObfuscationInput *input = [[GetHttpsApiRestShApiServiceObfuscationInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.app = @"app";
    input.contentType = @"Content-Type";

    [self.codeObfuscation getHttpsApiRestShApiServiceObfuscationAsyncWithGetHttpsApiRestShApiServiceObfuscationInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiServiceObfuscationResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_service_obfuscation_async_with_create_https_api_rest_sh_api_service_obfuscation_input"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.createHttpsApiRestShApiServiceObfuscationAsyncWithCreateHttpsApiRestShApiServiceObfuscationInput") createHttpsApiRestShApiServiceObfuscationAsyncWithCreateHttpsApiRestShApiServiceObfuscationInput

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```objc
function createHttpsApiRestShApiServiceObfuscationAsyncWithCreateHttpsApiRestShApiServiceObfuscationInput:(CreateHttpsApiRestShApiServiceObfuscationInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiServiceObfuscation) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiServiceObfuscationInput *input = [[CreateHttpsApiRestShApiServiceObfuscationInput alloc]init];
    input.body = [[HttpsApiRestShApiServiceObfuscationRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.codeObfuscation createHttpsApiRestShApiServiceObfuscationAsyncWithCreateHttpsApiRestShApiServiceObfuscationInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiServiceObfuscationResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting_controller"></a>![Class: ](https://apidocs.io/img/class.png ".HostingController") HostingController

### Get singleton instance
```objc
Hosting* hosting = [[Hosting alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_service_hosting_async_with_get_https_api_rest_sh_api_service_hosting_input"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.getHttpsApiRestShApiServiceHostingAsyncWithGetHttpsApiRestShApiServiceHostingInput") getHttpsApiRestShApiServiceHostingAsyncWithGetHttpsApiRestShApiServiceHostingInput

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```objc
function getHttpsApiRestShApiServiceHostingAsyncWithGetHttpsApiRestShApiServiceHostingInput:(GetHttpsApiRestShApiServiceHostingInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiServiceHosting) onCompleted(input)
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
    GetHttpsApiRestShApiServiceHostingInput *input = [[GetHttpsApiRestShApiServiceHostingInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.app = @"app";
    input.domain = @"domain";
    input.contentType = @"Content-Type";

    [self.hosting getHttpsApiRestShApiServiceHostingAsyncWithGetHttpsApiRestShApiServiceHostingInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiServiceHostingResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_service_hosting_async_with_create_https_api_rest_sh_api_service_hosting_input"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.createHttpsApiRestShApiServiceHostingAsyncWithCreateHttpsApiRestShApiServiceHostingInput") createHttpsApiRestShApiServiceHostingAsyncWithCreateHttpsApiRestShApiServiceHostingInput

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```objc
function createHttpsApiRestShApiServiceHostingAsyncWithCreateHttpsApiRestShApiServiceHostingInput:(CreateHttpsApiRestShApiServiceHostingInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiServiceHosting) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiServiceHostingInput *input = [[CreateHttpsApiRestShApiServiceHostingInput alloc]init];
    input.body = [[HttpsApiRestShApiServiceHostingRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.hosting createHttpsApiRestShApiServiceHostingAsyncWithCreateHttpsApiRestShApiServiceHostingInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiServiceHostingResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPIController") DataManipulationConversionSortingAndCompressionAPIController

### Get singleton instance
```objc
DataManipulationConversionSortingAndCompressionAPI* dataManipulationConversionSortingAndCompressionAPI = [[DataManipulationConversionSortingAndCompressionAPI alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_data_async_with_get_https_api_rest_sh_api_data_input"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.getHttpsApiRestShApiDataAsyncWithGetHttpsApiRestShApiDataInput") getHttpsApiRestShApiDataAsyncWithGetHttpsApiRestShApiDataInput

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function getHttpsApiRestShApiDataAsyncWithGetHttpsApiRestShApiDataInput:(GetHttpsApiRestShApiDataInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiData) onCompleted(input)
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
    GetHttpsApiRestShApiDataInput *input = [[GetHttpsApiRestShApiDataInput alloc]init];
    input.key = @"API";
    input.uid = @"UID";
    input.user = @"UID";
    input.apiuid = @"apiUID";
    input.data = @"https://static.yourcdn.com/data.file";
    input.contentType = @"application/json";

    [self.dataManipulationConversionSortingAndCompressionAPI getHttpsApiRestShApiDataAsyncWithGetHttpsApiRestShApiDataInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiDataResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_data_async_with_create_https_api_rest_sh_api_data_input"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.createHttpsApiRestShApiDataAsyncWithCreateHttpsApiRestShApiDataInput") createHttpsApiRestShApiDataAsyncWithCreateHttpsApiRestShApiDataInput

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function createHttpsApiRestShApiDataAsyncWithCreateHttpsApiRestShApiDataInput:(CreateHttpsApiRestShApiDataInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiData) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiDataInput *input = [[CreateHttpsApiRestShApiDataInput alloc]init];
    input.body = (HttpsApiRestShApiDataRequestModel*) [APIHelper jsonDeserialize: @"{
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
                toClass: HttpsApiRestShApiDataRequestModel.class];
    input.contentType = @"application/json";

    [self.dataManipulationConversionSortingAndCompressionAPI createHttpsApiRestShApiDataAsyncWithCreateHttpsApiRestShApiDataInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiDataResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPIController") ImageManipulationAndModerationAPIController

### Get singleton instance
```objc
ImageManipulationAndModerationAPI* imageManipulationAndModerationAPI = [[ImageManipulationAndModerationAPI alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_image_async_with_get_https_api_rest_sh_api_image_input"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.getHttpsApiRestShApiImageAsyncWithGetHttpsApiRestShApiImageInput") getHttpsApiRestShApiImageAsyncWithGetHttpsApiRestShApiImageInput

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```objc
function getHttpsApiRestShApiImageAsyncWithGetHttpsApiRestShApiImageInput:(GetHttpsApiRestShApiImageInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiImage) onCompleted(input)
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
    GetHttpsApiRestShApiImageInput *input = [[GetHttpsApiRestShApiImageInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.image = @"image";
    input.transform = @"transform";
    input.contentType = @"Content-Type";

    [self.imageManipulationAndModerationAPI getHttpsApiRestShApiImageAsyncWithGetHttpsApiRestShApiImageInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiImageResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_image_async_with_create_https_api_rest_sh_api_image_input"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.createHttpsApiRestShApiImageAsyncWithCreateHttpsApiRestShApiImageInput") createHttpsApiRestShApiImageAsyncWithCreateHttpsApiRestShApiImageInput

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```objc
function createHttpsApiRestShApiImageAsyncWithCreateHttpsApiRestShApiImageInput:(CreateHttpsApiRestShApiImageInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiImage) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiImageInput *input = [[CreateHttpsApiRestShApiImageInput alloc]init];
    input.body = [[HttpsApiRestShApiImageRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.imageManipulationAndModerationAPI createHttpsApiRestShApiImageAsyncWithCreateHttpsApiRestShApiImageInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiImageResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VerificationController") VerificationController

### Get singleton instance
```objc
Verification* verification = [[Verification alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_verify_address_async_with_get_https_api_rest_sh_api_verify_address_input"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVerifyAddressAsyncWithGetHttpsApiRestShApiVerifyAddressInput") getHttpsApiRestShApiVerifyAddressAsyncWithGetHttpsApiRestShApiVerifyAddressInput

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```objc
function getHttpsApiRestShApiVerifyAddressAsyncWithGetHttpsApiRestShApiVerifyAddressInput:(GetHttpsApiRestShApiVerifyAddressInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiVerifyAddress) onCompleted(input)
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
    GetHttpsApiRestShApiVerifyAddressInput *input = [[GetHttpsApiRestShApiVerifyAddressInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.a = @"a";
    input.sa = @"sa";
    input.c = @"c";
    input.s = @"s";
    input.z = 192;
    input.contentType = @"Content-Type";

    [self.verification getHttpsApiRestShApiVerifyAddressAsyncWithGetHttpsApiRestShApiVerifyAddressInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVerifyAddressResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_verify_address_async_with_create_https_api_rest_sh_api_verify_address_input"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVerifyAddressAsyncWithCreateHttpsApiRestShApiVerifyAddressInput") createHttpsApiRestShApiVerifyAddressAsyncWithCreateHttpsApiRestShApiVerifyAddressInput

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```objc
function createHttpsApiRestShApiVerifyAddressAsyncWithCreateHttpsApiRestShApiVerifyAddressInput:(CreateHttpsApiRestShApiVerifyAddressInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiVerifyAddress) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiVerifyAddressInput *input = [[CreateHttpsApiRestShApiVerifyAddressInput alloc]init];
    input.body = [[HttpsApiRestShApiVerifyAddressRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.verification createHttpsApiRestShApiVerifyAddressAsyncWithCreateHttpsApiRestShApiVerifyAddressInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVerifyAddressResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_verify_user_async_with_get_https_api_rest_sh_api_verify_user_input"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVerifyUserAsyncWithGetHttpsApiRestShApiVerifyUserInput") getHttpsApiRestShApiVerifyUserAsyncWithGetHttpsApiRestShApiVerifyUserInput

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```objc
function getHttpsApiRestShApiVerifyUserAsyncWithGetHttpsApiRestShApiVerifyUserInput:(GetHttpsApiRestShApiVerifyUserInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiVerifyUser) onCompleted(input)
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
    GetHttpsApiRestShApiVerifyUserInput *input = [[GetHttpsApiRestShApiVerifyUserInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.code = @"code";
    input.contentType = @"Content-Type";

    [self.verification getHttpsApiRestShApiVerifyUserAsyncWithGetHttpsApiRestShApiVerifyUserInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVerifyUserResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_verify_user_async_with_create_https_api_rest_sh_api_verify_user_input"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVerifyUserAsyncWithCreateHttpsApiRestShApiVerifyUserInput") createHttpsApiRestShApiVerifyUserAsyncWithCreateHttpsApiRestShApiVerifyUserInput

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```objc
function createHttpsApiRestShApiVerifyUserAsyncWithCreateHttpsApiRestShApiVerifyUserInput:(CreateHttpsApiRestShApiVerifyUserInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiVerifyUser) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiVerifyUserInput *input = [[CreateHttpsApiRestShApiVerifyUserInput alloc]init];
    input.body = [[HttpsApiRestShApiVerifyUserRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.verification createHttpsApiRestShApiVerifyUserAsyncWithCreateHttpsApiRestShApiVerifyUserInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVerifyUserResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_verify_async_with_get_https_api_rest_sh_api_verify_input"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVerifyAsyncWithGetHttpsApiRestShApiVerifyInput") getHttpsApiRestShApiVerifyAsyncWithGetHttpsApiRestShApiVerifyInput

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```objc
function getHttpsApiRestShApiVerifyAsyncWithGetHttpsApiRestShApiVerifyInput:(GetHttpsApiRestShApiVerifyInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiVerify) onCompleted(input)
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
    GetHttpsApiRestShApiVerifyInput *input = [[GetHttpsApiRestShApiVerifyInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.to = @"to";
    input.contentType = @"Content-Type";

    [self.verification getHttpsApiRestShApiVerifyAsyncWithGetHttpsApiRestShApiVerifyInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVerifyResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_verify_async_with_create_https_api_rest_sh_api_verify_input"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVerifyAsyncWithCreateHttpsApiRestShApiVerifyInput") createHttpsApiRestShApiVerifyAsyncWithCreateHttpsApiRestShApiVerifyInput

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```objc
function createHttpsApiRestShApiVerifyAsyncWithCreateHttpsApiRestShApiVerifyInput:(CreateHttpsApiRestShApiVerifyInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiVerify) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiVerifyInput *input = [[CreateHttpsApiRestShApiVerifyInput alloc]init];
    input.body = [[HttpsApiRestShApiVerifyRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.verification createHttpsApiRestShApiVerifyAsyncWithCreateHttpsApiRestShApiVerifyInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVerifyResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPIController") TwoFactorAuthenticationAPIController

### Get singleton instance
```objc
TwoFactorAuthenticationAPI* twoFactorAuthenticationAPI = [[TwoFactorAuthenticationAPI alloc]init] ;
```

### <a name="get_https_api_rest_sh_api2fa_token_async_with_get_https_api_rest_sh_api2fa_token_input"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2faTokenAsyncWithGetHttpsApiRestShApi2faTokenInput") getHttpsApiRestShApi2faTokenAsyncWithGetHttpsApiRestShApi2faTokenInput

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```objc
function getHttpsApiRestShApi2faTokenAsyncWithGetHttpsApiRestShApi2faTokenInput:(GetHttpsApiRestShApi2faTokenInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApi2faToken) onCompleted(input)
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
    GetHttpsApiRestShApi2faTokenInput *input = [[GetHttpsApiRestShApi2faTokenInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.code = @"code";
    input.contentType = @"Content-Type";

    [self.twoFactorAuthenticationAPI getHttpsApiRestShApi2faTokenAsyncWithGetHttpsApiRestShApi2faTokenInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faTokenResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api2fa_token_async_with_create_https_api_rest_sh_api2fa_token_input"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2faTokenAsyncWithCreateHttpsApiRestShApi2faTokenInput") createHttpsApiRestShApi2faTokenAsyncWithCreateHttpsApiRestShApi2faTokenInput

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```objc
function createHttpsApiRestShApi2faTokenAsyncWithCreateHttpsApiRestShApi2faTokenInput:(CreateHttpsApiRestShApi2faTokenInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApi2faToken) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApi2faTokenInput *input = [[CreateHttpsApiRestShApi2faTokenInput alloc]init];
    input.body = [[HttpsApiRestShApi2faTokenRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.twoFactorAuthenticationAPI createHttpsApiRestShApi2faTokenAsyncWithCreateHttpsApiRestShApi2faTokenInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faTokenResponseModel* response, NSError* error) { 
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

    [self.twoFactorAuthenticationAPI getHttpsApiRestShApi2faAsyncWithGetHttpsApiRestShApi2faInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faResponseModel* response, NSError* error) { 
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
    input.body = [[HttpsApiRestShApi2faRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.twoFactorAuthenticationAPI createHttpsApiRestShApi2faAsyncWithCreateHttpsApiRestShApi2faInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagementController") UserManagementController

### Get singleton instance
```objc
UserManagement* userManagement = [[UserManagement alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_user_info_async_with_get_https_api_rest_sh_api_user_info_input"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUserInfoAsyncWithGetHttpsApiRestShApiUserInfoInput") getHttpsApiRestShApiUserInfoAsyncWithGetHttpsApiRestShApiUserInfoInput

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```objc
function getHttpsApiRestShApiUserInfoAsyncWithGetHttpsApiRestShApiUserInfoInput:(GetHttpsApiRestShApiUserInfoInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiUserInfo) onCompleted(input)
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
    GetHttpsApiRestShApiUserInfoInput *input = [[GetHttpsApiRestShApiUserInfoInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.apiuid = @"apiuid";
    input.contentType = @"Content-Type";

    [self.userManagement getHttpsApiRestShApiUserInfoAsyncWithGetHttpsApiRestShApiUserInfoInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUserInfoResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_user_info_async_with_create_https_api_rest_sh_api_user_info_input"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUserInfoAsyncWithCreateHttpsApiRestShApiUserInfoInput") createHttpsApiRestShApiUserInfoAsyncWithCreateHttpsApiRestShApiUserInfoInput

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```objc
function createHttpsApiRestShApiUserInfoAsyncWithCreateHttpsApiRestShApiUserInfoInput:(CreateHttpsApiRestShApiUserInfoInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiUserInfo) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiUserInfoInput *input = [[CreateHttpsApiRestShApiUserInfoInput alloc]init];
    input.body = [[HttpsApiRestShApiUserInfoRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.userManagement createHttpsApiRestShApiUserInfoAsyncWithCreateHttpsApiRestShApiUserInfoInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUserInfoResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_user_update_async_with_get_https_api_rest_sh_api_user_update_input"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUserUpdateAsyncWithGetHttpsApiRestShApiUserUpdateInput") getHttpsApiRestShApiUserUpdateAsyncWithGetHttpsApiRestShApiUserUpdateInput

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```objc
function getHttpsApiRestShApiUserUpdateAsyncWithGetHttpsApiRestShApiUserUpdateInput:(GetHttpsApiRestShApiUserUpdateInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiUserUpdate) onCompleted(input)
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
    GetHttpsApiRestShApiUserUpdateInput *input = [[GetHttpsApiRestShApiUserUpdateInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.apiuid = @"apiuid";
    input.avatar = @"avatar";
    input.customInput = @"custom input";
    input.contentType = @"Content-Type";

    [self.userManagement getHttpsApiRestShApiUserUpdateAsyncWithGetHttpsApiRestShApiUserUpdateInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUserUpdateResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_user_update_async_with_create_https_api_rest_sh_api_user_update_input"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUserUpdateAsyncWithCreateHttpsApiRestShApiUserUpdateInput") createHttpsApiRestShApiUserUpdateAsyncWithCreateHttpsApiRestShApiUserUpdateInput

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```objc
function createHttpsApiRestShApiUserUpdateAsyncWithCreateHttpsApiRestShApiUserUpdateInput:(CreateHttpsApiRestShApiUserUpdateInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiUserUpdate) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiUserUpdateInput *input = [[CreateHttpsApiRestShApiUserUpdateInput alloc]init];
    input.body = [[HttpsApiRestShApiUserUpdateRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.userManagement createHttpsApiRestShApiUserUpdateAsyncWithCreateHttpsApiRestShApiUserUpdateInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUserUpdateResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_user_delete_async_with_get_https_api_rest_sh_api_user_delete_input"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUserDeleteAsyncWithGetHttpsApiRestShApiUserDeleteInput") getHttpsApiRestShApiUserDeleteAsyncWithGetHttpsApiRestShApiUserDeleteInput

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```objc
function getHttpsApiRestShApiUserDeleteAsyncWithGetHttpsApiRestShApiUserDeleteInput:(GetHttpsApiRestShApiUserDeleteInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiUserDelete) onCompleted(input)
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
    GetHttpsApiRestShApiUserDeleteInput *input = [[GetHttpsApiRestShApiUserDeleteInput alloc]init];
    input.api = @"api";
    input.uid = @"uid";
    input.user = @"user";
    input.apiuid = @"apiuid";
    input.contentType = @"Content-Type";

    [self.userManagement getHttpsApiRestShApiUserDeleteAsyncWithGetHttpsApiRestShApiUserDeleteInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUserDeleteResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_user_delete_async_with_create_https_api_rest_sh_api_user_delete_input"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUserDeleteAsyncWithCreateHttpsApiRestShApiUserDeleteInput") createHttpsApiRestShApiUserDeleteAsyncWithCreateHttpsApiRestShApiUserDeleteInput

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```objc
function createHttpsApiRestShApiUserDeleteAsyncWithCreateHttpsApiRestShApiUserDeleteInput:(CreateHttpsApiRestShApiUserDeleteInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiUserDelete) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiUserDeleteInput *input = [[CreateHttpsApiRestShApiUserDeleteInput alloc]init];
    input.body = [[HttpsApiRestShApiUserDeleteRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.userManagement createHttpsApiRestShApiUserDeleteAsyncWithCreateHttpsApiRestShApiUserDeleteInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUserDeleteResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration_controller"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistrationController") LoginAndRegistrationController

### Get singleton instance
```objc
LoginAndRegistration* loginAndRegistration = [[LoginAndRegistration alloc]init] ;
```

### <a name="get_https_api_rest_sh_api_auth_user_register_async_with_get_https_api_rest_sh_api_auth_user_register_input"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAuthUserRegisterAsyncWithGetHttpsApiRestShApiAuthUserRegisterInput") getHttpsApiRestShApiAuthUserRegisterAsyncWithGetHttpsApiRestShApiAuthUserRegisterInput

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```objc
function getHttpsApiRestShApiAuthUserRegisterAsyncWithGetHttpsApiRestShApiAuthUserRegisterInput:(GetHttpsApiRestShApiAuthUserRegisterInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiAuthUserRegister) onCompleted(input)
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
    GetHttpsApiRestShApiAuthUserRegisterInput *input = [[GetHttpsApiRestShApiAuthUserRegisterInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.password = @"password";
    input.name = @"name";
    input.email = @"email";
    input.phone = 192;
    input.countrycode = 192;
    input.address = @"address";
    input.contentType = @"Content-Type";

    [self.loginAndRegistration getHttpsApiRestShApiAuthUserRegisterAsyncWithGetHttpsApiRestShApiAuthUserRegisterInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAuthUserRegisterResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_auth_user_register_async_with_create_https_api_rest_sh_api_auth_user_register_input"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAuthUserRegisterAsyncWithCreateHttpsApiRestShApiAuthUserRegisterInput") createHttpsApiRestShApiAuthUserRegisterAsyncWithCreateHttpsApiRestShApiAuthUserRegisterInput

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```objc
function createHttpsApiRestShApiAuthUserRegisterAsyncWithCreateHttpsApiRestShApiAuthUserRegisterInput:(CreateHttpsApiRestShApiAuthUserRegisterInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiAuthUserRegister) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiAuthUserRegisterInput *input = [[CreateHttpsApiRestShApiAuthUserRegisterInput alloc]init];
    input.body = [[HttpsApiRestShApiAuthUserRegisterRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.loginAndRegistration createHttpsApiRestShApiAuthUserRegisterAsyncWithCreateHttpsApiRestShApiAuthUserRegisterInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAuthUserRegisterResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_https_api_rest_sh_api_auth_user_login_async_with_get_https_api_rest_sh_api_auth_user_login_input"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAuthUserLoginAsyncWithGetHttpsApiRestShApiAuthUserLoginInput") getHttpsApiRestShApiAuthUserLoginAsyncWithGetHttpsApiRestShApiAuthUserLoginInput

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```objc
function getHttpsApiRestShApiAuthUserLoginAsyncWithGetHttpsApiRestShApiAuthUserLoginInput:(GetHttpsApiRestShApiAuthUserLoginInput*) input
                completionBlock:(CompletedGetHttpsApiRestShApiAuthUserLogin) onCompleted(input)
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
    GetHttpsApiRestShApiAuthUserLoginInput *input = [[GetHttpsApiRestShApiAuthUserLoginInput alloc]init];
    input.key = @"key";
    input.uid = @"uid";
    input.user = @"user";
    input.password = @"password";
    input.contentType = @"Content-Type";

    [self.loginAndRegistration getHttpsApiRestShApiAuthUserLoginAsyncWithGetHttpsApiRestShApiAuthUserLoginInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAuthUserLoginResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_https_api_rest_sh_api_auth_user_login_async_with_create_https_api_rest_sh_api_auth_user_login_input"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAuthUserLoginAsyncWithCreateHttpsApiRestShApiAuthUserLoginInput") createHttpsApiRestShApiAuthUserLoginAsyncWithCreateHttpsApiRestShApiAuthUserLoginInput

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```objc
function createHttpsApiRestShApiAuthUserLoginAsyncWithCreateHttpsApiRestShApiAuthUserLoginInput:(CreateHttpsApiRestShApiAuthUserLoginInput*) input
                completionBlock:(CompletedPostHttpsApiRestShApiAuthUserLogin) onCompleted(input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CreateHttpsApiRestShApiAuthUserLoginInput *input = [[CreateHttpsApiRestShApiAuthUserLoginInput alloc]init];
    input.body = [[HttpsApiRestShApiAuthUserLoginRequestModel alloc]init];
    input.contentType = @"Content-Type";

    [self.loginAndRegistration createHttpsApiRestShApiAuthUserLoginAsyncWithCreateHttpsApiRestShApiAuthUserLoginInput: input completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAuthUserLoginResponseModel* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)



