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
| uid | Your user ID |
| secret | Your Private API Key |
| key | Your Public API Key |


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

### <a name="logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".advancedlogging_pkg.LoggingInfo") LoggingInfo

> WAF Log Info


```go
func (me *ADVANCEDLOGGING_IMPL) LoggingInfo(
            key string,
            uid string,
            name string,
            origin string,
            time string,
            contentType string)(*models_pkg.HttpsApiRestShApiSLIR,error)
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
key := "key"
uid := "uid"
name := "name"
origin := "origin"
time := "time"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSLIR
result,_ = advancedLogging.LoggingInfo(key, uid, name, origin, time, contentType)

```


### <a name="logging_setup"></a>![Method: ](https://apidocs.io/img/method.png ".advancedlogging_pkg.LoggingSetup") LoggingSetup

> WAF Log Setup


```go
func (me *ADVANCEDLOGGING_IMPL) LoggingSetup(
            key string,
            uid string,
            name string,
            origin string,
            activate bool,
            contentType string)(*models_pkg.HttpsApiRestShApiSLR,error)
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
key := "key"
uid := "uid"
name := "name"
origin := "origin"
activate := false
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSLR
result,_ = advancedLogging.LoggingSetup(key, uid, name, origin, activate, contentType)

```


### <a name="logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".advancedlogging_pkg.LoggingInfo") LoggingInfo

> WAF Log Info


```go
func (me *ADVANCEDLOGGING_IMPL) LoggingInfo(
            body *models_pkg.HttpsApiRestShApiSLI,
            contentType string)(*models_pkg.HttpsApiRestShApiSLIR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiSLI
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSLIR
result,_ = advancedLogging.LoggingInfo(body, contentType)

```


### <a name="logging_setup"></a>![Method: ](https://apidocs.io/img/method.png ".advancedlogging_pkg.LoggingSetup") LoggingSetup

> WAF Log Setup


```go
func (me *ADVANCEDLOGGING_IMPL) LoggingSetup(
            body *models_pkg.HttpsApiRestShApiSL,
            contentType string)(*models_pkg.HttpsApiRestShApiSLR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiSL
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSLR
result,_ = advancedLogging.LoggingSetup(body, contentType)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="waf&ddosprotection_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".waf&ddosprotection_pkg") waf&ddosprotection_pkg

### Get instance

Factory for the ``` WAF&DDOSPROTECTION ``` interface can be accessed from the package waf&ddosprotection_pkg.

```go
wAFDDOSProtection := waf&ddosprotection_pkg.NewWAF&DDOSPROTECTION()
```

### <a name="https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".waf&ddosprotection_pkg.HttpsApiRestShApiSWC") HttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *WAFDDOSPROTECTION_IMPL) HttpsApiRestShApiSWC(
            key string,
            uid string,
            name string,
            origin string,
            rule string,
            contentType string)(*models_pkg.HttpsApiRestShApiSWCR,error)
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
key := "API"
uid := "UID"
name := "origin-name"
origin := "origin.yourdomain.tld"
rule := "header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does"
contentType := "application/json"

var result *models_pkg.HttpsApiRestShApiSWCR
result,_ = wAFDDOSProtection.HttpsApiRestShApiSWC(key, uid, name, origin, rule, contentType)

```


### <a name="https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".waf&ddosprotection_pkg.HttpsApiRestShApiSW") HttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *WAFDDOSPROTECTION_IMPL) HttpsApiRestShApiSW(
            key string,
            uid string,
            origin string,
            cname string,
            contentType string)(*models_pkg.HttpsApiRestShApiSWR,error)
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
key := "API"
uid := "UID"
origin := "origin.yourdomain.tld"
cname := "yourdomain.tld,www.yourdomain.tld"
contentType := "application/json"

var result *models_pkg.HttpsApiRestShApiSWR
result,_ = wAFDDOSProtection.HttpsApiRestShApiSW(key, uid, origin, cname, contentType)

```


### <a name="https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".waf&ddosprotection_pkg.HttpsApiRestShApiSWC") HttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *WAFDDOSPROTECTION_IMPL) HttpsApiRestShApiSWC(
            body *models_pkg.HttpsApiRestShApiSWC,
            contentType string)(*models_pkg.HttpsApiRestShApiSWCR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
bodyValue := []byte("{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}")
var body *models_pkg.HttpsApiRestShApiSWC
json.Unmarshal(bodyValue,&body)
contentType := "application/json"

var result *models_pkg.HttpsApiRestShApiSWCR
result,_ = wAFDDOSProtection.HttpsApiRestShApiSWC(body, contentType)

```


### <a name="https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".waf&ddosprotection_pkg.HttpsApiRestShApiSW") HttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *WAFDDOSPROTECTION_IMPL) HttpsApiRestShApiSW(
            body *models_pkg.HttpsApiRestShApiSW,
            contentType string)(*models_pkg.HttpsApiRestShApiSWR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
bodyValue := []byte("{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}")
var body *models_pkg.HttpsApiRestShApiSW
json.Unmarshal(bodyValue,&body)
contentType := "application/json"

var result *models_pkg.HttpsApiRestShApiSWR
result,_ = wAFDDOSProtection.HttpsApiRestShApiSW(body, contentType)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".encryption_pkg") encryption_pkg

### Get instance

Factory for the ``` ENCRYPTION ``` interface can be accessed from the package encryption_pkg.

```go
encryption := encryption_pkg.NewENCRYPTION()
```

### <a name="data_and_file_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".encryption_pkg.DataAndFileEncryption") DataAndFileEncryption

> Data and File Encryption API


```go
func (me *ENCRYPTION_IMPL) DataAndFileEncryption(
            key string,
            uid string,
            data string,
            method string,
            bit int64,
            contentType string)(*models_pkg.HttpsApiRestShApiSER,error)
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
key := "key"
uid := "uid"
data := "data"
method := "method"
bit,_ := strconv.ParseInt("126", 10, 8)
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSER
result,_ = encryption.DataAndFileEncryption(key, uid, data, method, bit, contentType)

```


### <a name="data_and_file_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".encryption_pkg.DataAndFileEncryption") DataAndFileEncryption

> Data and File Encryption API


```go
func (me *ENCRYPTION_IMPL) DataAndFileEncryption(
            body *models_pkg.HttpsApiRestShApiSE,
            contentType string)(*models_pkg.HttpsApiRestShApiSER,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiSE
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSER
result,_ = encryption.DataAndFileEncryption(body, contentType)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".cdn_pkg") cdn_pkg

### Get instance

Factory for the ``` CDN ``` interface can be accessed from the package cdn_pkg.

```go
cDN := cdn_pkg.NewCDN()
```

### <a name="cdn_push_zone"></a>![Method: ](https://apidocs.io/img/method.png ".cdn_pkg.CDNPushZone") CDNPushZone

> CDN Push Zone API


```go
func (me *CDN_IMPL) CDNPushZone(
            key string,
            uid string,
            cname string,
            file string,
            contentType string)(*models_pkg.HttpsApiRestShApiSCPushR,error)
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
key := "key"
uid := "uid"
cname := "cname"
file := "file"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSCPushR
result,_ = cDN.CDNPushZone(key, uid, cname, file, contentType)

```


### <a name="cdn_pull_zone"></a>![Method: ](https://apidocs.io/img/method.png ".cdn_pkg.CDNPullZone") CDNPullZone

> CDN Pull Zone API


```go
func (me *CDN_IMPL) CDNPullZone(
            key string,
            uid string,
            origin string,
            cname string,
            contentType string)(*models_pkg.HttpsApiRestShApiSCPullR,error)
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
key := "key"
uid := "uid"
origin := "origin"
cname := "cname"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSCPullR
result,_ = cDN.CDNPullZone(key, uid, origin, cname, contentType)

```


### <a name="cdn_push_zone"></a>![Method: ](https://apidocs.io/img/method.png ".cdn_pkg.CDNPushZone") CDNPushZone

> CDN Push Zone API


```go
func (me *CDN_IMPL) CDNPushZone(
            body *models_pkg.HttpsApiRestShApiSCPush,
            contentType string)(*models_pkg.HttpsApiRestShApiSCPushR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiSCPush
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSCPushR
result,_ = cDN.CDNPushZone(body, contentType)

```


### <a name="cdn_pull_zone"></a>![Method: ](https://apidocs.io/img/method.png ".cdn_pkg.CDNPullZone") CDNPullZone

> CDN Pull Zone API


```go
func (me *CDN_IMPL) CDNPullZone(
            body *models_pkg.HttpsApiRestShApiSCPull,
            contentType string)(*models_pkg.HttpsApiRestShApiSCPullR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiSCPull
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSCPullR
result,_ = cDN.CDNPullZone(body, contentType)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".dns_pkg") dns_pkg

### Get instance

Factory for the ``` DNS ``` interface can be accessed from the package dns_pkg.

```go
dNS := dns_pkg.NewDNS()
```

### <a name="dns_configuration"></a>![Method: ](https://apidocs.io/img/method.png ".dns_pkg.DNSConfiguration") DNSConfiguration

> DNS Configuration API


```go
func (me *DNS_IMPL) DNSConfiguration(
            key string,
            uid string,
            domain string,
            records string,
            contentType string)(*models_pkg.HttpsApiRestShApiSDCR,error)
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
key := "key"
uid := "uid"
domain := "domain"
records := "records"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSDCR
result,_ = dNS.DNSConfiguration(key, uid, domain, records, contentType)

```


### <a name="dns_configuration"></a>![Method: ](https://apidocs.io/img/method.png ".dns_pkg.DNSConfiguration") DNSConfiguration

> DNS Configuration API


```go
func (me *DNS_IMPL) DNSConfiguration(
            body *models_pkg.HttpsApiRestShApiSDC,
            contentType string)(*models_pkg.HttpsApiRestShApiSDCR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiSDC
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSDCR
result,_ = dNS.DNSConfiguration(body, contentType)

```


### <a name="dns_creation"></a>![Method: ](https://apidocs.io/img/method.png ".dns_pkg.DNSCreation") DNSCreation

> DNS Creation API


```go
func (me *DNS_IMPL) DNSCreation(
            key string,
            uid string,
            domain string,
            contentType string)(*models_pkg.HttpsApiRestShApiSDAR,error)
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
key := "key"
uid := "uid"
domain := "domain"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSDAR
result,_ = dNS.DNSCreation(key, uid, domain, contentType)

```


### <a name="dns_creation"></a>![Method: ](https://apidocs.io/img/method.png ".dns_pkg.DNSCreation") DNSCreation

> DNS Creation API


```go
func (me *DNS_IMPL) DNSCreation(
            body *models_pkg.HttpsApiRestShApiSDA,
            contentType string)(*models_pkg.HttpsApiRestShApiSDAR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiSDA
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSDAR
result,_ = dNS.DNSCreation(body, contentType)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="codeobfuscation_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".codeobfuscation_pkg") codeobfuscation_pkg

### Get instance

Factory for the ``` CODEOBFUSCATION ``` interface can be accessed from the package codeobfuscation_pkg.

```go
codeObfuscation := codeobfuscation_pkg.NewCODEOBFUSCATION()
```

### <a name="obfuscation_and_anti_tampering"></a>![Method: ](https://apidocs.io/img/method.png ".codeobfuscation_pkg.ObfuscationAndAntiTampering") ObfuscationAndAntiTampering

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```go
func (me *CODEOBFUSCATION_IMPL) ObfuscationAndAntiTampering(
            key string,
            uid string,
            app string,
            contentType string)(*models_pkg.HttpsApiRestShApiSOR,error)
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
key := "key"
uid := "uid"
app := "app"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSOR
result,_ = codeObfuscation.ObfuscationAndAntiTampering(key, uid, app, contentType)

```


### <a name="obfuscation_and_anti_tampering"></a>![Method: ](https://apidocs.io/img/method.png ".codeobfuscation_pkg.ObfuscationAndAntiTampering") ObfuscationAndAntiTampering

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```go
func (me *CODEOBFUSCATION_IMPL) ObfuscationAndAntiTampering(
            body *models_pkg.HttpsApiRestShApiSO,
            contentType string)(*models_pkg.HttpsApiRestShApiSOR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiSO
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSOR
result,_ = codeObfuscation.ObfuscationAndAntiTampering(body, contentType)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".hosting_pkg") hosting_pkg

### Get instance

Factory for the ``` HOSTING ``` interface can be accessed from the package hosting_pkg.

```go
hosting := hosting_pkg.NewHOSTING()
```

### <a name="hosting_setup"></a>![Method: ](https://apidocs.io/img/method.png ".hosting_pkg.HostingSetup") HostingSetup

> Node.JS and Static Web APP Hosting


```go
func (me *HOSTING_IMPL) HostingSetup(
            key string,
            uid string,
            app string,
            domain string,
            contentType string)(*models_pkg.HttpsApiRestShApiSHR,error)
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
key := "key"
uid := "uid"
app := "app"
domain := "domain"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSHR
result,_ = hosting.HostingSetup(key, uid, app, domain, contentType)

```


### <a name="hosting_setup"></a>![Method: ](https://apidocs.io/img/method.png ".hosting_pkg.HostingSetup") HostingSetup

> Node.JS and Static Web APP Hosting


```go
func (me *HOSTING_IMPL) HostingSetup(
            body *models_pkg.HttpsApiRestShApiSH,
            contentType string)(*models_pkg.HttpsApiRestShApiSHR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiSH
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiSHR
result,_ = hosting.HostingSetup(body, contentType)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="datamanipulation,conversion,sorting,andcompressionapi_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".datamanipulation,conversion,sorting,andcompressionapi_pkg") datamanipulation,conversion,sorting,andcompressionapi_pkg

### Get instance

Factory for the ``` DATAMANIPULATION,CONVERSION,SORTING,ANDCOMPRESSIONAPI ``` interface can be accessed from the package datamanipulation,conversion,sorting,andcompressionapi_pkg.

```go
dataManipulationConversionSortingAndCompressionAPI := datamanipulation,conversion,sorting,andcompressionapi_pkg.NewDATAMANIPULATION,CONVERSION,SORTING,ANDCOMPRESSIONAPI()
```

### <a name="https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".datamanipulation,conversion,sorting,andcompressionapi_pkg.HttpsApiRestShApiD") HttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *DATAMANIPULATIONCONVERSIONSORTINGANDCOMPRESSIONAPI_IMPL) HttpsApiRestShApiD(
            key string,
            uid string,
            user string,
            apiuid string,
            data string,
            contentType string)(*models_pkg.HttpsApiRestShApiDR,error)
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
key := "API"
uid := "UID"
user := "UID"
apiuid := "apiUID"
data := "https://static.yourcdn.com/data.file"
contentType := "application/json"

var result *models_pkg.HttpsApiRestShApiDR
result,_ = dataManipulationConversionSortingAndCompressionAPI.HttpsApiRestShApiD(key, uid, user, apiuid, data, contentType)

```


### <a name="https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".datamanipulation,conversion,sorting,andcompressionapi_pkg.HttpsApiRestShApiD") HttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```go
func (me *DATAMANIPULATIONCONVERSIONSORTINGANDCOMPRESSIONAPI_IMPL) HttpsApiRestShApiD(
            body *models_pkg.HttpsApiRestShApiD,
            contentType string)(*models_pkg.HttpsApiRestShApiDR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
bodyValue := []byte("{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}")
var body *models_pkg.HttpsApiRestShApiD
json.Unmarshal(bodyValue,&body)
contentType := "application/json"

var result *models_pkg.HttpsApiRestShApiDR
result,_ = dataManipulationConversionSortingAndCompressionAPI.HttpsApiRestShApiD(body, contentType)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="imagemanipulationandmoderationapi_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".imagemanipulationandmoderationapi_pkg") imagemanipulationandmoderationapi_pkg

### Get instance

Factory for the ``` IMAGEMANIPULATIONANDMODERATIONAPI ``` interface can be accessed from the package imagemanipulationandmoderationapi_pkg.

```go
imageManipulationAndModerationAPI := imagemanipulationandmoderationapi_pkg.NewIMAGEMANIPULATIONANDMODERATIONAPI()
```

### <a name="image_manipulation"></a>![Method: ](https://apidocs.io/img/method.png ".imagemanipulationandmoderationapi_pkg.ImageManipulation") ImageManipulation

> Image Manipulation API


```go
func (me *IMAGEMANIPULATIONANDMODERATIONAPI_IMPL) ImageManipulation(
            key string,
            uid string,
            image string,
            transform string,
            contentType string)(*models_pkg.HttpsApiRestShApiIR,error)
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
key := "key"
uid := "uid"
image := "image"
transform := "transform"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiIR
result,_ = imageManipulationAndModerationAPI.ImageManipulation(key, uid, image, transform, contentType)

```


### <a name="image_manipulation"></a>![Method: ](https://apidocs.io/img/method.png ".imagemanipulationandmoderationapi_pkg.ImageManipulation") ImageManipulation

> Image Manipulation API


```go
func (me *IMAGEMANIPULATIONANDMODERATIONAPI_IMPL) ImageManipulation(
            body *models_pkg.HttpsApiRestShApiI,
            contentType string)(*models_pkg.HttpsApiRestShApiIR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiI
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiIR
result,_ = imageManipulationAndModerationAPI.ImageManipulation(body, contentType)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".verification_pkg") verification_pkg

### Get instance

Factory for the ``` VERIFICATION ``` interface can be accessed from the package verification_pkg.

```go
verification := verification_pkg.NewVERIFICATION()
```

### <a name="user_address_verification"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.UserAddressVerification") UserAddressVerification

> User Address Verification API


```go
func (me *VERIFICATION_IMPL) UserAddressVerification(
            key string,
            uid string,
            user string,
            a string,
            sa string,
            c string,
            s string,
            z int64,
            contentType string)(*models_pkg.HttpsApiRestShApiVAR,error)
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
key := "key"
uid := "uid"
user := "user"
a := "a"
sa := "sa"
c := "c"
s := "s"
z,_ := strconv.ParseInt("126", 10, 8)
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiVAR
result,_ = verification.UserAddressVerification(key, uid, user, a, sa, c, s, z, contentType)

```


### <a name="user_address_verification"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.UserAddressVerification") UserAddressVerification

> User Address Verification API


```go
func (me *VERIFICATION_IMPL) UserAddressVerification(
            body *models_pkg.HttpsApiRestShApiVA,
            contentType string)(*models_pkg.HttpsApiRestShApiVAR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiVA
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiVAR
result,_ = verification.UserAddressVerification(body, contentType)

```


### <a name="user_verification"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.UserVerification") UserVerification

> User Verification API


```go
func (me *VERIFICATION_IMPL) UserVerification(
            key string,
            uid string,
            user string,
            code string,
            contentType string)(*models_pkg.HttpsApiRestShApiVUR,error)
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
key := "key"
uid := "uid"
user := "user"
code := "code"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiVUR
result,_ = verification.UserVerification(key, uid, user, code, contentType)

```


### <a name="user_verification"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.UserVerification") UserVerification

> User Verification API


```go
func (me *VERIFICATION_IMPL) UserVerification(
            body *models_pkg.HttpsApiRestShApiVU,
            contentType string)(*models_pkg.HttpsApiRestShApiVUR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiVU
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiVUR
result,_ = verification.UserVerification(body, contentType)

```


### <a name="cellphone_verification"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.CellphoneVerification") CellphoneVerification

> Verification API


```go
func (me *VERIFICATION_IMPL) CellphoneVerification(
            key string,
            uid string,
            to string,
            contentType string)(*models_pkg.HttpsApiRestShApiVR,error)
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
key := "key"
uid := "uid"
to := "to"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiVR
result,_ = verification.CellphoneVerification(key, uid, to, contentType)

```


### <a name="cellphone_verification"></a>![Method: ](https://apidocs.io/img/method.png ".verification_pkg.CellphoneVerification") CellphoneVerification

> Verification API


```go
func (me *VERIFICATION_IMPL) CellphoneVerification(
            body *models_pkg.HttpsApiRestShApiV,
            contentType string)(*models_pkg.HttpsApiRestShApiVR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiV
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiVR
result,_ = verification.CellphoneVerification(body, contentType)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="twofactorauthenticationapi_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".twofactorauthenticationapi_pkg") twofactorauthenticationapi_pkg

### Get instance

Factory for the ``` TWOFACTORAUTHENTICATIONAPI ``` interface can be accessed from the package twofactorauthenticationapi_pkg.

```go
twoFactorAuthenticationAPI := twofactorauthenticationapi_pkg.NewTWOFACTORAUTHENTICATIONAPI()
```

### <a name="m2_fa_token_response"></a>![Method: ](https://apidocs.io/img/method.png ".twofactorauthenticationapi_pkg.M2FATokenResponse") M2FATokenResponse

> Two Factor Authentication Token Reply


```go
func (me *TWOFACTORAUTHENTICATIONAPI_IMPL) M2FATokenResponse(
            key string,
            uid string,
            user string,
            code string,
            contentType string)(*models_pkg.HttpsApiRestShApi2faTR,error)
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
key := "key"
uid := "uid"
user := "user"
code := "code"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApi2faTR
result,_ = twoFactorAuthenticationAPI.M2FATokenResponse(key, uid, user, code, contentType)

```


### <a name="m2_fa_token_response"></a>![Method: ](https://apidocs.io/img/method.png ".twofactorauthenticationapi_pkg.M2FATokenResponse") M2FATokenResponse

> Two Factor Authentication Token Reply


```go
func (me *TWOFACTORAUTHENTICATIONAPI_IMPL) M2FATokenResponse(
            body *models_pkg.HttpsApiRestShApi2faT,
            contentType string)(*models_pkg.HttpsApiRestShApi2faTR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApi2faT
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApi2faTR
result,_ = twoFactorAuthenticationAPI.M2FATokenResponse(body, contentType)

```


### <a name="two_factor_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".twofactorauthenticationapi_pkg.TwoFactorAuthentication") TwoFactorAuthentication

> Two Factor Authentication API


```go
func (me *TWOFACTORAUTHENTICATIONAPI_IMPL) TwoFactorAuthentication(
            key string,
            uid string,
            to string,
            contentType string)(*models_pkg.HttpsApiRestShApi2faR,error)
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
key := "key"
uid := "uid"
to := "to"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApi2faR
result,_ = twoFactorAuthenticationAPI.TwoFactorAuthentication(key, uid, to, contentType)

```


### <a name="two_factor_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".twofactorauthenticationapi_pkg.TwoFactorAuthentication") TwoFactorAuthentication

> Two Factor Authentication API


```go
func (me *TWOFACTORAUTHENTICATIONAPI_IMPL) TwoFactorAuthentication(
            body *models_pkg.HttpsApiRestShApi2fa,
            contentType string)(*models_pkg.HttpsApiRestShApi2faR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApi2fa
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApi2faR
result,_ = twoFactorAuthenticationAPI.TwoFactorAuthentication(body, contentType)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="usermanagement_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".usermanagement_pkg") usermanagement_pkg

### Get instance

Factory for the ``` USERMANAGEMENT ``` interface can be accessed from the package usermanagement_pkg.

```go
userManagement := usermanagement_pkg.NewUSERMANAGEMENT()
```

### <a name="get_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.GetUserInfo") GetUserInfo

> Get User Info API


```go
func (me *USERMANAGEMENT_IMPL) GetUserInfo(
            key string,
            uid string,
            user string,
            apiuid string,
            contentType string)(*models_pkg.HttpsApiRestShApiUIR,error)
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
key := "key"
uid := "uid"
user := "user"
apiuid := "apiuid"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiUIR
result,_ = userManagement.GetUserInfo(key, uid, user, apiuid, contentType)

```


### <a name="get_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.GetUserInfo") GetUserInfo

> Get User Info API


```go
func (me *USERMANAGEMENT_IMPL) GetUserInfo(
            body *models_pkg.HttpsApiRestShApiUI,
            contentType string)(*models_pkg.HttpsApiRestShApiUIR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiUI
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiUIR
result,_ = userManagement.GetUserInfo(body, contentType)

```


### <a name="update_user"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.UpdateUser") UpdateUser

> Update User API


```go
func (me *USERMANAGEMENT_IMPL) UpdateUser(
            key string,
            uid string,
            user string,
            apiuid string,
            avatar string,
            customInput string,
            contentType string)(*models_pkg.HttpsApiRestShApiUUR,error)
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
key := "key"
uid := "uid"
user := "user"
apiuid := "apiuid"
avatar := "avatar"
customInput := "custom input"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiUUR
result,_ = userManagement.UpdateUser(key, uid, user, apiuid, avatar, customInput, contentType)

```


### <a name="update_user"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.UpdateUser") UpdateUser

> Update User API


```go
func (me *USERMANAGEMENT_IMPL) UpdateUser(
            body *models_pkg.HttpsApiRestShApiUU,
            contentType string)(*models_pkg.HttpsApiRestShApiUUR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiUU
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiUUR
result,_ = userManagement.UpdateUser(body, contentType)

```


### <a name="delete_user"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.DeleteUser") DeleteUser

> Delete User API


```go
func (me *USERMANAGEMENT_IMPL) DeleteUser(
            api string,
            uid string,
            user string,
            apiuid string,
            contentType string)(*models_pkg.HttpsApiRestShApiUDR,error)
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
api := "api"
uid := "uid"
user := "user"
apiuid := "apiuid"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiUDR
result,_ = userManagement.DeleteUser(api, uid, user, apiuid, contentType)

```


### <a name="delete_user"></a>![Method: ](https://apidocs.io/img/method.png ".usermanagement_pkg.DeleteUser") DeleteUser

> Delete User API


```go
func (me *USERMANAGEMENT_IMPL) DeleteUser(
            body *models_pkg.HttpsApiRestShApiUD,
            contentType string)(*models_pkg.HttpsApiRestShApiUDR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiUD
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiUDR
result,_ = userManagement.DeleteUser(body, contentType)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="loginandregistration_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".loginandregistration_pkg") loginandregistration_pkg

### Get instance

Factory for the ``` LOGINANDREGISTRATION ``` interface can be accessed from the package loginandregistration_pkg.

```go
loginAndRegistration := loginandregistration_pkg.NewLOGINANDREGISTRATION()
```

### <a name="user_registration"></a>![Method: ](https://apidocs.io/img/method.png ".loginandregistration_pkg.UserRegistration") UserRegistration

> User Registration API


```go
func (me *LOGINANDREGISTRATION_IMPL) UserRegistration(
            key string,
            uid string,
            user string,
            password string,
            name string,
            email string,
            phone int64,
            countrycode int64,
            address string,
            contentType string)(*models_pkg.HttpsApiRestShApiAURR,error)
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
key := "key"
uid := "uid"
user := "user"
password := "password"
name := "name"
email := "email"
phone,_ := strconv.ParseInt("126", 10, 8)
countrycode,_ := strconv.ParseInt("126", 10, 8)
address := "address"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiAURR
result,_ = loginAndRegistration.UserRegistration(key, uid, user, password, name, email, phone, countrycode, address, contentType)

```


### <a name="user_registration"></a>![Method: ](https://apidocs.io/img/method.png ".loginandregistration_pkg.UserRegistration") UserRegistration

> User Registration API


```go
func (me *LOGINANDREGISTRATION_IMPL) UserRegistration(
            body *models_pkg.HttpsApiRestShApiAUR,
            contentType string)(*models_pkg.HttpsApiRestShApiAURR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiAUR
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiAURR
result,_ = loginAndRegistration.UserRegistration(body, contentType)

```


### <a name="user_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".loginandregistration_pkg.UserAuthentication") UserAuthentication

> User Authentication API


```go
func (me *LOGINANDREGISTRATION_IMPL) UserAuthentication(
            key string,
            uid string,
            user string,
            password string,
            contentType string)(*models_pkg.HttpsApiRestShApiAULR,error)
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
key := "key"
uid := "uid"
user := "user"
password := "password"
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiAULR
result,_ = loginAndRegistration.UserAuthentication(key, uid, user, password, contentType)

```


### <a name="user_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".loginandregistration_pkg.UserAuthentication") UserAuthentication

> User Authentication API


```go
func (me *LOGINANDREGISTRATION_IMPL) UserAuthentication(
            body *models_pkg.HttpsApiRestShApiAUL,
            contentType string)(*models_pkg.HttpsApiRestShApiAULR,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.HttpsApiRestShApiAUL
contentType := "Content-Type"

var result *models_pkg.HttpsApiRestShApiAULR
result,_ = loginAndRegistration.UserAuthentication(body, contentType)

```


[Back to List of Controllers](#list_of_controllers)



