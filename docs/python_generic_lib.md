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
| key | Your API Key |
| uid | Your User ID |



API client can be initialized as following.

```python
# Configuration parameters and credentials
key = 'API' # Your API Key
uid = 'UID' # Your User ID

client = SMASH(key, uid)
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

### Get controller instance

An instance of the ``` AdvancedLoggingController ``` class can be accessed from the API Client.

```python
 advanced_logging_client = client.advanced_logging
```

### <a name="get_https_api_rest_sh_api_s_l_i"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.get_https_api_rest_sh_api_s_l_i") get_https_api_rest_sh_api_s_l_i

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info

```python
def get_https_api_rest_sh_api_s_l_i(self,
                                        options=dict())
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
collect = {}

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


result = advanced_logging_client.get_https_api_rest_sh_api_s_l_i(collect)

```


### <a name="get_https_api_rest_sh_api_s_l"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.get_https_api_rest_sh_api_s_l") get_https_api_rest_sh_api_s_l

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup

```python
def get_https_api_rest_sh_api_s_l(self,
                                      options=dict())
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
collect = {}

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

name = 'name'
collect['name'] = name

origin = 'origin'
collect['origin'] = origin

activate = False
collect['activate'] = activate

content_type = 'Content-Type'
collect['content_type'] = content_type


result = advanced_logging_client.get_https_api_rest_sh_api_s_l(collect)

```


### <a name="create_https_api_rest_sh_api_s_l_i"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.create_https_api_rest_sh_api_s_l_i") create_https_api_rest_sh_api_s_l_i

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info

```python
def create_https_api_rest_sh_api_s_l_i(self,
                                           options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiSLIModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = advanced_logging_client.create_https_api_rest_sh_api_s_l_i(collect)

```


### <a name="create_https_api_rest_sh_api_s_l"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.create_https_api_rest_sh_api_s_l") create_https_api_rest_sh_api_s_l

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup

```python
def create_https_api_rest_sh_api_s_l(self,
                                         options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiSLModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = advanced_logging_client.create_https_api_rest_sh_api_s_l(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection_controller"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtectionController") WAFDDOSProtectionController

### Get controller instance

An instance of the ``` WAFDDOSProtectionController ``` class can be accessed from the API Client.

```python
 waf_ddos_protection_client = client.waf_ddos_protection
```

### <a name="get_https_api_rest_sh_api_s_w_c"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.get_https_api_rest_sh_api_s_w_c") get_https_api_rest_sh_api_s_w_c

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description

```python
def get_https_api_rest_sh_api_s_w_c(self,
                                        options=dict())
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
collect = {}

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


result = waf_ddos_protection_client.get_https_api_rest_sh_api_s_w_c(collect)

```


### <a name="get_https_api_rest_sh_api_s_w"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.get_https_api_rest_sh_api_s_w") get_https_api_rest_sh_api_s_w

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description

```python
def get_https_api_rest_sh_api_s_w(self,
                                      options=dict())
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
collect = {}

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


result = waf_ddos_protection_client.get_https_api_rest_sh_api_s_w(collect)

```


### <a name="create_https_api_rest_sh_api_s_w_c"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.create_https_api_rest_sh_api_s_w_c") create_https_api_rest_sh_api_s_w_c

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description

```python
def create_https_api_rest_sh_api_s_w_c(self,
                                           options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body_value = "{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}"
body = json.loads(body_value)
collect['body'] = body

content_type = 'application/json'
collect['content_type'] = content_type


result = waf_ddos_protection_client.create_https_api_rest_sh_api_s_w_c(collect)

```


### <a name="create_https_api_rest_sh_api_s_w"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.create_https_api_rest_sh_api_s_w") create_https_api_rest_sh_api_s_w

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description

```python
def create_https_api_rest_sh_api_s_w(self,
                                         options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body_value = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}"
body = json.loads(body_value)
collect['body'] = body

content_type = 'application/json'
collect['content_type'] = content_type


result = waf_ddos_protection_client.create_https_api_rest_sh_api_s_w(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EncryptionController") EncryptionController

### Get controller instance

An instance of the ``` EncryptionController ``` class can be accessed from the API Client.

```python
 encryption_client = client.encryption
```

### <a name="get_https_api_rest_sh_api_s_e"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.get_https_api_rest_sh_api_s_e") get_https_api_rest_sh_api_s_e

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API

```python
def get_https_api_rest_sh_api_s_e(self,
                                      options=dict())
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
collect = {}

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

data = 'data'
collect['data'] = data

method = 'method'
collect['method'] = method

bit = 12
collect['bit'] = bit

content_type = 'Content-Type'
collect['content_type'] = content_type


result = encryption_client.get_https_api_rest_sh_api_s_e(collect)

```


### <a name="create_https_api_rest_sh_api_s_e"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.create_https_api_rest_sh_api_s_e") create_https_api_rest_sh_api_s_e

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API

```python
def create_https_api_rest_sh_api_s_e(self,
                                         options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiSEModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = encryption_client.create_https_api_rest_sh_api_s_e(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CDNController") CDNController

### Get controller instance

An instance of the ``` CDNController ``` class can be accessed from the API Client.

```python
 cdn_client = client.cdn
```

### <a name="get_https_api_rest_sh_api_s_c_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.get_https_api_rest_sh_api_s_c_push") get_https_api_rest_sh_api_s_c_push

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API

```python
def get_https_api_rest_sh_api_s_c_push(self,
                                           options=dict())
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
collect = {}

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


result = cdn_client.get_https_api_rest_sh_api_s_c_push(collect)

```


### <a name="get_https_api_rest_sh_api_s_c_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.get_https_api_rest_sh_api_s_c_pull") get_https_api_rest_sh_api_s_c_pull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API

```python
def get_https_api_rest_sh_api_s_c_pull(self,
                                           options=dict())
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
collect = {}

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


result = cdn_client.get_https_api_rest_sh_api_s_c_pull(collect)

```


### <a name="create_https_api_rest_sh_api_s_c_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.create_https_api_rest_sh_api_s_c_push") create_https_api_rest_sh_api_s_c_push

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API

```python
def create_https_api_rest_sh_api_s_c_push(self,
                                              options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiSCPushModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = cdn_client.create_https_api_rest_sh_api_s_c_push(collect)

```


### <a name="create_https_api_rest_sh_api_s_c_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.create_https_api_rest_sh_api_s_c_pull") create_https_api_rest_sh_api_s_c_pull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API

```python
def create_https_api_rest_sh_api_s_c_pull(self,
                                              options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiSCPullModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = cdn_client.create_https_api_rest_sh_api_s_c_pull(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DNSController") DNSController

### Get controller instance

An instance of the ``` DNSController ``` class can be accessed from the API Client.

```python
 dns_client = client.dns
```

### <a name="get_https_api_rest_sh_api_s_d_c"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.get_https_api_rest_sh_api_s_d_c") get_https_api_rest_sh_api_s_d_c

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API

```python
def get_https_api_rest_sh_api_s_d_c(self,
                                        options=dict())
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
collect = {}

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


result = dns_client.get_https_api_rest_sh_api_s_d_c(collect)

```


### <a name="create_https_api_rest_sh_api_s_d_c"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.create_https_api_rest_sh_api_s_d_c") create_https_api_rest_sh_api_s_d_c

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API

```python
def create_https_api_rest_sh_api_s_d_c(self,
                                           options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiSDCModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = dns_client.create_https_api_rest_sh_api_s_d_c(collect)

```


### <a name="get_https_api_rest_sh_api_s_d_a"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.get_https_api_rest_sh_api_s_d_a") get_https_api_rest_sh_api_s_d_a

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API

```python
def get_https_api_rest_sh_api_s_d_a(self,
                                        options=dict())
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
collect = {}

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

domain = 'domain'
collect['domain'] = domain

content_type = 'Content-Type'
collect['content_type'] = content_type


result = dns_client.get_https_api_rest_sh_api_s_d_a(collect)

```


### <a name="create_https_api_rest_sh_api_s_d_a"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.create_https_api_rest_sh_api_s_d_a") create_https_api_rest_sh_api_s_d_a

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API

```python
def create_https_api_rest_sh_api_s_d_a(self,
                                           options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiSDAModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = dns_client.create_https_api_rest_sh_api_s_d_a(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscationController") CodeObfuscationController

### Get controller instance

An instance of the ``` CodeObfuscationController ``` class can be accessed from the API Client.

```python
 code_obfuscation_client = client.code_obfuscation
```

### <a name="get_https_api_rest_sh_api_s_o"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.get_https_api_rest_sh_api_s_o") get_https_api_rest_sh_api_s_o

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API

```python
def get_https_api_rest_sh_api_s_o(self,
                                      options=dict())
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
collect = {}

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

app = 'app'
collect['app'] = app

content_type = 'Content-Type'
collect['content_type'] = content_type


result = code_obfuscation_client.get_https_api_rest_sh_api_s_o(collect)

```


### <a name="create_https_api_rest_sh_api_s_o"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.create_https_api_rest_sh_api_s_o") create_https_api_rest_sh_api_s_o

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API

```python
def create_https_api_rest_sh_api_s_o(self,
                                         options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiSOModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = code_obfuscation_client.create_https_api_rest_sh_api_s_o(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting_controller"></a>![Class: ](https://apidocs.io/img/class.png ".HostingController") HostingController

### Get controller instance

An instance of the ``` HostingController ``` class can be accessed from the API Client.

```python
 hosting_client = client.hosting
```

### <a name="get_https_api_rest_sh_api_s_h"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.get_https_api_rest_sh_api_s_h") get_https_api_rest_sh_api_s_h

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting

```python
def get_https_api_rest_sh_api_s_h(self,
                                      options=dict())
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
collect = {}

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


result = hosting_client.get_https_api_rest_sh_api_s_h(collect)

```


### <a name="create_https_api_rest_sh_api_s_h"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.create_https_api_rest_sh_api_s_h") create_https_api_rest_sh_api_s_h

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting

```python
def create_https_api_rest_sh_api_s_h(self,
                                         options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiSHModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = hosting_client.create_https_api_rest_sh_api_s_h(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPIController") DataManipulationConversionSortingAndCompressionAPIController

### Get controller instance

An instance of the ``` DataManipulationConversionSortingAndCompressionAPIController ``` class can be accessed from the API Client.

```python
 data_manipulation_conversion_sorting_and_compression_api_client = client.data_manipulation_conversion_sorting_and_compression_api
```

### <a name="get_https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.get_https_api_rest_sh_api_d") get_https_api_rest_sh_api_d

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description

```python
def get_https_api_rest_sh_api_d(self,
                                    options=dict())
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
collect = {}

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


result = data_manipulation_conversion_sorting_and_compression_api_client.get_https_api_rest_sh_api_d(collect)

```


### <a name="create_https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.create_https_api_rest_sh_api_d") create_https_api_rest_sh_api_d

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description

```python
def create_https_api_rest_sh_api_d(self,
                                       options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body_value = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}"
body = json.loads(body_value)
collect['body'] = body

content_type = 'application/json'
collect['content_type'] = content_type


result = data_manipulation_conversion_sorting_and_compression_api_client.create_https_api_rest_sh_api_d(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPIController") ImageManipulationAndModerationAPIController

### Get controller instance

An instance of the ``` ImageManipulationAndModerationAPIController ``` class can be accessed from the API Client.

```python
 image_manipulation_and_moderation_api_client = client.image_manipulation_and_moderation_api
```

### <a name="get_https_api_rest_sh_api_i"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.get_https_api_rest_sh_api_i") get_https_api_rest_sh_api_i

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API

```python
def get_https_api_rest_sh_api_i(self,
                                    options=dict())
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
collect = {}

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


result = image_manipulation_and_moderation_api_client.get_https_api_rest_sh_api_i(collect)

```


### <a name="create_https_api_rest_sh_api_i"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.create_https_api_rest_sh_api_i") create_https_api_rest_sh_api_i

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API

```python
def create_https_api_rest_sh_api_i(self,
                                       options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiIModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = image_manipulation_and_moderation_api_client.create_https_api_rest_sh_api_i(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VerificationController") VerificationController

### Get controller instance

An instance of the ``` VerificationController ``` class can be accessed from the API Client.

```python
 verification_client = client.verification
```

### <a name="get_https_api_rest_sh_api_v_a"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.get_https_api_rest_sh_api_v_a") get_https_api_rest_sh_api_v_a

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API

```python
def get_https_api_rest_sh_api_v_a(self,
                                      options=dict())
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
collect = {}

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

z = 225
collect['z'] = z

content_type = 'Content-Type'
collect['content_type'] = content_type


result = verification_client.get_https_api_rest_sh_api_v_a(collect)

```


### <a name="create_https_api_rest_sh_api_v_a"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.create_https_api_rest_sh_api_v_a") create_https_api_rest_sh_api_v_a

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API

```python
def create_https_api_rest_sh_api_v_a(self,
                                         options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiVAModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = verification_client.create_https_api_rest_sh_api_v_a(collect)

```


### <a name="get_https_api_rest_sh_api_v_u"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.get_https_api_rest_sh_api_v_u") get_https_api_rest_sh_api_v_u

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API

```python
def get_https_api_rest_sh_api_v_u(self,
                                      options=dict())
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
collect = {}

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


result = verification_client.get_https_api_rest_sh_api_v_u(collect)

```


### <a name="create_https_api_rest_sh_api_v_u"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.create_https_api_rest_sh_api_v_u") create_https_api_rest_sh_api_v_u

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API

```python
def create_https_api_rest_sh_api_v_u(self,
                                         options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiVUModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = verification_client.create_https_api_rest_sh_api_v_u(collect)

```


### <a name="get_https_api_rest_sh_api_v"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.get_https_api_rest_sh_api_v") get_https_api_rest_sh_api_v

> *Tags:*  ``` Skips Authentication ``` 

> Verification API

```python
def get_https_api_rest_sh_api_v(self,
                                    options=dict())
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
collect = {}

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

to = 'to'
collect['to'] = to

content_type = 'Content-Type'
collect['content_type'] = content_type


result = verification_client.get_https_api_rest_sh_api_v(collect)

```


### <a name="create_https_api_rest_sh_api_v"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.create_https_api_rest_sh_api_v") create_https_api_rest_sh_api_v

> *Tags:*  ``` Skips Authentication ``` 

> Verification API

```python
def create_https_api_rest_sh_api_v(self,
                                       options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiVModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = verification_client.create_https_api_rest_sh_api_v(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPIController") TwoFactorAuthenticationAPIController

### Get controller instance

An instance of the ``` TwoFactorAuthenticationAPIController ``` class can be accessed from the API Client.

```python
 two_factor_authentication_api_client = client.two_factor_authentication_api
```

### <a name="get_https_api_rest_sh_api_2_fa_t"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.get_https_api_rest_sh_api_2_fa_t") get_https_api_rest_sh_api_2_fa_t

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply

```python
def get_https_api_rest_sh_api_2_fa_t(self,
                                         options=dict())
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
collect = {}

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


result = two_factor_authentication_api_client.get_https_api_rest_sh_api_2_fa_t(collect)

```


### <a name="create_https_api_rest_sh_api_2_fa_t"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.create_https_api_rest_sh_api_2_fa_t") create_https_api_rest_sh_api_2_fa_t

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply

```python
def create_https_api_rest_sh_api_2_fa_t(self,
                                            options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApi2faTModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = two_factor_authentication_api_client.create_https_api_rest_sh_api_2_fa_t(collect)

```


### <a name="get_https_api_rest_sh_api_2_fa"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.get_https_api_rest_sh_api_2_fa") get_https_api_rest_sh_api_2_fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API

```python
def get_https_api_rest_sh_api_2_fa(self,
                                       options=dict())
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
collect = {}

key = 'key'
collect['key'] = key

uid = 'uid'
collect['uid'] = uid

to = 'to'
collect['to'] = to

content_type = 'Content-Type'
collect['content_type'] = content_type


result = two_factor_authentication_api_client.get_https_api_rest_sh_api_2_fa(collect)

```


### <a name="create_https_api_rest_sh_api_2_fa"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.create_https_api_rest_sh_api_2_fa") create_https_api_rest_sh_api_2_fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API

```python
def create_https_api_rest_sh_api_2_fa(self,
                                          options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApi2faModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = two_factor_authentication_api_client.create_https_api_rest_sh_api_2_fa(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagementController") UserManagementController

### Get controller instance

An instance of the ``` UserManagementController ``` class can be accessed from the API Client.

```python
 user_management_client = client.user_management
```

### <a name="get_https_api_rest_sh_api_u_i"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.get_https_api_rest_sh_api_u_i") get_https_api_rest_sh_api_u_i

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API

```python
def get_https_api_rest_sh_api_u_i(self,
                                      options=dict())
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
collect = {}

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


result = user_management_client.get_https_api_rest_sh_api_u_i(collect)

```


### <a name="create_https_api_rest_sh_api_u_i"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.create_https_api_rest_sh_api_u_i") create_https_api_rest_sh_api_u_i

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API

```python
def create_https_api_rest_sh_api_u_i(self,
                                         options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiUIModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = user_management_client.create_https_api_rest_sh_api_u_i(collect)

```


### <a name="get_https_api_rest_sh_api_u_u"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.get_https_api_rest_sh_api_u_u") get_https_api_rest_sh_api_u_u

> *Tags:*  ``` Skips Authentication ``` 

> Update User API

```python
def get_https_api_rest_sh_api_u_u(self,
                                      options=dict())
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
collect = {}

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


result = user_management_client.get_https_api_rest_sh_api_u_u(collect)

```


### <a name="create_https_api_rest_sh_api_u_u"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.create_https_api_rest_sh_api_u_u") create_https_api_rest_sh_api_u_u

> *Tags:*  ``` Skips Authentication ``` 

> Update User API

```python
def create_https_api_rest_sh_api_u_u(self,
                                         options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiUUModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = user_management_client.create_https_api_rest_sh_api_u_u(collect)

```


### <a name="get_https_api_rest_sh_api_u_d"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.get_https_api_rest_sh_api_u_d") get_https_api_rest_sh_api_u_d

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API

```python
def get_https_api_rest_sh_api_u_d(self,
                                      options=dict())
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
collect = {}

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


result = user_management_client.get_https_api_rest_sh_api_u_d(collect)

```


### <a name="create_https_api_rest_sh_api_u_d"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.create_https_api_rest_sh_api_u_d") create_https_api_rest_sh_api_u_d

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API

```python
def create_https_api_rest_sh_api_u_d(self,
                                         options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiUDModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = user_management_client.create_https_api_rest_sh_api_u_d(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration_controller"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistrationController") LoginAndRegistrationController

### Get controller instance

An instance of the ``` LoginAndRegistrationController ``` class can be accessed from the API Client.

```python
 login_and_registration_client = client.login_and_registration
```

### <a name="get_https_api_rest_sh_api_a_u_r"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.get_https_api_rest_sh_api_a_u_r") get_https_api_rest_sh_api_a_u_r

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API

```python
def get_https_api_rest_sh_api_a_u_r(self,
                                        options=dict())
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
collect = {}

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

phone = 61
collect['phone'] = phone

countrycode = 61
collect['countrycode'] = countrycode

address = 'address'
collect['address'] = address

content_type = 'Content-Type'
collect['content_type'] = content_type


result = login_and_registration_client.get_https_api_rest_sh_api_a_u_r(collect)

```


### <a name="create_https_api_rest_sh_api_a_u_r"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.create_https_api_rest_sh_api_a_u_r") create_https_api_rest_sh_api_a_u_r

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API

```python
def create_https_api_rest_sh_api_a_u_r(self,
                                           options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiAURModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = login_and_registration_client.create_https_api_rest_sh_api_a_u_r(collect)

```


### <a name="get_https_api_rest_sh_api_a_u_l"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.get_https_api_rest_sh_api_a_u_l") get_https_api_rest_sh_api_a_u_l

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API

```python
def get_https_api_rest_sh_api_a_u_l(self,
                                        options=dict())
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
collect = {}

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


result = login_and_registration_client.get_https_api_rest_sh_api_a_u_l(collect)

```


### <a name="create_https_api_rest_sh_api_a_u_l"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.create_https_api_rest_sh_api_a_u_l") create_https_api_rest_sh_api_a_u_l

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API

```python
def create_https_api_rest_sh_api_a_u_l(self,
                                           options=dict())
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
collect = {}

body = HttpsApiRestShApiAULModel()
collect['body'] = body

content_type = 'Content-Type'
collect['content_type'] = content_type


result = login_and_registration_client.create_https_api_rest_sh_api_a_u_l(collect)

```


[Back to List of Controllers](#list_of_controllers)



