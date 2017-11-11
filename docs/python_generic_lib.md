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


You must have Python 2 >=2.7.9 or Python 3 >=3.4 installed on your system to install and run this SDK. This SDK package depends on other Python packages like nose, jsonpickle etc. 
These dependencies are defined in the ```requirements.txt``` file that comes with the SDK.
To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type ```pip --version```.
This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including ```requirements.txt```) for the SDK.
* Run the command ```pip install -r requirements.txt```. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?step=installDependencies&workspaceFolder=SMASH-Python)


## How to Use

The following section explains how to use the SMASH SDK package in a new project.

### 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=pyCharm)

Click on ```Open``` in PyCharm to browse to your generated SDK directory and then click ```OK```.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=openProject0&workspaceFolder=SMASH-Python)     

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=openProject1&workspaceFolder=SMASH-Python&projectName=smash)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=createDirectory&workspaceFolder=SMASH-Python&projectName=smash)

Name the directory as "test"

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=nameDirectory)
   
Add a python file to this project with the name "testsdk"

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=createFile&workspaceFolder=SMASH-Python&projectName=smash)

Name it "testsdk"

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```Python
from smash.smash import SMASH
```

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=projectFiles&workspaceFolder=SMASH-Python&libraryName=smash.smash&projectName=smash)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

### 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on ```Run```

![Run Test Project - Step 1](https://apidocs.io/illustration/python?step=runProject&workspaceFolder=SMASH-Python&libraryName=smash.smash&projectName=smash)


## How to Test

You can test the generated SDK and the server with automatically generated test
cases. unittest is used as the testing framework and nose is used as the test
runner. You can run the tests as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke 'pip install -r test-requirements.txt'
  3. Invoke 'nosetests'

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| uid | Your user ID |
| secret | Your Private API Key |
| key | Your Public API Key |



API client can be initialized as following.

```python
# Configuration parameters and credentials
uid = 'UID' # Your user ID
secret = 'SECRET' # Your Private API Key
key = 'KEY' # Your Public API Key

client = SMASH(uid, secret, key)
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

### Get controller instance

An instance of the ``` AdvancedLogging ``` class can be accessed from the API Client.

```python
 advanced_logging_client = client.advanced_logging
```

### <a name="logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.logging_info") logging_info

> WAF Log Info

```python
def logging_info(self,
                     key,
                     uid,
                     name,
                     origin,
                     time,
                     content_type)
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

```python
key = 'key'
uid = 'uid'
name = 'name'
origin = 'origin'
time = 'time'
content_type = 'Content-Type'

result = advanced_logging_client.logging_info(key, uid, name, origin, time, content_type)

```


### <a name="logging_setup"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.logging_setup") logging_setup

> WAF Log Setup

```python
def logging_setup(self,
                      key,
                      uid,
                      name,
                      origin,
                      activate,
                      content_type)
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

```python
key = 'key'
uid = 'uid'
name = 'name'
origin = 'origin'
activate = True
content_type = 'Content-Type'

result = advanced_logging_client.logging_setup(key, uid, name, origin, activate, content_type)

```


### <a name="logging_info1"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.logging_info1") logging_info1

> WAF Log Info

```python
def logging_info1(self,
                      body,
                      content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiSLI()
content_type = 'Content-Type'

result = advanced_logging_client.logging_info1(body, content_type)

```


### <a name="logging_setup1"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.logging_setup1") logging_setup1

> WAF Log Setup

```python
def logging_setup1(self,
                       body,
                       content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiSL()
content_type = 'Content-Type'

result = advanced_logging_client.logging_setup1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtection") WAFDDOSProtection

### Get controller instance

An instance of the ``` WAFDDOSProtection ``` class can be accessed from the API Client.

```python
 waf_ddos_protection_client = client.waf_ddos_protection
```

### <a name="https_api_rest_sh_api_s_w_c"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.https_api_rest_sh_api_s_w_c") https_api_rest_sh_api_s_w_c

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description

```python
def https_api_rest_sh_api_s_w_c(self,
                                    key,
                                    uid,
                                    name,
                                    origin,
                                    rule,
                                    content_type)
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

```python
key = 'API'
uid = 'UID'
name = 'origin-name'
origin = 'origin.yourdomain.tld'
rule = 'header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does'
content_type = 'application/json'

result = waf_ddos_protection_client.https_api_rest_sh_api_s_w_c(key, uid, name, origin, rule, content_type)

```


### <a name="https_api_rest_sh_api_s_w"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.https_api_rest_sh_api_s_w") https_api_rest_sh_api_s_w

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description

```python
def https_api_rest_sh_api_s_w(self,
                                  key,
                                  uid,
                                  origin,
                                  cname,
                                  content_type)
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

```python
key = 'API'
uid = 'UID'
origin = 'origin.yourdomain.tld'
cname = 'yourdomain.tld,www.yourdomain.tld'
content_type = 'application/json'

result = waf_ddos_protection_client.https_api_rest_sh_api_s_w(key, uid, origin, cname, content_type)

```


### <a name="https_api_rest_sh_api_s_w_c1"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.https_api_rest_sh_api_s_w_c1") https_api_rest_sh_api_s_w_c1

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description

```python
def https_api_rest_sh_api_s_w_c1(self,
                                     body,
                                     content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body_value = "{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}"
body = json.loads(body_value)
content_type = 'application/json'

result = waf_ddos_protection_client.https_api_rest_sh_api_s_w_c1(body, content_type)

```


### <a name="https_api_rest_sh_api_s_w1"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.https_api_rest_sh_api_s_w1") https_api_rest_sh_api_s_w1

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description

```python
def https_api_rest_sh_api_s_w1(self,
                                   body,
                                   content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body_value = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}"
body = json.loads(body_value)
content_type = 'application/json'

result = waf_ddos_protection_client.https_api_rest_sh_api_s_w1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption"></a>![Class: ](https://apidocs.io/img/class.png ".Encryption") Encryption

### Get controller instance

An instance of the ``` Encryption ``` class can be accessed from the API Client.

```python
 encryption_client = client.encryption
```

### <a name="data_and_file_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.data_and_file_encryption") data_and_file_encryption

> Data and File Encryption API

```python
def data_and_file_encryption(self,
                                 key,
                                 uid,
                                 data,
                                 method,
                                 bit,
                                 content_type)
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

```python
key = 'key'
uid = 'uid'
data = 'data'
method = 'method'
bit = 167
content_type = 'Content-Type'

result = encryption_client.data_and_file_encryption(key, uid, data, method, bit, content_type)

```


### <a name="data_and_file_encryption1"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.data_and_file_encryption1") data_and_file_encryption1

> Data and File Encryption API

```python
def data_and_file_encryption1(self,
                                  body,
                                  content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiSE()
content_type = 'Content-Type'

result = encryption_client.data_and_file_encryption1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn"></a>![Class: ](https://apidocs.io/img/class.png ".CDN") CDN

### Get controller instance

An instance of the ``` CDN ``` class can be accessed from the API Client.

```python
 cdn_client = client.cdn
```

### <a name="cdn_push_zone"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cdn_push_zone") cdn_push_zone

> CDN Push Zone API

```python
def cdn_push_zone(self,
                      key,
                      uid,
                      cname,
                      file,
                      content_type)
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

```python
key = 'key'
uid = 'uid'
cname = 'cname'
file = 'file'
content_type = 'Content-Type'

result = cdn_client.cdn_push_zone(key, uid, cname, file, content_type)

```


### <a name="cdn_pull_zone"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cdn_pull_zone") cdn_pull_zone

> CDN Pull Zone API

```python
def cdn_pull_zone(self,
                      key,
                      uid,
                      origin,
                      cname,
                      content_type)
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

```python
key = 'key'
uid = 'uid'
origin = 'origin'
cname = 'cname'
content_type = 'Content-Type'

result = cdn_client.cdn_pull_zone(key, uid, origin, cname, content_type)

```


### <a name="cdn_push_zone1"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cdn_push_zone1") cdn_push_zone1

> CDN Push Zone API

```python
def cdn_push_zone1(self,
                       body,
                       content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiSCPush()
content_type = 'Content-Type'

result = cdn_client.cdn_push_zone1(body, content_type)

```


### <a name="cdn_pull_zone1"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cdn_pull_zone1") cdn_pull_zone1

> CDN Pull Zone API

```python
def cdn_pull_zone1(self,
                       body,
                       content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiSCPull()
content_type = 'Content-Type'

result = cdn_client.cdn_pull_zone1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns"></a>![Class: ](https://apidocs.io/img/class.png ".DNS") DNS

### Get controller instance

An instance of the ``` DNS ``` class can be accessed from the API Client.

```python
 dns_client = client.dns
```

### <a name="dns_configuration"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dns_configuration") dns_configuration

> DNS Configuration API

```python
def dns_configuration(self,
                          key,
                          uid,
                          domain,
                          records,
                          content_type)
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

```python
key = 'key'
uid = 'uid'
domain = 'domain'
records = 'records'
content_type = 'Content-Type'

result = dns_client.dns_configuration(key, uid, domain, records, content_type)

```


### <a name="dns_configuration1"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dns_configuration1") dns_configuration1

> DNS Configuration API

```python
def dns_configuration1(self,
                           body,
                           content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiSDC()
content_type = 'Content-Type'

result = dns_client.dns_configuration1(body, content_type)

```


### <a name="dns_creation"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dns_creation") dns_creation

> DNS Creation API

```python
def dns_creation(self,
                     key,
                     uid,
                     domain,
                     content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| domain |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
key = 'key'
uid = 'uid'
domain = 'domain'
content_type = 'Content-Type'

result = dns_client.dns_creation(key, uid, domain, content_type)

```


### <a name="dns_creation1"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dns_creation1") dns_creation1

> DNS Creation API

```python
def dns_creation1(self,
                      body,
                      content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiSDA()
content_type = 'Content-Type'

result = dns_client.dns_creation1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscation") CodeObfuscation

### Get controller instance

An instance of the ``` CodeObfuscation ``` class can be accessed from the API Client.

```python
 code_obfuscation_client = client.code_obfuscation
```

### <a name="obfuscation_and_anti_tampering"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.obfuscation_and_anti_tampering") obfuscation_and_anti_tampering

> Javascript and Node.JS Obfuscation and Anti-Tampering API

```python
def obfuscation_and_anti_tampering(self,
                                       key,
                                       uid,
                                       app,
                                       content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| app |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
key = 'key'
uid = 'uid'
app = 'app'
content_type = 'Content-Type'

result = code_obfuscation_client.obfuscation_and_anti_tampering(key, uid, app, content_type)

```


### <a name="obfuscation_and_anti_tampering1"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.obfuscation_and_anti_tampering1") obfuscation_and_anti_tampering1

> Javascript and Node.JS Obfuscation and Anti-Tampering API

```python
def obfuscation_and_anti_tampering1(self,
                                        body,
                                        content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiSO()
content_type = 'Content-Type'

result = code_obfuscation_client.obfuscation_and_anti_tampering1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting"></a>![Class: ](https://apidocs.io/img/class.png ".Hosting") Hosting

### Get controller instance

An instance of the ``` Hosting ``` class can be accessed from the API Client.

```python
 hosting_client = client.hosting
```

### <a name="hosting_setup"></a>![Method: ](https://apidocs.io/img/method.png ".Hosting.hosting_setup") hosting_setup

> Node.JS and Static Web APP Hosting

```python
def hosting_setup(self,
                      key,
                      uid,
                      app,
                      domain,
                      content_type)
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

```python
key = 'key'
uid = 'uid'
app = 'app'
domain = 'domain'
content_type = 'Content-Type'

result = hosting_client.hosting_setup(key, uid, app, domain, content_type)

```


### <a name="hosting_setup1"></a>![Method: ](https://apidocs.io/img/method.png ".Hosting.hosting_setup1") hosting_setup1

> Node.JS and Static Web APP Hosting

```python
def hosting_setup1(self,
                       body,
                       content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiSH()
content_type = 'Content-Type'

result = hosting_client.hosting_setup1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPI") DataManipulationConversionSortingAndCompressionAPI

### Get controller instance

An instance of the ``` DataManipulationConversionSortingAndCompressionAPI ``` class can be accessed from the API Client.

```python
 data_manipulation_conversion_sorting_and_compression_api_client = client.data_manipulation_conversion_sorting_and_compression_api
```

### <a name="https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPI.https_api_rest_sh_api_d") https_api_rest_sh_api_d

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description

```python
def https_api_rest_sh_api_d(self,
                                key,
                                uid,
                                user,
                                apiuid,
                                data,
                                content_type)
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

```python
key = 'API'
uid = 'UID'
user = 'UID'
apiuid = 'apiUID'
data = 'https://static.yourcdn.com/data.file'
content_type = 'application/json'

result = data_manipulation_conversion_sorting_and_compression_api_client.https_api_rest_sh_api_d(key, uid, user, apiuid, data, content_type)

```


### <a name="https_api_rest_sh_api_d1"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPI.https_api_rest_sh_api_d1") https_api_rest_sh_api_d1

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description

```python
def https_api_rest_sh_api_d1(self,
                                 body,
                                 content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body_value = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}"
body = json.loads(body_value)
content_type = 'application/json'

result = data_manipulation_conversion_sorting_and_compression_api_client.https_api_rest_sh_api_d1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPI") ImageManipulationAndModerationAPI

### Get controller instance

An instance of the ``` ImageManipulationAndModerationAPI ``` class can be accessed from the API Client.

```python
 image_manipulation_and_moderation_api_client = client.image_manipulation_and_moderation_api
```

### <a name="image_manipulation"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPI.image_manipulation") image_manipulation

> Image Manipulation API

```python
def image_manipulation(self,
                           key,
                           uid,
                           image,
                           transform,
                           content_type)
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

```python
key = 'key'
uid = 'uid'
image = 'image'
transform = 'transform'
content_type = 'Content-Type'

result = image_manipulation_and_moderation_api_client.image_manipulation(key, uid, image, transform, content_type)

```


### <a name="image_manipulation1"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPI.image_manipulation1") image_manipulation1

> Image Manipulation API

```python
def image_manipulation1(self,
                            body,
                            content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiI()
content_type = 'Content-Type'

result = image_manipulation_and_moderation_api_client.image_manipulation1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification"></a>![Class: ](https://apidocs.io/img/class.png ".Verification") Verification

### Get controller instance

An instance of the ``` Verification ``` class can be accessed from the API Client.

```python
 verification_client = client.verification
```

### <a name="user_address_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.user_address_verification") user_address_verification

> User Address Verification API

```python
def user_address_verification(self,
                                  key,
                                  uid,
                                  user,
                                  a,
                                  sa,
                                  c,
                                  s,
                                  z,
                                  content_type)
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

```python
key = 'key'
uid = 'uid'
user = 'user'
a = 'a'
sa = 'sa'
c = 'c'
s = 's'
z = 125
content_type = 'Content-Type'

result = verification_client.user_address_verification(key, uid, user, a, sa, c, s, z, content_type)

```


### <a name="user_address_verification1"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.user_address_verification1") user_address_verification1

> User Address Verification API

```python
def user_address_verification1(self,
                                   body,
                                   content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiVA()
content_type = 'Content-Type'

result = verification_client.user_address_verification1(body, content_type)

```


### <a name="user_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.user_verification") user_verification

> User Verification API

```python
def user_verification(self,
                          key,
                          uid,
                          user,
                          code,
                          content_type)
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

```python
key = 'key'
uid = 'uid'
user = 'user'
code = 'code'
content_type = 'Content-Type'

result = verification_client.user_verification(key, uid, user, code, content_type)

```


### <a name="user_verification1"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.user_verification1") user_verification1

> User Verification API

```python
def user_verification1(self,
                           body,
                           content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiVU()
content_type = 'Content-Type'

result = verification_client.user_verification1(body, content_type)

```


### <a name="cellphone_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.cellphone_verification") cellphone_verification

> Verification API

```python
def cellphone_verification(self,
                               key,
                               uid,
                               to,
                               content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
key = 'key'
uid = 'uid'
to = 'to'
content_type = 'Content-Type'

result = verification_client.cellphone_verification(key, uid, to, content_type)

```


### <a name="cellphone_verification1"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.cellphone_verification1") cellphone_verification1

> Verification API

```python
def cellphone_verification1(self,
                                body,
                                content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiV()
content_type = 'Content-Type'

result = verification_client.cellphone_verification1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPI") TwoFactorAuthenticationAPI

### Get controller instance

An instance of the ``` TwoFactorAuthenticationAPI ``` class can be accessed from the API Client.

```python
 two_factor_authentication_api_client = client.two_factor_authentication_api
```

### <a name="2_fa_token_response"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.2_fa_token_response") 2_fa_token_response

> Two Factor Authentication Token Reply

```python
def 2_fa_token_response(self,
                            key,
                            uid,
                            user,
                            code,
                            content_type)
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

```python
key = 'key'
uid = 'uid'
user = 'user'
code = 'code'
content_type = 'Content-Type'

result = two_factor_authentication_api_client.2_fa_token_response(key, uid, user, code, content_type)

```


### <a name="2_fa_token_response1"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.2_fa_token_response1") 2_fa_token_response1

> Two Factor Authentication Token Reply

```python
def 2_fa_token_response1(self,
                             body,
                             content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApi2faT()
content_type = 'Content-Type'

result = two_factor_authentication_api_client.2_fa_token_response1(body, content_type)

```


### <a name="two_factor_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.two_factor_authentication") two_factor_authentication

> Two Factor Authentication API

```python
def two_factor_authentication(self,
                                  key,
                                  uid,
                                  to,
                                  content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
key = 'key'
uid = 'uid'
to = 'to'
content_type = 'Content-Type'

result = two_factor_authentication_api_client.two_factor_authentication(key, uid, to, content_type)

```


### <a name="two_factor_authentication1"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.two_factor_authentication1") two_factor_authentication1

> Two Factor Authentication API

```python
def two_factor_authentication1(self,
                                   body,
                                   content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApi2fa()
content_type = 'Content-Type'

result = two_factor_authentication_api_client.two_factor_authentication1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagement") UserManagement

### Get controller instance

An instance of the ``` UserManagement ``` class can be accessed from the API Client.

```python
 user_management_client = client.user_management
```

### <a name="get_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.get_user_info") get_user_info

> Get User Info API

```python
def get_user_info(self,
                      key,
                      uid,
                      user,
                      apiuid,
                      content_type)
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

```python
key = 'key'
uid = 'uid'
user = 'user'
apiuid = 'apiuid'
content_type = 'Content-Type'

result = user_management_client.get_user_info(key, uid, user, apiuid, content_type)

```


### <a name="get_user_info1"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.get_user_info1") get_user_info1

> Get User Info API

```python
def get_user_info1(self,
                       body,
                       content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiUI()
content_type = 'Content-Type'

result = user_management_client.get_user_info1(body, content_type)

```


### <a name="update_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.update_user") update_user

> Update User API

```python
def update_user(self,
                    key,
                    uid,
                    user,
                    apiuid,
                    avatar,
                    custom_input,
                    content_type)
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

```python
key = 'key'
uid = 'uid'
user = 'user'
apiuid = 'apiuid'
avatar = 'avatar'
custom_input = 'custom input'
content_type = 'Content-Type'

result = user_management_client.update_user(key, uid, user, apiuid, avatar, custom_input, content_type)

```


### <a name="update_user1"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.update_user1") update_user1

> Update User API

```python
def update_user1(self,
                     body,
                     content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiUU()
content_type = 'Content-Type'

result = user_management_client.update_user1(body, content_type)

```


### <a name="delete_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.delete_user") delete_user

> Delete User API

```python
def delete_user(self,
                    api,
                    uid,
                    user,
                    apiuid,
                    content_type)
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

```python
api = 'api'
uid = 'uid'
user = 'user'
apiuid = 'apiuid'
content_type = 'Content-Type'

result = user_management_client.delete_user(api, uid, user, apiuid, content_type)

```


### <a name="delete_user1"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.delete_user1") delete_user1

> Delete User API

```python
def delete_user1(self,
                     body,
                     content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiUD()
content_type = 'Content-Type'

result = user_management_client.delete_user1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistration") LoginAndRegistration

### Get controller instance

An instance of the ``` LoginAndRegistration ``` class can be accessed from the API Client.

```python
 login_and_registration_client = client.login_and_registration
```

### <a name="user_registration"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.user_registration") user_registration

> User Registration API

```python
def user_registration(self,
                          key,
                          uid,
                          user,
                          password,
                          name,
                          email,
                          phone,
                          countrycode,
                          address,
                          content_type)
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

```python
key = 'key'
uid = 'uid'
user = 'user'
password = 'password'
name = 'name'
email = 'email'
phone = 216
countrycode = 216
address = 'address'
content_type = 'Content-Type'

result = login_and_registration_client.user_registration(key, uid, user, password, name, email, phone, countrycode, address, content_type)

```


### <a name="user_registration1"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.user_registration1") user_registration1

> User Registration API

```python
def user_registration1(self,
                           body,
                           content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiAUR()
content_type = 'Content-Type'

result = login_and_registration_client.user_registration1(body, content_type)

```


### <a name="user_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.user_authentication") user_authentication

> User Authentication API

```python
def user_authentication(self,
                            key,
                            uid,
                            user,
                            password,
                            content_type)
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

```python
key = 'key'
uid = 'uid'
user = 'user'
password = 'password'
content_type = 'Content-Type'

result = login_and_registration_client.user_authentication(key, uid, user, password, content_type)

```


### <a name="user_authentication1"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.user_authentication1") user_authentication1

> User Authentication API

```python
def user_authentication1(self,
                             body,
                             content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = HttpsApiRestShApiAUL()
content_type = 'Content-Type'

result = login_and_registration_client.user_authentication1(body, content_type)

```


[Back to List of Controllers](#list_of_controllers)



