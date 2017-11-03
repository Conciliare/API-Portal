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


* In order to successfully build and run your SDK files, you are required to have the following setup in your system:
    * **Go**  (Visit [https://golang.org/doc/install](https://golang.org/doc/install) for more details on how to install Go)
    * **Java VM** Version 8 or later
    * **Eclipse 4.6 (Neon)** or later ([http://www.eclipse.org/neon/](http://www.eclipse.org/neon/))
    * **GoClipse** setup within above installed Eclipse (Follow the instructions at [this link](https://github.com/GoClipse/goclipse/blob/latest/documentation/Installation.md#instructions) to setup GoClipse)
* Ensure that ```GOPATH``` environment variable is set in the system variables. If not, set it to your workspace directory where you will be adding your Go projects.
* The generated code uses unirest-go http library. Therefore, you will need internet access to resolve this dependency. If Go is properly installed and configured, run the following command to pull the dependency:

```Go
go get github.com/apimatic/unirest-go
```

This will install unirest-go in the ```GOPATH``` you specified in the system variables.

Now follow the steps mentioned below to build your SDK:

1. Open eclipse in the Go language perspective and click on the ```Import``` option in ```File``` menu.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/go?step=import0)

2. Select ```General -> Existing Projects into Workspace``` option from the tree list.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/go?step=import1)

3. In ```Select root directory```, provide path to the unzipped archive for the generated code. Once the path is set and the Project becomes visible under ```Projects``` click ```Finish```

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/go?step=import2&workspaceFolder=SMASH-GoLang&projectName=smash_lib)

4. The Go library will be imported and its files will be visible in the Project Explorer

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/go?step=import3&projectName=smash_lib)

## How to Use

The following section explains how to use the SMASH library in a new project.

### 1. Add a new Test Project

Create a new project in Eclipse by ```File``` -> ```New``` -> ```Go Project```

![Add a new project in Eclipse](https://apidocs.io/illustration/go?step=createNewProject0)

Name the Project as ```Test``` and click ```Finish```

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/go?step=createNewProject1)

Create a new directory in the ```src``` directory of this project

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/go?step=createNewProject2&projectName=smash_lib)

Name it ```test.com```

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/go?step=createNewProject3&projectName=smash_lib)

Now create a new file inside ```src/test.com```

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/go?step=createNewProject4&projectName=smash_lib)

Name it ```testsdk.go```

![Create a new Maven Project - Step 5](https://apidocs.io/illustration/go?step=createNewProject5&projectName=smash_lib)

In this Go file, you can start adding code to initialize the client library. Sample code to initialize the client library and using its methods is given in the subsequent sections.

### 2. Configure the Test Project

You need to import your generated library in this project in order to make use of its functions. In order to import the library, you can add its path in the ```GOPATH``` for this project. Follow the below steps:

Right click on the project name and click on ```Properties```

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/go?step=testProject0&projectName=smash_lib)

Choose ```Go Compiler``` from the side menu. Check ```Use project specific settings``` and uncheck ```Use same value as the GOPATH environment variable.```. By default, the GOPATH value from the environment variables will be visible in ```Eclipse GOPATH```. Do not remove this as this points to the unirest dependency.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/go?step=testProject1)

Append the library path to this GOPATH

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/go?step=testProject2&workspaceFolder=SMASH-GoLang)

Once the path is appended, click on ```OK```

### 3. Build the Test Project

Right click on the project name and click on ```Build Project```

![Build Project](https://apidocs.io/illustration/go?step=buildProject&projectName=smash_lib)

### 4. Run the Test Project

If the build is successful, right click on your Go file and click on ```Run As``` -> ```Go Application```

![Run Project](https://apidocs.io/illustration/go?step=runProject&projectName=smash_lib)

## Initialization

### Authentication
In order to setup authentication of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| key | Your API Key |
| uid | Your User ID |


To configure these for your generated code, open the file "Configuration.go" and edit it's contents.


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [advancedlogging_pkg](#advancedlogging_pkg)
* [waf&ddosprotection_pkg](#waf&ddosprotection_pkg)
* [encryption_pkg](#encryption_pkg)
* [cdn_pkg](#cdn_pkg)
* [dns_pkg](#dns_pkg)
* [codeobfuscation_pkg](#codeobfuscation_pkg)
* [hosting_pkg](#hosting_pkg)
* [datamanipulation,conversion,sorting,andcompressionapi_pkg](#datamanipulation,conversion,sorting,andcompressionapi_pkg)
* [imagemanipulationandmoderationapi_pkg](#imagemanipulationandmoderationapi_pkg)
* [verification_pkg](#verification_pkg)
* [twofactorauthenticationapi_pkg](#twofactorauthenticationapi_pkg)
* [usermanagement_pkg](#usermanagement_pkg)
* [loginandregistration_pkg](#loginandregistration_pkg)

## <a name="advancedlogging_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".advancedlogging_pkg") advancedlogging_pkg

### Get instance

Factory for the ``` ADVANCEDLOGGING ``` interface can be accessed from the package advancedlogging_pkg.

```go
advancedLogging := advancedlogging_pkg.NewADVANCEDLOGGING()
```

### <a name="get_https_api_rest_sh_api_security_logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".advancedlogging_pkg.GetHttpsApiRestShApiSecurityLoggingInfo") GetHttpsApiRestShApiSecurityLoggingInfo

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```go
func (me *ADVANCEDLOGGING_IMPL) GetHttpsApiRestShApiSecurityLoggingInfo(input *GetHttpsApiRestShApiSecurityLoggingInfoInput)(*models_pkg.HttpsApiRestShApiSecurityLoggingInfoResponseModel,error)
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

```go
collect := new (advancedlogging_pkg.GetHttpsApiRestShApiSecurityLoggingInfoInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

name := "name"
collect.Name = name

origin := "origin"
collect.Origin = origin

time := "time"
collect.Time = time

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSecurityLoggingInfoResponseModel
result,_ = advancedLogging.GetHttpsApiRestShApiSecurityLoggingInfo(collect)

```


### <a name="get_https_api_rest_sh_api_security_logging"></a>![Method: ](https://apidocs.io/img/method.png ".advancedlogging_pkg.GetHttpsApiRestShApiSecurityLogging") GetHttpsApiRestShApiSecurityLogging

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```go
func (me *ADVANCEDLOGGING_IMPL) GetHttpsApiRestShApiSecurityLogging(input *GetHttpsApiRestShApiSecurityLoggingInput)(*models_pkg.HttpsApiRestShApiSecurityLoggingResponseModel,error)
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

```go
collect := new (advancedlogging_pkg.GetHttpsApiRestShApiSecurityLoggingInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

name := "name"
collect.Name = name

origin := "origin"
collect.Origin = origin

activate := true
collect.Activate = activate

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSecurityLoggingResponseModel
result,_ = advancedLogging.GetHttpsApiRestShApiSecurityLogging(collect)

```


### <a name="create_https_api_rest_sh_api_security_logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".advancedlogging_pkg.CreateHttpsApiRestShApiSecurityLoggingInfo") CreateHttpsApiRestShApiSecurityLoggingInfo

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```go
func (me *ADVANCEDLOGGING_IMPL) CreateHttpsApiRestShApiSecurityLoggingInfo(input *CreateHttpsApiRestShApiSecurityLoggingInfoInput)(*models_pkg.HttpsApiRestShApiSecurityLoggingInfoResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (advancedlogging_pkg.CreateHttpsApiRestShApiSecurityLoggingInfoInput)

var body *models_pkg.HttpsApiRestShApiSecurityLoggingInfoRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSecurityLoggingInfoResponseModel
result,_ = advancedLogging.CreateHttpsApiRestShApiSecurityLoggingInfo(collect)

```


### <a name="create_https_api_rest_sh_api_security_logging"></a>![Method: ](https://apidocs.io/img/method.png ".advancedlogging_pkg.CreateHttpsApiRestShApiSecurityLogging") CreateHttpsApiRestShApiSecurityLogging

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```go
func (me *ADVANCEDLOGGING_IMPL) CreateHttpsApiRestShApiSecurityLogging(input *CreateHttpsApiRestShApiSecurityLoggingInput)(*models_pkg.HttpsApiRestShApiSecurityLoggingResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (advancedlogging_pkg.CreateHttpsApiRestShApiSecurityLoggingInput)

var body *models_pkg.HttpsApiRestShApiSecurityLoggingRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSecurityLoggingResponseModel
result,_ = advancedLogging.CreateHttpsApiRestShApiSecurityLogging(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="waf&ddosprotection_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".waf&ddosprotection_pkg") waf&ddosprotection_pkg

### Get instance

Factory for the ``` WAF&DDOSPROTECTION ``` interface can be accessed from the package waf&ddosprotection_pkg.

```go
wAFDDOSProtection := waf&ddosprotection_pkg.NewWAF&DDOSPROTECTION()
```

### <a name="get_https_api_rest_sh_api_security_waf_configure"></a>![Method: ](https://apidocs.io/img/method.png ".waf&ddosprotection_pkg.GetHttpsApiRestShApiSecurityWafConfigure") GetHttpsApiRestShApiSecurityWafConfigure

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *WAFDDOSPROTECTION_IMPL) GetHttpsApiRestShApiSecurityWafConfigure(input *GetHttpsApiRestShApiSecurityWafConfigureInput)(*models_pkg.HttpsApiRestShApiSecurityWafConfigureResponseModel,error)
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

```go
collect := new (waf&ddosprotection_pkg.GetHttpsApiRestShApiSecurityWafConfigureInput)

key := "API"
collect.Key = key

uid := "UID"
collect.Uid = uid

name := "origin-name"
collect.Name = name

origin := "origin.yourdomain.tld"
collect.Origin = origin

rule := "header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does"
collect.Rule = rule

contentType := "application/json"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSecurityWafConfigureResponseModel
result,_ = wAFDDOSProtection.GetHttpsApiRestShApiSecurityWafConfigure(collect)

```


### <a name="get_https_api_rest_sh_api_security_waf"></a>![Method: ](https://apidocs.io/img/method.png ".waf&ddosprotection_pkg.GetHttpsApiRestShApiSecurityWaf") GetHttpsApiRestShApiSecurityWaf

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *WAFDDOSPROTECTION_IMPL) GetHttpsApiRestShApiSecurityWaf(input *GetHttpsApiRestShApiSecurityWafInput)(*models_pkg.HttpsApiRestShApiSecurityWafResponseModel,error)
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

```go
collect := new (waf&ddosprotection_pkg.GetHttpsApiRestShApiSecurityWafInput)

key := "API"
collect.Key = key

uid := "UID"
collect.Uid = uid

origin := "origin.yourdomain.tld"
collect.Origin = origin

cname := "yourdomain.tld,www.yourdomain.tld"
collect.Cname = cname

contentType := "application/json"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSecurityWafResponseModel
result,_ = wAFDDOSProtection.GetHttpsApiRestShApiSecurityWaf(collect)

```


### <a name="create_https_api_rest_sh_api_security_waf_configure"></a>![Method: ](https://apidocs.io/img/method.png ".waf&ddosprotection_pkg.CreateHttpsApiRestShApiSecurityWafConfigure") CreateHttpsApiRestShApiSecurityWafConfigure

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *WAFDDOSPROTECTION_IMPL) CreateHttpsApiRestShApiSecurityWafConfigure(input *CreateHttpsApiRestShApiSecurityWafConfigureInput)(*models_pkg.HttpsApiRestShApiSecurityWafConfigureResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (waf&ddosprotection_pkg.CreateHttpsApiRestShApiSecurityWafConfigureInput)

bodyValue := []byte("{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}")
var body *models_pkg.HttpsApiRestShApiSecurityWafConfigureRequestModel
json.Unmarshal(bodyValue,&body)
collect.Body = body

contentType := "application/json"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSecurityWafConfigureResponseModel
result,_ = wAFDDOSProtection.CreateHttpsApiRestShApiSecurityWafConfigure(collect)

```


### <a name="create_https_api_rest_sh_api_security_waf"></a>![Method: ](https://apidocs.io/img/method.png ".waf&ddosprotection_pkg.CreateHttpsApiRestShApiSecurityWaf") CreateHttpsApiRestShApiSecurityWaf

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *WAFDDOSPROTECTION_IMPL) CreateHttpsApiRestShApiSecurityWaf(input *CreateHttpsApiRestShApiSecurityWafInput)(*models_pkg.HttpsApiRestShApiSecurityWafResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (waf&ddosprotection_pkg.CreateHttpsApiRestShApiSecurityWafInput)

bodyValue := []byte("{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}")
var body *models_pkg.HttpsApiRestShApiSecurityWafRequestModel
json.Unmarshal(bodyValue,&body)
collect.Body = body

contentType := "application/json"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSecurityWafResponseModel
result,_ = wAFDDOSProtection.CreateHttpsApiRestShApiSecurityWaf(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".encryption_pkg") encryption_pkg

### Get instance

Factory for the ``` ENCRYPTION ``` interface can be accessed from the package encryption_pkg.

```go
encryption := encryption_pkg.NewENCRYPTION()
```

### <a name="get_https_api_rest_sh_api_security_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".encryption_pkg.GetHttpsApiRestShApiSecurityEncryption") GetHttpsApiRestShApiSecurityEncryption

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```go
func (me *ENCRYPTION_IMPL) GetHttpsApiRestShApiSecurityEncryption(input *GetHttpsApiRestShApiSecurityEncryptionInput)(*models_pkg.HttpsApiRestShApiSecurityEncryptionResponseModel,error)
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

```go
collect := new (encryption_pkg.GetHttpsApiRestShApiSecurityEncryptionInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

data := "data"
collect.Data = data

method := "method"
collect.Method = method

bit,_ := strconv.ParseInt("206", 10, 8)
collect.Bit = bit

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSecurityEncryptionResponseModel
result,_ = encryption.GetHttpsApiRestShApiSecurityEncryption(collect)

```


### <a name="create_https_api_rest_sh_api_security_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".encryption_pkg.CreateHttpsApiRestShApiSecurityEncryption") CreateHttpsApiRestShApiSecurityEncryption

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```go
func (me *ENCRYPTION_IMPL) CreateHttpsApiRestShApiSecurityEncryption(input *CreateHttpsApiRestShApiSecurityEncryptionInput)(*models_pkg.HttpsApiRestShApiSecurityEncryptionResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (encryption_pkg.CreateHttpsApiRestShApiSecurityEncryptionInput)

var body *models_pkg.HttpsApiRestShApiSecurityEncryptionRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSecurityEncryptionResponseModel
result,_ = encryption.CreateHttpsApiRestShApiSecurityEncryption(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".cdn_pkg") cdn_pkg

### Get instance

Factory for the ``` CDN ``` interface can be accessed from the package cdn_pkg.

```go
cDN := cdn_pkg.NewCDN()
```

### <a name="get_https_api_rest_sh_api_service_cdn_push"></a>![Method: ](https://apidocs.io/img/method.png ".cdn_pkg.GetHttpsApiRestShApiServiceCdnPush") GetHttpsApiRestShApiServiceCdnPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```go
func (me *CDN_IMPL) GetHttpsApiRestShApiServiceCdnPush(input *GetHttpsApiRestShApiServiceCdnPushInput)(*models_pkg.HttpsApiRestShApiServiceCdnPushResponseModel,error)
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

```go
collect := new (cdn_pkg.GetHttpsApiRestShApiServiceCdnPushInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

cname := "cname"
collect.Cname = cname

file := "file"
collect.File = file

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiServiceCdnPushResponseModel
result,_ = cDN.GetHttpsApiRestShApiServiceCdnPush(collect)

```


### <a name="get_https_api_rest_sh_api_service_cdn_pull"></a>![Method: ](https://apidocs.io/img/method.png ".cdn_pkg.GetHttpsApiRestShApiServiceCdnPull") GetHttpsApiRestShApiServiceCdnPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```go
func (me *CDN_IMPL) GetHttpsApiRestShApiServiceCdnPull(input *GetHttpsApiRestShApiServiceCdnPullInput)(*models_pkg.HttpsApiRestShApiServiceCdnPullResponseModel,error)
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

```go
collect := new (cdn_pkg.GetHttpsApiRestShApiServiceCdnPullInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

origin := "origin"
collect.Origin = origin

cname := "cname"
collect.Cname = cname

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiServiceCdnPullResponseModel
result,_ = cDN.GetHttpsApiRestShApiServiceCdnPull(collect)

```


### <a name="create_https_api_rest_sh_api_service_cdn_push"></a>![Method: ](https://apidocs.io/img/method.png ".cdn_pkg.CreateHttpsApiRestShApiServiceCdnPush") CreateHttpsApiRestShApiServiceCdnPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```go
func (me *CDN_IMPL) CreateHttpsApiRestShApiServiceCdnPush(input *CreateHttpsApiRestShApiServiceCdnPushInput)(*models_pkg.HttpsApiRestShApiServiceCdnPushResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (cdn_pkg.CreateHttpsApiRestShApiServiceCdnPushInput)

var body *models_pkg.HttpsApiRestShApiServiceCdnPushRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiServiceCdnPushResponseModel
result,_ = cDN.CreateHttpsApiRestShApiServiceCdnPush(collect)

```


### <a name="create_https_api_rest_sh_api_service_cdn_pull"></a>![Method: ](https://apidocs.io/img/method.png ".cdn_pkg.CreateHttpsApiRestShApiServiceCdnPull") CreateHttpsApiRestShApiServiceCdnPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```go
func (me *CDN_IMPL) CreateHttpsApiRestShApiServiceCdnPull(input *CreateHttpsApiRestShApiServiceCdnPullInput)(*models_pkg.HttpsApiRestShApiServiceCdnPullResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (cdn_pkg.CreateHttpsApiRestShApiServiceCdnPullInput)

var body *models_pkg.HttpsApiRestShApiServiceCdnPullRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiServiceCdnPullResponseModel
result,_ = cDN.CreateHttpsApiRestShApiServiceCdnPull(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".dns_pkg") dns_pkg

### Get instance

Factory for the ``` DNS ``` interface can be accessed from the package dns_pkg.

```go
dNS := dns_pkg.NewDNS()
```

### <a name="get_https_api_rest_sh_api_service_dns_configure"></a>![Method: ](https://apidocs.io/img/method.png ".dns_pkg.GetHttpsApiRestShApiServiceDnsConfigure") GetHttpsApiRestShApiServiceDnsConfigure

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```go
func (me *DNS_IMPL) GetHttpsApiRestShApiServiceDnsConfigure(input *GetHttpsApiRestShApiServiceDnsConfigureInput)(*models_pkg.HttpsApiRestShApiServiceDnsConfigureResponseModel,error)
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

```go
collect := new (dns_pkg.GetHttpsApiRestShApiServiceDnsConfigureInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

domain := "domain"
collect.Domain = domain

records := "records"
collect.Records = records

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiServiceDnsConfigureResponseModel
result,_ = dNS.GetHttpsApiRestShApiServiceDnsConfigure(collect)

```


### <a name="create_https_api_rest_sh_api_service_dns_configure"></a>![Method: ](https://apidocs.io/img/method.png ".dns_pkg.CreateHttpsApiRestShApiServiceDnsConfigure") CreateHttpsApiRestShApiServiceDnsConfigure

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```go
func (me *DNS_IMPL) CreateHttpsApiRestShApiServiceDnsConfigure(input *CreateHttpsApiRestShApiServiceDnsConfigureInput)(*models_pkg.HttpsApiRestShApiServiceDnsConfigureResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (dns_pkg.CreateHttpsApiRestShApiServiceDnsConfigureInput)

var body *models_pkg.HttpsApiRestShApiServiceDnsConfigureRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiServiceDnsConfigureResponseModel
result,_ = dNS.CreateHttpsApiRestShApiServiceDnsConfigure(collect)

```


### <a name="get_https_api_rest_sh_api_service_dns_add"></a>![Method: ](https://apidocs.io/img/method.png ".dns_pkg.GetHttpsApiRestShApiServiceDnsAdd") GetHttpsApiRestShApiServiceDnsAdd

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```go
func (me *DNS_IMPL) GetHttpsApiRestShApiServiceDnsAdd(input *GetHttpsApiRestShApiServiceDnsAddInput)(*models_pkg.HttpsApiRestShApiServiceDnsAddResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| domain |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (dns_pkg.GetHttpsApiRestShApiServiceDnsAddInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

domain := "domain"
collect.Domain = domain

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiServiceDnsAddResponseModel
result,_ = dNS.GetHttpsApiRestShApiServiceDnsAdd(collect)

```


### <a name="create_https_api_rest_sh_api_service_dns_add"></a>![Method: ](https://apidocs.io/img/method.png ".dns_pkg.CreateHttpsApiRestShApiServiceDnsAdd") CreateHttpsApiRestShApiServiceDnsAdd

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```go
func (me *DNS_IMPL) CreateHttpsApiRestShApiServiceDnsAdd(input *CreateHttpsApiRestShApiServiceDnsAddInput)(*models_pkg.HttpsApiRestShApiServiceDnsAddResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (dns_pkg.CreateHttpsApiRestShApiServiceDnsAddInput)

var body *models_pkg.HttpsApiRestShApiServiceDnsAddRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiServiceDnsAddResponseModel
result,_ = dNS.CreateHttpsApiRestShApiServiceDnsAdd(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="codeobfuscation_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".codeobfuscation_pkg") codeobfuscation_pkg

### Get instance

Factory for the ``` CODEOBFUSCATION ``` interface can be accessed from the package codeobfuscation_pkg.

```go
codeObfuscation := codeobfuscation_pkg.NewCODEOBFUSCATION()
```

### <a name="get_https_api_rest_sh_api_service_obfuscation"></a>![Method: ](https://apidocs.io/img/method.png ".codeobfuscation_pkg.GetHttpsApiRestShApiServiceObfuscation") GetHttpsApiRestShApiServiceObfuscation

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```go
func (me *CODEOBFUSCATION_IMPL) GetHttpsApiRestShApiServiceObfuscation(input *GetHttpsApiRestShApiServiceObfuscationInput)(*models_pkg.HttpsApiRestShApiServiceObfuscationResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| app |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (codeobfuscation_pkg.GetHttpsApiRestShApiServiceObfuscationInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

app := "app"
collect.App = app

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiServiceObfuscationResponseModel
result,_ = codeObfuscation.GetHttpsApiRestShApiServiceObfuscation(collect)

```


### <a name="create_https_api_rest_sh_api_service_obfuscation"></a>![Method: ](https://apidocs.io/img/method.png ".codeobfuscation_pkg.CreateHttpsApiRestShApiServiceObfuscation") CreateHttpsApiRestShApiServiceObfuscation

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```go
func (me *CODEOBFUSCATION_IMPL) CreateHttpsApiRestShApiServiceObfuscation(input *CreateHttpsApiRestShApiServiceObfuscationInput)(*models_pkg.HttpsApiRestShApiServiceObfuscationResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (codeobfuscation_pkg.CreateHttpsApiRestShApiServiceObfuscationInput)

var body *models_pkg.HttpsApiRestShApiServiceObfuscationRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiServiceObfuscationResponseModel
result,_ = codeObfuscation.CreateHttpsApiRestShApiServiceObfuscation(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".hosting_pkg") hosting_pkg

### Get instance

Factory for the ``` HOSTING ``` interface can be accessed from the package hosting_pkg.

```go
hosting := hosting_pkg.NewHOSTING()
```

### <a name="get_https_api_rest_sh_api_service_hosting"></a>![Method: ](https://apidocs.io/img/method.png ".hosting_pkg.GetHttpsApiRestShApiServiceHosting") GetHttpsApiRestShApiServiceHosting

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```go
func (me *HOSTING_IMPL) GetHttpsApiRestShApiServiceHosting(input *GetHttpsApiRestShApiServiceHostingInput)(*models_pkg.HttpsApiRestShApiServiceHostingResponseModel,error)
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

```go
collect := new (hosting_pkg.GetHttpsApiRestShApiServiceHostingInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

app := "app"
collect.App = app

domain := "domain"
collect.Domain = domain

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiServiceHostingResponseModel
result,_ = hosting.GetHttpsApiRestShApiServiceHosting(collect)

```


### <a name="create_https_api_rest_sh_api_service_hosting"></a>![Method: ](https://apidocs.io/img/method.png ".hosting_pkg.CreateHttpsApiRestShApiServiceHosting") CreateHttpsApiRestShApiServiceHosting

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```go
func (me *HOSTING_IMPL) CreateHttpsApiRestShApiServiceHosting(input *CreateHttpsApiRestShApiServiceHostingInput)(*models_pkg.HttpsApiRestShApiServiceHostingResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (hosting_pkg.CreateHttpsApiRestShApiServiceHostingInput)

var body *models_pkg.HttpsApiRestShApiServiceHostingRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiServiceHostingResponseModel
result,_ = hosting.CreateHttpsApiRestShApiServiceHosting(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="datamanipulation,conversion,sorting,andcompressionapi_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".datamanipulation,conversion,sorting,andcompressionapi_pkg") datamanipulation,conversion,sorting,andcompressionapi_pkg

### Get instance

Factory for the ``` DATAMANIPULATION,CONVERSION,SORTING,ANDCOMPRESSIONAPI ``` interface can be accessed from the package datamanipulation,conversion,sorting,andcompressionapi_pkg.

```go
dataManipulationConversionSortingAndCompressionAPI := datamanipulation,conversion,sorting,andcompressionapi_pkg.NewDATAMANIPULATION,CONVERSION,SORTING,ANDCOMPRESSIONAPI()
```

### <a name="get_https_api_rest_sh_api_data"></a>![Method: ](https://apidocs.io/img/method.png ".datamanipulation,conversion,sorting,andcompressionapi_pkg.GetHttpsApiRestShApiData") GetHttpsApiRestShApiData

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *DATAMANIPULATIONCONVERSIONSORTINGANDCOMPRESSIONAPI_IMPL) GetHttpsApiRestShApiData(input *GetHttpsApiRestShApiDataInput)(*models_pkg.HttpsApiRestShApiDataResponseModel,error)
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

```go
collect := new (datamanipulation,conversion,sorting,andcompressionapi_pkg.GetHttpsApiRestShApiDataInput)

key := "API"
collect.Key = key

uid := "UID"
collect.Uid = uid

user := "UID"
collect.User = user

apiuid := "apiUID"
collect.Apiuid = apiuid

data := "https://static.yourcdn.com/data.file"
collect.Data = data

contentType := "application/json"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiDataResponseModel
result,_ = dataManipulationConversionSortingAndCompressionAPI.GetHttpsApiRestShApiData(collect)

```


### <a name="create_https_api_rest_sh_api_data"></a>![Method: ](https://apidocs.io/img/method.png ".datamanipulation,conversion,sorting,andcompressionapi_pkg.CreateHttpsApiRestShApiData") CreateHttpsApiRestShApiData

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *DATAMANIPULATIONCONVERSIONSORTINGANDCOMPRESSIONAPI_IMPL) CreateHttpsApiRestShApiData(input *CreateHttpsApiRestShApiDataInput)(*models_pkg.HttpsApiRestShApiDataResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (datamanipulation,conversion,sorting,andcompressionapi_pkg.CreateHttpsApiRestShApiDataInput)

bodyValue := []byte("{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}")
var body *models_pkg.HttpsApiRestShApiDataRequestModel
json.Unmarshal(bodyValue,&body)
collect.Body = body

contentType := "application/json"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiDataResponseModel
result,_ = dataManipulationConversionSortingAndCompressionAPI.CreateHttpsApiRestShApiData(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="imagemanipulationandmoderationapi_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".imagemanipulationandmoderationapi_pkg") imagemanipulationandmoderationapi_pkg

### Get instance

Factory for the ``` IMAGEMANIPULATIONANDMODERATIONAPI ``` interface can be accessed from the package imagemanipulationandmoderationapi_pkg.

```go
imageManipulationAndModerationAPI := imagemanipulationandmoderationapi_pkg.NewIMAGEMANIPULATIONANDMODERATIONAPI()
```

### <a name="get_https_api_rest_sh_api_image"></a>![Method: ](https://apidocs.io/img/method.png ".imagemanipulationandmoderationapi_pkg.GetHttpsApiRestShApiImage") GetHttpsApiRestShApiImage

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```go
func (me *IMAGEMANIPULATIONANDMODERATIONAPI_IMPL) GetHttpsApiRestShApiImage(input *GetHttpsApiRestShApiImageInput)(*models_pkg.HttpsApiRestShApiImageResponseModel,error)
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

```go
collect := new (imagemanipulationandmoderationapi_pkg.GetHttpsApiRestShApiImageInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

image := "image"
collect.Image = image

transform := "transform"
collect.Transform = transform

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiImageResponseModel
result,_ = imageManipulationAndModerationAPI.GetHttpsApiRestShApiImage(collect)

```


### <a name="create_https_api_rest_sh_api_image"></a>![Method: ](https://apidocs.io/img/method.png ".imagemanipulationandmoderationapi_pkg.CreateHttpsApiRestShApiImage") CreateHttpsApiRestShApiImage

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```go
func (me *IMAGEMANIPULATIONANDMODERATIONAPI_IMPL) CreateHttpsApiRestShApiImage(input *CreateHttpsApiRestShApiImageInput)(*models_pkg.HttpsApiRestShApiImageResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (imagemanipulationandmoderationapi_pkg.CreateHttpsApiRestShApiImageInput)

var body *models_pkg.HttpsApiRestShApiImageRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiImageResponseModel
result,_ = imageManipulationAndModerationAPI.CreateHttpsApiRestShApiImage(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".verification_pkg") verification_pkg

### Get instance

Factory for the ``` VERIFICATION ``` interface can be accessed from the package verification_pkg.

```go
verification := verification_pkg.NewVERIFICATION()
```

### <a name="get_https_api_rest_sh_api_verify_address"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.GetHttpsApiRestShApiVerifyAddress") GetHttpsApiRestShApiVerifyAddress

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```go
func (me *VERIFICATION_IMPL) GetHttpsApiRestShApiVerifyAddress(input *GetHttpsApiRestShApiVerifyAddressInput)(*models_pkg.HttpsApiRestShApiVerifyAddressResponseModel,error)
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

```go
collect := new (verification_pkg.GetHttpsApiRestShApiVerifyAddressInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

user := "user"
collect.User = user

a := "a"
collect.A = a

sa := "sa"
collect.Sa = sa

c := "c"
collect.C = c

s := "s"
collect.S = s

z,_ := strconv.ParseInt("165", 10, 8)
collect.Z = z

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiVerifyAddressResponseModel
result,_ = verification.GetHttpsApiRestShApiVerifyAddress(collect)

```


### <a name="create_https_api_rest_sh_api_verify_address"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.CreateHttpsApiRestShApiVerifyAddress") CreateHttpsApiRestShApiVerifyAddress

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```go
func (me *VERIFICATION_IMPL) CreateHttpsApiRestShApiVerifyAddress(input *CreateHttpsApiRestShApiVerifyAddressInput)(*models_pkg.HttpsApiRestShApiVerifyAddressResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (verification_pkg.CreateHttpsApiRestShApiVerifyAddressInput)

var body *models_pkg.HttpsApiRestShApiVerifyAddressRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiVerifyAddressResponseModel
result,_ = verification.CreateHttpsApiRestShApiVerifyAddress(collect)

```


### <a name="get_https_api_rest_sh_api_verify_user"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.GetHttpsApiRestShApiVerifyUser") GetHttpsApiRestShApiVerifyUser

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```go
func (me *VERIFICATION_IMPL) GetHttpsApiRestShApiVerifyUser(input *GetHttpsApiRestShApiVerifyUserInput)(*models_pkg.HttpsApiRestShApiVerifyUserResponseModel,error)
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

```go
collect := new (verification_pkg.GetHttpsApiRestShApiVerifyUserInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

user := "user"
collect.User = user

code := "code"
collect.Code = code

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiVerifyUserResponseModel
result,_ = verification.GetHttpsApiRestShApiVerifyUser(collect)

```


### <a name="create_https_api_rest_sh_api_verify_user"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.CreateHttpsApiRestShApiVerifyUser") CreateHttpsApiRestShApiVerifyUser

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```go
func (me *VERIFICATION_IMPL) CreateHttpsApiRestShApiVerifyUser(input *CreateHttpsApiRestShApiVerifyUserInput)(*models_pkg.HttpsApiRestShApiVerifyUserResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (verification_pkg.CreateHttpsApiRestShApiVerifyUserInput)

var body *models_pkg.HttpsApiRestShApiVerifyUserRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiVerifyUserResponseModel
result,_ = verification.CreateHttpsApiRestShApiVerifyUser(collect)

```


### <a name="get_https_api_rest_sh_api_verify"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.GetHttpsApiRestShApiVerify") GetHttpsApiRestShApiVerify

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```go
func (me *VERIFICATION_IMPL) GetHttpsApiRestShApiVerify(input *GetHttpsApiRestShApiVerifyInput)(*models_pkg.HttpsApiRestShApiVerifyResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (verification_pkg.GetHttpsApiRestShApiVerifyInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

to := "to"
collect.To = to

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiVerifyResponseModel
result,_ = verification.GetHttpsApiRestShApiVerify(collect)

```


### <a name="create_https_api_rest_sh_api_verify"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.CreateHttpsApiRestShApiVerify") CreateHttpsApiRestShApiVerify

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```go
func (me *VERIFICATION_IMPL) CreateHttpsApiRestShApiVerify(input *CreateHttpsApiRestShApiVerifyInput)(*models_pkg.HttpsApiRestShApiVerifyResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (verification_pkg.CreateHttpsApiRestShApiVerifyInput)

var body *models_pkg.HttpsApiRestShApiVerifyRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiVerifyResponseModel
result,_ = verification.CreateHttpsApiRestShApiVerify(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="twofactorauthenticationapi_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".twofactorauthenticationapi_pkg") twofactorauthenticationapi_pkg

### Get instance

Factory for the ``` TWOFACTORAUTHENTICATIONAPI ``` interface can be accessed from the package twofactorauthenticationapi_pkg.

```go
twoFactorAuthenticationAPI := twofactorauthenticationapi_pkg.NewTWOFACTORAUTHENTICATIONAPI()
```

### <a name="get_https_api_rest_sh_api2fa_token"></a>![Method: ](https://apidocs.io/img/method.png ".twofactorauthenticationapi_pkg.GetHttpsApiRestShApi2faToken") GetHttpsApiRestShApi2faToken

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```go
func (me *TWOFACTORAUTHENTICATIONAPI_IMPL) GetHttpsApiRestShApi2faToken(input *GetHttpsApiRestShApi2faTokenInput)(*models_pkg.HttpsApiRestShApi2faTokenResponseModel,error)
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

```go
collect := new (twofactorauthenticationapi_pkg.GetHttpsApiRestShApi2faTokenInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

user := "user"
collect.User = user

code := "code"
collect.Code = code

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApi2faTokenResponseModel
result,_ = twoFactorAuthenticationAPI.GetHttpsApiRestShApi2faToken(collect)

```


### <a name="create_https_api_rest_sh_api2fa_token"></a>![Method: ](https://apidocs.io/img/method.png ".twofactorauthenticationapi_pkg.CreateHttpsApiRestShApi2faToken") CreateHttpsApiRestShApi2faToken

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```go
func (me *TWOFACTORAUTHENTICATIONAPI_IMPL) CreateHttpsApiRestShApi2faToken(input *CreateHttpsApiRestShApi2faTokenInput)(*models_pkg.HttpsApiRestShApi2faTokenResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (twofactorauthenticationapi_pkg.CreateHttpsApiRestShApi2faTokenInput)

var body *models_pkg.HttpsApiRestShApi2faTokenRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApi2faTokenResponseModel
result,_ = twoFactorAuthenticationAPI.CreateHttpsApiRestShApi2faToken(collect)

```


### <a name="get_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png ".twofactorauthenticationapi_pkg.GetHttpsApiRestShApi2fa") GetHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```go
func (me *TWOFACTORAUTHENTICATIONAPI_IMPL) GetHttpsApiRestShApi2fa(input *GetHttpsApiRestShApi2faInput)(*models_pkg.HttpsApiRestShApi2faResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (twofactorauthenticationapi_pkg.GetHttpsApiRestShApi2faInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

to := "to"
collect.To = to

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApi2faResponseModel
result,_ = twoFactorAuthenticationAPI.GetHttpsApiRestShApi2fa(collect)

```


### <a name="create_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png ".twofactorauthenticationapi_pkg.CreateHttpsApiRestShApi2fa") CreateHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```go
func (me *TWOFACTORAUTHENTICATIONAPI_IMPL) CreateHttpsApiRestShApi2fa(input *CreateHttpsApiRestShApi2faInput)(*models_pkg.HttpsApiRestShApi2faResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (twofactorauthenticationapi_pkg.CreateHttpsApiRestShApi2faInput)

var body *models_pkg.HttpsApiRestShApi2faRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApi2faResponseModel
result,_ = twoFactorAuthenticationAPI.CreateHttpsApiRestShApi2fa(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="usermanagement_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".usermanagement_pkg") usermanagement_pkg

### Get instance

Factory for the ``` USERMANAGEMENT ``` interface can be accessed from the package usermanagement_pkg.

```go
userManagement := usermanagement_pkg.NewUSERMANAGEMENT()
```

### <a name="get_https_api_rest_sh_api_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.GetHttpsApiRestShApiUserInfo") GetHttpsApiRestShApiUserInfo

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```go
func (me *USERMANAGEMENT_IMPL) GetHttpsApiRestShApiUserInfo(input *GetHttpsApiRestShApiUserInfoInput)(*models_pkg.HttpsApiRestShApiUserInfoResponseModel,error)
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

```go
collect := new (usermanagement_pkg.GetHttpsApiRestShApiUserInfoInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

user := "user"
collect.User = user

apiuid := "apiuid"
collect.Apiuid = apiuid

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiUserInfoResponseModel
result,_ = userManagement.GetHttpsApiRestShApiUserInfo(collect)

```


### <a name="create_https_api_rest_sh_api_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.CreateHttpsApiRestShApiUserInfo") CreateHttpsApiRestShApiUserInfo

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```go
func (me *USERMANAGEMENT_IMPL) CreateHttpsApiRestShApiUserInfo(input *CreateHttpsApiRestShApiUserInfoInput)(*models_pkg.HttpsApiRestShApiUserInfoResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (usermanagement_pkg.CreateHttpsApiRestShApiUserInfoInput)

var body *models_pkg.HttpsApiRestShApiUserInfoRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiUserInfoResponseModel
result,_ = userManagement.CreateHttpsApiRestShApiUserInfo(collect)

```


### <a name="get_https_api_rest_sh_api_user_update"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.GetHttpsApiRestShApiUserUpdate") GetHttpsApiRestShApiUserUpdate

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```go
func (me *USERMANAGEMENT_IMPL) GetHttpsApiRestShApiUserUpdate(input *GetHttpsApiRestShApiUserUpdateInput)(*models_pkg.HttpsApiRestShApiUserUpdateResponseModel,error)
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

```go
collect := new (usermanagement_pkg.GetHttpsApiRestShApiUserUpdateInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

user := "user"
collect.User = user

apiuid := "apiuid"
collect.Apiuid = apiuid

avatar := "avatar"
collect.Avatar = avatar

customInput := "custom input"
collect.CustomInput = customInput

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiUserUpdateResponseModel
result,_ = userManagement.GetHttpsApiRestShApiUserUpdate(collect)

```


### <a name="create_https_api_rest_sh_api_user_update"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.CreateHttpsApiRestShApiUserUpdate") CreateHttpsApiRestShApiUserUpdate

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```go
func (me *USERMANAGEMENT_IMPL) CreateHttpsApiRestShApiUserUpdate(input *CreateHttpsApiRestShApiUserUpdateInput)(*models_pkg.HttpsApiRestShApiUserUpdateResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (usermanagement_pkg.CreateHttpsApiRestShApiUserUpdateInput)

var body *models_pkg.HttpsApiRestShApiUserUpdateRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiUserUpdateResponseModel
result,_ = userManagement.CreateHttpsApiRestShApiUserUpdate(collect)

```


### <a name="get_https_api_rest_sh_api_user_delete"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.GetHttpsApiRestShApiUserDelete") GetHttpsApiRestShApiUserDelete

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```go
func (me *USERMANAGEMENT_IMPL) GetHttpsApiRestShApiUserDelete(input *GetHttpsApiRestShApiUserDeleteInput)(*models_pkg.HttpsApiRestShApiUserDeleteResponseModel,error)
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

```go
collect := new (usermanagement_pkg.GetHttpsApiRestShApiUserDeleteInput)

api := "api"
collect.Api = api

uid := "uid"
collect.Uid = uid

user := "user"
collect.User = user

apiuid := "apiuid"
collect.Apiuid = apiuid

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiUserDeleteResponseModel
result,_ = userManagement.GetHttpsApiRestShApiUserDelete(collect)

```


### <a name="create_https_api_rest_sh_api_user_delete"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.CreateHttpsApiRestShApiUserDelete") CreateHttpsApiRestShApiUserDelete

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```go
func (me *USERMANAGEMENT_IMPL) CreateHttpsApiRestShApiUserDelete(input *CreateHttpsApiRestShApiUserDeleteInput)(*models_pkg.HttpsApiRestShApiUserDeleteResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (usermanagement_pkg.CreateHttpsApiRestShApiUserDeleteInput)

var body *models_pkg.HttpsApiRestShApiUserDeleteRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiUserDeleteResponseModel
result,_ = userManagement.CreateHttpsApiRestShApiUserDelete(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="loginandregistration_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".loginandregistration_pkg") loginandregistration_pkg

### Get instance

Factory for the ``` LOGINANDREGISTRATION ``` interface can be accessed from the package loginandregistration_pkg.

```go
loginAndRegistration := loginandregistration_pkg.NewLOGINANDREGISTRATION()
```

### <a name="get_https_api_rest_sh_api_auth_user_register"></a>![Method: ](https://apidocs.io/img/method.png ".loginandregistration_pkg.GetHttpsApiRestShApiAuthUserRegister") GetHttpsApiRestShApiAuthUserRegister

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```go
func (me *LOGINANDREGISTRATION_IMPL) GetHttpsApiRestShApiAuthUserRegister(input *GetHttpsApiRestShApiAuthUserRegisterInput)(*models_pkg.HttpsApiRestShApiAuthUserRegisterResponseModel,error)
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

```go
collect := new (loginandregistration_pkg.GetHttpsApiRestShApiAuthUserRegisterInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

user := "user"
collect.User = user

password := "password"
collect.Password = password

name := "name"
collect.Name = name

email := "email"
collect.Email = email

phone,_ := strconv.ParseInt("165", 10, 8)
collect.Phone = phone

countrycode,_ := strconv.ParseInt("165", 10, 8)
collect.Countrycode = countrycode

address := "address"
collect.Address = address

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiAuthUserRegisterResponseModel
result,_ = loginAndRegistration.GetHttpsApiRestShApiAuthUserRegister(collect)

```


### <a name="create_https_api_rest_sh_api_auth_user_register"></a>![Method: ](https://apidocs.io/img/method.png ".loginandregistration_pkg.CreateHttpsApiRestShApiAuthUserRegister") CreateHttpsApiRestShApiAuthUserRegister

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```go
func (me *LOGINANDREGISTRATION_IMPL) CreateHttpsApiRestShApiAuthUserRegister(input *CreateHttpsApiRestShApiAuthUserRegisterInput)(*models_pkg.HttpsApiRestShApiAuthUserRegisterResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (loginandregistration_pkg.CreateHttpsApiRestShApiAuthUserRegisterInput)

var body *models_pkg.HttpsApiRestShApiAuthUserRegisterRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiAuthUserRegisterResponseModel
result,_ = loginAndRegistration.CreateHttpsApiRestShApiAuthUserRegister(collect)

```


### <a name="get_https_api_rest_sh_api_auth_user_login"></a>![Method: ](https://apidocs.io/img/method.png ".loginandregistration_pkg.GetHttpsApiRestShApiAuthUserLogin") GetHttpsApiRestShApiAuthUserLogin

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```go
func (me *LOGINANDREGISTRATION_IMPL) GetHttpsApiRestShApiAuthUserLogin(input *GetHttpsApiRestShApiAuthUserLoginInput)(*models_pkg.HttpsApiRestShApiAuthUserLoginResponseModel,error)
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

```go
collect := new (loginandregistration_pkg.GetHttpsApiRestShApiAuthUserLoginInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

user := "user"
collect.User = user

password := "password"
collect.Password = password

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiAuthUserLoginResponseModel
result,_ = loginAndRegistration.GetHttpsApiRestShApiAuthUserLogin(collect)

```


### <a name="create_https_api_rest_sh_api_auth_user_login"></a>![Method: ](https://apidocs.io/img/method.png ".loginandregistration_pkg.CreateHttpsApiRestShApiAuthUserLogin") CreateHttpsApiRestShApiAuthUserLogin

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```go
func (me *LOGINANDREGISTRATION_IMPL) CreateHttpsApiRestShApiAuthUserLogin(input *CreateHttpsApiRestShApiAuthUserLoginInput)(*models_pkg.HttpsApiRestShApiAuthUserLoginResponseModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (loginandregistration_pkg.CreateHttpsApiRestShApiAuthUserLoginInput)

var body *models_pkg.HttpsApiRestShApiAuthUserLoginRequestModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiAuthUserLoginResponseModel
result,_ = loginAndRegistration.CreateHttpsApiRestShApiAuthUserLogin(collect)

```


[Back to List of Controllers](#list_of_controllers)



