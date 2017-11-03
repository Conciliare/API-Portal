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

This client library is a Ruby gem which can be compiled and used in your Ruby and Ruby on Rails project. This library requires a few gems from the RubyGems repository.

1. Open the command line interface or the terminal and navigate to the folder containing the source code.
2. Run ``` gem build smash.gemspec ``` to build the gem.
3. Once built, the gem can be installed on the current work environment using ``` gem install smash-1.2.0.gem ```

![Building Gem](https://apidocs.io/illustration/ruby?step=buildSDK&workspaceFolder=SMASH-Ruby&workspaceName=SMASH-Ruby&projectName=smash&gemName=smash&gemVer=1.2.0)

## How to Use

The following section explains how to use the SMASH Ruby Gem in a new Rails project using RubyMine&trade;. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

### 1. Starting a new project

Close any existing projects in RubyMine&trade; by selecting ``` File -> Close Project ```. Next, click on ``` Create New Project ``` to create a new project from scratch.

![Create a new project in RubyMine](https://apidocs.io/illustration/ruby?step=createNewProject0&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.2.0)

Next, provide ``` TestApp ``` as the project name, choose ``` Rails Application ``` as the project type, and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 1](https://apidocs.io/illustration/ruby?step=createNewProject1&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.2.0)

In the next dialog make sure that correct *Ruby SDK* is being used (minimum 2.0.0) and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 2](https://apidocs.io/illustration/ruby?step=createNewProject2&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.2.0)

This will create a new Rails Application project with an existing set of files and folder.

### 2. Add reference of the gem

In order to use the SMASH gem in the new project we must add a gem reference. Locate the ```Gemfile``` in the *Project Explorer* window under the ``` TestApp ``` project node. The file contains references to all gems being used in the project. Here, add the reference to the library gem by adding the following line: ``` gem 'smash', '~> 1.2.0' ```

![Add references of the Gemfile](https://apidocs.io/illustration/ruby?step=addReference&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.2.0)

### 3. Adding a new Rails Controller

Once the ``` TestApp ``` project is created, a folder named ``` controllers ``` will be visible in the *Project Explorer* under the following path: ``` TestApp > app > controllers ```. Right click on this folder and select ``` New -> Run Rails Generator... ```.

![Run Rails Generator on Controllers Folder](https://apidocs.io/illustration/ruby?step=addCode0&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.2.0)

Selecting the said option will popup a small window where the generator names are displayed. Here, select the ``` controller ``` template.

![Create a new Controller](https://apidocs.io/illustration/ruby?step=addCode1&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.2.0)

Next, a popup window will ask you for a Controller name and included Actions. For controller name provide ``` Hello ``` and include an action named ``` Index ``` and click ``` OK ```.

![Add a new Controller](https://apidocs.io/illustration/ruby?step=addCode2&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.2.0)

A new controller class anmed ``` HelloController ``` will be created in a file named ``` hello_controller.rb ``` containing a method named ``` Index ```. In this method, add code for initialization and a sample for its usage.

![Initialize the library](https://apidocs.io/illustration/ruby?step=addCode3&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.2.0)

## How to Test

You can test the generated SDK and the server with automatically generated test
cases as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke: `bundle exec rake`

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| key | Your API Key |
| uid | Your User ID |



API client can be initialized as following.

```ruby
# Configuration parameters and credentials
key = 'API' # Your API Key
uid = 'UID' # Your User ID

client = Smash::SMASH.new(
  key: key,
  uid: uid
)
```

The added initlization code can be debugged by putting a breakpoint in the ``` Index ``` method and running the project in debug mode by selecting ``` Run -> Debug 'Development: TestApp' ```.

![Debug the TestApp](https://apidocs.io/illustration/ruby?step=addCode4&workspaceFolder=SMASH%20-%20API-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.2.0&initLine=client%2520%253D%2520SMASH.new%2528%2527key%2527%252C%2520%2527uid%2527%2529)



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

```ruby
advancedLogging = client.advanced_logging
```

### <a name="get_https_api_rest_sh_api_security_logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.get_https_api_rest_sh_api_security_logging_info") get_https_api_rest_sh_api_security_logging_info

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```ruby
def get_https_api_rest_sh_api_security_logging_info(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| name |  ``` Required ```  | TODO: Add a parameter description |
| origin |  ``` Required ```  | TODO: Add a parameter description |
| time |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

name = 'name'
collect['name'] = name

origin = 'origin'
collect['origin'] = origin

time = 'time'
collect['time'] = time

content_type = 'Content-Type'
collect['content_type'] = content_type


result = advancedLogging.get_https_api_rest_sh_api_security_logging_info(collect)

```


### <a name="get_https_api_rest_sh_api_security_logging"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.get_https_api_rest_sh_api_security_logging") get_https_api_rest_sh_api_security_logging

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```ruby
def get_https_api_rest_sh_api_security_logging(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| name |  ``` Required ```  | TODO: Add a parameter description |
| origin |  ``` Required ```  | TODO: Add a parameter description |
| activate |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

name = 'name'
collect['name'] = name

origin = 'origin'
collect['origin'] = origin

activate = true
collect['activate'] = activate

content_type = 'Content-Type'
collect['content_type'] = content_type


result = advancedLogging.get_https_api_rest_sh_api_security_logging(collect)

```


### <a name="create_https_api_rest_sh_api_security_logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.create_https_api_rest_sh_api_security_logging_info") create_https_api_rest_sh_api_security_logging_info

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```ruby
def create_https_api_rest_sh_api_security_logging_info(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiSecurityLoggingInfoRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = advancedLogging.create_https_api_rest_sh_api_security_logging_info(collect)

```


### <a name="create_https_api_rest_sh_api_security_logging"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.create_https_api_rest_sh_api_security_logging") create_https_api_rest_sh_api_security_logging

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```ruby
def create_https_api_rest_sh_api_security_logging(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiSecurityLoggingRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = advancedLogging.create_https_api_rest_sh_api_security_logging(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection_controller"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtectionController") WAFDDOSProtectionController

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtectionController ``` class can be accessed from the API Client.

```ruby
wAFDDOSProtection = client.wafddos_protection
```

### <a name="get_https_api_rest_sh_api_security_waf_configure"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.get_https_api_rest_sh_api_security_waf_configure") get_https_api_rest_sh_api_security_waf_configure

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```ruby
def get_https_api_rest_sh_api_security_waf_configure(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| name |  ``` Required ```  | TODO: Add a parameter description |
| origin |  ``` Required ```  | TODO: Add a parameter description |
| rule |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'API'
collect['key'] = key

uid = 'UID'
collect['uid'] = uid

name = 'origin-name'
collect['name'] = name

origin = 'origin.yourdomain.tld'
collect['origin'] = origin

rule = 'header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does'
collect['rule'] = rule

content_type = 'application/json'
collect['content_type'] = content_type


result = wAFDDOSProtection.get_https_api_rest_sh_api_security_waf_configure(collect)

```


### <a name="get_https_api_rest_sh_api_security_waf"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.get_https_api_rest_sh_api_security_waf") get_https_api_rest_sh_api_security_waf

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```ruby
def get_https_api_rest_sh_api_security_waf(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| origin |  ``` Required ```  | TODO: Add a parameter description |
| cname |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'API'
collect['key'] = key

uid = 'UID'
collect['uid'] = uid

origin = 'origin.yourdomain.tld'
collect['origin'] = origin

cname = 'yourdomain.tld,www.yourdomain.tld'
collect['cname'] = cname

content_type = 'application/json'
collect['content_type'] = content_type


result = wAFDDOSProtection.get_https_api_rest_sh_api_security_waf(collect)

```


### <a name="create_https_api_rest_sh_api_security_waf_configure"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.create_https_api_rest_sh_api_security_waf_configure") create_https_api_rest_sh_api_security_waf_configure

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```ruby
def create_https_api_rest_sh_api_security_waf_configure(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body_value = "{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}";
body = JSON.parse(body_value);
collect['body'] = body

content_type = 'application/json'
collect['content_type'] = content_type


result = wAFDDOSProtection.create_https_api_rest_sh_api_security_waf_configure(collect)

```


### <a name="create_https_api_rest_sh_api_security_waf"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.create_https_api_rest_sh_api_security_waf") create_https_api_rest_sh_api_security_waf

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```ruby
def create_https_api_rest_sh_api_security_waf(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body_value = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}";
body = JSON.parse(body_value);
collect['body'] = body

content_type = 'application/json'
collect['content_type'] = content_type


result = wAFDDOSProtection.create_https_api_rest_sh_api_security_waf(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EncryptionController") EncryptionController

### Get singleton instance

The singleton instance of the ``` EncryptionController ``` class can be accessed from the API Client.

```ruby
encryption = client.encryption
```

### <a name="get_https_api_rest_sh_api_security_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.get_https_api_rest_sh_api_security_encryption") get_https_api_rest_sh_api_security_encryption

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```ruby
def get_https_api_rest_sh_api_security_encryption(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| data |  ``` Required ```  | TODO: Add a parameter description |
| method |  ``` Required ```  | TODO: Add a parameter description |
| bit |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

data = 'data'
collect['data'] = data

method = 'method'
collect['method'] = method

bit = 206
collect['bit'] = bit

content_type = 'Content-Type'
collect['content_type'] = content_type


result = encryption.get_https_api_rest_sh_api_security_encryption(collect)

```


### <a name="create_https_api_rest_sh_api_security_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.create_https_api_rest_sh_api_security_encryption") create_https_api_rest_sh_api_security_encryption

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```ruby
def create_https_api_rest_sh_api_security_encryption(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiSecurityEncryptionRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = encryption.create_https_api_rest_sh_api_security_encryption(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CDNController") CDNController

### Get singleton instance

The singleton instance of the ``` CDNController ``` class can be accessed from the API Client.

```ruby
cDN = client.cdn
```

### <a name="get_https_api_rest_sh_api_service_cdn_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.get_https_api_rest_sh_api_service_cdn_push") get_https_api_rest_sh_api_service_cdn_push

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```ruby
def get_https_api_rest_sh_api_service_cdn_push(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| cname |  ``` Required ```  | TODO: Add a parameter description |
| file |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

cname = 'cname'
collect['cname'] = cname

file = 'file'
collect['file'] = file

content_type = 'Content-Type'
collect['content_type'] = content_type


result = cDN.get_https_api_rest_sh_api_service_cdn_push(collect)

```


### <a name="get_https_api_rest_sh_api_service_cdn_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.get_https_api_rest_sh_api_service_cdn_pull") get_https_api_rest_sh_api_service_cdn_pull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```ruby
def get_https_api_rest_sh_api_service_cdn_pull(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| origin |  ``` Required ```  | TODO: Add a parameter description |
| cname |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

origin = 'origin'
collect['origin'] = origin

cname = 'cname'
collect['cname'] = cname

content_type = 'Content-Type'
collect['content_type'] = content_type


result = cDN.get_https_api_rest_sh_api_service_cdn_pull(collect)

```


### <a name="create_https_api_rest_sh_api_service_cdn_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.create_https_api_rest_sh_api_service_cdn_push") create_https_api_rest_sh_api_service_cdn_push

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```ruby
def create_https_api_rest_sh_api_service_cdn_push(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiServiceCdnPushRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = cDN.create_https_api_rest_sh_api_service_cdn_push(collect)

```


### <a name="create_https_api_rest_sh_api_service_cdn_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.create_https_api_rest_sh_api_service_cdn_pull") create_https_api_rest_sh_api_service_cdn_pull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```ruby
def create_https_api_rest_sh_api_service_cdn_pull(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiServiceCdnPullRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = cDN.create_https_api_rest_sh_api_service_cdn_pull(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DNSController") DNSController

### Get singleton instance

The singleton instance of the ``` DNSController ``` class can be accessed from the API Client.

```ruby
dNS = client.dns
```

### <a name="get_https_api_rest_sh_api_service_dns_configure"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.get_https_api_rest_sh_api_service_dns_configure") get_https_api_rest_sh_api_service_dns_configure

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```ruby
def get_https_api_rest_sh_api_service_dns_configure(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| domain |  ``` Required ```  | TODO: Add a parameter description |
| records |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

domain = 'domain'
collect['domain'] = domain

records = 'records'
collect['records'] = records

content_type = 'Content-Type'
collect['content_type'] = content_type


result = dNS.get_https_api_rest_sh_api_service_dns_configure(collect)

```


### <a name="create_https_api_rest_sh_api_service_dns_configure"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.create_https_api_rest_sh_api_service_dns_configure") create_https_api_rest_sh_api_service_dns_configure

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```ruby
def create_https_api_rest_sh_api_service_dns_configure(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiServiceDnsConfigureRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = dNS.create_https_api_rest_sh_api_service_dns_configure(collect)

```


### <a name="get_https_api_rest_sh_api_service_dns_add"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.get_https_api_rest_sh_api_service_dns_add") get_https_api_rest_sh_api_service_dns_add

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```ruby
def get_https_api_rest_sh_api_service_dns_add(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| domain |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

domain = 'domain'
collect['domain'] = domain

content_type = 'Content-Type'
collect['content_type'] = content_type


result = dNS.get_https_api_rest_sh_api_service_dns_add(collect)

```


### <a name="create_https_api_rest_sh_api_service_dns_add"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.create_https_api_rest_sh_api_service_dns_add") create_https_api_rest_sh_api_service_dns_add

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```ruby
def create_https_api_rest_sh_api_service_dns_add(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiServiceDnsAddRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = dNS.create_https_api_rest_sh_api_service_dns_add(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscationController") CodeObfuscationController

### Get singleton instance

The singleton instance of the ``` CodeObfuscationController ``` class can be accessed from the API Client.

```ruby
codeObfuscation = client.code_obfuscation
```

### <a name="get_https_api_rest_sh_api_service_obfuscation"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.get_https_api_rest_sh_api_service_obfuscation") get_https_api_rest_sh_api_service_obfuscation

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```ruby
def get_https_api_rest_sh_api_service_obfuscation(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| app |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

app = 'app'
collect['app'] = app

content_type = 'Content-Type'
collect['content_type'] = content_type


result = codeObfuscation.get_https_api_rest_sh_api_service_obfuscation(collect)

```


### <a name="create_https_api_rest_sh_api_service_obfuscation"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.create_https_api_rest_sh_api_service_obfuscation") create_https_api_rest_sh_api_service_obfuscation

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```ruby
def create_https_api_rest_sh_api_service_obfuscation(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiServiceObfuscationRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = codeObfuscation.create_https_api_rest_sh_api_service_obfuscation(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting_controller"></a>![Class: ](https://apidocs.io/img/class.png ".HostingController") HostingController

### Get singleton instance

The singleton instance of the ``` HostingController ``` class can be accessed from the API Client.

```ruby
hosting = client.hosting
```

### <a name="get_https_api_rest_sh_api_service_hosting"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.get_https_api_rest_sh_api_service_hosting") get_https_api_rest_sh_api_service_hosting

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```ruby
def get_https_api_rest_sh_api_service_hosting(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| app |  ``` Required ```  | TODO: Add a parameter description |
| domain |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

app = 'app'
collect['app'] = app

domain = 'domain'
collect['domain'] = domain

content_type = 'Content-Type'
collect['content_type'] = content_type


result = hosting.get_https_api_rest_sh_api_service_hosting(collect)

```


### <a name="create_https_api_rest_sh_api_service_hosting"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.create_https_api_rest_sh_api_service_hosting") create_https_api_rest_sh_api_service_hosting

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```ruby
def create_https_api_rest_sh_api_service_hosting(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiServiceHostingRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = hosting.create_https_api_rest_sh_api_service_hosting(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPIController") DataManipulationConversionSortingAndCompressionAPIController

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPIController ``` class can be accessed from the API Client.

```ruby
dataManipulationConversionSortingAndCompressionAPI = client.data_manipulation_conversion_sorting_and_compression_api
```

### <a name="get_https_api_rest_sh_api_data"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.get_https_api_rest_sh_api_data") get_https_api_rest_sh_api_data

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```ruby
def get_https_api_rest_sh_api_data(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| apiuid |  ``` Required ```  | TODO: Add a parameter description |
| data |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'API'
collect['key'] = key

uid = 'UID'
collect['uid'] = uid

user = 'UID'
collect['user'] = user

apiuid = 'apiUID'
collect['apiuid'] = apiuid

data = 'https://static.yourcdn.com/data.file'
collect['data'] = data

content_type = 'application/json'
collect['content_type'] = content_type


result = dataManipulationConversionSortingAndCompressionAPI.get_https_api_rest_sh_api_data(collect)

```


### <a name="create_https_api_rest_sh_api_data"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.create_https_api_rest_sh_api_data") create_https_api_rest_sh_api_data

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```ruby
def create_https_api_rest_sh_api_data(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body_value = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}";
body = JSON.parse(body_value);
collect['body'] = body

content_type = 'application/json'
collect['content_type'] = content_type


result = dataManipulationConversionSortingAndCompressionAPI.create_https_api_rest_sh_api_data(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPIController") ImageManipulationAndModerationAPIController

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPIController ``` class can be accessed from the API Client.

```ruby
imageManipulationAndModerationAPI = client.image_manipulation_and_moderation_api
```

### <a name="get_https_api_rest_sh_api_image"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.get_https_api_rest_sh_api_image") get_https_api_rest_sh_api_image

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```ruby
def get_https_api_rest_sh_api_image(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| image |  ``` Required ```  | TODO: Add a parameter description |
| transform |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

image = 'image'
collect['image'] = image

transform = 'transform'
collect['transform'] = transform

content_type = 'Content-Type'
collect['content_type'] = content_type


result = imageManipulationAndModerationAPI.get_https_api_rest_sh_api_image(collect)

```


### <a name="create_https_api_rest_sh_api_image"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.create_https_api_rest_sh_api_image") create_https_api_rest_sh_api_image

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```ruby
def create_https_api_rest_sh_api_image(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiImageRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = imageManipulationAndModerationAPI.create_https_api_rest_sh_api_image(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VerificationController") VerificationController

### Get singleton instance

The singleton instance of the ``` VerificationController ``` class can be accessed from the API Client.

```ruby
verification = client.verification
```

### <a name="get_https_api_rest_sh_api_verify_address"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.get_https_api_rest_sh_api_verify_address") get_https_api_rest_sh_api_verify_address

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```ruby
def get_https_api_rest_sh_api_verify_address(options = {}); end
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
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

user = 'user'
collect['user'] = user

a = 'a'
collect['a'] = a

sa = 'sa'
collect['sa'] = sa

c = 'c'
collect['c'] = c

s = 's'
collect['s'] = s

z = 42
collect['z'] = z

content_type = 'Content-Type'
collect['content_type'] = content_type


result = verification.get_https_api_rest_sh_api_verify_address(collect)

```


### <a name="create_https_api_rest_sh_api_verify_address"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.create_https_api_rest_sh_api_verify_address") create_https_api_rest_sh_api_verify_address

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```ruby
def create_https_api_rest_sh_api_verify_address(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiVerifyAddressRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = verification.create_https_api_rest_sh_api_verify_address(collect)

```


### <a name="get_https_api_rest_sh_api_verify_user"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.get_https_api_rest_sh_api_verify_user") get_https_api_rest_sh_api_verify_user

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```ruby
def get_https_api_rest_sh_api_verify_user(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| code |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

user = 'user'
collect['user'] = user

code = 'code'
collect['code'] = code

content_type = 'Content-Type'
collect['content_type'] = content_type


result = verification.get_https_api_rest_sh_api_verify_user(collect)

```


### <a name="create_https_api_rest_sh_api_verify_user"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.create_https_api_rest_sh_api_verify_user") create_https_api_rest_sh_api_verify_user

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```ruby
def create_https_api_rest_sh_api_verify_user(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiVerifyUserRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = verification.create_https_api_rest_sh_api_verify_user(collect)

```


### <a name="get_https_api_rest_sh_api_verify"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.get_https_api_rest_sh_api_verify") get_https_api_rest_sh_api_verify

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```ruby
def get_https_api_rest_sh_api_verify(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

to = 'to'
collect['to'] = to

content_type = 'Content-Type'
collect['content_type'] = content_type


result = verification.get_https_api_rest_sh_api_verify(collect)

```


### <a name="create_https_api_rest_sh_api_verify"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.create_https_api_rest_sh_api_verify") create_https_api_rest_sh_api_verify

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```ruby
def create_https_api_rest_sh_api_verify(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiVerifyRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = verification.create_https_api_rest_sh_api_verify(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPIController") TwoFactorAuthenticationAPIController

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPIController ``` class can be accessed from the API Client.

```ruby
twoFactorAuthenticationAPI = client.two_factor_authentication_api
```

### <a name="get_https_api_rest_sh_api_2_fa_token"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.get_https_api_rest_sh_api_2_fa_token") get_https_api_rest_sh_api_2_fa_token

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```ruby
def get_https_api_rest_sh_api_2_fa_token(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| code |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

user = 'user'
collect['user'] = user

code = 'code'
collect['code'] = code

content_type = 'Content-Type'
collect['content_type'] = content_type


result = twoFactorAuthenticationAPI.get_https_api_rest_sh_api_2_fa_token(collect)

```


### <a name="create_https_api_rest_sh_api_2_fa_token"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.create_https_api_rest_sh_api_2_fa_token") create_https_api_rest_sh_api_2_fa_token

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```ruby
def create_https_api_rest_sh_api_2_fa_token(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApi2faTokenRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = twoFactorAuthenticationAPI.create_https_api_rest_sh_api_2_fa_token(collect)

```


### <a name="get_https_api_rest_sh_api_2_fa"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.get_https_api_rest_sh_api_2_fa") get_https_api_rest_sh_api_2_fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```ruby
def get_https_api_rest_sh_api_2_fa(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

to = 'to'
collect['to'] = to

content_type = 'Content-Type'
collect['content_type'] = content_type


result = twoFactorAuthenticationAPI.get_https_api_rest_sh_api_2_fa(collect)

```


### <a name="create_https_api_rest_sh_api_2_fa"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.create_https_api_rest_sh_api_2_fa") create_https_api_rest_sh_api_2_fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```ruby
def create_https_api_rest_sh_api_2_fa(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApi2faRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = twoFactorAuthenticationAPI.create_https_api_rest_sh_api_2_fa(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagementController") UserManagementController

### Get singleton instance

The singleton instance of the ``` UserManagementController ``` class can be accessed from the API Client.

```ruby
userManagement = client.user_management
```

### <a name="get_https_api_rest_sh_api_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.get_https_api_rest_sh_api_user_info") get_https_api_rest_sh_api_user_info

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```ruby
def get_https_api_rest_sh_api_user_info(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| apiuid |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

user = 'user'
collect['user'] = user

apiuid = 'apiuid'
collect['apiuid'] = apiuid

content_type = 'Content-Type'
collect['content_type'] = content_type


result = userManagement.get_https_api_rest_sh_api_user_info(collect)

```


### <a name="create_https_api_rest_sh_api_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.create_https_api_rest_sh_api_user_info") create_https_api_rest_sh_api_user_info

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```ruby
def create_https_api_rest_sh_api_user_info(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiUserInfoRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = userManagement.create_https_api_rest_sh_api_user_info(collect)

```


### <a name="get_https_api_rest_sh_api_user_update"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.get_https_api_rest_sh_api_user_update") get_https_api_rest_sh_api_user_update

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```ruby
def get_https_api_rest_sh_api_user_update(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| apiuid |  ``` Required ```  | TODO: Add a parameter description |
| avatar |  ``` Required ```  | TODO: Add a parameter description |
| custom_input |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

user = 'user'
collect['user'] = user

apiuid = 'apiuid'
collect['apiuid'] = apiuid

avatar = 'avatar'
collect['avatar'] = avatar

custom_input = 'custom input'
collect['custom_input'] = custom_input

content_type = 'Content-Type'
collect['content_type'] = content_type


result = userManagement.get_https_api_rest_sh_api_user_update(collect)

```


### <a name="create_https_api_rest_sh_api_user_update"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.create_https_api_rest_sh_api_user_update") create_https_api_rest_sh_api_user_update

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```ruby
def create_https_api_rest_sh_api_user_update(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiUserUpdateRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = userManagement.create_https_api_rest_sh_api_user_update(collect)

```


### <a name="get_https_api_rest_sh_api_user_delete"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.get_https_api_rest_sh_api_user_delete") get_https_api_rest_sh_api_user_delete

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```ruby
def get_https_api_rest_sh_api_user_delete(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| api |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| apiuid |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

api = 'api'
collect['api'] = api

uid = 'uid'
collect['uid'] = uid

user = 'user'
collect['user'] = user

apiuid = 'apiuid'
collect['apiuid'] = apiuid

content_type = 'Content-Type'
collect['content_type'] = content_type


result = userManagement.get_https_api_rest_sh_api_user_delete(collect)

```


### <a name="create_https_api_rest_sh_api_user_delete"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.create_https_api_rest_sh_api_user_delete") create_https_api_rest_sh_api_user_delete

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```ruby
def create_https_api_rest_sh_api_user_delete(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiUserDeleteRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = userManagement.create_https_api_rest_sh_api_user_delete(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration_controller"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistrationController") LoginAndRegistrationController

### Get singleton instance

The singleton instance of the ``` LoginAndRegistrationController ``` class can be accessed from the API Client.

```ruby
loginAndRegistration = client.login_and_registration
```

### <a name="get_https_api_rest_sh_api_auth_user_register"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.get_https_api_rest_sh_api_auth_user_register") get_https_api_rest_sh_api_auth_user_register

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```ruby
def get_https_api_rest_sh_api_auth_user_register(options = {}); end
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
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

user = 'user'
collect['user'] = user

password = 'password'
collect['password'] = password

name = 'name'
collect['name'] = name

email = 'email'
collect['email'] = email

phone = 42
collect['phone'] = phone

countrycode = 42
collect['countrycode'] = countrycode

address = 'address'
collect['address'] = address

content_type = 'Content-Type'
collect['content_type'] = content_type


result = loginAndRegistration.get_https_api_rest_sh_api_auth_user_register(collect)

```


### <a name="create_https_api_rest_sh_api_auth_user_register"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.create_https_api_rest_sh_api_auth_user_register") create_https_api_rest_sh_api_auth_user_register

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```ruby
def create_https_api_rest_sh_api_auth_user_register(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiAuthUserRegisterRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = loginAndRegistration.create_https_api_rest_sh_api_auth_user_register(collect)

```


### <a name="get_https_api_rest_sh_api_auth_user_login"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.get_https_api_rest_sh_api_auth_user_login") get_https_api_rest_sh_api_auth_user_login

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```ruby
def get_https_api_rest_sh_api_auth_user_login(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| user |  ``` Required ```  | TODO: Add a parameter description |
| password |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

user = 'user'
collect['user'] = user

password = 'password'
collect['password'] = password

content_type = 'Content-Type'
collect['content_type'] = content_type


result = loginAndRegistration.get_https_api_rest_sh_api_auth_user_login(collect)

```


### <a name="create_https_api_rest_sh_api_auth_user_login"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.create_https_api_rest_sh_api_auth_user_login") create_https_api_rest_sh_api_auth_user_login

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```ruby
def create_https_api_rest_sh_api_auth_user_login(options = {}); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
collect = Hash.new

body = HttpsApiRestShApiAuthUserLoginRequestModel.new
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = loginAndRegistration.create_https_api_rest_sh_api_auth_user_login(collect)

```


[Back to List of Controllers](#list_of_controllers)



