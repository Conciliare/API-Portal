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
| uid | Your user ID |
| secret | Your Private API Key |
| key | Your Public API Key |



API client can be initialized as following:

```JavaScript
const lib = require('lib');

// Configuration parameters and credentials
lib.Configuration.uid = "UID"; // Your user ID
lib.Configuration.secret = "SECRET"; // Your Private API Key
lib.Configuration.key = "KEY"; // Your Public API Key

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

The singleton instance of the ``` AdvancedLogging ``` class can be accessed from the API Client.

```javascript
var controller = lib.AdvancedLogging;
```

### <a name="logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingInfo") loggingInfo

> WAF Log Info


```javascript
function loggingInfo(key, uid, name, origin, time, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var name = 'name';
    var origin = 'origin';
    var time = 'time';
    var contentType = 'Content-Type';

    controller.loggingInfo(key, uid, name, origin, time, contentType, function(error, response, context) {

    
    });
```



### <a name="logging_setup"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingSetup") loggingSetup

> WAF Log Setup


```javascript
function loggingSetup(key, uid, name, origin, activate, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var name = 'name';
    var origin = 'origin';
    var activate = true;
    var contentType = 'Content-Type';

    controller.loggingSetup(key, uid, name, origin, activate, contentType, function(error, response, context) {

    
    });
```



### <a name="logging_info1"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingInfo1") loggingInfo1

> WAF Log Info


```javascript
function loggingInfo1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiSLI({"key":"value"});
    var contentType = 'Content-Type';

    controller.loggingInfo1(body, contentType, function(error, response, context) {

    
    });
```



### <a name="logging_setup1"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingSetup1") loggingSetup1

> WAF Log Setup


```javascript
function loggingSetup1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiSL({"key":"value"});
    var contentType = 'Content-Type';

    controller.loggingSetup1(body, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtection") WAFDDOSProtection

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtection ``` class can be accessed from the API Client.

```javascript
var controller = lib.WAFDDOSProtection;
```

### <a name="https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSWC") httpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function httpsApiRestShApiSWC(key, uid, name, origin, rule, contentType, callback)
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

    var key = 'API';
    var uid = 'UID';
    var name = 'origin-name';
    var origin = 'origin.yourdomain.tld';
    var rule = 'header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does';
    var contentType = 'application/json';

    controller.httpsApiRestShApiSWC(key, uid, name, origin, rule, contentType, function(error, response, context) {

    
    });
```



### <a name="https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSW") httpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function httpsApiRestShApiSW(key, uid, origin, cname, contentType, callback)
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

    var key = 'API';
    var uid = 'UID';
    var origin = 'origin.yourdomain.tld';
    var cname = 'yourdomain.tld,www.yourdomain.tld';
    var contentType = 'application/json';

    controller.httpsApiRestShApiSW(key, uid, origin, cname, contentType, function(error, response, context) {

    
    });
```



### <a name="https_api_rest_sh_api_swc1"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSWC1") httpsApiRestShApiSWC1

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function httpsApiRestShApiSWC1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiSWC({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "name": "WHAT YOU WISH TO NAME YOUR WAF",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
});
    var contentType = 'application/json';

    controller.httpsApiRestShApiSWC1(body, contentType, function(error, response, context) {

    
    });
```



### <a name="https_api_rest_sh_api_sw1"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSW1") httpsApiRestShApiSW1

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function httpsApiRestShApiSW1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiSW({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
});
    var contentType = 'application/json';

    controller.httpsApiRestShApiSW1(body, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="encryption"></a>![Class: ](https://apidocs.io/img/class.png ".Encryption") Encryption

### Get singleton instance

The singleton instance of the ``` Encryption ``` class can be accessed from the API Client.

```javascript
var controller = lib.Encryption;
```

### <a name="data_and_file_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.dataAndFileEncryption") dataAndFileEncryption

> Data and File Encryption API


```javascript
function dataAndFileEncryption(key, uid, data, method, bit, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var data = 'data';
    var method = 'method';
    var bit = 175;
    var contentType = 'Content-Type';

    controller.dataAndFileEncryption(key, uid, data, method, bit, contentType, function(error, response, context) {

    
    });
```



### <a name="data_and_file_encryption1"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.dataAndFileEncryption1") dataAndFileEncryption1

> Data and File Encryption API


```javascript
function dataAndFileEncryption1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiSE({"key":"value"});
    var contentType = 'Content-Type';

    controller.dataAndFileEncryption1(body, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="cdn"></a>![Class: ](https://apidocs.io/img/class.png ".CDN") CDN

### Get singleton instance

The singleton instance of the ``` CDN ``` class can be accessed from the API Client.

```javascript
var controller = lib.CDN;
```

### <a name="c_dn_push_zone"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPushZone") cDNPushZone

> CDN Push Zone API


```javascript
function cDNPushZone(key, uid, cname, file, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var cname = 'cname';
    var file = 'file';
    var contentType = 'Content-Type';

    controller.cDNPushZone(key, uid, cname, file, contentType, function(error, response, context) {

    
    });
```



### <a name="c_dn_pull_zone"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPullZone") cDNPullZone

> CDN Pull Zone API


```javascript
function cDNPullZone(key, uid, origin, cname, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var origin = 'origin';
    var cname = 'cname';
    var contentType = 'Content-Type';

    controller.cDNPullZone(key, uid, origin, cname, contentType, function(error, response, context) {

    
    });
```



### <a name="c_dn_push_zone1"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPushZone1") cDNPushZone1

> CDN Push Zone API


```javascript
function cDNPushZone1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiSCPush({"key":"value"});
    var contentType = 'Content-Type';

    controller.cDNPushZone1(body, contentType, function(error, response, context) {

    
    });
```



### <a name="c_dn_pull_zone1"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPullZone1") cDNPullZone1

> CDN Pull Zone API


```javascript
function cDNPullZone1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiSCPull({"key":"value"});
    var contentType = 'Content-Type';

    controller.cDNPullZone1(body, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="dns"></a>![Class: ](https://apidocs.io/img/class.png ".DNS") DNS

### Get singleton instance

The singleton instance of the ``` DNS ``` class can be accessed from the API Client.

```javascript
var controller = lib.DNS;
```

### <a name="d_ns_configuration"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSConfiguration") dNSConfiguration

> DNS Configuration API


```javascript
function dNSConfiguration(key, uid, domain, records, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var domain = 'domain';
    var records = 'records';
    var contentType = 'Content-Type';

    controller.dNSConfiguration(key, uid, domain, records, contentType, function(error, response, context) {

    
    });
```



### <a name="d_ns_configuration1"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSConfiguration1") dNSConfiguration1

> DNS Configuration API


```javascript
function dNSConfiguration1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiSDC({"key":"value"});
    var contentType = 'Content-Type';

    controller.dNSConfiguration1(body, contentType, function(error, response, context) {

    
    });
```



### <a name="d_ns_creation"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSCreation") dNSCreation

> DNS Creation API


```javascript
function dNSCreation(key, uid, domain, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var domain = 'domain';
    var contentType = 'Content-Type';

    controller.dNSCreation(key, uid, domain, contentType, function(error, response, context) {

    
    });
```



### <a name="d_ns_creation1"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSCreation1") dNSCreation1

> DNS Creation API


```javascript
function dNSCreation1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiSDA({"key":"value"});
    var contentType = 'Content-Type';

    controller.dNSCreation1(body, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscation") CodeObfuscation

### Get singleton instance

The singleton instance of the ``` CodeObfuscation ``` class can be accessed from the API Client.

```javascript
var controller = lib.CodeObfuscation;
```

### <a name="obfuscation_and_anti_tampering"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.obfuscationAndAntiTampering") obfuscationAndAntiTampering

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```javascript
function obfuscationAndAntiTampering(key, uid, app, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var app = 'app';
    var contentType = 'Content-Type';

    controller.obfuscationAndAntiTampering(key, uid, app, contentType, function(error, response, context) {

    
    });
```



### <a name="obfuscation_and_anti_tampering1"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.obfuscationAndAntiTampering1") obfuscationAndAntiTampering1

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```javascript
function obfuscationAndAntiTampering1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiSO({"key":"value"});
    var contentType = 'Content-Type';

    controller.obfuscationAndAntiTampering1(body, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="hosting"></a>![Class: ](https://apidocs.io/img/class.png ".Hosting") Hosting

### Get singleton instance

The singleton instance of the ``` Hosting ``` class can be accessed from the API Client.

```javascript
var controller = lib.Hosting;
```

### <a name="hosting_setup"></a>![Method: ](https://apidocs.io/img/method.png ".Hosting.hostingSetup") hostingSetup

> Node.JS and Static Web APP Hosting


```javascript
function hostingSetup(key, uid, app, domain, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var app = 'app';
    var domain = 'domain';
    var contentType = 'Content-Type';

    controller.hostingSetup(key, uid, app, domain, contentType, function(error, response, context) {

    
    });
```



### <a name="hosting_setup1"></a>![Method: ](https://apidocs.io/img/method.png ".Hosting.hostingSetup1") hostingSetup1

> Node.JS and Static Web APP Hosting


```javascript
function hostingSetup1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiSH({"key":"value"});
    var contentType = 'Content-Type';

    controller.hostingSetup1(body, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPI") DataManipulationConversionSortingAndCompressionAPI

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPI ``` class can be accessed from the API Client.

```javascript
var controller = lib.DataManipulationConversionSortingAndCompressionAPI;
```

### <a name="https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiD") httpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function httpsApiRestShApiD(key, uid, user, apiuid, data, contentType, callback)
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

    var key = 'API';
    var uid = 'UID';
    var user = 'UID';
    var apiuid = 'apiUID';
    var data = 'https://static.yourcdn.com/data.file';
    var contentType = 'application/json';

    controller.httpsApiRestShApiD(key, uid, user, apiuid, data, contentType, function(error, response, context) {

    
    });
```



### <a name="https_api_rest_sh_api_d1"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiD1") httpsApiRestShApiD1

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function httpsApiRestShApiD1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiD({
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
    var contentType = 'application/json';

    controller.httpsApiRestShApiD1(body, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPI") ImageManipulationAndModerationAPI

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPI ``` class can be accessed from the API Client.

```javascript
var controller = lib.ImageManipulationAndModerationAPI;
```

### <a name="image_manipulation"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPI.imageManipulation") imageManipulation

> Image Manipulation API


```javascript
function imageManipulation(key, uid, image, transform, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var image = 'image';
    var transform = 'transform';
    var contentType = 'Content-Type';

    controller.imageManipulation(key, uid, image, transform, contentType, function(error, response, context) {

    
    });
```



### <a name="image_manipulation1"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPI.imageManipulation1") imageManipulation1

> Image Manipulation API


```javascript
function imageManipulation1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiI({"key":"value"});
    var contentType = 'Content-Type';

    controller.imageManipulation1(body, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="verification"></a>![Class: ](https://apidocs.io/img/class.png ".Verification") Verification

### Get singleton instance

The singleton instance of the ``` Verification ``` class can be accessed from the API Client.

```javascript
var controller = lib.Verification;
```

### <a name="user_address_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userAddressVerification") userAddressVerification

> User Address Verification API


```javascript
function userAddressVerification(key, uid, user, a, sa, c, s, z, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var user = 'user';
    var a = 'a';
    var sa = 'sa';
    var c = 'c';
    var s = 's';
    var z = 12;
    var contentType = 'Content-Type';

    controller.userAddressVerification(key, uid, user, a, sa, c, s, z, contentType, function(error, response, context) {

    
    });
```



### <a name="user_address_verification1"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userAddressVerification1") userAddressVerification1

> User Address Verification API


```javascript
function userAddressVerification1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiVA({"key":"value"});
    var contentType = 'Content-Type';

    controller.userAddressVerification1(body, contentType, function(error, response, context) {

    
    });
```



### <a name="user_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userVerification") userVerification

> User Verification API


```javascript
function userVerification(key, uid, user, code, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var user = 'user';
    var code = 'code';
    var contentType = 'Content-Type';

    controller.userVerification(key, uid, user, code, contentType, function(error, response, context) {

    
    });
```



### <a name="user_verification1"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userVerification1") userVerification1

> User Verification API


```javascript
function userVerification1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiVU({"key":"value"});
    var contentType = 'Content-Type';

    controller.userVerification1(body, contentType, function(error, response, context) {

    
    });
```



### <a name="cellphone_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.cellphoneVerification") cellphoneVerification

> Verification API


```javascript
function cellphoneVerification(key, uid, to, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var to = 'to';
    var contentType = 'Content-Type';

    controller.cellphoneVerification(key, uid, to, contentType, function(error, response, context) {

    
    });
```



### <a name="cellphone_verification1"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.cellphoneVerification1") cellphoneVerification1

> Verification API


```javascript
function cellphoneVerification1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiV({"key":"value"});
    var contentType = 'Content-Type';

    controller.cellphoneVerification1(body, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPI") TwoFactorAuthenticationAPI

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPI ``` class can be accessed from the API Client.

```javascript
var controller = lib.TwoFactorAuthenticationAPI;
```

### <a name="m2_fa_token_response"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.m2FATokenResponse") m2FATokenResponse

> Two Factor Authentication Token Reply


```javascript
function m2FATokenResponse(key, uid, user, code, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var user = 'user';
    var code = 'code';
    var contentType = 'Content-Type';

    controller.m2FATokenResponse(key, uid, user, code, contentType, function(error, response, context) {

    
    });
```



### <a name="m2_fa_token_response1"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.m2FATokenResponse1") m2FATokenResponse1

> Two Factor Authentication Token Reply


```javascript
function m2FATokenResponse1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApi2faT({"key":"value"});
    var contentType = 'Content-Type';

    controller.m2FATokenResponse1(body, contentType, function(error, response, context) {

    
    });
```



### <a name="two_factor_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.twoFactorAuthentication") twoFactorAuthentication

> Two Factor Authentication API


```javascript
function twoFactorAuthentication(key, uid, to, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var to = 'to';
    var contentType = 'Content-Type';

    controller.twoFactorAuthentication(key, uid, to, contentType, function(error, response, context) {

    
    });
```



### <a name="two_factor_authentication1"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.twoFactorAuthentication1") twoFactorAuthentication1

> Two Factor Authentication API


```javascript
function twoFactorAuthentication1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApi2fa({"key":"value"});
    var contentType = 'Content-Type';

    controller.twoFactorAuthentication1(body, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="user_management"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagement") UserManagement

### Get singleton instance

The singleton instance of the ``` UserManagement ``` class can be accessed from the API Client.

```javascript
var controller = lib.UserManagement;
```

### <a name="get_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.getUserInfo") getUserInfo

> Get User Info API


```javascript
function getUserInfo(key, uid, user, apiuid, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var user = 'user';
    var apiuid = 'apiuid';
    var contentType = 'Content-Type';

    controller.getUserInfo(key, uid, user, apiuid, contentType, function(error, response, context) {

    
    });
```



### <a name="get_user_info1"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.getUserInfo1") getUserInfo1

> Get User Info API


```javascript
function getUserInfo1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiUI({"key":"value"});
    var contentType = 'Content-Type';

    controller.getUserInfo1(body, contentType, function(error, response, context) {

    
    });
```



### <a name="update_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.updateUser") updateUser

> Update User API


```javascript
function updateUser(key, uid, user, apiuid, avatar, customInput, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var user = 'user';
    var apiuid = 'apiuid';
    var avatar = 'avatar';
    var customInput = custom input;
    var contentType = 'Content-Type';

    controller.updateUser(key, uid, user, apiuid, avatar, customInput, contentType, function(error, response, context) {

    
    });
```



### <a name="update_user1"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.updateUser1") updateUser1

> Update User API


```javascript
function updateUser1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiUU({"key":"value"});
    var contentType = 'Content-Type';

    controller.updateUser1(body, contentType, function(error, response, context) {

    
    });
```



### <a name="delete_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.deleteUser") deleteUser

> Delete User API


```javascript
function deleteUser(api, uid, user, apiuid, contentType, callback)
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

    var api = 'api';
    var uid = 'uid';
    var user = 'user';
    var apiuid = 'apiuid';
    var contentType = 'Content-Type';

    controller.deleteUser(api, uid, user, apiuid, contentType, function(error, response, context) {

    
    });
```



### <a name="delete_user1"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.deleteUser1") deleteUser1

> Delete User API


```javascript
function deleteUser1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiUD({"key":"value"});
    var contentType = 'Content-Type';

    controller.deleteUser1(body, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistration") LoginAndRegistration

### Get singleton instance

The singleton instance of the ``` LoginAndRegistration ``` class can be accessed from the API Client.

```javascript
var controller = lib.LoginAndRegistration;
```

### <a name="user_registration"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userRegistration") userRegistration

> User Registration API


```javascript
function userRegistration(key, uid, user, password, name, email, phone, countrycode, address, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var user = 'user';
    var password = 'password';
    var name = 'name';
    var email = 'email';
    var phone = 12;
    var countrycode = 12;
    var address = 'address';
    var contentType = 'Content-Type';

    controller.userRegistration(key, uid, user, password, name, email, phone, countrycode, address, contentType, function(error, response, context) {

    
    });
```



### <a name="user_registration1"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userRegistration1") userRegistration1

> User Registration API


```javascript
function userRegistration1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiAUR({"key":"value"});
    var contentType = 'Content-Type';

    controller.userRegistration1(body, contentType, function(error, response, context) {

    
    });
```



### <a name="user_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userAuthentication") userAuthentication

> User Authentication API


```javascript
function userAuthentication(key, uid, user, password, contentType, callback)
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

    var key = 'key';
    var uid = 'uid';
    var user = 'user';
    var password = 'password';
    var contentType = 'Content-Type';

    controller.userAuthentication(key, uid, user, password, contentType, function(error, response, context) {

    
    });
```



### <a name="user_authentication1"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userAuthentication1") userAuthentication1

> User Authentication API


```javascript
function userAuthentication1(body, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new HttpsApiRestShApiAUL({"key":"value"});
    var contentType = 'Content-Type';

    controller.userAuthentication1(body, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)



