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
| basicAuthUserName | The username to use with basic authentication |
| basicAuthPassword | The password to use with basic authentication |



Configuration variables can be set as following.
```Objc
// Configuration parameters and credentials
Configuration_BasicAuthUserName = "Configuration_BasicAuthUserName"; // The username to use with basic authentication
Configuration_BasicAuthPassword = "Configuration_BasicAuthPassword"; // The password to use with basic authentication

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

## <a name="advanced_logging"></a>![Class: ](https://apidocs.io/img/class.png ".AdvancedLogging") AdvancedLogging

### Get singleton instance
```objc
AdvancedLogging* advancedLogging = [[AdvancedLogging alloc]init] ;
```

### <a name="logging_info_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingInfoAsyncWithKey") loggingInfoAsyncWithKey

> WAF Log Info


```objc
function loggingInfoAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                name:(NSString*) name
                origin:(NSString*) origin
                time:(NSString*) time
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetLoggingInfo) onCompleted(key uid : uid name : name origin : origin time : time contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* name = @"name";
    NSString* origin = @"origin";
    NSString* time = @"time";
    NSString* contentType = @"Content-Type";

    [self.advancedLogging loggingInfoAsyncWithKey: key uid : uid name : name origin : origin time : time contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSLIR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="logging_setup_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingSetupAsyncWithKey") loggingSetupAsyncWithKey

> WAF Log Setup


```objc
function loggingSetupAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                name:(NSString*) name
                origin:(NSString*) origin
                activate:(BOOL) activate
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetLoggingSetup) onCompleted(key uid : uid name : name origin : origin activate : activate contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* name = @"name";
    NSString* origin = @"origin";
    BOOL activate = true;
    NSString* contentType = @"Content-Type";

    [self.advancedLogging loggingSetupAsyncWithKey: key uid : uid name : name origin : origin activate : activate contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSLR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="logging_info1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingInfo1AsyncWithBody") loggingInfo1AsyncWithBody

> WAF Log Info


```objc
function loggingInfo1AsyncWithBody:(HttpsApiRestShApiSLI*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostLoggingInfo1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiSLI* body = [[HttpsApiRestShApiSLI alloc]init];
    NSString* contentType = @"Content-Type";

    [self.advancedLogging loggingInfo1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSLIR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="logging_setup1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingSetup1AsyncWithBody") loggingSetup1AsyncWithBody

> WAF Log Setup


```objc
function loggingSetup1AsyncWithBody:(HttpsApiRestShApiSL*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostLoggingSetup1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiSL* body = [[HttpsApiRestShApiSL alloc]init];
    NSString* contentType = @"Content-Type";

    [self.advancedLogging loggingSetup1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSLR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtection") WAFDDOSProtection

### Get singleton instance
```objc
WAFDDOSProtection* wAFDDOSProtection = [[WAFDDOSProtection alloc]init] ;
```

### <a name="https_api_rest_sh_api_swc_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSWCAsyncWithKey") httpsApiRestShApiSWCAsyncWithKey

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function httpsApiRestShApiSWCAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                name:(NSString*) name
                origin:(NSString*) origin
                rule:(NSString*) rule
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetHttpsApiRestShApiSWC) onCompleted(key uid : uid name : name origin : origin rule : rule contentType : contentType)
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
    NSString* key = @"API";
    NSString* uid = @"UID";
    NSString* name = @"origin-name";
    NSString* origin = @"origin.yourdomain.tld";
    NSString* rule = @"header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does";
    NSString* contentType = @"application/json";

    [self.wAFDDOSProtection httpsApiRestShApiSWCAsyncWithKey: key uid : uid name : name origin : origin rule : rule contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSWCR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="https_api_rest_sh_api_sw_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSWAsyncWithKey") httpsApiRestShApiSWAsyncWithKey

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function httpsApiRestShApiSWAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                origin:(NSString*) origin
                cname:(NSString*) cname
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetHttpsApiRestShApiSW) onCompleted(key uid : uid origin : origin cname : cname contentType : contentType)
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
    NSString* key = @"API";
    NSString* uid = @"UID";
    NSString* origin = @"origin.yourdomain.tld";
    NSString* cname = @"yourdomain.tld,www.yourdomain.tld";
    NSString* contentType = @"application/json";

    [self.wAFDDOSProtection httpsApiRestShApiSWAsyncWithKey: key uid : uid origin : origin cname : cname contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSWR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="https_api_rest_sh_api_swc1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSWC1AsyncWithBody") httpsApiRestShApiSWC1AsyncWithBody

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function httpsApiRestShApiSWC1AsyncWithBody:(HttpsApiRestShApiSWC*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostHttpsApiRestShApiSWC1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiSWC* body = (HttpsApiRestShApiSWC*) [APIHelper jsonDeserialize: @"{
  \"key\": \"YOUR API KEY\",
  \"uid\": \"YOUR USER ID\",
  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",
  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",
  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"
}"
                toClass: HttpsApiRestShApiSWC.class];
    NSString* contentType = @"application/json";

    [self.wAFDDOSProtection httpsApiRestShApiSWC1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSWCR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="https_api_rest_sh_api_sw1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSW1AsyncWithBody") httpsApiRestShApiSW1AsyncWithBody

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function httpsApiRestShApiSW1AsyncWithBody:(HttpsApiRestShApiSW*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostHttpsApiRestShApiSW1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiSW* body = (HttpsApiRestShApiSW*) [APIHelper jsonDeserialize: @"{
  \"key\": \"YOUR API KEY\",
  \"uid\": \"YOUR USER ID\",
  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",
  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"
}"
                toClass: HttpsApiRestShApiSW.class];
    NSString* contentType = @"application/json";

    [self.wAFDDOSProtection httpsApiRestShApiSW1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSWR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption"></a>![Class: ](https://apidocs.io/img/class.png ".Encryption") Encryption

### Get singleton instance
```objc
Encryption* encryption = [[Encryption alloc]init] ;
```

### <a name="data_and_file_encryption_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.dataAndFileEncryptionAsyncWithKey") dataAndFileEncryptionAsyncWithKey

> Data and File Encryption API


```objc
function dataAndFileEncryptionAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                data:(NSString*) data
                method:(NSString*) method
                bit:(int) bit
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetDataAndFileEncryption) onCompleted(key uid : uid data : data method : method bit : bit contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* data = @"data";
    NSString* method = @"method";
    int bit = 24;
    NSString* contentType = @"Content-Type";

    [self.encryption dataAndFileEncryptionAsyncWithKey: key uid : uid data : data method : method bit : bit contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSER* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="data_and_file_encryption1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.dataAndFileEncryption1AsyncWithBody") dataAndFileEncryption1AsyncWithBody

> Data and File Encryption API


```objc
function dataAndFileEncryption1AsyncWithBody:(HttpsApiRestShApiSE*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostDataAndFileEncryption1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiSE* body = [[HttpsApiRestShApiSE alloc]init];
    NSString* contentType = @"Content-Type";

    [self.encryption dataAndFileEncryption1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSER* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn"></a>![Class: ](https://apidocs.io/img/class.png ".CDN") CDN

### Get singleton instance
```objc
CDN* cDN = [[CDN alloc]init] ;
```

### <a name="c_dn_push_zone_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPushZoneAsyncWithKey") cDNPushZoneAsyncWithKey

> CDN Push Zone API


```objc
function cDNPushZoneAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                cname:(NSString*) cname
                file:(NSString*) file
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetCDNPushZone) onCompleted(key uid : uid cname : cname file : file contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* cname = @"cname";
    NSString* file = @"file";
    NSString* contentType = @"Content-Type";

    [self.cDN cDNPushZoneAsyncWithKey: key uid : uid cname : cname file : file contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSCPushR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="c_dn_pull_zone_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPullZoneAsyncWithKey") cDNPullZoneAsyncWithKey

> CDN Pull Zone API


```objc
function cDNPullZoneAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                origin:(NSString*) origin
                cname:(NSString*) cname
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetCDNPullZone) onCompleted(key uid : uid origin : origin cname : cname contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* origin = @"origin";
    NSString* cname = @"cname";
    NSString* contentType = @"Content-Type";

    [self.cDN cDNPullZoneAsyncWithKey: key uid : uid origin : origin cname : cname contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSCPullR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="c_dn_push_zone1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPushZone1AsyncWithBody") cDNPushZone1AsyncWithBody

> CDN Push Zone API


```objc
function cDNPushZone1AsyncWithBody:(HttpsApiRestShApiSCPush*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostCDNPushZone1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiSCPush* body = [[HttpsApiRestShApiSCPush alloc]init];
    NSString* contentType = @"Content-Type";

    [self.cDN cDNPushZone1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSCPushR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="c_dn_pull_zone1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPullZone1AsyncWithBody") cDNPullZone1AsyncWithBody

> CDN Pull Zone API


```objc
function cDNPullZone1AsyncWithBody:(HttpsApiRestShApiSCPull*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostCDNPullZone1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiSCPull* body = [[HttpsApiRestShApiSCPull alloc]init];
    NSString* contentType = @"Content-Type";

    [self.cDN cDNPullZone1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSCPullR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns"></a>![Class: ](https://apidocs.io/img/class.png ".DNS") DNS

### Get singleton instance
```objc
DNS* dNS = [[DNS alloc]init] ;
```

### <a name="d_ns_configuration_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSConfigurationAsyncWithKey") dNSConfigurationAsyncWithKey

> DNS Configuration API


```objc
function dNSConfigurationAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                domain:(NSString*) domain
                records:(NSString*) records
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetDNSConfiguration) onCompleted(key uid : uid domain : domain records : records contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* domain = @"domain";
    NSString* records = @"records";
    NSString* contentType = @"Content-Type";

    [self.dNS dNSConfigurationAsyncWithKey: key uid : uid domain : domain records : records contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSDCR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="d_ns_configuration1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSConfiguration1AsyncWithBody") dNSConfiguration1AsyncWithBody

> DNS Configuration API


```objc
function dNSConfiguration1AsyncWithBody:(HttpsApiRestShApiSDC*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostDNSConfiguration1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiSDC* body = [[HttpsApiRestShApiSDC alloc]init];
    NSString* contentType = @"Content-Type";

    [self.dNS dNSConfiguration1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSDCR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="d_ns_creation_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSCreationAsyncWithKey") dNSCreationAsyncWithKey

> DNS Creation API


```objc
function dNSCreationAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                domain:(NSString*) domain
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetDNSCreation) onCompleted(key uid : uid domain : domain contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* domain = @"domain";
    NSString* contentType = @"Content-Type";

    [self.dNS dNSCreationAsyncWithKey: key uid : uid domain : domain contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSDAR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="d_ns_creation1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSCreation1AsyncWithBody") dNSCreation1AsyncWithBody

> DNS Creation API


```objc
function dNSCreation1AsyncWithBody:(HttpsApiRestShApiSDA*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostDNSCreation1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiSDA* body = [[HttpsApiRestShApiSDA alloc]init];
    NSString* contentType = @"Content-Type";

    [self.dNS dNSCreation1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSDAR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscation") CodeObfuscation

### Get singleton instance
```objc
CodeObfuscation* codeObfuscation = [[CodeObfuscation alloc]init] ;
```

### <a name="obfuscation_and_anti_tampering_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.obfuscationAndAntiTamperingAsyncWithKey") obfuscationAndAntiTamperingAsyncWithKey

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```objc
function obfuscationAndAntiTamperingAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                app:(NSString*) app
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetObfuscationAndAntiTampering) onCompleted(key uid : uid app : app contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* app = @"app";
    NSString* contentType = @"Content-Type";

    [self.codeObfuscation obfuscationAndAntiTamperingAsyncWithKey: key uid : uid app : app contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSOR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="obfuscation_and_anti_tampering1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.obfuscationAndAntiTampering1AsyncWithBody") obfuscationAndAntiTampering1AsyncWithBody

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```objc
function obfuscationAndAntiTampering1AsyncWithBody:(HttpsApiRestShApiSO*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostObfuscationAndAntiTampering1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiSO* body = [[HttpsApiRestShApiSO alloc]init];
    NSString* contentType = @"Content-Type";

    [self.codeObfuscation obfuscationAndAntiTampering1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSOR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting"></a>![Class: ](https://apidocs.io/img/class.png ".Hosting") Hosting

### Get singleton instance
```objc
Hosting* hosting = [[Hosting alloc]init] ;
```

### <a name="hosting_setup_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".Hosting.hostingSetupAsyncWithKey") hostingSetupAsyncWithKey

> Node.JS and Static Web APP Hosting


```objc
function hostingSetupAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                app:(NSString*) app
                domain:(NSString*) domain
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetHostingSetup) onCompleted(key uid : uid app : app domain : domain contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* app = @"app";
    NSString* domain = @"domain";
    NSString* contentType = @"Content-Type";

    [self.hosting hostingSetupAsyncWithKey: key uid : uid app : app domain : domain contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSHR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="hosting_setup1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".Hosting.hostingSetup1AsyncWithBody") hostingSetup1AsyncWithBody

> Node.JS and Static Web APP Hosting


```objc
function hostingSetup1AsyncWithBody:(HttpsApiRestShApiSH*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostHostingSetup1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiSH* body = [[HttpsApiRestShApiSH alloc]init];
    NSString* contentType = @"Content-Type";

    [self.hosting hostingSetup1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSHR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPI") DataManipulationConversionSortingAndCompressionAPI

### Get singleton instance
```objc
DataManipulationConversionSortingAndCompressionAPI* dataManipulationConversionSortingAndCompressionAPI = [[DataManipulationConversionSortingAndCompressionAPI alloc]init] ;
```

### <a name="https_api_rest_sh_api_d_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiDAsyncWithKey") httpsApiRestShApiDAsyncWithKey

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function httpsApiRestShApiDAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                user:(NSString*) user
                apiuid:(NSString*) apiuid
                data:(NSString*) data
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetHttpsApiRestShApiD) onCompleted(key uid : uid user : user apiuid : apiuid data : data contentType : contentType)
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
    NSString* key = @"API";
    NSString* uid = @"UID";
    NSString* user = @"UID";
    NSString* apiuid = @"apiUID";
    NSString* data = @"https://static.yourcdn.com/data.file";
    NSString* contentType = @"application/json";

    [self.dataManipulationConversionSortingAndCompressionAPI httpsApiRestShApiDAsyncWithKey: key uid : uid user : user apiuid : apiuid data : data contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiDR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="https_api_rest_sh_api_d1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiD1AsyncWithBody") httpsApiRestShApiD1AsyncWithBody

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```objc
function httpsApiRestShApiD1AsyncWithBody:(HttpsApiRestShApiD*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostHttpsApiRestShApiD1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiD* body = (HttpsApiRestShApiD*) [APIHelper jsonDeserialize: @"{
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
                toClass: HttpsApiRestShApiD.class];
    NSString* contentType = @"application/json";

    [self.dataManipulationConversionSortingAndCompressionAPI httpsApiRestShApiD1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiDR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPI") ImageManipulationAndModerationAPI

### Get singleton instance
```objc
ImageManipulationAndModerationAPI* imageManipulationAndModerationAPI = [[ImageManipulationAndModerationAPI alloc]init] ;
```

### <a name="image_manipulation_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPI.imageManipulationAsyncWithKey") imageManipulationAsyncWithKey

> Image Manipulation API


```objc
function imageManipulationAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                image:(NSString*) image
                transform:(NSString*) transform
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetImageManipulation) onCompleted(key uid : uid image : image transform : transform contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* image = @"image";
    NSString* transform = @"transform";
    NSString* contentType = @"Content-Type";

    [self.imageManipulationAndModerationAPI imageManipulationAsyncWithKey: key uid : uid image : image transform : transform contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiIR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="image_manipulation1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPI.imageManipulation1AsyncWithBody") imageManipulation1AsyncWithBody

> Image Manipulation API


```objc
function imageManipulation1AsyncWithBody:(HttpsApiRestShApiI*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostImageManipulation1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiI* body = [[HttpsApiRestShApiI alloc]init];
    NSString* contentType = @"Content-Type";

    [self.imageManipulationAndModerationAPI imageManipulation1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiIR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification"></a>![Class: ](https://apidocs.io/img/class.png ".Verification") Verification

### Get singleton instance
```objc
Verification* verification = [[Verification alloc]init] ;
```

### <a name="user_address_verification_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userAddressVerificationAsyncWithKey") userAddressVerificationAsyncWithKey

> User Address Verification API


```objc
function userAddressVerificationAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                user:(NSString*) user
                a:(NSString*) a
                sa:(NSString*) sa
                c:(NSString*) c
                s:(NSString*) s
                z:(int) z
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetUserAddressVerification) onCompleted(key uid : uid user : user a : a sa : sa c : c s : s z : z contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* user = @"user";
    NSString* a = @"a";
    NSString* sa = @"sa";
    NSString* c = @"c";
    NSString* s = @"s";
    int z = 237;
    NSString* contentType = @"Content-Type";

    [self.verification userAddressVerificationAsyncWithKey: key uid : uid user : user a : a sa : sa c : c s : s z : z contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVAR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="user_address_verification1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userAddressVerification1AsyncWithBody") userAddressVerification1AsyncWithBody

> User Address Verification API


```objc
function userAddressVerification1AsyncWithBody:(HttpsApiRestShApiVA*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostUserAddressVerification1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiVA* body = [[HttpsApiRestShApiVA alloc]init];
    NSString* contentType = @"Content-Type";

    [self.verification userAddressVerification1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVAR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="user_verification_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userVerificationAsyncWithKey") userVerificationAsyncWithKey

> User Verification API


```objc
function userVerificationAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                user:(NSString*) user
                code:(NSString*) code
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetUserVerification) onCompleted(key uid : uid user : user code : code contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* user = @"user";
    NSString* code = @"code";
    NSString* contentType = @"Content-Type";

    [self.verification userVerificationAsyncWithKey: key uid : uid user : user code : code contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVUR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="user_verification1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userVerification1AsyncWithBody") userVerification1AsyncWithBody

> User Verification API


```objc
function userVerification1AsyncWithBody:(HttpsApiRestShApiVU*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostUserVerification1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiVU* body = [[HttpsApiRestShApiVU alloc]init];
    NSString* contentType = @"Content-Type";

    [self.verification userVerification1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVUR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="cellphone_verification_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.cellphoneVerificationAsyncWithKey") cellphoneVerificationAsyncWithKey

> Verification API


```objc
function cellphoneVerificationAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                to:(NSString*) to
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetCellphoneVerification) onCompleted(key uid : uid to : to contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* to = @"to";
    NSString* contentType = @"Content-Type";

    [self.verification cellphoneVerificationAsyncWithKey: key uid : uid to : to contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="cellphone_verification1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.cellphoneVerification1AsyncWithBody") cellphoneVerification1AsyncWithBody

> Verification API


```objc
function cellphoneVerification1AsyncWithBody:(HttpsApiRestShApiV*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostCellphoneVerification1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiV* body = [[HttpsApiRestShApiV alloc]init];
    NSString* contentType = @"Content-Type";

    [self.verification cellphoneVerification1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPI") TwoFactorAuthenticationAPI

### Get singleton instance
```objc
TwoFactorAuthenticationAPI* twoFactorAuthenticationAPI = [[TwoFactorAuthenticationAPI alloc]init] ;
```

### <a name="m2_fa_token_response_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.m2FATokenResponseAsyncWithKey") m2FATokenResponseAsyncWithKey

> Two Factor Authentication Token Reply


```objc
function m2FATokenResponseAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                user:(NSString*) user
                code:(NSString*) code
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetM2FATokenResponse) onCompleted(key uid : uid user : user code : code contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* user = @"user";
    NSString* code = @"code";
    NSString* contentType = @"Content-Type";

    [self.twoFactorAuthenticationAPI m2FATokenResponseAsyncWithKey: key uid : uid user : user code : code contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faTR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="m2_fa_token_response1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.m2FATokenResponse1AsyncWithBody") m2FATokenResponse1AsyncWithBody

> Two Factor Authentication Token Reply


```objc
function m2FATokenResponse1AsyncWithBody:(HttpsApiRestShApi2faT*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostM2FATokenResponse1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApi2faT* body = [[HttpsApiRestShApi2faT alloc]init];
    NSString* contentType = @"Content-Type";

    [self.twoFactorAuthenticationAPI m2FATokenResponse1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faTR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="two_factor_authentication_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.twoFactorAuthenticationAsyncWithKey") twoFactorAuthenticationAsyncWithKey

> Two Factor Authentication API


```objc
function twoFactorAuthenticationAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                to:(NSString*) to
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetTwoFactorAuthentication) onCompleted(key uid : uid to : to contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* to = @"to";
    NSString* contentType = @"Content-Type";

    [self.twoFactorAuthenticationAPI twoFactorAuthenticationAsyncWithKey: key uid : uid to : to contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="two_factor_authentication1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.twoFactorAuthentication1AsyncWithBody") twoFactorAuthentication1AsyncWithBody

> Two Factor Authentication API


```objc
function twoFactorAuthentication1AsyncWithBody:(HttpsApiRestShApi2fa*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostTwoFactorAuthentication1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApi2fa* body = [[HttpsApiRestShApi2fa alloc]init];
    NSString* contentType = @"Content-Type";

    [self.twoFactorAuthenticationAPI twoFactorAuthentication1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagement") UserManagement

### Get singleton instance
```objc
UserManagement* userManagement = [[UserManagement alloc]init] ;
```

### <a name="get_user_info_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.getUserInfoAsyncWithKey") getUserInfoAsyncWithKey

> Get User Info API


```objc
function getUserInfoAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                user:(NSString*) user
                apiuid:(NSString*) apiuid
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetUserInfo) onCompleted(key uid : uid user : user apiuid : apiuid contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* user = @"user";
    NSString* apiuid = @"apiuid";
    NSString* contentType = @"Content-Type";

    [self.userManagement getUserInfoAsyncWithKey: key uid : uid user : user apiuid : apiuid contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUIR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_user_info1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.getUserInfo1AsyncWithBody") getUserInfo1AsyncWithBody

> Get User Info API


```objc
function getUserInfo1AsyncWithBody:(HttpsApiRestShApiUI*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostGetUserInfo1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiUI* body = [[HttpsApiRestShApiUI alloc]init];
    NSString* contentType = @"Content-Type";

    [self.userManagement getUserInfo1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUIR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="update_user_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.updateUserAsyncWithKey") updateUserAsyncWithKey

> Update User API


```objc
function updateUserAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                user:(NSString*) user
                apiuid:(NSString*) apiuid
                avatar:(NSString*) avatar
                customInput:(NSString*) customInput
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetUpdateUser) onCompleted(key uid : uid user : user apiuid : apiuid avatar : avatar customInput : customInput contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* user = @"user";
    NSString* apiuid = @"apiuid";
    NSString* avatar = @"avatar";
    NSString* customInput = @"custom input";
    NSString* contentType = @"Content-Type";

    [self.userManagement updateUserAsyncWithKey: key uid : uid user : user apiuid : apiuid avatar : avatar customInput : customInput contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUUR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="update_user1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.updateUser1AsyncWithBody") updateUser1AsyncWithBody

> Update User API


```objc
function updateUser1AsyncWithBody:(HttpsApiRestShApiUU*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostUpdateUser1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiUU* body = [[HttpsApiRestShApiUU alloc]init];
    NSString* contentType = @"Content-Type";

    [self.userManagement updateUser1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUUR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="delete_user_async_with_api"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.deleteUserAsyncWithApi") deleteUserAsyncWithApi

> Delete User API


```objc
function deleteUserAsyncWithApi:(NSString*) api
                uid:(NSString*) uid
                user:(NSString*) user
                apiuid:(NSString*) apiuid
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetDeleteUser) onCompleted(api uid : uid user : user apiuid : apiuid contentType : contentType)
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
    NSString* api = @"api";
    NSString* uid = @"uid";
    NSString* user = @"user";
    NSString* apiuid = @"apiuid";
    NSString* contentType = @"Content-Type";

    [self.userManagement deleteUserAsyncWithApi: api uid : uid user : user apiuid : apiuid contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUDR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="delete_user1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.deleteUser1AsyncWithBody") deleteUser1AsyncWithBody

> Delete User API


```objc
function deleteUser1AsyncWithBody:(HttpsApiRestShApiUD*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostDeleteUser1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiUD* body = [[HttpsApiRestShApiUD alloc]init];
    NSString* contentType = @"Content-Type";

    [self.userManagement deleteUser1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUDR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistration") LoginAndRegistration

### Get singleton instance
```objc
LoginAndRegistration* loginAndRegistration = [[LoginAndRegistration alloc]init] ;
```

### <a name="user_registration_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userRegistrationAsyncWithKey") userRegistrationAsyncWithKey

> User Registration API


```objc
function userRegistrationAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                user:(NSString*) user
                password:(NSString*) password
                name:(NSString*) name
                email:(NSString*) email
                phone:(int) phone
                countrycode:(int) countrycode
                address:(NSString*) address
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetUserRegistration) onCompleted(key uid : uid user : user password : password name : name email : email phone : phone countrycode : countrycode address : address contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* user = @"user";
    NSString* password = @"password";
    NSString* name = @"name";
    NSString* email = @"email";
    int phone = 237;
    int countrycode = 237;
    NSString* address = @"address";
    NSString* contentType = @"Content-Type";

    [self.loginAndRegistration userRegistrationAsyncWithKey: key uid : uid user : user password : password name : name email : email phone : phone countrycode : countrycode address : address contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAURR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="user_registration1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userRegistration1AsyncWithBody") userRegistration1AsyncWithBody

> User Registration API


```objc
function userRegistration1AsyncWithBody:(HttpsApiRestShApiAUR*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostUserRegistration1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiAUR* body = [[HttpsApiRestShApiAUR alloc]init];
    NSString* contentType = @"Content-Type";

    [self.loginAndRegistration userRegistration1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAURR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="user_authentication_async_with_key"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userAuthenticationAsyncWithKey") userAuthenticationAsyncWithKey

> User Authentication API


```objc
function userAuthenticationAsyncWithKey:(NSString*) key
                uid:(NSString*) uid
                user:(NSString*) user
                password:(NSString*) password
                contentType:(NSString*) contentType
                completionBlock:(CompletedGetUserAuthentication) onCompleted(key uid : uid user : user password : password contentType : contentType)
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
    NSString* key = @"key";
    NSString* uid = @"uid";
    NSString* user = @"user";
    NSString* password = @"password";
    NSString* contentType = @"Content-Type";

    [self.loginAndRegistration userAuthenticationAsyncWithKey: key uid : uid user : user password : password contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAULR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="user_authentication1_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userAuthentication1AsyncWithBody") userAuthentication1AsyncWithBody

> User Authentication API


```objc
function userAuthentication1AsyncWithBody:(HttpsApiRestShApiAUL*) body
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostUserAuthentication1) onCompleted(body contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    HttpsApiRestShApiAUL* body = [[HttpsApiRestShApiAUL alloc]init];
    NSString* contentType = @"Content-Type";

    [self.loginAndRegistration userAuthentication1AsyncWithBody: body contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAULR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)



