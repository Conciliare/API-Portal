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

### <a name="get_https_api_rest_sh_api_sli"></a>![Method: ](https://apidocs.io/img/method.png ".advancedlogging_pkg.GetHttpsApiRestShApiSLI") GetHttpsApiRestShApiSLI

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```go
func (me *ADVANCEDLOGGING_IMPL) GetHttpsApiRestShApiSLI(input *GetHttpsApiRestShApiSLIInput)(*models_pkg.HttpsApiRestShApiSLIRModel,error)
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
collect := new (advancedlogging_pkg.GetHttpsApiRestShApiSLIInput)

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


var result *models_pkg.HttpsApiRestShApiSLIRModel
result,_ = advancedLogging.GetHttpsApiRestShApiSLI(collect)

```


### <a name="get_https_api_rest_sh_api_sl"></a>![Method: ](https://apidocs.io/img/method.png ".advancedlogging_pkg.GetHttpsApiRestShApiSL") GetHttpsApiRestShApiSL

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```go
func (me *ADVANCEDLOGGING_IMPL) GetHttpsApiRestShApiSL(input *GetHttpsApiRestShApiSLInput)(*models_pkg.HttpsApiRestShApiSLRModel,error)
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
collect := new (advancedlogging_pkg.GetHttpsApiRestShApiSLInput)

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


var result *models_pkg.HttpsApiRestShApiSLRModel
result,_ = advancedLogging.GetHttpsApiRestShApiSL(collect)

```


### <a name="create_https_api_rest_sh_api_sli"></a>![Method: ](https://apidocs.io/img/method.png ".advancedlogging_pkg.CreateHttpsApiRestShApiSLI") CreateHttpsApiRestShApiSLI

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```go
func (me *ADVANCEDLOGGING_IMPL) CreateHttpsApiRestShApiSLI(input *CreateHttpsApiRestShApiSLIInput)(*models_pkg.HttpsApiRestShApiSLIRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (advancedlogging_pkg.CreateHttpsApiRestShApiSLIInput)

var body *models_pkg.HttpsApiRestShApiSLIModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSLIRModel
result,_ = advancedLogging.CreateHttpsApiRestShApiSLI(collect)

```


### <a name="create_https_api_rest_sh_api_sl"></a>![Method: ](https://apidocs.io/img/method.png ".advancedlogging_pkg.CreateHttpsApiRestShApiSL") CreateHttpsApiRestShApiSL

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```go
func (me *ADVANCEDLOGGING_IMPL) CreateHttpsApiRestShApiSL(input *CreateHttpsApiRestShApiSLInput)(*models_pkg.HttpsApiRestShApiSLRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (advancedlogging_pkg.CreateHttpsApiRestShApiSLInput)

var body *models_pkg.HttpsApiRestShApiSLModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSLRModel
result,_ = advancedLogging.CreateHttpsApiRestShApiSL(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="waf&ddosprotection_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".waf&ddosprotection_pkg") waf&ddosprotection_pkg

### Get instance

Factory for the ``` WAF&DDOSPROTECTION ``` interface can be accessed from the package waf&ddosprotection_pkg.

```go
wAFDDOSProtection := waf&ddosprotection_pkg.NewWAF&DDOSPROTECTION()
```

### <a name="get_https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".waf&ddosprotection_pkg.GetHttpsApiRestShApiSWC") GetHttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *WAFDDOSPROTECTION_IMPL) GetHttpsApiRestShApiSWC(input *GetHttpsApiRestShApiSWCInput)(*models_pkg.HttpsApiRestShApiSWCRModel,error)
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
collect := new (waf&ddosprotection_pkg.GetHttpsApiRestShApiSWCInput)

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


var result *models_pkg.HttpsApiRestShApiSWCRModel
result,_ = wAFDDOSProtection.GetHttpsApiRestShApiSWC(collect)

```


### <a name="get_https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".waf&ddosprotection_pkg.GetHttpsApiRestShApiSW") GetHttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *WAFDDOSPROTECTION_IMPL) GetHttpsApiRestShApiSW(input *GetHttpsApiRestShApiSWInput)(*models_pkg.HttpsApiRestShApiSWRModel,error)
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
collect := new (waf&ddosprotection_pkg.GetHttpsApiRestShApiSWInput)

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


var result *models_pkg.HttpsApiRestShApiSWRModel
result,_ = wAFDDOSProtection.GetHttpsApiRestShApiSW(collect)

```


### <a name="create_https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".waf&ddosprotection_pkg.CreateHttpsApiRestShApiSWC") CreateHttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *WAFDDOSPROTECTION_IMPL) CreateHttpsApiRestShApiSWC(input *CreateHttpsApiRestShApiSWCInput)(*models_pkg.HttpsApiRestShApiSWCRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (waf&ddosprotection_pkg.CreateHttpsApiRestShApiSWCInput)

bodyValue := []byte("{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}")
var body *models_pkg.HttpsApiRestShApiSWCModel
json.Unmarshal(bodyValue,&body)
collect.Body = body

contentType := "application/json"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSWCRModel
result,_ = wAFDDOSProtection.CreateHttpsApiRestShApiSWC(collect)

```


### <a name="create_https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".waf&ddosprotection_pkg.CreateHttpsApiRestShApiSW") CreateHttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *WAFDDOSPROTECTION_IMPL) CreateHttpsApiRestShApiSW(input *CreateHttpsApiRestShApiSWInput)(*models_pkg.HttpsApiRestShApiSWRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (waf&ddosprotection_pkg.CreateHttpsApiRestShApiSWInput)

bodyValue := []byte("{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}")
var body *models_pkg.HttpsApiRestShApiSWModel
json.Unmarshal(bodyValue,&body)
collect.Body = body

contentType := "application/json"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSWRModel
result,_ = wAFDDOSProtection.CreateHttpsApiRestShApiSW(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".encryption_pkg") encryption_pkg

### Get instance

Factory for the ``` ENCRYPTION ``` interface can be accessed from the package encryption_pkg.

```go
encryption := encryption_pkg.NewENCRYPTION()
```

### <a name="get_https_api_rest_sh_api_se"></a>![Method: ](https://apidocs.io/img/method.png ".encryption_pkg.GetHttpsApiRestShApiSE") GetHttpsApiRestShApiSE

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```go
func (me *ENCRYPTION_IMPL) GetHttpsApiRestShApiSE(input *GetHttpsApiRestShApiSEInput)(*models_pkg.HttpsApiRestShApiSERModel,error)
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
collect := new (encryption_pkg.GetHttpsApiRestShApiSEInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

data := "data"
collect.Data = data

method := "method"
collect.Method = method

bit,_ := strconv.ParseInt("253", 10, 8)
collect.Bit = bit

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSERModel
result,_ = encryption.GetHttpsApiRestShApiSE(collect)

```


### <a name="create_https_api_rest_sh_api_se"></a>![Method: ](https://apidocs.io/img/method.png ".encryption_pkg.CreateHttpsApiRestShApiSE") CreateHttpsApiRestShApiSE

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```go
func (me *ENCRYPTION_IMPL) CreateHttpsApiRestShApiSE(input *CreateHttpsApiRestShApiSEInput)(*models_pkg.HttpsApiRestShApiSERModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (encryption_pkg.CreateHttpsApiRestShApiSEInput)

var body *models_pkg.HttpsApiRestShApiSEModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSERModel
result,_ = encryption.CreateHttpsApiRestShApiSE(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".cdn_pkg") cdn_pkg

### Get instance

Factory for the ``` CDN ``` interface can be accessed from the package cdn_pkg.

```go
cDN := cdn_pkg.NewCDN()
```

### <a name="get_https_api_rest_sh_api_sc_push"></a>![Method: ](https://apidocs.io/img/method.png ".cdn_pkg.GetHttpsApiRestShApiSCPush") GetHttpsApiRestShApiSCPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```go
func (me *CDN_IMPL) GetHttpsApiRestShApiSCPush(input *GetHttpsApiRestShApiSCPushInput)(*models_pkg.HttpsApiRestShApiSCPushRModel,error)
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
collect := new (cdn_pkg.GetHttpsApiRestShApiSCPushInput)

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


var result *models_pkg.HttpsApiRestShApiSCPushRModel
result,_ = cDN.GetHttpsApiRestShApiSCPush(collect)

```


### <a name="get_https_api_rest_sh_api_sc_pull"></a>![Method: ](https://apidocs.io/img/method.png ".cdn_pkg.GetHttpsApiRestShApiSCPull") GetHttpsApiRestShApiSCPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```go
func (me *CDN_IMPL) GetHttpsApiRestShApiSCPull(input *GetHttpsApiRestShApiSCPullInput)(*models_pkg.HttpsApiRestShApiSCPullRModel,error)
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
collect := new (cdn_pkg.GetHttpsApiRestShApiSCPullInput)

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


var result *models_pkg.HttpsApiRestShApiSCPullRModel
result,_ = cDN.GetHttpsApiRestShApiSCPull(collect)

```


### <a name="create_https_api_rest_sh_api_sc_push"></a>![Method: ](https://apidocs.io/img/method.png ".cdn_pkg.CreateHttpsApiRestShApiSCPush") CreateHttpsApiRestShApiSCPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```go
func (me *CDN_IMPL) CreateHttpsApiRestShApiSCPush(input *CreateHttpsApiRestShApiSCPushInput)(*models_pkg.HttpsApiRestShApiSCPushRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (cdn_pkg.CreateHttpsApiRestShApiSCPushInput)

var body *models_pkg.HttpsApiRestShApiSCPushModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSCPushRModel
result,_ = cDN.CreateHttpsApiRestShApiSCPush(collect)

```


### <a name="create_https_api_rest_sh_api_sc_pull"></a>![Method: ](https://apidocs.io/img/method.png ".cdn_pkg.CreateHttpsApiRestShApiSCPull") CreateHttpsApiRestShApiSCPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```go
func (me *CDN_IMPL) CreateHttpsApiRestShApiSCPull(input *CreateHttpsApiRestShApiSCPullInput)(*models_pkg.HttpsApiRestShApiSCPullRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (cdn_pkg.CreateHttpsApiRestShApiSCPullInput)

var body *models_pkg.HttpsApiRestShApiSCPullModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSCPullRModel
result,_ = cDN.CreateHttpsApiRestShApiSCPull(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".dns_pkg") dns_pkg

### Get instance

Factory for the ``` DNS ``` interface can be accessed from the package dns_pkg.

```go
dNS := dns_pkg.NewDNS()
```

### <a name="get_https_api_rest_sh_api_sdc"></a>![Method: ](https://apidocs.io/img/method.png ".dns_pkg.GetHttpsApiRestShApiSDC") GetHttpsApiRestShApiSDC

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```go
func (me *DNS_IMPL) GetHttpsApiRestShApiSDC(input *GetHttpsApiRestShApiSDCInput)(*models_pkg.HttpsApiRestShApiSDCRModel,error)
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
collect := new (dns_pkg.GetHttpsApiRestShApiSDCInput)

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


var result *models_pkg.HttpsApiRestShApiSDCRModel
result,_ = dNS.GetHttpsApiRestShApiSDC(collect)

```


### <a name="create_https_api_rest_sh_api_sdc"></a>![Method: ](https://apidocs.io/img/method.png ".dns_pkg.CreateHttpsApiRestShApiSDC") CreateHttpsApiRestShApiSDC

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```go
func (me *DNS_IMPL) CreateHttpsApiRestShApiSDC(input *CreateHttpsApiRestShApiSDCInput)(*models_pkg.HttpsApiRestShApiSDCRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (dns_pkg.CreateHttpsApiRestShApiSDCInput)

var body *models_pkg.HttpsApiRestShApiSDCModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSDCRModel
result,_ = dNS.CreateHttpsApiRestShApiSDC(collect)

```


### <a name="get_https_api_rest_sh_api_sda"></a>![Method: ](https://apidocs.io/img/method.png ".dns_pkg.GetHttpsApiRestShApiSDA") GetHttpsApiRestShApiSDA

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```go
func (me *DNS_IMPL) GetHttpsApiRestShApiSDA(input *GetHttpsApiRestShApiSDAInput)(*models_pkg.HttpsApiRestShApiSDARModel,error)
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
collect := new (dns_pkg.GetHttpsApiRestShApiSDAInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

domain := "domain"
collect.Domain = domain

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSDARModel
result,_ = dNS.GetHttpsApiRestShApiSDA(collect)

```


### <a name="create_https_api_rest_sh_api_sda"></a>![Method: ](https://apidocs.io/img/method.png ".dns_pkg.CreateHttpsApiRestShApiSDA") CreateHttpsApiRestShApiSDA

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```go
func (me *DNS_IMPL) CreateHttpsApiRestShApiSDA(input *CreateHttpsApiRestShApiSDAInput)(*models_pkg.HttpsApiRestShApiSDARModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (dns_pkg.CreateHttpsApiRestShApiSDAInput)

var body *models_pkg.HttpsApiRestShApiSDAModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSDARModel
result,_ = dNS.CreateHttpsApiRestShApiSDA(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="codeobfuscation_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".codeobfuscation_pkg") codeobfuscation_pkg

### Get instance

Factory for the ``` CODEOBFUSCATION ``` interface can be accessed from the package codeobfuscation_pkg.

```go
codeObfuscation := codeobfuscation_pkg.NewCODEOBFUSCATION()
```

### <a name="get_https_api_rest_sh_api_so"></a>![Method: ](https://apidocs.io/img/method.png ".codeobfuscation_pkg.GetHttpsApiRestShApiSO") GetHttpsApiRestShApiSO

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```go
func (me *CODEOBFUSCATION_IMPL) GetHttpsApiRestShApiSO(input *GetHttpsApiRestShApiSOInput)(*models_pkg.HttpsApiRestShApiSORModel,error)
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
collect := new (codeobfuscation_pkg.GetHttpsApiRestShApiSOInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

app := "app"
collect.App = app

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSORModel
result,_ = codeObfuscation.GetHttpsApiRestShApiSO(collect)

```


### <a name="create_https_api_rest_sh_api_so"></a>![Method: ](https://apidocs.io/img/method.png ".codeobfuscation_pkg.CreateHttpsApiRestShApiSO") CreateHttpsApiRestShApiSO

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```go
func (me *CODEOBFUSCATION_IMPL) CreateHttpsApiRestShApiSO(input *CreateHttpsApiRestShApiSOInput)(*models_pkg.HttpsApiRestShApiSORModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (codeobfuscation_pkg.CreateHttpsApiRestShApiSOInput)

var body *models_pkg.HttpsApiRestShApiSOModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSORModel
result,_ = codeObfuscation.CreateHttpsApiRestShApiSO(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".hosting_pkg") hosting_pkg

### Get instance

Factory for the ``` HOSTING ``` interface can be accessed from the package hosting_pkg.

```go
hosting := hosting_pkg.NewHOSTING()
```

### <a name="get_https_api_rest_sh_api_sh"></a>![Method: ](https://apidocs.io/img/method.png ".hosting_pkg.GetHttpsApiRestShApiSH") GetHttpsApiRestShApiSH

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```go
func (me *HOSTING_IMPL) GetHttpsApiRestShApiSH(input *GetHttpsApiRestShApiSHInput)(*models_pkg.HttpsApiRestShApiSHRModel,error)
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
collect := new (hosting_pkg.GetHttpsApiRestShApiSHInput)

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


var result *models_pkg.HttpsApiRestShApiSHRModel
result,_ = hosting.GetHttpsApiRestShApiSH(collect)

```


### <a name="create_https_api_rest_sh_api_sh"></a>![Method: ](https://apidocs.io/img/method.png ".hosting_pkg.CreateHttpsApiRestShApiSH") CreateHttpsApiRestShApiSH

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```go
func (me *HOSTING_IMPL) CreateHttpsApiRestShApiSH(input *CreateHttpsApiRestShApiSHInput)(*models_pkg.HttpsApiRestShApiSHRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (hosting_pkg.CreateHttpsApiRestShApiSHInput)

var body *models_pkg.HttpsApiRestShApiSHModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiSHRModel
result,_ = hosting.CreateHttpsApiRestShApiSH(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="datamanipulation,conversion,sorting,andcompressionapi_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".datamanipulation,conversion,sorting,andcompressionapi_pkg") datamanipulation,conversion,sorting,andcompressionapi_pkg

### Get instance

Factory for the ``` DATAMANIPULATION,CONVERSION,SORTING,ANDCOMPRESSIONAPI ``` interface can be accessed from the package datamanipulation,conversion,sorting,andcompressionapi_pkg.

```go
dataManipulationConversionSortingAndCompressionAPI := datamanipulation,conversion,sorting,andcompressionapi_pkg.NewDATAMANIPULATION,CONVERSION,SORTING,ANDCOMPRESSIONAPI()
```

### <a name="get_https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".datamanipulation,conversion,sorting,andcompressionapi_pkg.GetHttpsApiRestShApiD") GetHttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *DATAMANIPULATIONCONVERSIONSORTINGANDCOMPRESSIONAPI_IMPL) GetHttpsApiRestShApiD(input *GetHttpsApiRestShApiDInput)(*models_pkg.HttpsApiRestShApiDRModel,error)
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
collect := new (datamanipulation,conversion,sorting,andcompressionapi_pkg.GetHttpsApiRestShApiDInput)

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


var result *models_pkg.HttpsApiRestShApiDRModel
result,_ = dataManipulationConversionSortingAndCompressionAPI.GetHttpsApiRestShApiD(collect)

```


### <a name="create_https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".datamanipulation,conversion,sorting,andcompressionapi_pkg.CreateHttpsApiRestShApiD") CreateHttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *DATAMANIPULATIONCONVERSIONSORTINGANDCOMPRESSIONAPI_IMPL) CreateHttpsApiRestShApiD(input *CreateHttpsApiRestShApiDInput)(*models_pkg.HttpsApiRestShApiDRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (datamanipulation,conversion,sorting,andcompressionapi_pkg.CreateHttpsApiRestShApiDInput)

bodyValue := []byte("{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}")
var body *models_pkg.HttpsApiRestShApiDModel
json.Unmarshal(bodyValue,&body)
collect.Body = body

contentType := "application/json"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiDRModel
result,_ = dataManipulationConversionSortingAndCompressionAPI.CreateHttpsApiRestShApiD(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="imagemanipulationandmoderationapi_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".imagemanipulationandmoderationapi_pkg") imagemanipulationandmoderationapi_pkg

### Get instance

Factory for the ``` IMAGEMANIPULATIONANDMODERATIONAPI ``` interface can be accessed from the package imagemanipulationandmoderationapi_pkg.

```go
imageManipulationAndModerationAPI := imagemanipulationandmoderationapi_pkg.NewIMAGEMANIPULATIONANDMODERATIONAPI()
```

### <a name="get_https_api_rest_sh_api_i"></a>![Method: ](https://apidocs.io/img/method.png ".imagemanipulationandmoderationapi_pkg.GetHttpsApiRestShApiI") GetHttpsApiRestShApiI

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```go
func (me *IMAGEMANIPULATIONANDMODERATIONAPI_IMPL) GetHttpsApiRestShApiI(input *GetHttpsApiRestShApiIInput)(*models_pkg.HttpsApiRestShApiIRModel,error)
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
collect := new (imagemanipulationandmoderationapi_pkg.GetHttpsApiRestShApiIInput)

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


var result *models_pkg.HttpsApiRestShApiIRModel
result,_ = imageManipulationAndModerationAPI.GetHttpsApiRestShApiI(collect)

```


### <a name="create_https_api_rest_sh_api_i"></a>![Method: ](https://apidocs.io/img/method.png ".imagemanipulationandmoderationapi_pkg.CreateHttpsApiRestShApiI") CreateHttpsApiRestShApiI

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```go
func (me *IMAGEMANIPULATIONANDMODERATIONAPI_IMPL) CreateHttpsApiRestShApiI(input *CreateHttpsApiRestShApiIInput)(*models_pkg.HttpsApiRestShApiIRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (imagemanipulationandmoderationapi_pkg.CreateHttpsApiRestShApiIInput)

var body *models_pkg.HttpsApiRestShApiIModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiIRModel
result,_ = imageManipulationAndModerationAPI.CreateHttpsApiRestShApiI(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".verification_pkg") verification_pkg

### Get instance

Factory for the ``` VERIFICATION ``` interface can be accessed from the package verification_pkg.

```go
verification := verification_pkg.NewVERIFICATION()
```

### <a name="get_https_api_rest_sh_api_va"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.GetHttpsApiRestShApiVA") GetHttpsApiRestShApiVA

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```go
func (me *VERIFICATION_IMPL) GetHttpsApiRestShApiVA(input *GetHttpsApiRestShApiVAInput)(*models_pkg.HttpsApiRestShApiVARModel,error)
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
collect := new (verification_pkg.GetHttpsApiRestShApiVAInput)

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

z,_ := strconv.ParseInt("212", 10, 8)
collect.Z = z

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiVARModel
result,_ = verification.GetHttpsApiRestShApiVA(collect)

```


### <a name="create_https_api_rest_sh_api_va"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.CreateHttpsApiRestShApiVA") CreateHttpsApiRestShApiVA

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```go
func (me *VERIFICATION_IMPL) CreateHttpsApiRestShApiVA(input *CreateHttpsApiRestShApiVAInput)(*models_pkg.HttpsApiRestShApiVARModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (verification_pkg.CreateHttpsApiRestShApiVAInput)

var body *models_pkg.HttpsApiRestShApiVAModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiVARModel
result,_ = verification.CreateHttpsApiRestShApiVA(collect)

```


### <a name="get_https_api_rest_sh_api_vu"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.GetHttpsApiRestShApiVU") GetHttpsApiRestShApiVU

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```go
func (me *VERIFICATION_IMPL) GetHttpsApiRestShApiVU(input *GetHttpsApiRestShApiVUInput)(*models_pkg.HttpsApiRestShApiVURModel,error)
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
collect := new (verification_pkg.GetHttpsApiRestShApiVUInput)

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


var result *models_pkg.HttpsApiRestShApiVURModel
result,_ = verification.GetHttpsApiRestShApiVU(collect)

```


### <a name="create_https_api_rest_sh_api_vu"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.CreateHttpsApiRestShApiVU") CreateHttpsApiRestShApiVU

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```go
func (me *VERIFICATION_IMPL) CreateHttpsApiRestShApiVU(input *CreateHttpsApiRestShApiVUInput)(*models_pkg.HttpsApiRestShApiVURModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (verification_pkg.CreateHttpsApiRestShApiVUInput)

var body *models_pkg.HttpsApiRestShApiVUModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiVURModel
result,_ = verification.CreateHttpsApiRestShApiVU(collect)

```


### <a name="get_https_api_rest_sh_api_v"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.GetHttpsApiRestShApiV") GetHttpsApiRestShApiV

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```go
func (me *VERIFICATION_IMPL) GetHttpsApiRestShApiV(input *GetHttpsApiRestShApiVInput)(*models_pkg.HttpsApiRestShApiVRModel,error)
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
collect := new (verification_pkg.GetHttpsApiRestShApiVInput)

key := "key"
collect.Key = key

uid := "uid"
collect.Uid = uid

to := "to"
collect.To = to

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiVRModel
result,_ = verification.GetHttpsApiRestShApiV(collect)

```


### <a name="create_https_api_rest_sh_api_v"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.CreateHttpsApiRestShApiV") CreateHttpsApiRestShApiV

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```go
func (me *VERIFICATION_IMPL) CreateHttpsApiRestShApiV(input *CreateHttpsApiRestShApiVInput)(*models_pkg.HttpsApiRestShApiVRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (verification_pkg.CreateHttpsApiRestShApiVInput)

var body *models_pkg.HttpsApiRestShApiVModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiVRModel
result,_ = verification.CreateHttpsApiRestShApiV(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="twofactorauthenticationapi_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".twofactorauthenticationapi_pkg") twofactorauthenticationapi_pkg

### Get instance

Factory for the ``` TWOFACTORAUTHENTICATIONAPI ``` interface can be accessed from the package twofactorauthenticationapi_pkg.

```go
twoFactorAuthenticationAPI := twofactorauthenticationapi_pkg.NewTWOFACTORAUTHENTICATIONAPI()
```

### <a name="get_https_api_rest_sh_api2fa_t"></a>![Method: ](https://apidocs.io/img/method.png ".twofactorauthenticationapi_pkg.GetHttpsApiRestShApi2faT") GetHttpsApiRestShApi2faT

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```go
func (me *TWOFACTORAUTHENTICATIONAPI_IMPL) GetHttpsApiRestShApi2faT(input *GetHttpsApiRestShApi2faTInput)(*models_pkg.HttpsApiRestShApi2faTRModel,error)
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
collect := new (twofactorauthenticationapi_pkg.GetHttpsApiRestShApi2faTInput)

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


var result *models_pkg.HttpsApiRestShApi2faTRModel
result,_ = twoFactorAuthenticationAPI.GetHttpsApiRestShApi2faT(collect)

```


### <a name="create_https_api_rest_sh_api2fa_t"></a>![Method: ](https://apidocs.io/img/method.png ".twofactorauthenticationapi_pkg.CreateHttpsApiRestShApi2faT") CreateHttpsApiRestShApi2faT

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```go
func (me *TWOFACTORAUTHENTICATIONAPI_IMPL) CreateHttpsApiRestShApi2faT(input *CreateHttpsApiRestShApi2faTInput)(*models_pkg.HttpsApiRestShApi2faTRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (twofactorauthenticationapi_pkg.CreateHttpsApiRestShApi2faTInput)

var body *models_pkg.HttpsApiRestShApi2faTModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApi2faTRModel
result,_ = twoFactorAuthenticationAPI.CreateHttpsApiRestShApi2faT(collect)

```


### <a name="get_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png ".twofactorauthenticationapi_pkg.GetHttpsApiRestShApi2fa") GetHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```go
func (me *TWOFACTORAUTHENTICATIONAPI_IMPL) GetHttpsApiRestShApi2fa(input *GetHttpsApiRestShApi2faInput)(*models_pkg.HttpsApiRestShApi2faRModel,error)
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


var result *models_pkg.HttpsApiRestShApi2faRModel
result,_ = twoFactorAuthenticationAPI.GetHttpsApiRestShApi2fa(collect)

```


### <a name="create_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png ".twofactorauthenticationapi_pkg.CreateHttpsApiRestShApi2fa") CreateHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```go
func (me *TWOFACTORAUTHENTICATIONAPI_IMPL) CreateHttpsApiRestShApi2fa(input *CreateHttpsApiRestShApi2faInput)(*models_pkg.HttpsApiRestShApi2faRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (twofactorauthenticationapi_pkg.CreateHttpsApiRestShApi2faInput)

var body *models_pkg.HttpsApiRestShApi2faModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApi2faRModel
result,_ = twoFactorAuthenticationAPI.CreateHttpsApiRestShApi2fa(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="usermanagement_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".usermanagement_pkg") usermanagement_pkg

### Get instance

Factory for the ``` USERMANAGEMENT ``` interface can be accessed from the package usermanagement_pkg.

```go
userManagement := usermanagement_pkg.NewUSERMANAGEMENT()
```

### <a name="get_https_api_rest_sh_api_ui"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.GetHttpsApiRestShApiUI") GetHttpsApiRestShApiUI

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```go
func (me *USERMANAGEMENT_IMPL) GetHttpsApiRestShApiUI(input *GetHttpsApiRestShApiUIInput)(*models_pkg.HttpsApiRestShApiUIRModel,error)
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
collect := new (usermanagement_pkg.GetHttpsApiRestShApiUIInput)

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


var result *models_pkg.HttpsApiRestShApiUIRModel
result,_ = userManagement.GetHttpsApiRestShApiUI(collect)

```


### <a name="create_https_api_rest_sh_api_ui"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.CreateHttpsApiRestShApiUI") CreateHttpsApiRestShApiUI

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```go
func (me *USERMANAGEMENT_IMPL) CreateHttpsApiRestShApiUI(input *CreateHttpsApiRestShApiUIInput)(*models_pkg.HttpsApiRestShApiUIRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (usermanagement_pkg.CreateHttpsApiRestShApiUIInput)

var body *models_pkg.HttpsApiRestShApiUIModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiUIRModel
result,_ = userManagement.CreateHttpsApiRestShApiUI(collect)

```


### <a name="get_https_api_rest_sh_api_uu"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.GetHttpsApiRestShApiUU") GetHttpsApiRestShApiUU

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```go
func (me *USERMANAGEMENT_IMPL) GetHttpsApiRestShApiUU(input *GetHttpsApiRestShApiUUInput)(*models_pkg.HttpsApiRestShApiUURModel,error)
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
collect := new (usermanagement_pkg.GetHttpsApiRestShApiUUInput)

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


var result *models_pkg.HttpsApiRestShApiUURModel
result,_ = userManagement.GetHttpsApiRestShApiUU(collect)

```


### <a name="create_https_api_rest_sh_api_uu"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.CreateHttpsApiRestShApiUU") CreateHttpsApiRestShApiUU

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```go
func (me *USERMANAGEMENT_IMPL) CreateHttpsApiRestShApiUU(input *CreateHttpsApiRestShApiUUInput)(*models_pkg.HttpsApiRestShApiUURModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (usermanagement_pkg.CreateHttpsApiRestShApiUUInput)

var body *models_pkg.HttpsApiRestShApiUUModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiUURModel
result,_ = userManagement.CreateHttpsApiRestShApiUU(collect)

```


### <a name="get_https_api_rest_sh_api_ud"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.GetHttpsApiRestShApiUD") GetHttpsApiRestShApiUD

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```go
func (me *USERMANAGEMENT_IMPL) GetHttpsApiRestShApiUD(input *GetHttpsApiRestShApiUDInput)(*models_pkg.HttpsApiRestShApiUDRModel,error)
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
collect := new (usermanagement_pkg.GetHttpsApiRestShApiUDInput)

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


var result *models_pkg.HttpsApiRestShApiUDRModel
result,_ = userManagement.GetHttpsApiRestShApiUD(collect)

```


### <a name="create_https_api_rest_sh_api_ud"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.CreateHttpsApiRestShApiUD") CreateHttpsApiRestShApiUD

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```go
func (me *USERMANAGEMENT_IMPL) CreateHttpsApiRestShApiUD(input *CreateHttpsApiRestShApiUDInput)(*models_pkg.HttpsApiRestShApiUDRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (usermanagement_pkg.CreateHttpsApiRestShApiUDInput)

var body *models_pkg.HttpsApiRestShApiUDModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiUDRModel
result,_ = userManagement.CreateHttpsApiRestShApiUD(collect)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="loginandregistration_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".loginandregistration_pkg") loginandregistration_pkg

### Get instance

Factory for the ``` LOGINANDREGISTRATION ``` interface can be accessed from the package loginandregistration_pkg.

```go
loginAndRegistration := loginandregistration_pkg.NewLOGINANDREGISTRATION()
```

### <a name="get_https_api_rest_sh_api_aur"></a>![Method: ](https://apidocs.io/img/method.png ".loginandregistration_pkg.GetHttpsApiRestShApiAUR") GetHttpsApiRestShApiAUR

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```go
func (me *LOGINANDREGISTRATION_IMPL) GetHttpsApiRestShApiAUR(input *GetHttpsApiRestShApiAURInput)(*models_pkg.HttpsApiRestShApiAURRModel,error)
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
collect := new (loginandregistration_pkg.GetHttpsApiRestShApiAURInput)

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

phone,_ := strconv.ParseInt("212", 10, 8)
collect.Phone = phone

countrycode,_ := strconv.ParseInt("212", 10, 8)
collect.Countrycode = countrycode

address := "address"
collect.Address = address

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiAURRModel
result,_ = loginAndRegistration.GetHttpsApiRestShApiAUR(collect)

```


### <a name="create_https_api_rest_sh_api_aur"></a>![Method: ](https://apidocs.io/img/method.png ".loginandregistration_pkg.CreateHttpsApiRestShApiAUR") CreateHttpsApiRestShApiAUR

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```go
func (me *LOGINANDREGISTRATION_IMPL) CreateHttpsApiRestShApiAUR(input *CreateHttpsApiRestShApiAURInput)(*models_pkg.HttpsApiRestShApiAURRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (loginandregistration_pkg.CreateHttpsApiRestShApiAURInput)

var body *models_pkg.HttpsApiRestShApiAURModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiAURRModel
result,_ = loginAndRegistration.CreateHttpsApiRestShApiAUR(collect)

```


### <a name="get_https_api_rest_sh_api_aul"></a>![Method: ](https://apidocs.io/img/method.png ".loginandregistration_pkg.GetHttpsApiRestShApiAUL") GetHttpsApiRestShApiAUL

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```go
func (me *LOGINANDREGISTRATION_IMPL) GetHttpsApiRestShApiAUL(input *GetHttpsApiRestShApiAULInput)(*models_pkg.HttpsApiRestShApiAULRModel,error)
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
collect := new (loginandregistration_pkg.GetHttpsApiRestShApiAULInput)

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


var result *models_pkg.HttpsApiRestShApiAULRModel
result,_ = loginAndRegistration.GetHttpsApiRestShApiAUL(collect)

```


### <a name="create_https_api_rest_sh_api_aul"></a>![Method: ](https://apidocs.io/img/method.png ".loginandregistration_pkg.CreateHttpsApiRestShApiAUL") CreateHttpsApiRestShApiAUL

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```go
func (me *LOGINANDREGISTRATION_IMPL) CreateHttpsApiRestShApiAUL(input *CreateHttpsApiRestShApiAULInput)(*models_pkg.HttpsApiRestShApiAULRModel,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
collect := new (loginandregistration_pkg.CreateHttpsApiRestShApiAULInput)

var body *models_pkg.HttpsApiRestShApiAULModel
collect.Body = body

contentType := "Content-Type"
collect.ContentType = contentType


var result *models_pkg.HttpsApiRestShApiAULRModel
result,_ = loginAndRegistration.CreateHttpsApiRestShApiAUL(collect)

```


[Back to List of Controllers](#list_of_controllers)



