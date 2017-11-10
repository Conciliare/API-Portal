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

### <a name="get_https_api_rest_sh_api_sli"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSLI") getHttpsApiRestShApiSLI

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```javascript
function getHttpsApiRestShApiSLI(input, callback)
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

    controller.getHttpsApiRestShApiSLI(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_sl"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSL") getHttpsApiRestShApiSL

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```javascript
function getHttpsApiRestShApiSL(input, callback)
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

    controller.getHttpsApiRestShApiSL(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_sli"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSLI") createHttpsApiRestShApiSLI

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```javascript
function createHttpsApiRestShApiSLI(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSLIModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiSLI(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_sl"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSL") createHttpsApiRestShApiSL

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```javascript
function createHttpsApiRestShApiSL(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSLModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiSL(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection_controller"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtectionController") WAFDDOSProtectionController

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtectionController ``` class can be accessed from the API Client.

```javascript
var controller = lib.WAFDDOSProtectionController;
```

### <a name="get_https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSWC") getHttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function getHttpsApiRestShApiSWC(input, callback)
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

    controller.getHttpsApiRestShApiSWC(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSW") getHttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function getHttpsApiRestShApiSW(input, callback)
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

    controller.getHttpsApiRestShApiSW(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSWC") createHttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function createHttpsApiRestShApiSWC(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSWCModel({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "name": "WHAT YOU WISH TO NAME YOUR WAF",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
});
        input['contentType'] = 'application/json';

    controller.createHttpsApiRestShApiSWC(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSW") createHttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function createHttpsApiRestShApiSW(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSWModel({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
});
        input['contentType'] = 'application/json';

    controller.createHttpsApiRestShApiSW(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="encryption_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EncryptionController") EncryptionController

### Get singleton instance

The singleton instance of the ``` EncryptionController ``` class can be accessed from the API Client.

```javascript
var controller = lib.EncryptionController;
```

### <a name="get_https_api_rest_sh_api_se"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.getHttpsApiRestShApiSE") getHttpsApiRestShApiSE

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```javascript
function getHttpsApiRestShApiSE(input, callback)
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
        input['bit'] = 6;
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiSE(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_se"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.createHttpsApiRestShApiSE") createHttpsApiRestShApiSE

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```javascript
function createHttpsApiRestShApiSE(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSEModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiSE(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="cdn_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CDNController") CDNController

### Get singleton instance

The singleton instance of the ``` CDNController ``` class can be accessed from the API Client.

```javascript
var controller = lib.CDNController;
```

### <a name="get_https_api_rest_sh_api_sc_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiSCPush") getHttpsApiRestShApiSCPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```javascript
function getHttpsApiRestShApiSCPush(input, callback)
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

    controller.getHttpsApiRestShApiSCPush(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_sc_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiSCPull") getHttpsApiRestShApiSCPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```javascript
function getHttpsApiRestShApiSCPull(input, callback)
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

    controller.getHttpsApiRestShApiSCPull(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_sc_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiSCPush") createHttpsApiRestShApiSCPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```javascript
function createHttpsApiRestShApiSCPush(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSCPushModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiSCPush(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_sc_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiSCPull") createHttpsApiRestShApiSCPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```javascript
function createHttpsApiRestShApiSCPull(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSCPullModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiSCPull(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="dns_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DNSController") DNSController

### Get singleton instance

The singleton instance of the ``` DNSController ``` class can be accessed from the API Client.

```javascript
var controller = lib.DNSController;
```

### <a name="get_https_api_rest_sh_api_sdc"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiSDC") getHttpsApiRestShApiSDC

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```javascript
function getHttpsApiRestShApiSDC(input, callback)
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

    controller.getHttpsApiRestShApiSDC(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_sdc"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiSDC") createHttpsApiRestShApiSDC

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```javascript
function createHttpsApiRestShApiSDC(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSDCModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiSDC(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_sda"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiSDA") getHttpsApiRestShApiSDA

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```javascript
function getHttpsApiRestShApiSDA(input, callback)
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

    controller.getHttpsApiRestShApiSDA(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_sda"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiSDA") createHttpsApiRestShApiSDA

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```javascript
function createHttpsApiRestShApiSDA(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSDAModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiSDA(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscationController") CodeObfuscationController

### Get singleton instance

The singleton instance of the ``` CodeObfuscationController ``` class can be accessed from the API Client.

```javascript
var controller = lib.CodeObfuscationController;
```

### <a name="get_https_api_rest_sh_api_so"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.getHttpsApiRestShApiSO") getHttpsApiRestShApiSO

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```javascript
function getHttpsApiRestShApiSO(input, callback)
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

    controller.getHttpsApiRestShApiSO(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_so"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.createHttpsApiRestShApiSO") createHttpsApiRestShApiSO

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```javascript
function createHttpsApiRestShApiSO(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSOModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiSO(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="hosting_controller"></a>![Class: ](https://apidocs.io/img/class.png ".HostingController") HostingController

### Get singleton instance

The singleton instance of the ``` HostingController ``` class can be accessed from the API Client.

```javascript
var controller = lib.HostingController;
```

### <a name="get_https_api_rest_sh_api_sh"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.getHttpsApiRestShApiSH") getHttpsApiRestShApiSH

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```javascript
function getHttpsApiRestShApiSH(input, callback)
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

    controller.getHttpsApiRestShApiSH(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_sh"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.createHttpsApiRestShApiSH") createHttpsApiRestShApiSH

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```javascript
function createHttpsApiRestShApiSH(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiSHModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiSH(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPIController") DataManipulationConversionSortingAndCompressionAPIController

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPIController ``` class can be accessed from the API Client.

```javascript
var controller = lib.DataManipulationConversionSortingAndCompressionAPIController;
```

### <a name="get_https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.getHttpsApiRestShApiD") getHttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function getHttpsApiRestShApiD(input, callback)
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

    controller.getHttpsApiRestShApiD(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.createHttpsApiRestShApiD") createHttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function createHttpsApiRestShApiD(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiDModel({
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

    controller.createHttpsApiRestShApiD(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPIController") ImageManipulationAndModerationAPIController

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPIController ``` class can be accessed from the API Client.

```javascript
var controller = lib.ImageManipulationAndModerationAPIController;
```

### <a name="get_https_api_rest_sh_api_i"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.getHttpsApiRestShApiI") getHttpsApiRestShApiI

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```javascript
function getHttpsApiRestShApiI(input, callback)
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

    controller.getHttpsApiRestShApiI(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_i"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.createHttpsApiRestShApiI") createHttpsApiRestShApiI

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```javascript
function createHttpsApiRestShApiI(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiIModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiI(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="verification_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VerificationController") VerificationController

### Get singleton instance

The singleton instance of the ``` VerificationController ``` class can be accessed from the API Client.

```javascript
var controller = lib.VerificationController;
```

### <a name="get_https_api_rest_sh_api_va"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVA") getHttpsApiRestShApiVA

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```javascript
function getHttpsApiRestShApiVA(input, callback)
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
        input['z'] = 6;
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiVA(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_va"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVA") createHttpsApiRestShApiVA

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```javascript
function createHttpsApiRestShApiVA(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiVAModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiVA(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_vu"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVU") getHttpsApiRestShApiVU

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```javascript
function getHttpsApiRestShApiVU(input, callback)
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

    controller.getHttpsApiRestShApiVU(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_vu"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVU") createHttpsApiRestShApiVU

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```javascript
function createHttpsApiRestShApiVU(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiVUModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiVU(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_v"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiV") getHttpsApiRestShApiV

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```javascript
function getHttpsApiRestShApiV(input, callback)
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

    controller.getHttpsApiRestShApiV(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_v"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiV") createHttpsApiRestShApiV

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```javascript
function createHttpsApiRestShApiV(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiVModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiV(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPIController") TwoFactorAuthenticationAPIController

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPIController ``` class can be accessed from the API Client.

```javascript
var controller = lib.TwoFactorAuthenticationAPIController;
```

### <a name="get_https_api_rest_sh_api2fa_t"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2faT") getHttpsApiRestShApi2faT

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```javascript
function getHttpsApiRestShApi2faT(input, callback)
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

    controller.getHttpsApiRestShApi2faT(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api2fa_t"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2faT") createHttpsApiRestShApi2faT

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```javascript
function createHttpsApiRestShApi2faT(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApi2faTModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApi2faT(input, function(error, response, context) {

    
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
        input['body'] = new HttpsApiRestShApi2faModel({"key":"value"});
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

### <a name="get_https_api_rest_sh_api_ui"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUI") getHttpsApiRestShApiUI

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```javascript
function getHttpsApiRestShApiUI(input, callback)
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

    controller.getHttpsApiRestShApiUI(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_ui"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUI") createHttpsApiRestShApiUI

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```javascript
function createHttpsApiRestShApiUI(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiUIModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiUI(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_uu"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUU") getHttpsApiRestShApiUU

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```javascript
function getHttpsApiRestShApiUU(input, callback)
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

    controller.getHttpsApiRestShApiUU(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_uu"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUU") createHttpsApiRestShApiUU

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```javascript
function createHttpsApiRestShApiUU(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiUUModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiUU(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_ud"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUD") getHttpsApiRestShApiUD

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```javascript
function getHttpsApiRestShApiUD(input, callback)
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

    controller.getHttpsApiRestShApiUD(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_ud"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUD") createHttpsApiRestShApiUD

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```javascript
function createHttpsApiRestShApiUD(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiUDModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiUD(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration_controller"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistrationController") LoginAndRegistrationController

### Get singleton instance

The singleton instance of the ``` LoginAndRegistrationController ``` class can be accessed from the API Client.

```javascript
var controller = lib.LoginAndRegistrationController;
```

### <a name="get_https_api_rest_sh_api_aur"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAUR") getHttpsApiRestShApiAUR

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```javascript
function getHttpsApiRestShApiAUR(input, callback)
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
        input['phone'] = 98;
        input['countrycode'] = 98;
        input['address'] = 'address';
        input['contentType'] = 'Content-Type';

    controller.getHttpsApiRestShApiAUR(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_aur"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAUR") createHttpsApiRestShApiAUR

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```javascript
function createHttpsApiRestShApiAUR(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiAURModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiAUR(input, function(error, response, context) {

    
    });
```



### <a name="get_https_api_rest_sh_api_aul"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAUL") getHttpsApiRestShApiAUL

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```javascript
function getHttpsApiRestShApiAUL(input, callback)
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

    controller.getHttpsApiRestShApiAUL(input, function(error, response, context) {

    
    });
```



### <a name="create_https_api_rest_sh_api_aul"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAUL") createHttpsApiRestShApiAUL

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```javascript
function createHttpsApiRestShApiAUL(input, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var input = [];
        input['body'] = new HttpsApiRestShApiAULModel({"key":"value"});
        input['contentType'] = 'Content-Type';

    controller.createHttpsApiRestShApiAUL(input, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)



