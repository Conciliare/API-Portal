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
3. Once built, the gem can be installed on the current work environment using ``` gem install smash-1.8.0.gem ```

![Building Gem](https://apidocs.io/illustration/ruby?step=buildSDK&workspaceFolder=SMASH-Ruby&workspaceName=SMASH-Ruby&projectName=smash&gemName=smash&gemVer=1.8.0)

## How to Use

The following section explains how to use the SMASH Ruby Gem in a new Rails project using RubyMine&trade;. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

### 1. Starting a new project

Close any existing projects in RubyMine&trade; by selecting ``` File -> Close Project ```. Next, click on ``` Create New Project ``` to create a new project from scratch.

![Create a new project in RubyMine](https://apidocs.io/illustration/ruby?step=createNewProject0&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.8.0)

Next, provide ``` TestApp ``` as the project name, choose ``` Rails Application ``` as the project type, and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 1](https://apidocs.io/illustration/ruby?step=createNewProject1&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.8.0)

In the next dialog make sure that correct *Ruby SDK* is being used (minimum 2.0.0) and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 2](https://apidocs.io/illustration/ruby?step=createNewProject2&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.8.0)

This will create a new Rails Application project with an existing set of files and folder.

### 2. Add reference of the gem

In order to use the SMASH gem in the new project we must add a gem reference. Locate the ```Gemfile``` in the *Project Explorer* window under the ``` TestApp ``` project node. The file contains references to all gems being used in the project. Here, add the reference to the library gem by adding the following line: ``` gem 'smash', '~> 1.8.0' ```

![Add references of the Gemfile](https://apidocs.io/illustration/ruby?step=addReference&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.8.0)

### 3. Adding a new Rails Controller

Once the ``` TestApp ``` project is created, a folder named ``` controllers ``` will be visible in the *Project Explorer* under the following path: ``` TestApp > app > controllers ```. Right click on this folder and select ``` New -> Run Rails Generator... ```.

![Run Rails Generator on Controllers Folder](https://apidocs.io/illustration/ruby?step=addCode0&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.8.0)

Selecting the said option will popup a small window where the generator names are displayed. Here, select the ``` controller ``` template.

![Create a new Controller](https://apidocs.io/illustration/ruby?step=addCode1&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.8.0)

Next, a popup window will ask you for a Controller name and included Actions. For controller name provide ``` Hello ``` and include an action named ``` Index ``` and click ``` OK ```.

![Add a new Controller](https://apidocs.io/illustration/ruby?step=addCode2&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.8.0)

A new controller class anmed ``` HelloController ``` will be created in a file named ``` hello_controller.rb ``` containing a method named ``` Index ```. In this method, add code for initialization and a sample for its usage.

![Initialize the library](https://apidocs.io/illustration/ruby?step=addCode3&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.8.0)

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
| basic_auth_user_name | The username to use with basic authentication |
| basic_auth_password | The password to use with basic authentication |



API client can be initialized as following.

```ruby
# Configuration parameters and credentials
basic_auth_user_name = 'basic_auth_user_name' # The username to use with basic authentication
basic_auth_password = 'basic_auth_password' # The password to use with basic authentication

client = Smash::SMASH.new(
  basic_auth_user_name: basic_auth_user_name,
  basic_auth_password: basic_auth_password
)
```

The added initlization code can be debugged by putting a breakpoint in the ``` Index ``` method and running the project in debug mode by selecting ``` Run -> Debug 'Development: TestApp' ```.

![Debug the TestApp](https://apidocs.io/illustration/ruby?step=addCode4&workspaceFolder=SMASH%20-%20API-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.8.0&initLine=client%2520%253D%2520SMASH.new%2528%2527basic_auth_user_name%2527%252C%2520%2527basic_auth_password%2527%2529)



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

```ruby
advancedLogging = client.advanced_logging
```

### <a name="logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.logging_info") logging_info

> WAF Log Info


```ruby
def logging_info(key,
                     uid,
                     name,
                     origin,
                     time,
                     content_type); end
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
key = 'key'
uid = 'uid'
name = 'name'
origin = 'origin'
time = 'time'
content_type = 'Content-Type'

result = advancedLogging.logging_info(key, uid, name, origin, time, content_type)

```


### <a name="logging_setup"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.logging_setup") logging_setup

> WAF Log Setup


```ruby
def logging_setup(key,
                      uid,
                      name,
                      origin,
                      activate,
                      content_type); end
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
key = 'key'
uid = 'uid'
name = 'name'
origin = 'origin'
activate = true
content_type = 'Content-Type'

result = advancedLogging.logging_setup(key, uid, name, origin, activate, content_type)

```


### <a name="logging_info1"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.logging_info1") logging_info1

> WAF Log Info


```ruby
def logging_info1(body,
                      content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiSLI.new
content_type = 'Content-Type'

result = advancedLogging.logging_info1(body, content_type)

```


### <a name="logging_setup1"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.logging_setup1") logging_setup1

> WAF Log Setup


```ruby
def logging_setup1(body,
                       content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiSL.new
content_type = 'Content-Type'

result = advancedLogging.logging_setup1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtection") WAFDDOSProtection

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtection ``` class can be accessed from the API Client.

```ruby
wAFDDOSProtection = client.wafddos_protection
```

### <a name="https_api_rest_sh_api_s_w_c"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.https_api_rest_sh_api_s_w_c") https_api_rest_sh_api_s_w_c

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```ruby
def https_api_rest_sh_api_s_w_c(key,
                                    uid,
                                    name,
                                    origin,
                                    rule,
                                    content_type); end
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
key = 'API'
uid = 'UID'
name = 'origin-name'
origin = 'origin.yourdomain.tld'
rule = 'header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does'
content_type = 'application/json'

result = wAFDDOSProtection.https_api_rest_sh_api_s_w_c(key, uid, name, origin, rule, content_type)

```


### <a name="https_api_rest_sh_api_s_w"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.https_api_rest_sh_api_s_w") https_api_rest_sh_api_s_w

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```ruby
def https_api_rest_sh_api_s_w(key,
                                  uid,
                                  origin,
                                  cname,
                                  content_type); end
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
key = 'API'
uid = 'UID'
origin = 'origin.yourdomain.tld'
cname = 'yourdomain.tld,www.yourdomain.tld'
content_type = 'application/json'

result = wAFDDOSProtection.https_api_rest_sh_api_s_w(key, uid, origin, cname, content_type)

```


### <a name="https_api_rest_sh_api_s_w_c1"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.https_api_rest_sh_api_s_w_c1") https_api_rest_sh_api_s_w_c1

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```ruby
def https_api_rest_sh_api_s_w_c1(body,
                                     content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body_value = "{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}";
body = JSON.parse(body_value);
content_type = 'application/json'

result = wAFDDOSProtection.https_api_rest_sh_api_s_w_c1(body, content_type)

```


### <a name="https_api_rest_sh_api_s_w1"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.https_api_rest_sh_api_s_w1") https_api_rest_sh_api_s_w1

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```ruby
def https_api_rest_sh_api_s_w1(body,
                                   content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body_value = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}";
body = JSON.parse(body_value);
content_type = 'application/json'

result = wAFDDOSProtection.https_api_rest_sh_api_s_w1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption"></a>![Class: ](https://apidocs.io/img/class.png ".Encryption") Encryption

### Get singleton instance

The singleton instance of the ``` Encryption ``` class can be accessed from the API Client.

```ruby
encryption = client.encryption
```

### <a name="data_and_file_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.data_and_file_encryption") data_and_file_encryption

> Data and File Encryption API


```ruby
def data_and_file_encryption(key,
                                 uid,
                                 data,
                                 method,
                                 bit,
                                 content_type); end
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
key = 'key'
uid = 'uid'
data = 'data'
method = 'method'
bit = 201
content_type = 'Content-Type'

result = encryption.data_and_file_encryption(key, uid, data, method, bit, content_type)

```


### <a name="data_and_file_encryption1"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.data_and_file_encryption1") data_and_file_encryption1

> Data and File Encryption API


```ruby
def data_and_file_encryption1(body,
                                  content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiSE.new
content_type = 'Content-Type'

result = encryption.data_and_file_encryption1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn"></a>![Class: ](https://apidocs.io/img/class.png ".CDN") CDN

### Get singleton instance

The singleton instance of the ``` CDN ``` class can be accessed from the API Client.

```ruby
cDN = client.cdn
```

### <a name="cdn_push_zone"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cdn_push_zone") cdn_push_zone

> CDN Push Zone API


```ruby
def cdn_push_zone(key,
                      uid,
                      cname,
                      file,
                      content_type); end
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
key = 'key'
uid = 'uid'
cname = 'cname'
file = 'file'
content_type = 'Content-Type'

result = cDN.cdn_push_zone(key, uid, cname, file, content_type)

```


### <a name="cdn_pull_zone"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cdn_pull_zone") cdn_pull_zone

> CDN Pull Zone API


```ruby
def cdn_pull_zone(key,
                      uid,
                      origin,
                      cname,
                      content_type); end
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
key = 'key'
uid = 'uid'
origin = 'origin'
cname = 'cname'
content_type = 'Content-Type'

result = cDN.cdn_pull_zone(key, uid, origin, cname, content_type)

```


### <a name="cdn_push_zone1"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cdn_push_zone1") cdn_push_zone1

> CDN Push Zone API


```ruby
def cdn_push_zone1(body,
                       content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiSCPush.new
content_type = 'Content-Type'

result = cDN.cdn_push_zone1(body, content_type)

```


### <a name="cdn_pull_zone1"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cdn_pull_zone1") cdn_pull_zone1

> CDN Pull Zone API


```ruby
def cdn_pull_zone1(body,
                       content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiSCPull.new
content_type = 'Content-Type'

result = cDN.cdn_pull_zone1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns"></a>![Class: ](https://apidocs.io/img/class.png ".DNS") DNS

### Get singleton instance

The singleton instance of the ``` DNS ``` class can be accessed from the API Client.

```ruby
dNS = client.dns
```

### <a name="dns_configuration"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dns_configuration") dns_configuration

> DNS Configuration API


```ruby
def dns_configuration(key,
                          uid,
                          domain,
                          records,
                          content_type); end
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
key = 'key'
uid = 'uid'
domain = 'domain'
records = 'records'
content_type = 'Content-Type'

result = dNS.dns_configuration(key, uid, domain, records, content_type)

```


### <a name="dns_configuration1"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dns_configuration1") dns_configuration1

> DNS Configuration API


```ruby
def dns_configuration1(body,
                           content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiSDC.new
content_type = 'Content-Type'

result = dNS.dns_configuration1(body, content_type)

```


### <a name="dns_creation"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dns_creation") dns_creation

> DNS Creation API


```ruby
def dns_creation(key,
                     uid,
                     domain,
                     content_type); end
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
key = 'key'
uid = 'uid'
domain = 'domain'
content_type = 'Content-Type'

result = dNS.dns_creation(key, uid, domain, content_type)

```


### <a name="dns_creation1"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dns_creation1") dns_creation1

> DNS Creation API


```ruby
def dns_creation1(body,
                      content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiSDA.new
content_type = 'Content-Type'

result = dNS.dns_creation1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscation") CodeObfuscation

### Get singleton instance

The singleton instance of the ``` CodeObfuscation ``` class can be accessed from the API Client.

```ruby
codeObfuscation = client.code_obfuscation
```

### <a name="obfuscation_and_anti_tampering"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.obfuscation_and_anti_tampering") obfuscation_and_anti_tampering

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```ruby
def obfuscation_and_anti_tampering(key,
                                       uid,
                                       app,
                                       content_type); end
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
key = 'key'
uid = 'uid'
app = 'app'
content_type = 'Content-Type'

result = codeObfuscation.obfuscation_and_anti_tampering(key, uid, app, content_type)

```


### <a name="obfuscation_and_anti_tampering1"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.obfuscation_and_anti_tampering1") obfuscation_and_anti_tampering1

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```ruby
def obfuscation_and_anti_tampering1(body,
                                        content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiSO.new
content_type = 'Content-Type'

result = codeObfuscation.obfuscation_and_anti_tampering1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting"></a>![Class: ](https://apidocs.io/img/class.png ".Hosting") Hosting

### Get singleton instance

The singleton instance of the ``` Hosting ``` class can be accessed from the API Client.

```ruby
hosting = client.hosting
```

### <a name="hosting_setup"></a>![Method: ](https://apidocs.io/img/method.png ".Hosting.hosting_setup") hosting_setup

> Node.JS and Static Web APP Hosting


```ruby
def hosting_setup(key,
                      uid,
                      app,
                      domain,
                      content_type); end
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
key = 'key'
uid = 'uid'
app = 'app'
domain = 'domain'
content_type = 'Content-Type'

result = hosting.hosting_setup(key, uid, app, domain, content_type)

```


### <a name="hosting_setup1"></a>![Method: ](https://apidocs.io/img/method.png ".Hosting.hosting_setup1") hosting_setup1

> Node.JS and Static Web APP Hosting


```ruby
def hosting_setup1(body,
                       content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiSH.new
content_type = 'Content-Type'

result = hosting.hosting_setup1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPI") DataManipulationConversionSortingAndCompressionAPI

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPI ``` class can be accessed from the API Client.

```ruby
dataManipulationConversionSortingAndCompressionAPI = client.data_manipulation_conversion_sorting_and_compression_api
```

### <a name="https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPI.https_api_rest_sh_api_d") https_api_rest_sh_api_d

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```ruby
def https_api_rest_sh_api_d(key,
                                uid,
                                user,
                                apiuid,
                                data,
                                content_type); end
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
key = 'API'
uid = 'UID'
user = 'UID'
apiuid = 'apiUID'
data = 'https://static.yourcdn.com/data.file'
content_type = 'application/json'

result = dataManipulationConversionSortingAndCompressionAPI.https_api_rest_sh_api_d(key, uid, user, apiuid, data, content_type)

```


### <a name="https_api_rest_sh_api_d1"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPI.https_api_rest_sh_api_d1") https_api_rest_sh_api_d1

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```ruby
def https_api_rest_sh_api_d1(body,
                                 content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body_value = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}";
body = JSON.parse(body_value);
content_type = 'application/json'

result = dataManipulationConversionSortingAndCompressionAPI.https_api_rest_sh_api_d1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPI") ImageManipulationAndModerationAPI

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPI ``` class can be accessed from the API Client.

```ruby
imageManipulationAndModerationAPI = client.image_manipulation_and_moderation_api
```

### <a name="image_manipulation"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPI.image_manipulation") image_manipulation

> Image Manipulation API


```ruby
def image_manipulation(key,
                           uid,
                           image,
                           transform,
                           content_type); end
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
key = 'key'
uid = 'uid'
image = 'image'
transform = 'transform'
content_type = 'Content-Type'

result = imageManipulationAndModerationAPI.image_manipulation(key, uid, image, transform, content_type)

```


### <a name="image_manipulation1"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPI.image_manipulation1") image_manipulation1

> Image Manipulation API


```ruby
def image_manipulation1(body,
                            content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiI.new
content_type = 'Content-Type'

result = imageManipulationAndModerationAPI.image_manipulation1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification"></a>![Class: ](https://apidocs.io/img/class.png ".Verification") Verification

### Get singleton instance

The singleton instance of the ``` Verification ``` class can be accessed from the API Client.

```ruby
verification = client.verification
```

### <a name="user_address_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.user_address_verification") user_address_verification

> User Address Verification API


```ruby
def user_address_verification(key,
                                  uid,
                                  user,
                                  a,
                                  sa,
                                  c,
                                  s,
                                  z,
                                  content_type); end
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
key = 'key'
uid = 'uid'
user = 'user'
a = 'a'
sa = 'sa'
c = 'c'
s = 's'
z = 37
content_type = 'Content-Type'

result = verification.user_address_verification(key, uid, user, a, sa, c, s, z, content_type)

```


### <a name="user_address_verification1"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.user_address_verification1") user_address_verification1

> User Address Verification API


```ruby
def user_address_verification1(body,
                                   content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiVA.new
content_type = 'Content-Type'

result = verification.user_address_verification1(body, content_type)

```


### <a name="user_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.user_verification") user_verification

> User Verification API


```ruby
def user_verification(key,
                          uid,
                          user,
                          code,
                          content_type); end
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
key = 'key'
uid = 'uid'
user = 'user'
code = 'code'
content_type = 'Content-Type'

result = verification.user_verification(key, uid, user, code, content_type)

```


### <a name="user_verification1"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.user_verification1") user_verification1

> User Verification API


```ruby
def user_verification1(body,
                           content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiVU.new
content_type = 'Content-Type'

result = verification.user_verification1(body, content_type)

```


### <a name="cellphone_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.cellphone_verification") cellphone_verification

> Verification API


```ruby
def cellphone_verification(key,
                               uid,
                               to,
                               content_type); end
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
key = 'key'
uid = 'uid'
to = 'to'
content_type = 'Content-Type'

result = verification.cellphone_verification(key, uid, to, content_type)

```


### <a name="cellphone_verification1"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.cellphone_verification1") cellphone_verification1

> Verification API


```ruby
def cellphone_verification1(body,
                                content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiV.new
content_type = 'Content-Type'

result = verification.cellphone_verification1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPI") TwoFactorAuthenticationAPI

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPI ``` class can be accessed from the API Client.

```ruby
twoFactorAuthenticationAPI = client.two_factor_authentication_api
```

### <a name="2_fa_token_response"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.2_fa_token_response") 2_fa_token_response

> Two Factor Authentication Token Reply


```ruby
def 2_fa_token_response(key,
                            uid,
                            user,
                            code,
                            content_type); end
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
key = 'key'
uid = 'uid'
user = 'user'
code = 'code'
content_type = 'Content-Type'

result = twoFactorAuthenticationAPI.2_fa_token_response(key, uid, user, code, content_type)

```


### <a name="2_fa_token_response1"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.2_fa_token_response1") 2_fa_token_response1

> Two Factor Authentication Token Reply


```ruby
def 2_fa_token_response1(body,
                             content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApi2faT.new
content_type = 'Content-Type'

result = twoFactorAuthenticationAPI.2_fa_token_response1(body, content_type)

```


### <a name="two_factor_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.two_factor_authentication") two_factor_authentication

> Two Factor Authentication API


```ruby
def two_factor_authentication(key,
                                  uid,
                                  to,
                                  content_type); end
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
key = 'key'
uid = 'uid'
to = 'to'
content_type = 'Content-Type'

result = twoFactorAuthenticationAPI.two_factor_authentication(key, uid, to, content_type)

```


### <a name="two_factor_authentication1"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.two_factor_authentication1") two_factor_authentication1

> Two Factor Authentication API


```ruby
def two_factor_authentication1(body,
                                   content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApi2fa.new
content_type = 'Content-Type'

result = twoFactorAuthenticationAPI.two_factor_authentication1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagement") UserManagement

### Get singleton instance

The singleton instance of the ``` UserManagement ``` class can be accessed from the API Client.

```ruby
userManagement = client.user_management
```

### <a name="get_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.get_user_info") get_user_info

> Get User Info API


```ruby
def get_user_info(key,
                      uid,
                      user,
                      apiuid,
                      content_type); end
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
key = 'key'
uid = 'uid'
user = 'user'
apiuid = 'apiuid'
content_type = 'Content-Type'

result = userManagement.get_user_info(key, uid, user, apiuid, content_type)

```


### <a name="get_user_info1"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.get_user_info1") get_user_info1

> Get User Info API


```ruby
def get_user_info1(body,
                       content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiUI.new
content_type = 'Content-Type'

result = userManagement.get_user_info1(body, content_type)

```


### <a name="update_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.update_user") update_user

> Update User API


```ruby
def update_user(key,
                    uid,
                    user,
                    apiuid,
                    avatar,
                    custom_input,
                    content_type); end
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
key = 'key'
uid = 'uid'
user = 'user'
apiuid = 'apiuid'
avatar = 'avatar'
custom_input = 'custom input'
content_type = 'Content-Type'

result = userManagement.update_user(key, uid, user, apiuid, avatar, custom_input, content_type)

```


### <a name="update_user1"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.update_user1") update_user1

> Update User API


```ruby
def update_user1(body,
                     content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiUU.new
content_type = 'Content-Type'

result = userManagement.update_user1(body, content_type)

```


### <a name="delete_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.delete_user") delete_user

> Delete User API


```ruby
def delete_user(api,
                    uid,
                    user,
                    apiuid,
                    content_type); end
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
api = 'api'
uid = 'uid'
user = 'user'
apiuid = 'apiuid'
content_type = 'Content-Type'

result = userManagement.delete_user(api, uid, user, apiuid, content_type)

```


### <a name="delete_user1"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.delete_user1") delete_user1

> Delete User API


```ruby
def delete_user1(body,
                     content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiUD.new
content_type = 'Content-Type'

result = userManagement.delete_user1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistration") LoginAndRegistration

### Get singleton instance

The singleton instance of the ``` LoginAndRegistration ``` class can be accessed from the API Client.

```ruby
loginAndRegistration = client.login_and_registration
```

### <a name="user_registration"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.user_registration") user_registration

> User Registration API


```ruby
def user_registration(key,
                          uid,
                          user,
                          password,
                          name,
                          email,
                          phone,
                          countrycode,
                          address,
                          content_type); end
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
key = 'key'
uid = 'uid'
user = 'user'
password = 'password'
name = 'name'
email = 'email'
phone = 37
countrycode = 37
address = 'address'
content_type = 'Content-Type'

result = loginAndRegistration.user_registration(key, uid, user, password, name, email, phone, countrycode, address, content_type)

```


### <a name="user_registration1"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.user_registration1") user_registration1

> User Registration API


```ruby
def user_registration1(body,
                           content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiAUR.new
content_type = 'Content-Type'

result = loginAndRegistration.user_registration1(body, content_type)

```


### <a name="user_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.user_authentication") user_authentication

> User Authentication API


```ruby
def user_authentication(key,
                            uid,
                            user,
                            password,
                            content_type); end
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
key = 'key'
uid = 'uid'
user = 'user'
password = 'password'
content_type = 'Content-Type'

result = loginAndRegistration.user_authentication(key, uid, user, password, content_type)

```


### <a name="user_authentication1"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.user_authentication1") user_authentication1

> User Authentication API


```ruby
def user_authentication1(body,
                             content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = HttpsApiRestShApiAUL.new
content_type = 'Content-Type'

result = loginAndRegistration.user_authentication1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)



