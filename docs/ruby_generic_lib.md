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
3. Once built, the gem can be installed on the current work environment using ``` gem install smash-1.11.0.gem ```

![Building Gem](https://apidocs.io/illustration/ruby?step=buildSDK&workspaceFolder=SMASH-Ruby&workspaceName=SMASH-Ruby&projectName=smash&gemName=smash&gemVer=1.11.0)

## How to Use

The following section explains how to use the SMASH Ruby Gem in a new Rails project using RubyMine&trade;. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

### 1. Starting a new project

Close any existing projects in RubyMine&trade; by selecting ``` File -> Close Project ```. Next, click on ``` Create New Project ``` to create a new project from scratch.

![Create a new project in RubyMine](https://apidocs.io/illustration/ruby?step=createNewProject0&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.11.0)

Next, provide ``` TestApp ``` as the project name, choose ``` Rails Application ``` as the project type, and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 1](https://apidocs.io/illustration/ruby?step=createNewProject1&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.11.0)

In the next dialog make sure that correct *Ruby SDK* is being used (minimum 2.0.0) and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 2](https://apidocs.io/illustration/ruby?step=createNewProject2&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.11.0)

This will create a new Rails Application project with an existing set of files and folder.

### 2. Add reference of the gem

In order to use the SMASH gem in the new project we must add a gem reference. Locate the ```Gemfile``` in the *Project Explorer* window under the ``` TestApp ``` project node. The file contains references to all gems being used in the project. Here, add the reference to the library gem by adding the following line: ``` gem 'smash', '~> 1.11.0' ```

![Add references of the Gemfile](https://apidocs.io/illustration/ruby?step=addReference&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.11.0)

### 3. Adding a new Rails Controller

Once the ``` TestApp ``` project is created, a folder named ``` controllers ``` will be visible in the *Project Explorer* under the following path: ``` TestApp > app > controllers ```. Right click on this folder and select ``` New -> Run Rails Generator... ```.

![Run Rails Generator on Controllers Folder](https://apidocs.io/illustration/ruby?step=addCode0&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.11.0)

Selecting the said option will popup a small window where the generator names are displayed. Here, select the ``` controller ``` template.

![Create a new Controller](https://apidocs.io/illustration/ruby?step=addCode1&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.11.0)

Next, a popup window will ask you for a Controller name and included Actions. For controller name provide ``` Hello ``` and include an action named ``` Index ``` and click ``` OK ```.

![Add a new Controller](https://apidocs.io/illustration/ruby?step=addCode2&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.11.0)

A new controller class anmed ``` HelloController ``` will be created in a file named ``` hello_controller.rb ``` containing a method named ``` Index ```. In this method, add code for initialization and a sample for its usage.

![Initialize the library](https://apidocs.io/illustration/ruby?step=addCode3&workspaceFolder=SMASH-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.11.0)

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
| uid | Your user ID |
| secret | Your Private API Key |
| key | Your Public API Key |



API client can be initialized as following.

```ruby
# Configuration parameters and credentials
uid = 'UID' # Your user ID
secret = 'SECRET' # Your Private API Key
key = 'KEY' # Your Public API Key

client = Smash::SMASH.new(
  uid: uid,
  secret: secret,
  key: key
)
```

The added initlization code can be debugged by putting a breakpoint in the ``` Index ``` method and running the project in debug mode by selecting ``` Run -> Debug 'Development: TestApp' ```.

![Debug the TestApp](https://apidocs.io/illustration/ruby?step=addCode4&workspaceFolder=SMASH%20-%20API-Ruby&workspaceName=SMASH&projectName=smash&gemName=smash&gemVer=1.11.0&initLine=client%2520%253D%2520SMASH.new%2528%2527uid%2527%252C%2520%2527secret%2527%252C%2520%2527key%2527%2529)



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
def logging_info(name,
                     origin,
                     time = nil); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| name |  ``` Required ```  | Name of your WAF zone |
| origin |  ``` Required ```  | IP Address of the Web Application |
| time |  ``` Optional ```  | Specific times or dates to lookup separated by a comma in MMDDYYHHMMSS Format ( Month Month Day Day Year Year Year Hour Hour Minute Minute Second Second [01012017120059]) |


#### Example Usage

```ruby
name = 'name'
origin = 'origin'
time = 'time'

result = advancedLogging.logging_info(name, origin, time)

```


### <a name="logging_configuration"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.logging_configuration") logging_configuration

> WAF Log Configuration


```ruby
def logging_configuration(name,
                              origin,
                              activate); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| name |  ``` Required ```  | Name of the WAF zone |
| origin |  ``` Required ```  | IP Address of the Web Application you wish to configure logging on |
| activate |  ``` Required ```  | True or False |


#### Example Usage

```ruby
name = 'name'
origin = 'origin'
activate = 'activate'

result = advancedLogging.logging_configuration(name, origin, activate)

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
def data_and_file_encryption(data,
                                 method,
                                 bit); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Required ```  | GIT URL, file URL, direct upload of file, or data as a query string |
| method |  ``` Required ```  | Single or multiple encryption types to apply to data or files separated by a comma (DES, RSA, BLOWFISH, TWOFISH, AES, IDEA, PGP) |
| bit |  ``` Required ```  | Encryption key size (4096) |


#### Example Usage

```ruby
data = 'data'
method = 'method'
bit = 49

result = encryption.data_and_file_encryption(data, method, bit)

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
def cdn_push_zone(cname,
                      file); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| cname |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access |
| file |  ``` Required ```  | GIT URL, file URL, or direct upload of file |


#### Example Usage

```ruby
cname = 'cname'
file = 'file'

result = cDN.cdn_push_zone(cname, file)

```


### <a name="cdn_pull_zone"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cdn_pull_zone") cdn_pull_zone

> CDN Pull Zone API


```ruby
def cdn_pull_zone(origin,
                      cname); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| origin |  ``` Required ```  | Domain or domain names separated by a comma |
| cname |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access |


#### Example Usage

```ruby
origin = 'origin'
cname = 'cname'

result = cDN.cdn_pull_zone(origin, cname)

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
def dns_configuration(domain,
                          records); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| domain |  ``` Required ```  | Domain or domain names separated by a comma |
| records |  ``` Required ```  | Records to append to domain separated by a comma (a;www.mydomain.com;127.0.0.0,cname;mydomain.com;otherdomain.com) |


#### Example Usage

```ruby
domain = 'domain'
records = 'records'

result = dNS.dns_configuration(domain, records)

```


### <a name="dns_creation"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dns_creation") dns_creation

> DNS Creation API


```ruby
def dns_creation(domain); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| domain |  ``` Required ```  | Domain or domain names separated by a comma |


#### Example Usage

```ruby
domain = 'domain'

result = dNS.dns_creation(domain)

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
def obfuscation_and_anti_tampering(app); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| app |  ``` Required ```  | GIT URL or ZIP package containing your APP |


#### Example Usage

```ruby
app = 'app'

result = codeObfuscation.obfuscation_and_anti_tampering(app)

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
def hosting_setup(app,
                      domain); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| app |  ``` Required ```  | GIT URL or ZIP package containing your APP |
| domain |  ``` Required ```  | Domain or domain names separated by a comma |


#### Example Usage

```ruby
app = 'app'
domain = 'domain'

result = hosting.hosting_setup(app, domain)

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
def image_manipulation(image,
                           transform); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| image |  ``` Required ```  | Image URL or direct upload |
| transform |  ``` Required ```  | Transformations to perform |


#### Example Usage

```ruby
image = 'image'
transform = 'transform'

result = imageManipulationAndModerationAPI.image_manipulation(image, transform)

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
def user_address_verification(user,
                                  a,
                                  sa,
                                  c,
                                  s,
                                  z,
                                  address = nil); end
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

```ruby
user = 'user'
a = 'a'
sa = 'sa'
c = 'c'
s = 's'
z = 7
address = 'address'

result = verification.user_address_verification(user, a, sa, c, s, z, address)

```


### <a name="user_verification_response"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.user_verification_response") user_verification_response

> Users Verification Response API


```ruby
def user_verification_response(user,
                                   code); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |
| code |  ``` Required ```  | Verification code entered by the user |


#### Example Usage

```ruby
user = 'user'
code = 'code'

result = verification.user_verification_response(user, code)

```


### <a name="user_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.user_verification") user_verification

> User Verification API


```ruby
def user_verification(user); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |


#### Example Usage

```ruby
user = 'user'

result = verification.user_verification(user)

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
def 2_fa_token_response(user,
                            code); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username or Email |
| code |  ``` Required ```  | Response From User Containing 2FA Code |


#### Example Usage

```ruby
user = 'user'
code = 'code'

result = twoFactorAuthenticationAPI.2_fa_token_response(user, code)

```


### <a name="two_factor_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.two_factor_authentication") two_factor_authentication

> Two Factor Authentication API


```ruby
def two_factor_authentication(to); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| to |  ``` Required ```  | Users UID, Username, Email, Or Cellphone number |


#### Example Usage

```ruby
to = 'to'

result = twoFactorAuthenticationAPI.two_factor_authentication(to)

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
def get_user_info(user); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users User ID |


#### Example Usage

```ruby
user = 'user'

result = userManagement.get_user_info(user)

```


### <a name="update_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.update_user") update_user

> Update User API


```ruby
def update_user(user,
                    avatar,
                    custom_input,
                    _query_parameters = nil); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |
| avatar |  ``` Required ```  | Avatar Image URL |
| custom_input |  ``` Required ```  | Custom input variable for users profile |
| _query_parameters | ``` Optional ``` | Additional optional query parameters are supported by this method |


#### Example Usage

```ruby
user = 'user'
avatar = 'avatar'
custom_input = 'custom input'
# key-value map for optional query parameters
queryParams = { 'key' => 'value' }

result = userManagement.update_user(user, avatar, custom_input, queryParams)

```


### <a name="delete_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.delete_user") delete_user

> Delete User API


```ruby
def delete_user(user); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, or Email |


#### Example Usage

```ruby
user = 'user'

result = userManagement.delete_user(user)

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
def user_registration(email,
                          user,
                          password,
                          name = nil,
                          phone = nil,
                          countrycode = nil,
                          address = nil,
                          _query_parameters = nil); end
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
| _query_parameters | ``` Optional ``` | Additional optional query parameters are supported by this method |


#### Example Usage

```ruby
email = 'email'
user = 'user'
password = 'password'
name = 'name'
phone = 7
countrycode = 7
address = 'address'
# key-value map for optional query parameters
queryParams = { 'key' => 'value' }

result = loginAndRegistration.user_registration(email, user, password, name, phone, countrycode, address, queryParams)

```


### <a name="user_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.user_authentication") user_authentication

> User Authentication API


```ruby
def user_authentication(user,
                            password); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users Username or Email |
| password |  ``` Required ```  | Users Password |


#### Example Usage

```ruby
user = 'user'
password = 'password'

result = loginAndRegistration.user_authentication(user, password)

```


[Back to List of Controllers](#list_of_controllers)



