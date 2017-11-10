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

The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```composer.json``` file that comes with the SDK. 
To resolve these dependencies, we use the Composer package manager which requires PHP greater than 5.3.2 installed in your system. 
Visit [https://getcomposer.org/download/](https://getcomposer.org/download/) to download the installer file for Composer and run it in your system. 
Open command prompt and type ```composer --version```. This should display the current version of the Composer installed if the installation was successful.

* Using command line, navigate to the directory containing the generated files (including ```composer.json```) for the SDK. 
* Run the command ```composer install```. This should install all the required dependencies and create the ```vendor``` directory in your project directory.

![Building SDK - Step 1](https://apidocs.io/illustration/php?step=installDependencies&workspaceFolder=SMASH-PHP)

### [For Windows Users Only] Configuring CURL Certificate Path in php.ini

CURL used to include a list of accepted CAs, but no longer bundles ANY CA certs. So by default it will reject all SSL certificates as unverifiable. You will have to get your CA's cert and point curl at it. The steps are as follows:

1. Download the certificate bundle (.pem file) from [https://curl.haxx.se/docs/caextract.html](https://curl.haxx.se/docs/caextract.html) on to your system.
2. Add curl.cainfo = "PATH_TO/cacert.pem" to your php.ini file located in your php installation. “PATH_TO” must be an absolute path containing the .pem file.

```ini
[curl]
; A default value for the CURLOPT_CAINFO option. This is required to be an
; absolute path.
;curl.cainfo =
```

## How to Use

The following section explains how to use the SMASH library in a new project.

### 1. Open Project in an IDE

Open an IDE for PHP like PhpStorm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=openIDE&workspaceFolder=SMASH-PHP)

Click on ```Open``` in PhpStorm to browse to your generated SDK directory and then click ```OK```.

![Open project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=openProject0&workspaceFolder=SMASH-PHP)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=createDirectory&workspaceFolder=SMASH-PHP)

Name the directory as "test"

![Add a new project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=nameDirectory&workspaceFolder=SMASH-PHP)
   
Add a PHP file to this project

![Add a new project in PHPStorm - Step 3](https://apidocs.io/illustration/php?step=createFile&workspaceFolder=SMASH-PHP)

Name it "testSDK"

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=nameFile&workspaceFolder=SMASH-PHP)

Depending on your project setup, you might need to include composer's autoloader in your PHP code to enable auto loading of classes.

```PHP
require_once "../vendor/autoload.php";
```

It is important that the path inside require_once correctly points to the file ```autoload.php``` inside the vendor directory created during dependency installations.

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=projectFiles&workspaceFolder=SMASH-PHP)

After this you can add code to initialize the client library and acquire the instance of a Controller class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

### 3. Run the Test Project

To run your project you must set the Interpreter for your project. Interpreter is the PHP engine installed on your computer.

Open ```Settings``` from ```File``` menu.

![Run Test Project - Step 1](https://apidocs.io/illustration/php?step=openSettings&workspaceFolder=SMASH-PHP)

Select ```PHP``` from within ```Languages & Frameworks```

![Run Test Project - Step 2](https://apidocs.io/illustration/php?step=setInterpreter0&workspaceFolder=SMASH-PHP)

Browse for Interpreters near the ```Interpreter``` option and choose your interpreter.

![Run Test Project - Step 3](https://apidocs.io/illustration/php?step=setInterpreter1&workspaceFolder=SMASH-PHP)

Once the interpreter is selected, click ```OK```

![Run Test Project - Step 4](https://apidocs.io/illustration/php?step=setInterpreter2&workspaceFolder=SMASH-PHP)

To run your project, right click on your PHP file inside your Test project and click on ```Run```

![Run Test Project - Step 5](https://apidocs.io/illustration/php?step=runProject&workspaceFolder=SMASH-PHP)

## How to Test

Unit tests in this SDK can be run using PHPUnit. 

1. First install the dependencies using composer including the `require-dev` dependencies.
2. Run `vendor\bin\phpunit --verbose` from commandline to execute tests. If you have 
   installed PHPUnit globally, run tests using `phpunit --verbose` instead.

You can change the PHPUnit test configuration in the `phpunit.xml` file.

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| key | Your API Key |
| uid | Your User ID |



API client can be initialized as following.

```php
$key = 'API'; // Your API Key
$uid = 'UID'; // Your User ID

$client = new SMASHLib\SMASHClient($key, $uid);
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

```php
$advancedLogging = $client->getAdvancedLogging();
```

### <a name="get_https_api_rest_sh_api_sli"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSLI") getHttpsApiRestShApiSLI

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```php
function getHttpsApiRestShApiSLI($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$name = 'name';
$collect['name'] = $name;

$origin = 'origin';
$collect['origin'] = $origin;

$time = 'time';
$collect['time'] = $time;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $advancedLogging->getHttpsApiRestShApiSLI($collect);

```


### <a name="get_https_api_rest_sh_api_sl"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSL") getHttpsApiRestShApiSL

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```php
function getHttpsApiRestShApiSL($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$name = 'name';
$collect['name'] = $name;

$origin = 'origin';
$collect['origin'] = $origin;

$activate = false;
$collect['activate'] = $activate;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $advancedLogging->getHttpsApiRestShApiSL($collect);

```


### <a name="create_https_api_rest_sh_api_sli"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSLI") createHttpsApiRestShApiSLI

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```php
function createHttpsApiRestShApiSLI($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSLIModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $advancedLogging->createHttpsApiRestShApiSLI($collect);

```


### <a name="create_https_api_rest_sh_api_sl"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSL") createHttpsApiRestShApiSL

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```php
function createHttpsApiRestShApiSL($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSLModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $advancedLogging->createHttpsApiRestShApiSL($collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection_controller"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtectionController") WAFDDOSProtectionController

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtectionController ``` class can be accessed from the API Client.

```php
$wAFDDOSProtection = $client->getWAFDDOSProtection();
```

### <a name="get_https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSWC") getHttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```php
function getHttpsApiRestShApiSWC($options)
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

```php
$key = 'API';
$collect['key'] = $key;

$uid = 'UID';
$collect['uid'] = $uid;

$name = 'origin-name';
$collect['name'] = $name;

$origin = 'origin.yourdomain.tld';
$collect['origin'] = $origin;

$rule = 'header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does';
$collect['rule'] = $rule;

$contentType = 'application/json';
$collect['contentType'] = $contentType;


$result = $wAFDDOSProtection->getHttpsApiRestShApiSWC($collect);

```


### <a name="get_https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSW") getHttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```php
function getHttpsApiRestShApiSW($options)
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

```php
$key = 'API';
$collect['key'] = $key;

$uid = 'UID';
$collect['uid'] = $uid;

$origin = 'origin.yourdomain.tld';
$collect['origin'] = $origin;

$cname = 'yourdomain.tld,www.yourdomain.tld';
$collect['cname'] = $cname;

$contentType = 'application/json';
$collect['contentType'] = $contentType;


$result = $wAFDDOSProtection->getHttpsApiRestShApiSW($collect);

```


### <a name="create_https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSWC") createHttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```php
function createHttpsApiRestShApiSWC($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$bodyValue = "{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}";
$body = APIHelper::deserialize($bodyValue);
$collect['body'] = $body;

$contentType = 'application/json';
$collect['contentType'] = $contentType;


$result = $wAFDDOSProtection->createHttpsApiRestShApiSWC($collect);

```


### <a name="create_https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSW") createHttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```php
function createHttpsApiRestShApiSW($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}";
$body = APIHelper::deserialize($bodyValue);
$collect['body'] = $body;

$contentType = 'application/json';
$collect['contentType'] = $contentType;


$result = $wAFDDOSProtection->createHttpsApiRestShApiSW($collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EncryptionController") EncryptionController

### Get singleton instance

The singleton instance of the ``` EncryptionController ``` class can be accessed from the API Client.

```php
$encryption = $client->getEncryption();
```

### <a name="get_https_api_rest_sh_api_se"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.getHttpsApiRestShApiSE") getHttpsApiRestShApiSE

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```php
function getHttpsApiRestShApiSE($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$data = 'data';
$collect['data'] = $data;

$method = 'method';
$collect['method'] = $method;

$bit = 34;
$collect['bit'] = $bit;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $encryption->getHttpsApiRestShApiSE($collect);

```


### <a name="create_https_api_rest_sh_api_se"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.createHttpsApiRestShApiSE") createHttpsApiRestShApiSE

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```php
function createHttpsApiRestShApiSE($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSEModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $encryption->createHttpsApiRestShApiSE($collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CDNController") CDNController

### Get singleton instance

The singleton instance of the ``` CDNController ``` class can be accessed from the API Client.

```php
$cDN = $client->getCDN();
```

### <a name="get_https_api_rest_sh_api_sc_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiSCPush") getHttpsApiRestShApiSCPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```php
function getHttpsApiRestShApiSCPush($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$cname = 'cname';
$collect['cname'] = $cname;

$file = 'file';
$collect['file'] = $file;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $cDN->getHttpsApiRestShApiSCPush($collect);

```


### <a name="get_https_api_rest_sh_api_sc_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiSCPull") getHttpsApiRestShApiSCPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```php
function getHttpsApiRestShApiSCPull($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$origin = 'origin';
$collect['origin'] = $origin;

$cname = 'cname';
$collect['cname'] = $cname;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $cDN->getHttpsApiRestShApiSCPull($collect);

```


### <a name="create_https_api_rest_sh_api_sc_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiSCPush") createHttpsApiRestShApiSCPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```php
function createHttpsApiRestShApiSCPush($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSCPushModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $cDN->createHttpsApiRestShApiSCPush($collect);

```


### <a name="create_https_api_rest_sh_api_sc_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiSCPull") createHttpsApiRestShApiSCPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```php
function createHttpsApiRestShApiSCPull($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSCPullModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $cDN->createHttpsApiRestShApiSCPull($collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DNSController") DNSController

### Get singleton instance

The singleton instance of the ``` DNSController ``` class can be accessed from the API Client.

```php
$dNS = $client->getDNS();
```

### <a name="get_https_api_rest_sh_api_sdc"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiSDC") getHttpsApiRestShApiSDC

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```php
function getHttpsApiRestShApiSDC($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$domain = 'domain';
$collect['domain'] = $domain;

$records = 'records';
$collect['records'] = $records;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $dNS->getHttpsApiRestShApiSDC($collect);

```


### <a name="create_https_api_rest_sh_api_sdc"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiSDC") createHttpsApiRestShApiSDC

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```php
function createHttpsApiRestShApiSDC($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSDCModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $dNS->createHttpsApiRestShApiSDC($collect);

```


### <a name="get_https_api_rest_sh_api_sda"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiSDA") getHttpsApiRestShApiSDA

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```php
function getHttpsApiRestShApiSDA($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| domain |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$domain = 'domain';
$collect['domain'] = $domain;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $dNS->getHttpsApiRestShApiSDA($collect);

```


### <a name="create_https_api_rest_sh_api_sda"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiSDA") createHttpsApiRestShApiSDA

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```php
function createHttpsApiRestShApiSDA($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSDAModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $dNS->createHttpsApiRestShApiSDA($collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscationController") CodeObfuscationController

### Get singleton instance

The singleton instance of the ``` CodeObfuscationController ``` class can be accessed from the API Client.

```php
$codeObfuscation = $client->getCodeObfuscation();
```

### <a name="get_https_api_rest_sh_api_so"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.getHttpsApiRestShApiSO") getHttpsApiRestShApiSO

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```php
function getHttpsApiRestShApiSO($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| app |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$app = 'app';
$collect['app'] = $app;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $codeObfuscation->getHttpsApiRestShApiSO($collect);

```


### <a name="create_https_api_rest_sh_api_so"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.createHttpsApiRestShApiSO") createHttpsApiRestShApiSO

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```php
function createHttpsApiRestShApiSO($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSOModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $codeObfuscation->createHttpsApiRestShApiSO($collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting_controller"></a>![Class: ](https://apidocs.io/img/class.png ".HostingController") HostingController

### Get singleton instance

The singleton instance of the ``` HostingController ``` class can be accessed from the API Client.

```php
$hosting = $client->getHosting();
```

### <a name="get_https_api_rest_sh_api_sh"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.getHttpsApiRestShApiSH") getHttpsApiRestShApiSH

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```php
function getHttpsApiRestShApiSH($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$app = 'app';
$collect['app'] = $app;

$domain = 'domain';
$collect['domain'] = $domain;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $hosting->getHttpsApiRestShApiSH($collect);

```


### <a name="create_https_api_rest_sh_api_sh"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.createHttpsApiRestShApiSH") createHttpsApiRestShApiSH

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```php
function createHttpsApiRestShApiSH($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSHModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $hosting->createHttpsApiRestShApiSH($collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPIController") DataManipulationConversionSortingAndCompressionAPIController

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPIController ``` class can be accessed from the API Client.

```php
$dataManipulationConversionSortingAndCompressionAPI = $client->getDataManipulationConversionSortingAndCompressionAPI();
```

### <a name="get_https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.getHttpsApiRestShApiD") getHttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```php
function getHttpsApiRestShApiD($options)
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

```php
$key = 'API';
$collect['key'] = $key;

$uid = 'UID';
$collect['uid'] = $uid;

$user = 'UID';
$collect['user'] = $user;

$apiuid = 'apiUID';
$collect['apiuid'] = $apiuid;

$data = 'https://static.yourcdn.com/data.file';
$collect['data'] = $data;

$contentType = 'application/json';
$collect['contentType'] = $contentType;


$result = $dataManipulationConversionSortingAndCompressionAPI->getHttpsApiRestShApiD($collect);

```


### <a name="create_https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.createHttpsApiRestShApiD") createHttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```php
function createHttpsApiRestShApiD($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}";
$body = APIHelper::deserialize($bodyValue);
$collect['body'] = $body;

$contentType = 'application/json';
$collect['contentType'] = $contentType;


$result = $dataManipulationConversionSortingAndCompressionAPI->createHttpsApiRestShApiD($collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPIController") ImageManipulationAndModerationAPIController

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPIController ``` class can be accessed from the API Client.

```php
$imageManipulationAndModerationAPI = $client->getImageManipulationAndModerationAPI();
```

### <a name="get_https_api_rest_sh_api_i"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.getHttpsApiRestShApiI") getHttpsApiRestShApiI

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```php
function getHttpsApiRestShApiI($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$image = 'image';
$collect['image'] = $image;

$transform = 'transform';
$collect['transform'] = $transform;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $imageManipulationAndModerationAPI->getHttpsApiRestShApiI($collect);

```


### <a name="create_https_api_rest_sh_api_i"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.createHttpsApiRestShApiI") createHttpsApiRestShApiI

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```php
function createHttpsApiRestShApiI($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiIModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $imageManipulationAndModerationAPI->createHttpsApiRestShApiI($collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VerificationController") VerificationController

### Get singleton instance

The singleton instance of the ``` VerificationController ``` class can be accessed from the API Client.

```php
$verification = $client->getVerification();
```

### <a name="get_https_api_rest_sh_api_va"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVA") getHttpsApiRestShApiVA

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```php
function getHttpsApiRestShApiVA($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$user = 'user';
$collect['user'] = $user;

$a = 'a';
$collect['a'] = $a;

$sa = 'sa';
$collect['sa'] = $sa;

$c = 'c';
$collect['c'] = $c;

$s = 's';
$collect['s'] = $s;

$z = 125;
$collect['z'] = $z;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $verification->getHttpsApiRestShApiVA($collect);

```


### <a name="create_https_api_rest_sh_api_va"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVA") createHttpsApiRestShApiVA

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```php
function createHttpsApiRestShApiVA($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiVAModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $verification->createHttpsApiRestShApiVA($collect);

```


### <a name="get_https_api_rest_sh_api_vu"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVU") getHttpsApiRestShApiVU

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```php
function getHttpsApiRestShApiVU($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$user = 'user';
$collect['user'] = $user;

$code = 'code';
$collect['code'] = $code;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $verification->getHttpsApiRestShApiVU($collect);

```


### <a name="create_https_api_rest_sh_api_vu"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVU") createHttpsApiRestShApiVU

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```php
function createHttpsApiRestShApiVU($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiVUModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $verification->createHttpsApiRestShApiVU($collect);

```


### <a name="get_https_api_rest_sh_api_v"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiV") getHttpsApiRestShApiV

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```php
function getHttpsApiRestShApiV($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$to = 'to';
$collect['to'] = $to;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $verification->getHttpsApiRestShApiV($collect);

```


### <a name="create_https_api_rest_sh_api_v"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiV") createHttpsApiRestShApiV

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```php
function createHttpsApiRestShApiV($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiVModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $verification->createHttpsApiRestShApiV($collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPIController") TwoFactorAuthenticationAPIController

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPIController ``` class can be accessed from the API Client.

```php
$twoFactorAuthenticationAPI = $client->getTwoFactorAuthenticationAPI();
```

### <a name="get_https_api_rest_sh_api2fa_t"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2faT") getHttpsApiRestShApi2faT

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```php
function getHttpsApiRestShApi2faT($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$user = 'user';
$collect['user'] = $user;

$code = 'code';
$collect['code'] = $code;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $twoFactorAuthenticationAPI->getHttpsApiRestShApi2faT($collect);

```


### <a name="create_https_api_rest_sh_api2fa_t"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2faT") createHttpsApiRestShApi2faT

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```php
function createHttpsApiRestShApi2faT($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApi2faTModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $twoFactorAuthenticationAPI->createHttpsApiRestShApi2faT($collect);

```


### <a name="get_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2fa") getHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```php
function getHttpsApiRestShApi2fa($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$to = 'to';
$collect['to'] = $to;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $twoFactorAuthenticationAPI->getHttpsApiRestShApi2fa($collect);

```


### <a name="create_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2fa") createHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```php
function createHttpsApiRestShApi2fa($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApi2faModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $twoFactorAuthenticationAPI->createHttpsApiRestShApi2fa($collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagementController") UserManagementController

### Get singleton instance

The singleton instance of the ``` UserManagementController ``` class can be accessed from the API Client.

```php
$userManagement = $client->getUserManagement();
```

### <a name="get_https_api_rest_sh_api_ui"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUI") getHttpsApiRestShApiUI

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```php
function getHttpsApiRestShApiUI($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$user = 'user';
$collect['user'] = $user;

$apiuid = 'apiuid';
$collect['apiuid'] = $apiuid;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $userManagement->getHttpsApiRestShApiUI($collect);

```


### <a name="create_https_api_rest_sh_api_ui"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUI") createHttpsApiRestShApiUI

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```php
function createHttpsApiRestShApiUI($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiUIModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $userManagement->createHttpsApiRestShApiUI($collect);

```


### <a name="get_https_api_rest_sh_api_uu"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUU") getHttpsApiRestShApiUU

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```php
function getHttpsApiRestShApiUU($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$user = 'user';
$collect['user'] = $user;

$apiuid = 'apiuid';
$collect['apiuid'] = $apiuid;

$avatar = 'avatar';
$collect['avatar'] = $avatar;

$customInput = 'custom input';
$collect['customInput'] = $customInput;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $userManagement->getHttpsApiRestShApiUU($collect);

```


### <a name="create_https_api_rest_sh_api_uu"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUU") createHttpsApiRestShApiUU

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```php
function createHttpsApiRestShApiUU($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiUUModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $userManagement->createHttpsApiRestShApiUU($collect);

```


### <a name="get_https_api_rest_sh_api_ud"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUD") getHttpsApiRestShApiUD

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```php
function getHttpsApiRestShApiUD($options)
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

```php
$api = 'api';
$collect['api'] = $api;

$uid = 'uid';
$collect['uid'] = $uid;

$user = 'user';
$collect['user'] = $user;

$apiuid = 'apiuid';
$collect['apiuid'] = $apiuid;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $userManagement->getHttpsApiRestShApiUD($collect);

```


### <a name="create_https_api_rest_sh_api_ud"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUD") createHttpsApiRestShApiUD

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```php
function createHttpsApiRestShApiUD($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiUDModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $userManagement->createHttpsApiRestShApiUD($collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration_controller"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistrationController") LoginAndRegistrationController

### Get singleton instance

The singleton instance of the ``` LoginAndRegistrationController ``` class can be accessed from the API Client.

```php
$loginAndRegistration = $client->getLoginAndRegistration();
```

### <a name="get_https_api_rest_sh_api_aur"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAUR") getHttpsApiRestShApiAUR

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```php
function getHttpsApiRestShApiAUR($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$user = 'user';
$collect['user'] = $user;

$password = 'password';
$collect['password'] = $password;

$name = 'name';
$collect['name'] = $name;

$email = 'email';
$collect['email'] = $email;

$phone = 84;
$collect['phone'] = $phone;

$countrycode = 84;
$collect['countrycode'] = $countrycode;

$address = 'address';
$collect['address'] = $address;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $loginAndRegistration->getHttpsApiRestShApiAUR($collect);

```


### <a name="create_https_api_rest_sh_api_aur"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAUR") createHttpsApiRestShApiAUR

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```php
function createHttpsApiRestShApiAUR($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiAURModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $loginAndRegistration->createHttpsApiRestShApiAUR($collect);

```


### <a name="get_https_api_rest_sh_api_aul"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAUL") getHttpsApiRestShApiAUL

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```php
function getHttpsApiRestShApiAUL($options)
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

```php
$key = 'key';
$collect['key'] = $key;

$uid = 'uid';
$collect['uid'] = $uid;

$user = 'user';
$collect['user'] = $user;

$password = 'password';
$collect['password'] = $password;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $loginAndRegistration->getHttpsApiRestShApiAUL($collect);

```


### <a name="create_https_api_rest_sh_api_aul"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAUL") createHttpsApiRestShApiAUL

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```php
function createHttpsApiRestShApiAUL($options)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiAULModel();
$collect['body'] = $body;

$contentType = 'Content-Type';
$collect['contentType'] = $contentType;


$result = $loginAndRegistration->createHttpsApiRestShApiAUL($collect);

```


[Back to List of Controllers](#list_of_controllers)



