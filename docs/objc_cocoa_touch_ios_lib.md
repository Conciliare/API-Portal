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
| uid | Your user ID |
| secret | Your Private API Key |
| key | Your Public API Key |



Configuration variables can be set as following.
```Objc
// Configuration parameters and credentials
Configuration_Uid = "UID"; // Your user ID
Configuration_Secret = "SECRET"; // Your Private API Key
Configuration_Key = "KEY"; // Your Public API Key

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

### <a name="logging_info_async_with_name"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingInfoAsyncWithName") loggingInfoAsyncWithName

> WAF Log Info


```objc
function loggingInfoAsyncWithName:(NSString*) name
                origin:(NSString*) origin
                time:(NSString*) time
                completionBlock:(CompletedGetLoggingInfo) onCompleted(name origin : origin time : time)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| name |  ``` Required ```  | Name of your WAF zone |
| origin |  ``` Required ```  | IP Address of the Web Application |
| time |  ``` Optional ```  | Specific times or dates to lookup separated by a comma in MMDDYYHHMMSS Format ( Month Month Day Day Year Year Year Hour Hour Minute Minute Second Second [01012017120059]) |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* name = @"name";
    NSString* origin = @"origin";
    NSString* time = @"time";

    [self.advancedLogging loggingInfoAsyncWithName: name origin : origin time : time  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSLIR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="logging_configuration_async_with_name"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingConfigurationAsyncWithName") loggingConfigurationAsyncWithName

> WAF Log Configuration


```objc
function loggingConfigurationAsyncWithName:(NSString*) name
                origin:(NSString*) origin
                activate:(NSString*) activate
                completionBlock:(CompletedGetLoggingConfiguration) onCompleted(name origin : origin activate : activate)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| name |  ``` Required ```  | Name of the WAF zone |
| origin |  ``` Required ```  | IP Address of the Web Application you wish to configure logging on |
| activate |  ``` Required ```  | True or False |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* name = @"name";
    NSString* origin = @"origin";
    NSString* activate = @"activate";

    [self.advancedLogging loggingConfigurationAsyncWithName: name origin : origin activate : activate  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSLR* response, NSError* error) { 
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

### <a name="data_and_file_encryption_async_with_data"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.dataAndFileEncryptionAsyncWithData") dataAndFileEncryptionAsyncWithData

> Data and File Encryption API


```objc
function dataAndFileEncryptionAsyncWithData:(NSString*) data
                method:(NSString*) method
                bit:(int) bit
                completionBlock:(CompletedGetDataAndFileEncryption) onCompleted(data method : method bit : bit)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Required ```  | GIT URL, file URL, direct upload of file, or data as a query string |
| method |  ``` Required ```  | Single or multiple encryption types to apply to data or files separated by a comma (DES, RSA, BLOWFISH, TWOFISH, AES, IDEA, PGP) |
| bit |  ``` Required ```  | Encryption key size (4096) |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* data = @"data";
    NSString* method = @"method";
    int bit = 135;

    [self.encryption dataAndFileEncryptionAsyncWithData: data method : method bit : bit  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSER* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn"></a>![Class: ](https://apidocs.io/img/class.png ".CDN") CDN

### Get singleton instance
```objc
CDN* cDN = [[CDN alloc]init] ;
```

### <a name="c_dn_push_zone_async_with_cname"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPushZoneAsyncWithCname") cDNPushZoneAsyncWithCname

> CDN Push Zone API


```objc
function cDNPushZoneAsyncWithCname:(NSString*) cname
                file:(NSString*) file
                completionBlock:(CompletedGetCDNPushZone) onCompleted(cname file : file)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| cname |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access |
| file |  ``` Required ```  | GIT URL, file URL, or direct upload of file |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* cname = @"cname";
    NSString* file = @"file";

    [self.cDN cDNPushZoneAsyncWithCname: cname file : file  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSCPushR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="c_dn_pull_zone_async_with_origin"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPullZoneAsyncWithOrigin") cDNPullZoneAsyncWithOrigin

> CDN Pull Zone API


```objc
function cDNPullZoneAsyncWithOrigin:(NSString*) origin
                cname:(NSString*) cname
                completionBlock:(CompletedGetCDNPullZone) onCompleted(origin cname : cname)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| origin |  ``` Required ```  | Domain or domain names separated by a comma |
| cname |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* origin = @"origin";
    NSString* cname = @"cname";

    [self.cDN cDNPullZoneAsyncWithOrigin: origin cname : cname  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSCPullR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns"></a>![Class: ](https://apidocs.io/img/class.png ".DNS") DNS

### Get singleton instance
```objc
DNS* dNS = [[DNS alloc]init] ;
```

### <a name="d_ns_configuration_async_with_domain"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSConfigurationAsyncWithDomain") dNSConfigurationAsyncWithDomain

> DNS Configuration API


```objc
function dNSConfigurationAsyncWithDomain:(NSString*) domain
                records:(NSString*) records
                completionBlock:(CompletedGetDNSConfiguration) onCompleted(domain records : records)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| domain |  ``` Required ```  | Domain or domain names separated by a comma |
| records |  ``` Required ```  | Records to append to domain separated by a comma (a;www.mydomain.com;127.0.0.0,cname;mydomain.com;otherdomain.com) |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* domain = @"domain";
    NSString* records = @"records";

    [self.dNS dNSConfigurationAsyncWithDomain: domain records : records  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSDCR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="d_ns_creation_async_with_domain"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSCreationAsyncWithDomain") dNSCreationAsyncWithDomain

> DNS Creation API


```objc
function dNSCreationAsyncWithDomain:(NSString*) domain
                completionBlock:(CompletedGetDNSCreation) onCompleted(domain)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| domain |  ``` Required ```  | Domain or domain names separated by a comma |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* domain = @"domain";

    [self.dNS dNSCreationAsyncWithDomain: domain  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSDAR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscation") CodeObfuscation

### Get singleton instance
```objc
CodeObfuscation* codeObfuscation = [[CodeObfuscation alloc]init] ;
```

### <a name="obfuscation_and_anti_tampering_async_with_app"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.obfuscationAndAntiTamperingAsyncWithApp") obfuscationAndAntiTamperingAsyncWithApp

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```objc
function obfuscationAndAntiTamperingAsyncWithApp:(NSString*) app
                completionBlock:(CompletedGetObfuscationAndAntiTampering) onCompleted(app)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| app |  ``` Required ```  | GIT URL or ZIP package containing your APP |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* app = @"app";

    [self.codeObfuscation obfuscationAndAntiTamperingAsyncWithApp: app  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSOR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting"></a>![Class: ](https://apidocs.io/img/class.png ".Hosting") Hosting

### Get singleton instance
```objc
Hosting* hosting = [[Hosting alloc]init] ;
```

### <a name="hosting_setup_async_with_app"></a>![Method: ](https://apidocs.io/img/method.png ".Hosting.hostingSetupAsyncWithApp") hostingSetupAsyncWithApp

> Node.JS and Static Web APP Hosting


```objc
function hostingSetupAsyncWithApp:(NSString*) app
                domain:(NSString*) domain
                completionBlock:(CompletedGetHostingSetup) onCompleted(app domain : domain)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| app |  ``` Required ```  | GIT URL or ZIP package containing your APP |
| domain |  ``` Required ```  | Domain or domain names separated by a comma |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* app = @"app";
    NSString* domain = @"domain";

    [self.hosting hostingSetupAsyncWithApp: app domain : domain  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiSHR* response, NSError* error) { 
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

### <a name="image_manipulation_async_with_image"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPI.imageManipulationAsyncWithImage") imageManipulationAsyncWithImage

> Image Manipulation API


```objc
function imageManipulationAsyncWithImage:(NSString*) image
                transform:(NSString*) transform
                completionBlock:(CompletedGetImageManipulation) onCompleted(image transform : transform)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| image |  ``` Required ```  | Image URL or direct upload |
| transform |  ``` Required ```  | Transformations to perform |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* image = @"image";
    NSString* transform = @"transform";

    [self.imageManipulationAndModerationAPI imageManipulationAsyncWithImage: image transform : transform  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiIR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification"></a>![Class: ](https://apidocs.io/img/class.png ".Verification") Verification

### Get singleton instance
```objc
Verification* verification = [[Verification alloc]init] ;
```

### <a name="user_address_verification_async_with_user"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userAddressVerificationAsyncWithUser") userAddressVerificationAsyncWithUser

> User Address Verification API


```objc
function userAddressVerificationAsyncWithUser:(NSString*) user
                a:(NSString*) a
                sa:(NSString*) sa
                c:(NSString*) c
                s:(NSString*) s
                z:(int) z
                address:(NSString*) address
                completionBlock:(CompletedGetUserAddressVerification) onCompleted(user a : a sa : sa c : c s : s z : z address : address)
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

```objc
    // Parameters for the API call
    NSString* user = @"user";
    NSString* a = @"a";
    NSString* sa = @"sa";
    NSString* c = @"c";
    NSString* s = @"s";
    int z = 135;
    NSString* address = @"address";

    [self.verification userAddressVerificationAsyncWithUser: user a : a sa : sa c : c s : s z : z address : address  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVAR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="user_verification_response_async_with_user"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userVerificationResponseAsyncWithUser") userVerificationResponseAsyncWithUser

> Users Verification Response API


```objc
function userVerificationResponseAsyncWithUser:(NSString*) user
                code:(NSString*) code
                completionBlock:(CompletedGetUserVerificationResponse) onCompleted(user code : code)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |
| code |  ``` Required ```  | Verification code entered by the user |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* user = @"user";
    NSString* code = @"code";

    [self.verification userVerificationResponseAsyncWithUser: user code : code  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVUR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="user_verification_async_with_user"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userVerificationAsyncWithUser") userVerificationAsyncWithUser

> User Verification API


```objc
function userVerificationAsyncWithUser:(NSString*) user
                completionBlock:(CompletedGetUserVerification) onCompleted(user)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* user = @"user";

    [self.verification userVerificationAsyncWithUser: user  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiVR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPI") TwoFactorAuthenticationAPI

### Get singleton instance
```objc
TwoFactorAuthenticationAPI* twoFactorAuthenticationAPI = [[TwoFactorAuthenticationAPI alloc]init] ;
```

### <a name="m2_fa_token_response_async_with_user"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.m2FATokenResponseAsyncWithUser") m2FATokenResponseAsyncWithUser

> Two Factor Authentication Token Reply


```objc
function m2FATokenResponseAsyncWithUser:(NSString*) user
                code:(NSString*) code
                completionBlock:(CompletedGetM2FATokenResponse) onCompleted(user code : code)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username or Email |
| code |  ``` Required ```  | Response From User Containing 2FA Code |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* user = @"user";
    NSString* code = @"code";

    [self.twoFactorAuthenticationAPI m2FATokenResponseAsyncWithUser: user code : code  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faTR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="two_factor_authentication_async_with_to"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.twoFactorAuthenticationAsyncWithTo") twoFactorAuthenticationAsyncWithTo

> Two Factor Authentication API


```objc
function twoFactorAuthenticationAsyncWithTo:(NSString*) to
                completionBlock:(CompletedGetTwoFactorAuthentication) onCompleted(to)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| to |  ``` Required ```  | Users UID, Username, Email, Or Cellphone number |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* to = @"to";

    [self.twoFactorAuthenticationAPI twoFactorAuthenticationAsyncWithTo: to  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApi2faR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagement") UserManagement

### Get singleton instance
```objc
UserManagement* userManagement = [[UserManagement alloc]init] ;
```

### <a name="get_user_info_async_with_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.getUserInfoAsyncWithUser") getUserInfoAsyncWithUser

> Get User Info API


```objc
function getUserInfoAsyncWithUser:(NSString*) user
                completionBlock:(CompletedGetUserInfo) onCompleted(user)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users User ID |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* user = @"user";

    [self.userManagement getUserInfoAsyncWithUser: user  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUIR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="update_user_async_with_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.updateUserAsyncWithUser") updateUserAsyncWithUser

> Update User API


```objc
function updateUserAsyncWithUser:(NSString*) user
                avatar:(NSString*) avatar
                customInput:(NSString*) customInput
                queryParameters:(NSDictionary*) queryParameters
                completionBlock:(CompletedGetUpdateUser) onCompleted(user avatar : avatar customInput : customInput  queryParameters : queryParams)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |
| avatar |  ``` Required ```  | Avatar Image URL |
| customInput |  ``` Required ```  | Custom input variable for users profile |
| queryParameters | ``` Optional ``` | Additional optional query parameters are supported by this method |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* user = @"user";
    NSString* avatar = @"avatar";
    NSString* customInput = @"custom input";
    // Dictionary for optional query parameters
    NSMutableDictionary* queryParamsMutable = [[NSMutableDictionary alloc] init];
    NSDictionary *queryParams= [queryParamsMutable copy];

    [self.userManagement updateUserAsyncWithUser: user avatar : avatar customInput : customInput  queryParameters : queryParams  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUUR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="delete_user_async_with_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.deleteUserAsyncWithUser") deleteUserAsyncWithUser

> Delete User API


```objc
function deleteUserAsyncWithUser:(NSString*) user
                completionBlock:(CompletedGetDeleteUser) onCompleted(user)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, or Email |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* user = @"user";

    [self.userManagement deleteUserAsyncWithUser: user  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiUDR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistration") LoginAndRegistration

### Get singleton instance
```objc
LoginAndRegistration* loginAndRegistration = [[LoginAndRegistration alloc]init] ;
```

### <a name="user_registration_async_with_email"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userRegistrationAsyncWithEmail") userRegistrationAsyncWithEmail

> User Registration API


```objc
function userRegistrationAsyncWithEmail:(NSString*) email
                user:(NSString*) user
                password:(NSString*) password
                name:(NSString*) name
                phone:(NSNumber*) phone
                countrycode:(NSNumber*) countrycode
                address:(NSString*) address
                queryParameters:(NSDictionary*) queryParameters
                completionBlock:(CompletedGetUserRegistration) onCompleted(email user : user password : password name : name phone : phone countrycode : countrycode address : address  queryParameters : queryParams)
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

```objc
    // Parameters for the API call
    NSString* email = @"email";
    NSString* user = @"user";
    NSString* password = @"password";
    NSString* name = @"name";
    NSNumber* phone = 135;
    NSNumber* countrycode = 135;
    NSString* address = @"address";
    // Dictionary for optional query parameters
    NSMutableDictionary* queryParamsMutable = [[NSMutableDictionary alloc] init];
    NSDictionary *queryParams= [queryParamsMutable copy];

    [self.loginAndRegistration userRegistrationAsyncWithEmail: email user : user password : password name : name phone : phone countrycode : countrycode address : address  queryParameters : queryParams  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAURR* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="user_authentication_async_with_user"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userAuthenticationAsyncWithUser") userAuthenticationAsyncWithUser

> User Authentication API


```objc
function userAuthenticationAsyncWithUser:(NSString*) user
                password:(NSString*) password
                completionBlock:(CompletedGetUserAuthentication) onCompleted(user password : password)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users Username or Email |
| password |  ``` Required ```  | Users Password |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* user = @"user";
    NSString* password = @"password";

    [self.loginAndRegistration userAuthenticationAsyncWithUser: user password : password  completionBlock:^(BOOL success, HttpContext* context, HttpsApiRestShApiAULR* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)



