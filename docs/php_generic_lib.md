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
| uid | Your user ID |
| secret | Your Private API Key |
| key | Your Public API Key |



API client can be initialized as following.

```php
$uid = 'UID'; // Your user ID
$secret = 'SECRET'; // Your Private API Key
$key = 'KEY'; // Your Public API Key

$client = new SMASHLib\SMASHClient($uid, $secret, $key);
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

```php
$advancedLogging = $client->getAdvancedLogging();
```

### <a name="logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingInfo") loggingInfo

> WAF Log Info


```php
function loggingInfo(
        $key,
        $uid,
        $name,
        $origin,
        $time,
        $contentType)
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
$uid = 'uid';
$name = 'name';
$origin = 'origin';
$time = 'time';
$contentType = 'Content-Type';

$result = $advancedLogging->loggingInfo($key, $uid, $name, $origin, $time, $contentType);

```


### <a name="logging_setup"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingSetup") loggingSetup

> WAF Log Setup


```php
function loggingSetup(
        $key,
        $uid,
        $name,
        $origin,
        $activate,
        $contentType)
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
$uid = 'uid';
$name = 'name';
$origin = 'origin';
$activate = true;
$contentType = 'Content-Type';

$result = $advancedLogging->loggingSetup($key, $uid, $name, $origin, $activate, $contentType);

```


### <a name="logging_info1"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingInfo1") loggingInfo1

> WAF Log Info


```php
function loggingInfo1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSLI();
$contentType = 'Content-Type';

$result = $advancedLogging->loggingInfo1($body, $contentType);

```


### <a name="logging_setup1"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingSetup1") loggingSetup1

> WAF Log Setup


```php
function loggingSetup1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSL();
$contentType = 'Content-Type';

$result = $advancedLogging->loggingSetup1($body, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtection") WAFDDOSProtection

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtection ``` class can be accessed from the API Client.

```php
$wAFDDOSProtection = $client->getWAFDDOSProtection();
```

### <a name="https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSWC") httpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```php
function httpsApiRestShApiSWC(
        $key,
        $uid,
        $name,
        $origin,
        $rule,
        $contentType)
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
$uid = 'UID';
$name = 'origin-name';
$origin = 'origin.yourdomain.tld';
$rule = 'header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does';
$contentType = 'application/json';

$result = $wAFDDOSProtection->httpsApiRestShApiSWC($key, $uid, $name, $origin, $rule, $contentType);

```


### <a name="https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSW") httpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```php
function httpsApiRestShApiSW(
        $key,
        $uid,
        $origin,
        $cname,
        $contentType)
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
$uid = 'UID';
$origin = 'origin.yourdomain.tld';
$cname = 'yourdomain.tld,www.yourdomain.tld';
$contentType = 'application/json';

$result = $wAFDDOSProtection->httpsApiRestShApiSW($key, $uid, $origin, $cname, $contentType);

```


### <a name="https_api_rest_sh_api_swc1"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSWC1") httpsApiRestShApiSWC1

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```php
function httpsApiRestShApiSWC1(
        $body,
        $contentType)
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
$contentType = 'application/json';

$result = $wAFDDOSProtection->httpsApiRestShApiSWC1($body, $contentType);

```


### <a name="https_api_rest_sh_api_sw1"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSW1") httpsApiRestShApiSW1

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```php
function httpsApiRestShApiSW1(
        $body,
        $contentType)
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
$contentType = 'application/json';

$result = $wAFDDOSProtection->httpsApiRestShApiSW1($body, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption"></a>![Class: ](https://apidocs.io/img/class.png ".Encryption") Encryption

### Get singleton instance

The singleton instance of the ``` Encryption ``` class can be accessed from the API Client.

```php
$encryption = $client->getEncryption();
```

### <a name="data_and_file_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.dataAndFileEncryption") dataAndFileEncryption

> Data and File Encryption API


```php
function dataAndFileEncryption(
        $key,
        $uid,
        $data,
        $method,
        $bit,
        $contentType)
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
$uid = 'uid';
$data = 'data';
$method = 'method';
$bit = 25;
$contentType = 'Content-Type';

$result = $encryption->dataAndFileEncryption($key, $uid, $data, $method, $bit, $contentType);

```


### <a name="data_and_file_encryption1"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.dataAndFileEncryption1") dataAndFileEncryption1

> Data and File Encryption API


```php
function dataAndFileEncryption1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSE();
$contentType = 'Content-Type';

$result = $encryption->dataAndFileEncryption1($body, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn"></a>![Class: ](https://apidocs.io/img/class.png ".CDN") CDN

### Get singleton instance

The singleton instance of the ``` CDN ``` class can be accessed from the API Client.

```php
$cDN = $client->getCDN();
```

### <a name="c_dn_push_zone"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPushZone") cDNPushZone

> CDN Push Zone API


```php
function cDNPushZone(
        $key,
        $uid,
        $cname,
        $file,
        $contentType)
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
$uid = 'uid';
$cname = 'cname';
$file = 'file';
$contentType = 'Content-Type';

$result = $cDN->cDNPushZone($key, $uid, $cname, $file, $contentType);

```


### <a name="c_dn_pull_zone"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPullZone") cDNPullZone

> CDN Pull Zone API


```php
function cDNPullZone(
        $key,
        $uid,
        $origin,
        $cname,
        $contentType)
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
$uid = 'uid';
$origin = 'origin';
$cname = 'cname';
$contentType = 'Content-Type';

$result = $cDN->cDNPullZone($key, $uid, $origin, $cname, $contentType);

```


### <a name="c_dn_push_zone1"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPushZone1") cDNPushZone1

> CDN Push Zone API


```php
function cDNPushZone1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSCPush();
$contentType = 'Content-Type';

$result = $cDN->cDNPushZone1($body, $contentType);

```


### <a name="c_dn_pull_zone1"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPullZone1") cDNPullZone1

> CDN Pull Zone API


```php
function cDNPullZone1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSCPull();
$contentType = 'Content-Type';

$result = $cDN->cDNPullZone1($body, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns"></a>![Class: ](https://apidocs.io/img/class.png ".DNS") DNS

### Get singleton instance

The singleton instance of the ``` DNS ``` class can be accessed from the API Client.

```php
$dNS = $client->getDNS();
```

### <a name="d_ns_configuration"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSConfiguration") dNSConfiguration

> DNS Configuration API


```php
function dNSConfiguration(
        $key,
        $uid,
        $domain,
        $records,
        $contentType)
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
$uid = 'uid';
$domain = 'domain';
$records = 'records';
$contentType = 'Content-Type';

$result = $dNS->dNSConfiguration($key, $uid, $domain, $records, $contentType);

```


### <a name="d_ns_configuration1"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSConfiguration1") dNSConfiguration1

> DNS Configuration API


```php
function dNSConfiguration1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSDC();
$contentType = 'Content-Type';

$result = $dNS->dNSConfiguration1($body, $contentType);

```


### <a name="d_ns_creation"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSCreation") dNSCreation

> DNS Creation API


```php
function dNSCreation(
        $key,
        $uid,
        $domain,
        $contentType)
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
$uid = 'uid';
$domain = 'domain';
$contentType = 'Content-Type';

$result = $dNS->dNSCreation($key, $uid, $domain, $contentType);

```


### <a name="d_ns_creation1"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSCreation1") dNSCreation1

> DNS Creation API


```php
function dNSCreation1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSDA();
$contentType = 'Content-Type';

$result = $dNS->dNSCreation1($body, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscation") CodeObfuscation

### Get singleton instance

The singleton instance of the ``` CodeObfuscation ``` class can be accessed from the API Client.

```php
$codeObfuscation = $client->getCodeObfuscation();
```

### <a name="obfuscation_and_anti_tampering"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.obfuscationAndAntiTampering") obfuscationAndAntiTampering

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```php
function obfuscationAndAntiTampering(
        $key,
        $uid,
        $app,
        $contentType)
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
$uid = 'uid';
$app = 'app';
$contentType = 'Content-Type';

$result = $codeObfuscation->obfuscationAndAntiTampering($key, $uid, $app, $contentType);

```


### <a name="obfuscation_and_anti_tampering1"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.obfuscationAndAntiTampering1") obfuscationAndAntiTampering1

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```php
function obfuscationAndAntiTampering1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSO();
$contentType = 'Content-Type';

$result = $codeObfuscation->obfuscationAndAntiTampering1($body, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting"></a>![Class: ](https://apidocs.io/img/class.png ".Hosting") Hosting

### Get singleton instance

The singleton instance of the ``` Hosting ``` class can be accessed from the API Client.

```php
$hosting = $client->getHosting();
```

### <a name="hosting_setup"></a>![Method: ](https://apidocs.io/img/method.png ".Hosting.hostingSetup") hostingSetup

> Node.JS and Static Web APP Hosting


```php
function hostingSetup(
        $key,
        $uid,
        $app,
        $domain,
        $contentType)
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
$uid = 'uid';
$app = 'app';
$domain = 'domain';
$contentType = 'Content-Type';

$result = $hosting->hostingSetup($key, $uid, $app, $domain, $contentType);

```


### <a name="hosting_setup1"></a>![Method: ](https://apidocs.io/img/method.png ".Hosting.hostingSetup1") hostingSetup1

> Node.JS and Static Web APP Hosting


```php
function hostingSetup1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiSH();
$contentType = 'Content-Type';

$result = $hosting->hostingSetup1($body, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPI") DataManipulationConversionSortingAndCompressionAPI

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPI ``` class can be accessed from the API Client.

```php
$dataManipulationConversionSortingAndCompressionAPI = $client->getDataManipulationConversionSortingAndCompressionAPI();
```

### <a name="https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiD") httpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```php
function httpsApiRestShApiD(
        $key,
        $uid,
        $user,
        $apiuid,
        $data,
        $contentType)
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
$uid = 'UID';
$user = 'UID';
$apiuid = 'apiUID';
$data = 'https://static.yourcdn.com/data.file';
$contentType = 'application/json';

$result = $dataManipulationConversionSortingAndCompressionAPI->httpsApiRestShApiD($key, $uid, $user, $apiuid, $data, $contentType);

```


### <a name="https_api_rest_sh_api_d1"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiD1") httpsApiRestShApiD1

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```php
function httpsApiRestShApiD1(
        $body,
        $contentType)
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
$contentType = 'application/json';

$result = $dataManipulationConversionSortingAndCompressionAPI->httpsApiRestShApiD1($body, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPI") ImageManipulationAndModerationAPI

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPI ``` class can be accessed from the API Client.

```php
$imageManipulationAndModerationAPI = $client->getImageManipulationAndModerationAPI();
```

### <a name="image_manipulation"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPI.imageManipulation") imageManipulation

> Image Manipulation API


```php
function imageManipulation(
        $key,
        $uid,
        $image,
        $transform,
        $contentType)
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
$uid = 'uid';
$image = 'image';
$transform = 'transform';
$contentType = 'Content-Type';

$result = $imageManipulationAndModerationAPI->imageManipulation($key, $uid, $image, $transform, $contentType);

```


### <a name="image_manipulation1"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPI.imageManipulation1") imageManipulation1

> Image Manipulation API


```php
function imageManipulation1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiI();
$contentType = 'Content-Type';

$result = $imageManipulationAndModerationAPI->imageManipulation1($body, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification"></a>![Class: ](https://apidocs.io/img/class.png ".Verification") Verification

### Get singleton instance

The singleton instance of the ``` Verification ``` class can be accessed from the API Client.

```php
$verification = $client->getVerification();
```

### <a name="user_address_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userAddressVerification") userAddressVerification

> User Address Verification API


```php
function userAddressVerification(
        $key,
        $uid,
        $user,
        $a,
        $sa,
        $c,
        $s,
        $z,
        $contentType)
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
$uid = 'uid';
$user = 'user';
$a = 'a';
$sa = 'sa';
$c = 'c';
$s = 's';
$z = 25;
$contentType = 'Content-Type';

$result = $verification->userAddressVerification($key, $uid, $user, $a, $sa, $c, $s, $z, $contentType);

```


### <a name="user_address_verification1"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userAddressVerification1") userAddressVerification1

> User Address Verification API


```php
function userAddressVerification1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiVA();
$contentType = 'Content-Type';

$result = $verification->userAddressVerification1($body, $contentType);

```


### <a name="user_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userVerification") userVerification

> User Verification API


```php
function userVerification(
        $key,
        $uid,
        $user,
        $code,
        $contentType)
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
$uid = 'uid';
$user = 'user';
$code = 'code';
$contentType = 'Content-Type';

$result = $verification->userVerification($key, $uid, $user, $code, $contentType);

```


### <a name="user_verification1"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userVerification1") userVerification1

> User Verification API


```php
function userVerification1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiVU();
$contentType = 'Content-Type';

$result = $verification->userVerification1($body, $contentType);

```


### <a name="cellphone_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.cellphoneVerification") cellphoneVerification

> Verification API


```php
function cellphoneVerification(
        $key,
        $uid,
        $to,
        $contentType)
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
$uid = 'uid';
$to = 'to';
$contentType = 'Content-Type';

$result = $verification->cellphoneVerification($key, $uid, $to, $contentType);

```


### <a name="cellphone_verification1"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.cellphoneVerification1") cellphoneVerification1

> Verification API


```php
function cellphoneVerification1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiV();
$contentType = 'Content-Type';

$result = $verification->cellphoneVerification1($body, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPI") TwoFactorAuthenticationAPI

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPI ``` class can be accessed from the API Client.

```php
$twoFactorAuthenticationAPI = $client->getTwoFactorAuthenticationAPI();
```

### <a name="m2_fa_token_response"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.m2FATokenResponse") m2FATokenResponse

> Two Factor Authentication Token Reply


```php
function m2FATokenResponse(
        $key,
        $uid,
        $user,
        $code,
        $contentType)
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
$uid = 'uid';
$user = 'user';
$code = 'code';
$contentType = 'Content-Type';

$result = $twoFactorAuthenticationAPI->m2FATokenResponse($key, $uid, $user, $code, $contentType);

```


### <a name="m2_fa_token_response1"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.m2FATokenResponse1") m2FATokenResponse1

> Two Factor Authentication Token Reply


```php
function m2FATokenResponse1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApi2faT();
$contentType = 'Content-Type';

$result = $twoFactorAuthenticationAPI->m2FATokenResponse1($body, $contentType);

```


### <a name="two_factor_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.twoFactorAuthentication") twoFactorAuthentication

> Two Factor Authentication API


```php
function twoFactorAuthentication(
        $key,
        $uid,
        $to,
        $contentType)
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
$uid = 'uid';
$to = 'to';
$contentType = 'Content-Type';

$result = $twoFactorAuthenticationAPI->twoFactorAuthentication($key, $uid, $to, $contentType);

```


### <a name="two_factor_authentication1"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.twoFactorAuthentication1") twoFactorAuthentication1

> Two Factor Authentication API


```php
function twoFactorAuthentication1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApi2fa();
$contentType = 'Content-Type';

$result = $twoFactorAuthenticationAPI->twoFactorAuthentication1($body, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagement") UserManagement

### Get singleton instance

The singleton instance of the ``` UserManagement ``` class can be accessed from the API Client.

```php
$userManagement = $client->getUserManagement();
```

### <a name="get_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.getUserInfo") getUserInfo

> Get User Info API


```php
function getUserInfo(
        $key,
        $uid,
        $user,
        $apiuid,
        $contentType)
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
$uid = 'uid';
$user = 'user';
$apiuid = 'apiuid';
$contentType = 'Content-Type';

$result = $userManagement->getUserInfo($key, $uid, $user, $apiuid, $contentType);

```


### <a name="get_user_info1"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.getUserInfo1") getUserInfo1

> Get User Info API


```php
function getUserInfo1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiUI();
$contentType = 'Content-Type';

$result = $userManagement->getUserInfo1($body, $contentType);

```


### <a name="update_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.updateUser") updateUser

> Update User API


```php
function updateUser(
        $key,
        $uid,
        $user,
        $apiuid,
        $avatar,
        $customInput,
        $contentType)
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
$uid = 'uid';
$user = 'user';
$apiuid = 'apiuid';
$avatar = 'avatar';
$customInput = 'custom input';
$contentType = 'Content-Type';

$result = $userManagement->updateUser($key, $uid, $user, $apiuid, $avatar, $customInput, $contentType);

```


### <a name="update_user1"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.updateUser1") updateUser1

> Update User API


```php
function updateUser1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiUU();
$contentType = 'Content-Type';

$result = $userManagement->updateUser1($body, $contentType);

```


### <a name="delete_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.deleteUser") deleteUser

> Delete User API


```php
function deleteUser(
        $api,
        $uid,
        $user,
        $apiuid,
        $contentType)
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
$uid = 'uid';
$user = 'user';
$apiuid = 'apiuid';
$contentType = 'Content-Type';

$result = $userManagement->deleteUser($api, $uid, $user, $apiuid, $contentType);

```


### <a name="delete_user1"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.deleteUser1") deleteUser1

> Delete User API


```php
function deleteUser1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiUD();
$contentType = 'Content-Type';

$result = $userManagement->deleteUser1($body, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistration") LoginAndRegistration

### Get singleton instance

The singleton instance of the ``` LoginAndRegistration ``` class can be accessed from the API Client.

```php
$loginAndRegistration = $client->getLoginAndRegistration();
```

### <a name="user_registration"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userRegistration") userRegistration

> User Registration API


```php
function userRegistration(
        $key,
        $uid,
        $user,
        $password,
        $name,
        $email,
        $phone,
        $countrycode,
        $address,
        $contentType)
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
$uid = 'uid';
$user = 'user';
$password = 'password';
$name = 'name';
$email = 'email';
$phone = 117;
$countrycode = 117;
$address = 'address';
$contentType = 'Content-Type';

$result = $loginAndRegistration->userRegistration($key, $uid, $user, $password, $name, $email, $phone, $countrycode, $address, $contentType);

```


### <a name="user_registration1"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userRegistration1") userRegistration1

> User Registration API


```php
function userRegistration1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiAUR();
$contentType = 'Content-Type';

$result = $loginAndRegistration->userRegistration1($body, $contentType);

```


### <a name="user_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userAuthentication") userAuthentication

> User Authentication API


```php
function userAuthentication(
        $key,
        $uid,
        $user,
        $password,
        $contentType)
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
$uid = 'uid';
$user = 'user';
$password = 'password';
$contentType = 'Content-Type';

$result = $loginAndRegistration->userAuthentication($key, $uid, $user, $password, $contentType);

```


### <a name="user_authentication1"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userAuthentication1") userAuthentication1

> User Authentication API


```php
function userAuthentication1(
        $body,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new HttpsApiRestShApiAUL();
$contentType = 'Content-Type';

$result = $loginAndRegistration->userAuthentication1($body, $contentType);

```


[Back to List of Controllers](#list_of_controllers)



