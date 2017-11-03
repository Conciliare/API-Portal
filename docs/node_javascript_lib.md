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

The generated SDK relies on [Node Package Manager](https://www.npmjs.com/) (NPM) being available to resolve dependencies. If you don't already have NPM installed, please go ahead and follow instructions to install NPM from [here](https://nodejs.org/en/download/).
The SDK also requires Node to be installed. If Node isn't already installed, please install it from [here](https://nodejs.org/en/download/)
> NPM is installed by default when Node is installed

To check if node and npm have been successfully installed, write the following commands in command prompt:

* `node --version`
* `npm -version`

![Version Check](https://apidocs.io/illustration/nodejs?step=versionCheck&workspaceFolder=SMASH-Node)

Now use npm to resolve all dependencies by running the following command in the root directory (of the SDK folder):

```bash
npm install
```

![Resolve Dependencies](https://apidocs.io/illustration/nodejs?step=resolveDependency1&workspaceFolder=SMASH-Node)

![Resolve Dependencies](https://apidocs.io/illustration/nodejs?step=resolveDependency2)

This will install all dependencies in the `node_modules` folder.

Once dependencies are resolved, you will need to move the folder `SMASH ` in to your `node_modules` folder.

## How to Use

The following section explains how to use the library in a new project.

### 1. Open Project Folder
Open an IDE/Text Editor for JavaScript like Sublime Text. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

Click on `File` and select `Open Folder`.

![Open Folder](https://apidocs.io/illustration/nodejs?step=openFolder)

Select the folder of your SDK and click on `Select Folder` to open it up in Sublime Text. The folder will become visible in the bar on the left.

![Open Project](https://apidocs.io/illustration/nodejs?step=openProject&workspaceFolder=SMASH-Node)

### 2. Creating a Test File

Now right click on the folder name and select the `New File` option to create a new test file. Save it as `index.js` Now import the generated NodeJS library using the following lines of code:

```js
var lib = require('lib');
```

Save changes.

![Create new file](https://apidocs.io/illustration/nodejs?step=createNewFile&workspaceFolder=SMASH-Node)

![Save new file](https://apidocs.io/illustration/nodejs?step=saveNewFile&workspaceFolder=SMASH-Node)

### 3. Running The Test File

To run the `index.js` file, open up the command prompt and navigate to the Path where the SDK folder resides. Type the following command to run the file:

```
node index.js
```

![Run file](https://apidocs.io/illustration/nodejs?step=runProject&workspaceFolder=SMASH-Node)


## How to Test

These tests use Mocha framework for testing, coupled with Chai for assertions. These dependencies need to be installed for tests to run.
Tests can be run in a number of ways:

### Method 1 (Run all tests)

1. Navigate to the root directory of the SDK folder from command prompt.
2. Type `mocha --recursive` to run all the tests.

### Method 2 (Run all tests)

1. Navigate to the `../test/Controllers/` directory from command prompt.
2. Type `mocha *` to run all the tests.

### Method 3 (Run specific controller's tests)

1. Navigate to the `../test/Controllers/` directory from command prompt.
2. Type `mocha  SMASH - APIController`  to run all the tests in that controller file.

> To increase mocha's default timeout, you can change the `TEST_TIMEOUT` parameter's value in `TestBootstrap.js`.

![Run Tests](https://apidocs.io/illustration/nodejs?step=runTests&controllerName=SMASH%20-%20APIController)

## Initialization

### Authentication
In order to setup authentication in the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| key | Your API Key |
| uid | Your User ID |



API client can be initialized as following:

```JavaScript
const lib = require('lib');

// Configuration parameters and credentials
lib.Configuration.key = "API"; // Your API Key
lib.Configuration.uid = "UID"; // Your User ID

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

The singleton instance of the ``` AdvancedLoggingController ``` class can be accessed from the API Client.

```javascript
var controller = lib.AdvancedLoggingController;
```

### <a name="get_https_api_rest_sh_api_security_logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSecurityLoggingInfo") getHttpsApiRestShApiSecurityLoggingInfo

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```javascript
function getHttpsApiRestShApiSecurityLoggingInfo(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['name'] = 'name';
        input['origin'] = 'origin';
        input['time'] = 'time';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiSecurityLoggingInfo(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_security_logging"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSecurityLogging") getHttpsApiRestShApiSecurityLogging

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```javascript
function getHttpsApiRestShApiSecurityLogging(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['name'] = 'name';
        input['origin'] = 'origin';
        input['activate'] = false;
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiSecurityLogging(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_security_logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSecurityLoggingInfo") createHttpsApiRestShApiSecurityLoggingInfo

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```javascript
function createHttpsApiRestShApiSecurityLoggingInfo(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSecurityLoggingInfoRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiSecurityLoggingInfo(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_security_logging"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSecurityLogging") createHttpsApiRestShApiSecurityLogging

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```javascript
function createHttpsApiRestShApiSecurityLogging(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSecurityLoggingRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiSecurityLogging(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection_controller"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtectionController") WAFDDOSProtectionController

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtectionController ``` class can be accessed from the API Client.

```javascript
var controller = lib.WAFDDOSProtectionController;
```

### <a name="get_https_api_rest_sh_api_security_waf_configure"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSecurityWafConfigure") getHttpsApiRestShApiSecurityWafConfigure

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function getHttpsApiRestShApiSecurityWafConfigure(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'API';
        input['uid'] = 'UID';
        input['name'] = 'origin-name';
        input['origin'] = 'origin.yourdomain.tld';
        input['rule'] = 'header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does';
        input['contentType'] = 'application/json';

    controller.getHttpsApiRestShApiSecurityWafConfigure(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_security_waf"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSecurityWaf") getHttpsApiRestShApiSecurityWaf

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function getHttpsApiRestShApiSecurityWaf(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'API';
        input['uid'] = 'UID';
        input['origin'] = 'origin.yourdomain.tld';
        input['cname'] = 'yourdomain.tld,www.yourdomain.tld';
        input['contentType'] = 'application/json';

    controller.getHttpsApiRestShApiSecurityWaf(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_security_waf_configure"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSecurityWafConfigure") createHttpsApiRestShApiSecurityWafConfigure

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function createHttpsApiRestShApiSecurityWafConfigure(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSecurityWafConfigureRequestModel({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "name": "WHAT YOU WISH TO NAME YOUR WAF",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
});
        input['contentType'] = 'application/json';

    controller.createHttpsApiRestShApiSecurityWafConfigure(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_security_waf"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSecurityWaf") createHttpsApiRestShApiSecurityWaf

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function createHttpsApiRestShApiSecurityWaf(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSecurityWafRequestModel({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
});
        input['contentType'] = 'application/json';

    controller.createHttpsApiRestShApiSecurityWaf(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="encryption_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EncryptionController") EncryptionController

### Get singleton instance

The singleton instance of the ``` EncryptionController ``` class can be accessed from the API Client.

```javascript
var controller = lib.EncryptionController;
```

### <a name="get_https_api_rest_sh_api_security_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.getHttpsApiRestShApiSecurityEncryption") getHttpsApiRestShApiSecurityEncryption

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```javascript
function getHttpsApiRestShApiSecurityEncryption(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['data'] = 'data';
        input['method'] = 'method';
        input['bit'] = 93;
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiSecurityEncryption(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_security_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.createHttpsApiRestShApiSecurityEncryption") createHttpsApiRestShApiSecurityEncryption

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```javascript
function createHttpsApiRestShApiSecurityEncryption(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSecurityEncryptionRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiSecurityEncryption(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="cdn_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CDNController") CDNController

### Get singleton instance

The singleton instance of the ``` CDNController ``` class can be accessed from the API Client.

```javascript
var controller = lib.CDNController;
```

### <a name="get_https_api_rest_sh_api_service_cdn_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiServiceCdnPush") getHttpsApiRestShApiServiceCdnPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```javascript
function getHttpsApiRestShApiServiceCdnPush(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['cname'] = 'cname';
        input['file'] = 'file';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiServiceCdnPush(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_service_cdn_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiServiceCdnPull") getHttpsApiRestShApiServiceCdnPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```javascript
function getHttpsApiRestShApiServiceCdnPull(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['origin'] = 'origin';
        input['cname'] = 'cname';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiServiceCdnPull(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_service_cdn_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiServiceCdnPush") createHttpsApiRestShApiServiceCdnPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```javascript
function createHttpsApiRestShApiServiceCdnPush(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiServiceCdnPushRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiServiceCdnPush(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_service_cdn_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiServiceCdnPull") createHttpsApiRestShApiServiceCdnPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```javascript
function createHttpsApiRestShApiServiceCdnPull(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiServiceCdnPullRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiServiceCdnPull(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="dns_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DNSController") DNSController

### Get singleton instance

The singleton instance of the ``` DNSController ``` class can be accessed from the API Client.

```javascript
var controller = lib.DNSController;
```

### <a name="get_https_api_rest_sh_api_service_dns_configure"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiServiceDnsConfigure") getHttpsApiRestShApiServiceDnsConfigure

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```javascript
function getHttpsApiRestShApiServiceDnsConfigure(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['domain'] = 'domain';
        input['records'] = 'records';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiServiceDnsConfigure(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_service_dns_configure"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiServiceDnsConfigure") createHttpsApiRestShApiServiceDnsConfigure

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```javascript
function createHttpsApiRestShApiServiceDnsConfigure(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiServiceDnsConfigureRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiServiceDnsConfigure(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_service_dns_add"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiServiceDnsAdd") getHttpsApiRestShApiServiceDnsAdd

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```javascript
function getHttpsApiRestShApiServiceDnsAdd(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| domain |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['domain'] = 'domain';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiServiceDnsAdd(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_service_dns_add"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiServiceDnsAdd") createHttpsApiRestShApiServiceDnsAdd

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```javascript
function createHttpsApiRestShApiServiceDnsAdd(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiServiceDnsAddRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiServiceDnsAdd(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscationController") CodeObfuscationController

### Get singleton instance

The singleton instance of the ``` CodeObfuscationController ``` class can be accessed from the API Client.

```javascript
var controller = lib.CodeObfuscationController;
```

### <a name="get_https_api_rest_sh_api_service_obfuscation"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.getHttpsApiRestShApiServiceObfuscation") getHttpsApiRestShApiServiceObfuscation

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```javascript
function getHttpsApiRestShApiServiceObfuscation(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| app |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['app'] = 'app';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiServiceObfuscation(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_service_obfuscation"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.createHttpsApiRestShApiServiceObfuscation") createHttpsApiRestShApiServiceObfuscation

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```javascript
function createHttpsApiRestShApiServiceObfuscation(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiServiceObfuscationRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiServiceObfuscation(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="hosting_controller"></a>![Class: ](https://apidocs.io/img/class.png ".HostingController") HostingController

### Get singleton instance

The singleton instance of the ``` HostingController ``` class can be accessed from the API Client.

```javascript
var controller = lib.HostingController;
```

### <a name="get_https_api_rest_sh_api_service_hosting"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.getHttpsApiRestShApiServiceHosting") getHttpsApiRestShApiServiceHosting

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```javascript
function getHttpsApiRestShApiServiceHosting(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['app'] = 'app';
        input['domain'] = 'domain';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiServiceHosting(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_service_hosting"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.createHttpsApiRestShApiServiceHosting") createHttpsApiRestShApiServiceHosting

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```javascript
function createHttpsApiRestShApiServiceHosting(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiServiceHostingRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiServiceHosting(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPIController") DataManipulationConversionSortingAndCompressionAPIController

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPIController ``` class can be accessed from the API Client.

```javascript
var controller = lib.DataManipulationConversionSortingAndCompressionAPIController;
```

### <a name="get_https_api_rest_sh_api_data"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.getHttpsApiRestShApiData") getHttpsApiRestShApiData

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function getHttpsApiRestShApiData(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'API';
        input['uid'] = 'UID';
        input['user'] = 'UID';
        input['apiuid'] = 'apiUID';
        input['data'] = 'https://static.yourcdn.com/data.file';
        input['contentType'] = 'application/json';

    controller.getHttpsApiRestShApiData(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_data"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.createHttpsApiRestShApiData") createHttpsApiRestShApiData

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function createHttpsApiRestShApiData(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiDataRequestModel({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "apiuid": "USERS API SIDE USER ID",
  "url": "DATA URL OR DIRECT FILE UPLOAD FROM CLIENT",
  "manipulation": "DATA MANIPULATION DIRECTIVES",
  "conversion": "CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)",
  "sorting": "SORT BY (NAME, DATE, TYPE, SIZE)",
  "compression": "COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)"
});
        input['contentType'] = 'application/json';

    controller.createHttpsApiRestShApiData(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPIController") ImageManipulationAndModerationAPIController

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPIController ``` class can be accessed from the API Client.

```javascript
var controller = lib.ImageManipulationAndModerationAPIController;
```

### <a name="get_https_api_rest_sh_api_image"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.getHttpsApiRestShApiImage") getHttpsApiRestShApiImage

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```javascript
function getHttpsApiRestShApiImage(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['image'] = 'image';
        input['transform'] = 'transform';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiImage(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_image"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.createHttpsApiRestShApiImage") createHttpsApiRestShApiImage

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```javascript
function createHttpsApiRestShApiImage(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiImageRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiImage(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="verification_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VerificationController") VerificationController

### Get singleton instance

The singleton instance of the ``` VerificationController ``` class can be accessed from the API Client.

```javascript
var controller = lib.VerificationController;
```

### <a name="get_https_api_rest_sh_api_verify_address"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVerifyAddress") getHttpsApiRestShApiVerifyAddress

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```javascript
function getHttpsApiRestShApiVerifyAddress(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['a'] = 'a';
        input['sa'] = 'sa';
        input['c'] = 'c';
        input['s'] = 's';
        input['z'] = 93;
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiVerifyAddress(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_verify_address"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVerifyAddress") createHttpsApiRestShApiVerifyAddress

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```javascript
function createHttpsApiRestShApiVerifyAddress(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiVerifyAddressRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiVerifyAddress(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_verify_user"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVerifyUser") getHttpsApiRestShApiVerifyUser

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```javascript
function getHttpsApiRestShApiVerifyUser(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['code'] = 'code';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiVerifyUser(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_verify_user"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVerifyUser") createHttpsApiRestShApiVerifyUser

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```javascript
function createHttpsApiRestShApiVerifyUser(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiVerifyUserRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiVerifyUser(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_verify"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVerify") getHttpsApiRestShApiVerify

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```javascript
function getHttpsApiRestShApiVerify(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['to'] = 'to';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiVerify(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_verify"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVerify") createHttpsApiRestShApiVerify

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```javascript
function createHttpsApiRestShApiVerify(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiVerifyRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiVerify(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPIController") TwoFactorAuthenticationAPIController

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPIController ``` class can be accessed from the API Client.

```javascript
var controller = lib.TwoFactorAuthenticationAPIController;
```

### <a name="get_https_api_rest_sh_api2fa_token"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2faToken") getHttpsApiRestShApi2faToken

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```javascript
function getHttpsApiRestShApi2faToken(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['code'] = 'code';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApi2faToken(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api2fa_token"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2faToken") createHttpsApiRestShApi2faToken

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```javascript
function createHttpsApiRestShApi2faToken(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApi2faTokenRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApi2faToken(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2fa") getHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```javascript
function getHttpsApiRestShApi2fa(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['to'] = 'to';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApi2fa(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2fa") createHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```javascript
function createHttpsApiRestShApi2fa(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApi2faRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApi2fa(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="user_management_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagementController") UserManagementController

### Get singleton instance

The singleton instance of the ``` UserManagementController ``` class can be accessed from the API Client.

```javascript
var controller = lib.UserManagementController;
```

### <a name="get_https_api_rest_sh_api_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUserInfo") getHttpsApiRestShApiUserInfo

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```javascript
function getHttpsApiRestShApiUserInfo(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['apiuid'] = 'apiuid';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiUserInfo(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUserInfo") createHttpsApiRestShApiUserInfo

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```javascript
function createHttpsApiRestShApiUserInfo(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiUserInfoRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiUserInfo(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_user_update"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUserUpdate") getHttpsApiRestShApiUserUpdate

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```javascript
function getHttpsApiRestShApiUserUpdate(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['apiuid'] = 'apiuid';
        input['avatar'] = 'avatar';
        input['customInput'] = custom input;
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiUserUpdate(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_user_update"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUserUpdate") createHttpsApiRestShApiUserUpdate

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```javascript
function createHttpsApiRestShApiUserUpdate(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiUserUpdateRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiUserUpdate(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_user_delete"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUserDelete") getHttpsApiRestShApiUserDelete

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```javascript
function getHttpsApiRestShApiUserDelete(input, callback)
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

```javascript

    var input = [];
        input['api'] = 'api';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['apiuid'] = 'apiuid';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiUserDelete(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_user_delete"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUserDelete") createHttpsApiRestShApiUserDelete

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```javascript
function createHttpsApiRestShApiUserDelete(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiUserDeleteRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiUserDelete(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration_controller"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistrationController") LoginAndRegistrationController

### Get singleton instance

The singleton instance of the ``` LoginAndRegistrationController ``` class can be accessed from the API Client.

```javascript
var controller = lib.LoginAndRegistrationController;
```

### <a name="get_https_api_rest_sh_api_auth_user_register"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAuthUserRegister") getHttpsApiRestShApiAuthUserRegister

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```javascript
function getHttpsApiRestShApiAuthUserRegister(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['password'] = 'password';
        input['name'] = 'name';
        input['email'] = 'email';
        input['phone'] = 51;
        input['countrycode'] = 51;
        input['address'] = 'address';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiAuthUserRegister(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_auth_user_register"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAuthUserRegister") createHttpsApiRestShApiAuthUserRegister

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```javascript
function createHttpsApiRestShApiAuthUserRegister(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiAuthUserRegisterRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiAuthUserRegister(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_auth_user_login"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAuthUserLogin") getHttpsApiRestShApiAuthUserLogin

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```javascript
function getHttpsApiRestShApiAuthUserLogin(input, callback)
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

```javascript

    var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['password'] = 'password';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiAuthUserLogin(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_auth_user_login"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAuthUserLogin") createHttpsApiRestShApiAuthUserLogin

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```javascript
function createHttpsApiRestShApiAuthUserLogin(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiAuthUserLoginRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiAuthUserLogin(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)



