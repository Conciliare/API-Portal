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

The generated code uses the Newtonsoft Json.NET NuGet Package. If the automatic NuGet package restore
is enabled, these dependencies will be installed automatically. Therefore,
you will need internet access for build.

1. Open the solution (SMASH.sln) file.
2. Invoke the build process using `Ctrl+Shift+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Visual Studio](https://apidocs.io/illustration/cs?step=buildSDK&workspaceFolder=SMASH-CSharp&workspaceName=SMASH&projectName=SMASH.Tests)

## How to Use

The build process generates a portable class library, which can be used like a normal class library. The generated library is compatible with Windows Forms, Windows RT, Windows Phone 8,
Silverlight 5, Xamarin iOS, Xamarin Android and Mono. More information on how to use can be found at the [MSDN Portable Class Libraries documentation](http://msdn.microsoft.com/en-us/library/vstudio/gg597391%28v=vs.100%29.aspx).

The following section explains how to use the SMASH library in a new console project.

### 1. Starting a new project

For starting a new project, right click on the current solution from the *solution explorer* and choose  ``` Add -> New Project ```.

![Add a new project in the existing solution using Visual Studio](https://apidocs.io/illustration/cs?step=addProject&workspaceFolder=SMASH-CSharp&workspaceName=SMASH&projectName=SMASH.Tests)

Next, choose "Console Application", provide a ``` TestConsoleProject ``` as the project name and click ``` OK ```.

![Create a new console project using Visual Studio](https://apidocs.io/illustration/cs?step=createProject&workspaceFolder=SMASH-CSharp&workspaceName=SMASH&projectName=SMASH.Tests)

### 2. Set as startup project

The new console project is the entry point for the eventual execution. This requires us to set the ``` TestConsoleProject ``` as the start-up project. To do this, right-click on the  ``` TestConsoleProject ``` and choose  ``` Set as StartUp Project ``` form the context menu.

![Set the new cosole project as the start up project](https://apidocs.io/illustration/cs?step=setStartup&workspaceFolder=SMASH-CSharp&workspaceName=SMASH&projectName=SMASH.Tests)

### 3. Add reference of the library project

In order to use the SMASH library in the new project, first we must add a projet reference to the ``` TestConsoleProject ```. First, right click on the ``` References ``` node in the *solution explorer* and click ``` Add Reference... ```.

![Open references of the TestConsoleProject](https://apidocs.io/illustration/cs?step=addReference&workspaceFolder=SMASH-CSharp&workspaceName=SMASH&projectName=SMASH.Tests)

Next, a window will be displayed where we must set the ``` checkbox ``` on ``` SMASH.Tests ``` and click ``` OK ```. By doing this, we have added a reference of the ```SMASH.Tests``` project into the new ``` TestConsoleProject ```.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=createReference&workspaceFolder=SMASH-CSharp&workspaceName=SMASH&projectName=SMASH.Tests)

### 4. Write sample code

Once the ``` TestConsoleProject ``` is created, a file named ``` Program.cs ``` will be visible in the *solution explorer* with an empty ``` Main ``` method. This is the entry point for the execution of the entire solution.
Here, you can add code to initialize the client library and acquire the instance of a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=addCode&workspaceFolder=SMASH-CSharp&workspaceName=SMASH&projectName=SMASH.Tests)

## How to Test

The generated SDK also contain one or more Tests, which are contained in the Tests project.
In order to invoke these test cases, you will need *NUnit 3.0 Test Adapter Extension for Visual Studio*.
Once the SDK is complied, the test cases should appear in the Test Explorer window.
Here, you can click *Run All* to execute these test cases.

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| basicAuthUserName | The username to use with basic authentication |
| basicAuthPassword | The password to use with basic authentication |



API client can be initialized as following.

```csharp
// Configuration parameters and credentials
string basicAuthUserName = "basicAuthUserName"; // The username to use with basic authentication
string basicAuthPassword = "basicAuthPassword"; // The password to use with basic authentication

SMASHClient client = new SMASHClient(basicAuthUserName, basicAuthPassword);
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

## <a name="advanced_logging"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.AdvancedLogging") AdvancedLogging

### Get singleton instance

The singleton instance of the ``` AdvancedLogging ``` class can be accessed from the API Client.

```csharp
IAdvancedLogging advancedLogging = client.AdvancedLogging;
```

### <a name="logging_info"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLogging.LoggingInfo") LoggingInfo

> WAF Log Info


```csharp
Task<Models.HttpsApiRestShApiSLIR> LoggingInfo(
        string key,
        string uid,
        string name,
        string origin,
        string time,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string name = "name";
string origin = "origin";
string time = "time";
string contentType = "Content-Type";

Models.HttpsApiRestShApiSLIR result = await advancedLogging.LoggingInfo(key, uid, name, origin, time, contentType);

```


### <a name="logging_setup"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLogging.LoggingSetup") LoggingSetup

> WAF Log Setup


```csharp
Task<Models.HttpsApiRestShApiSLR> LoggingSetup(
        string key,
        string uid,
        string name,
        string origin,
        bool activate,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string name = "name";
string origin = "origin";
bool activate = false;
string contentType = "Content-Type";

Models.HttpsApiRestShApiSLR result = await advancedLogging.LoggingSetup(key, uid, name, origin, activate, contentType);

```


### <a name="logging_info"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLogging.LoggingInfo") LoggingInfo

> WAF Log Info


```csharp
Task<Models.HttpsApiRestShApiSLIR> LoggingInfo(Models.HttpsApiRestShApiSLI body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiSLI();
string contentType = "Content-Type";

Models.HttpsApiRestShApiSLIR result = await advancedLogging.LoggingInfo(body, contentType);

```


### <a name="logging_setup"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLogging.LoggingSetup") LoggingSetup

> WAF Log Setup


```csharp
Task<Models.HttpsApiRestShApiSLR> LoggingSetup(Models.HttpsApiRestShApiSL body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiSL();
string contentType = "Content-Type";

Models.HttpsApiRestShApiSLR result = await advancedLogging.LoggingSetup(body, contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.WAFDDOSProtection") WAFDDOSProtection

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtection ``` class can be accessed from the API Client.

```csharp
IWAFDDOSProtection wAFDDOSProtection = client.WAFDDOSProtection;
```

### <a name="https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFDDOSProtection.HttpsApiRestShApiSWC") HttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiSWCR> HttpsApiRestShApiSWC(
        string key,
        string uid,
        string name,
        string origin,
        string rule,
        string contentType)
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

```csharp
string key = "API";
string uid = "UID";
string name = "origin-name";
string origin = "origin.yourdomain.tld";
string rule = "header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does";
string contentType = "application/json";

Models.HttpsApiRestShApiSWCR result = await wAFDDOSProtection.HttpsApiRestShApiSWC(key, uid, name, origin, rule, contentType);

```


### <a name="https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFDDOSProtection.HttpsApiRestShApiSW") HttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiSWR> HttpsApiRestShApiSW(
        string key,
        string uid,
        string origin,
        string cname,
        string contentType)
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

```csharp
string key = "API";
string uid = "UID";
string origin = "origin.yourdomain.tld";
string cname = "yourdomain.tld,www.yourdomain.tld";
string contentType = "application/json";

Models.HttpsApiRestShApiSWR result = await wAFDDOSProtection.HttpsApiRestShApiSW(key, uid, origin, cname, contentType);

```


### <a name="https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFDDOSProtection.HttpsApiRestShApiSWC") HttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiSWCR> HttpsApiRestShApiSWC(Models.HttpsApiRestShApiSWC body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string bodyValue = "{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<Models.HttpsApiRestShApiSWC>(bodyValue);
string contentType = "application/json";

Models.HttpsApiRestShApiSWCR result = await wAFDDOSProtection.HttpsApiRestShApiSWC(body, contentType);

```


### <a name="https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFDDOSProtection.HttpsApiRestShApiSW") HttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiSWR> HttpsApiRestShApiSW(Models.HttpsApiRestShApiSW body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<Models.HttpsApiRestShApiSW>(bodyValue);
string contentType = "application/json";

Models.HttpsApiRestShApiSWR result = await wAFDDOSProtection.HttpsApiRestShApiSW(body, contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.Encryption") Encryption

### Get singleton instance

The singleton instance of the ``` Encryption ``` class can be accessed from the API Client.

```csharp
IEncryption encryption = client.Encryption;
```

### <a name="data_and_file_encryption"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.Encryption.DataAndFileEncryption") DataAndFileEncryption

> Data and File Encryption API


```csharp
Task<Models.HttpsApiRestShApiSER> DataAndFileEncryption(
        string key,
        string uid,
        string data,
        string method,
        int bit,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string data = "data";
string method = "method";
int bit = 110;
string contentType = "Content-Type";

Models.HttpsApiRestShApiSER result = await encryption.DataAndFileEncryption(key, uid, data, method, bit, contentType);

```


### <a name="data_and_file_encryption"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.Encryption.DataAndFileEncryption") DataAndFileEncryption

> Data and File Encryption API


```csharp
Task<Models.HttpsApiRestShApiSER> DataAndFileEncryption(Models.HttpsApiRestShApiSE body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiSE();
string contentType = "Content-Type";

Models.HttpsApiRestShApiSER result = await encryption.DataAndFileEncryption(body, contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.CDN") CDN

### Get singleton instance

The singleton instance of the ``` CDN ``` class can be accessed from the API Client.

```csharp
ICDN cDN = client.CDN;
```

### <a name="cdn_push_zone"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CDN.CDNPushZone") CDNPushZone

> CDN Push Zone API


```csharp
Task<Models.HttpsApiRestShApiSCPushR> CDNPushZone(
        string key,
        string uid,
        string cname,
        string file,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string cname = "cname";
string file = "file";
string contentType = "Content-Type";

Models.HttpsApiRestShApiSCPushR result = await cDN.CDNPushZone(key, uid, cname, file, contentType);

```


### <a name="cdn_pull_zone"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CDN.CDNPullZone") CDNPullZone

> CDN Pull Zone API


```csharp
Task<Models.HttpsApiRestShApiSCPullR> CDNPullZone(
        string key,
        string uid,
        string origin,
        string cname,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string origin = "origin";
string cname = "cname";
string contentType = "Content-Type";

Models.HttpsApiRestShApiSCPullR result = await cDN.CDNPullZone(key, uid, origin, cname, contentType);

```


### <a name="cdn_push_zone"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CDN.CDNPushZone") CDNPushZone

> CDN Push Zone API


```csharp
Task<Models.HttpsApiRestShApiSCPushR> CDNPushZone(Models.HttpsApiRestShApiSCPush body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiSCPush();
string contentType = "Content-Type";

Models.HttpsApiRestShApiSCPushR result = await cDN.CDNPushZone(body, contentType);

```


### <a name="cdn_pull_zone"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CDN.CDNPullZone") CDNPullZone

> CDN Pull Zone API


```csharp
Task<Models.HttpsApiRestShApiSCPullR> CDNPullZone(Models.HttpsApiRestShApiSCPull body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiSCPull();
string contentType = "Content-Type";

Models.HttpsApiRestShApiSCPullR result = await cDN.CDNPullZone(body, contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.DNS") DNS

### Get singleton instance

The singleton instance of the ``` DNS ``` class can be accessed from the API Client.

```csharp
IDNS dNS = client.DNS;
```

### <a name="dns_configuration"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DNS.DNSConfiguration") DNSConfiguration

> DNS Configuration API


```csharp
Task<Models.HttpsApiRestShApiSDCR> DNSConfiguration(
        string key,
        string uid,
        string domain,
        string records,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string domain = "domain";
string records = "records";
string contentType = "Content-Type";

Models.HttpsApiRestShApiSDCR result = await dNS.DNSConfiguration(key, uid, domain, records, contentType);

```


### <a name="dns_configuration"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DNS.DNSConfiguration") DNSConfiguration

> DNS Configuration API


```csharp
Task<Models.HttpsApiRestShApiSDCR> DNSConfiguration(Models.HttpsApiRestShApiSDC body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiSDC();
string contentType = "Content-Type";

Models.HttpsApiRestShApiSDCR result = await dNS.DNSConfiguration(body, contentType);

```


### <a name="dns_creation"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DNS.DNSCreation") DNSCreation

> DNS Creation API


```csharp
Task<Models.HttpsApiRestShApiSDAR> DNSCreation(
        string key,
        string uid,
        string domain,
        string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| domain |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string key = "key";
string uid = "uid";
string domain = "domain";
string contentType = "Content-Type";

Models.HttpsApiRestShApiSDAR result = await dNS.DNSCreation(key, uid, domain, contentType);

```


### <a name="dns_creation"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DNS.DNSCreation") DNSCreation

> DNS Creation API


```csharp
Task<Models.HttpsApiRestShApiSDAR> DNSCreation(Models.HttpsApiRestShApiSDA body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiSDA();
string contentType = "Content-Type";

Models.HttpsApiRestShApiSDAR result = await dNS.DNSCreation(body, contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.CodeObfuscation") CodeObfuscation

### Get singleton instance

The singleton instance of the ``` CodeObfuscation ``` class can be accessed from the API Client.

```csharp
ICodeObfuscation codeObfuscation = client.CodeObfuscation;
```

### <a name="obfuscation_and_anti_tampering"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CodeObfuscation.ObfuscationAndAntiTampering") ObfuscationAndAntiTampering

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```csharp
Task<Models.HttpsApiRestShApiSOR> ObfuscationAndAntiTampering(
        string key,
        string uid,
        string app,
        string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| app |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string key = "key";
string uid = "uid";
string app = "app";
string contentType = "Content-Type";

Models.HttpsApiRestShApiSOR result = await codeObfuscation.ObfuscationAndAntiTampering(key, uid, app, contentType);

```


### <a name="obfuscation_and_anti_tampering"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CodeObfuscation.ObfuscationAndAntiTampering") ObfuscationAndAntiTampering

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```csharp
Task<Models.HttpsApiRestShApiSOR> ObfuscationAndAntiTampering(Models.HttpsApiRestShApiSO body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiSO();
string contentType = "Content-Type";

Models.HttpsApiRestShApiSOR result = await codeObfuscation.ObfuscationAndAntiTampering(body, contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.Hosting") Hosting

### Get singleton instance

The singleton instance of the ``` Hosting ``` class can be accessed from the API Client.

```csharp
IHosting hosting = client.Hosting;
```

### <a name="hosting_setup"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.Hosting.HostingSetup") HostingSetup

> Node.JS and Static Web APP Hosting


```csharp
Task<Models.HttpsApiRestShApiSHR> HostingSetup(
        string key,
        string uid,
        string app,
        string domain,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string app = "app";
string domain = "domain";
string contentType = "Content-Type";

Models.HttpsApiRestShApiSHR result = await hosting.HostingSetup(key, uid, app, domain, contentType);

```


### <a name="hosting_setup"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.Hosting.HostingSetup") HostingSetup

> Node.JS and Static Web APP Hosting


```csharp
Task<Models.HttpsApiRestShApiSHR> HostingSetup(Models.HttpsApiRestShApiSH body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiSH();
string contentType = "Content-Type";

Models.HttpsApiRestShApiSHR result = await hosting.HostingSetup(body, contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.DataManipulationConversionSortingAndCompressionAPI") DataManipulationConversionSortingAndCompressionAPI

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPI ``` class can be accessed from the API Client.

```csharp
IDataManipulationConversionSortingAndCompressionAPI dataManipulationConversionSortingAndCompressionAPI = client.DataManipulationConversionSortingAndCompressionAPI;
```

### <a name="https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DataManipulationConversionSortingAndCompressionAPI.HttpsApiRestShApiD") HttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiDR> HttpsApiRestShApiD(
        string key,
        string uid,
        string user,
        string apiuid,
        string data,
        string contentType)
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

```csharp
string key = "API";
string uid = "UID";
string user = "UID";
string apiuid = "apiUID";
string data = "https://static.yourcdn.com/data.file";
string contentType = "application/json";

Models.HttpsApiRestShApiDR result = await dataManipulationConversionSortingAndCompressionAPI.HttpsApiRestShApiD(key, uid, user, apiuid, data, contentType);

```


### <a name="https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DataManipulationConversionSortingAndCompressionAPI.HttpsApiRestShApiD") HttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiDR> HttpsApiRestShApiD(Models.HttpsApiRestShApiD body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<Models.HttpsApiRestShApiD>(bodyValue);
string contentType = "application/json";

Models.HttpsApiRestShApiDR result = await dataManipulationConversionSortingAndCompressionAPI.HttpsApiRestShApiD(body, contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.ImageManipulationAndModerationAPI") ImageManipulationAndModerationAPI

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPI ``` class can be accessed from the API Client.

```csharp
IImageManipulationAndModerationAPI imageManipulationAndModerationAPI = client.ImageManipulationAndModerationAPI;
```

### <a name="image_manipulation"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.ImageManipulationAndModerationAPI.ImageManipulation") ImageManipulation

> Image Manipulation API


```csharp
Task<Models.HttpsApiRestShApiIR> ImageManipulation(
        string key,
        string uid,
        string image,
        string transform,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string image = "image";
string transform = "transform";
string contentType = "Content-Type";

Models.HttpsApiRestShApiIR result = await imageManipulationAndModerationAPI.ImageManipulation(key, uid, image, transform, contentType);

```


### <a name="image_manipulation"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.ImageManipulationAndModerationAPI.ImageManipulation") ImageManipulation

> Image Manipulation API


```csharp
Task<Models.HttpsApiRestShApiIR> ImageManipulation(Models.HttpsApiRestShApiI body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiI();
string contentType = "Content-Type";

Models.HttpsApiRestShApiIR result = await imageManipulationAndModerationAPI.ImageManipulation(body, contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.Verification") Verification

### Get singleton instance

The singleton instance of the ``` Verification ``` class can be accessed from the API Client.

```csharp
IVerification verification = client.Verification;
```

### <a name="user_address_verification"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.Verification.UserAddressVerification") UserAddressVerification

> User Address Verification API


```csharp
Task<Models.HttpsApiRestShApiVAR> UserAddressVerification(
        string key,
        string uid,
        string user,
        string a,
        string sa,
        string c,
        string s,
        int z,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string user = "user";
string a = "a";
string sa = "sa";
string c = "c";
string s = "s";
int z = 110;
string contentType = "Content-Type";

Models.HttpsApiRestShApiVAR result = await verification.UserAddressVerification(key, uid, user, a, sa, c, s, z, contentType);

```


### <a name="user_address_verification"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.Verification.UserAddressVerification") UserAddressVerification

> User Address Verification API


```csharp
Task<Models.HttpsApiRestShApiVAR> UserAddressVerification(Models.HttpsApiRestShApiVA body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiVA();
string contentType = "Content-Type";

Models.HttpsApiRestShApiVAR result = await verification.UserAddressVerification(body, contentType);

```


### <a name="user_verification"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.Verification.UserVerification") UserVerification

> User Verification API


```csharp
Task<Models.HttpsApiRestShApiVUR> UserVerification(
        string key,
        string uid,
        string user,
        string code,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string user = "user";
string code = "code";
string contentType = "Content-Type";

Models.HttpsApiRestShApiVUR result = await verification.UserVerification(key, uid, user, code, contentType);

```


### <a name="user_verification"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.Verification.UserVerification") UserVerification

> User Verification API


```csharp
Task<Models.HttpsApiRestShApiVUR> UserVerification(Models.HttpsApiRestShApiVU body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiVU();
string contentType = "Content-Type";

Models.HttpsApiRestShApiVUR result = await verification.UserVerification(body, contentType);

```


### <a name="cellphone_verification"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.Verification.CellphoneVerification") CellphoneVerification

> Verification API


```csharp
Task<Models.HttpsApiRestShApiVR> CellphoneVerification(
        string key,
        string uid,
        string to,
        string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string key = "key";
string uid = "uid";
string to = "to";
string contentType = "Content-Type";

Models.HttpsApiRestShApiVR result = await verification.CellphoneVerification(key, uid, to, contentType);

```


### <a name="cellphone_verification"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.Verification.CellphoneVerification") CellphoneVerification

> Verification API


```csharp
Task<Models.HttpsApiRestShApiVR> CellphoneVerification(Models.HttpsApiRestShApiV body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiV();
string contentType = "Content-Type";

Models.HttpsApiRestShApiVR result = await verification.CellphoneVerification(body, contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.TwoFactorAuthenticationAPI") TwoFactorAuthenticationAPI

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPI ``` class can be accessed from the API Client.

```csharp
ITwoFactorAuthenticationAPI twoFactorAuthenticationAPI = client.TwoFactorAuthenticationAPI;
```

### <a name="m2_fa_token_response"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.TwoFactorAuthenticationAPI.M2FATokenResponse") M2FATokenResponse

> Two Factor Authentication Token Reply


```csharp
Task<Models.HttpsApiRestShApi2faTR> M2FATokenResponse(
        string key,
        string uid,
        string user,
        string code,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string user = "user";
string code = "code";
string contentType = "Content-Type";

Models.HttpsApiRestShApi2faTR result = await twoFactorAuthenticationAPI.M2FATokenResponse(key, uid, user, code, contentType);

```


### <a name="m2_fa_token_response"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.TwoFactorAuthenticationAPI.M2FATokenResponse") M2FATokenResponse

> Two Factor Authentication Token Reply


```csharp
Task<Models.HttpsApiRestShApi2faTR> M2FATokenResponse(Models.HttpsApiRestShApi2faT body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApi2faT();
string contentType = "Content-Type";

Models.HttpsApiRestShApi2faTR result = await twoFactorAuthenticationAPI.M2FATokenResponse(body, contentType);

```


### <a name="two_factor_authentication"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.TwoFactorAuthenticationAPI.TwoFactorAuthentication") TwoFactorAuthentication

> Two Factor Authentication API


```csharp
Task<Models.HttpsApiRestShApi2faR> TwoFactorAuthentication(
        string key,
        string uid,
        string to,
        string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string key = "key";
string uid = "uid";
string to = "to";
string contentType = "Content-Type";

Models.HttpsApiRestShApi2faR result = await twoFactorAuthenticationAPI.TwoFactorAuthentication(key, uid, to, contentType);

```


### <a name="two_factor_authentication"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.TwoFactorAuthenticationAPI.TwoFactorAuthentication") TwoFactorAuthentication

> Two Factor Authentication API


```csharp
Task<Models.HttpsApiRestShApi2faR> TwoFactorAuthentication(Models.HttpsApiRestShApi2fa body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApi2fa();
string contentType = "Content-Type";

Models.HttpsApiRestShApi2faR result = await twoFactorAuthenticationAPI.TwoFactorAuthentication(body, contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.UserManagement") UserManagement

### Get singleton instance

The singleton instance of the ``` UserManagement ``` class can be accessed from the API Client.

```csharp
IUserManagement userManagement = client.UserManagement;
```

### <a name="get_user_info"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagement.GetUserInfo") GetUserInfo

> Get User Info API


```csharp
Task<Models.HttpsApiRestShApiUIR> GetUserInfo(
        string key,
        string uid,
        string user,
        string apiuid,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string user = "user";
string apiuid = "apiuid";
string contentType = "Content-Type";

Models.HttpsApiRestShApiUIR result = await userManagement.GetUserInfo(key, uid, user, apiuid, contentType);

```


### <a name="get_user_info"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagement.GetUserInfo") GetUserInfo

> Get User Info API


```csharp
Task<Models.HttpsApiRestShApiUIR> GetUserInfo(Models.HttpsApiRestShApiUI body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiUI();
string contentType = "Content-Type";

Models.HttpsApiRestShApiUIR result = await userManagement.GetUserInfo(body, contentType);

```


### <a name="update_user"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagement.UpdateUser") UpdateUser

> Update User API


```csharp
Task<Models.HttpsApiRestShApiUUR> UpdateUser(
        string key,
        string uid,
        string user,
        string apiuid,
        string avatar,
        string customInput,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string user = "user";
string apiuid = "apiuid";
string avatar = "avatar";
string customInput = "custom input";
string contentType = "Content-Type";

Models.HttpsApiRestShApiUUR result = await userManagement.UpdateUser(key, uid, user, apiuid, avatar, customInput, contentType);

```


### <a name="update_user"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagement.UpdateUser") UpdateUser

> Update User API


```csharp
Task<Models.HttpsApiRestShApiUUR> UpdateUser(Models.HttpsApiRestShApiUU body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiUU();
string contentType = "Content-Type";

Models.HttpsApiRestShApiUUR result = await userManagement.UpdateUser(body, contentType);

```


### <a name="delete_user"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagement.DeleteUser") DeleteUser

> Delete User API


```csharp
Task<Models.HttpsApiRestShApiUDR> DeleteUser(
        string api,
        string uid,
        string user,
        string apiuid,
        string contentType)
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

```csharp
string api = "api";
string uid = "uid";
string user = "user";
string apiuid = "apiuid";
string contentType = "Content-Type";

Models.HttpsApiRestShApiUDR result = await userManagement.DeleteUser(api, uid, user, apiuid, contentType);

```


### <a name="delete_user"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagement.DeleteUser") DeleteUser

> Delete User API


```csharp
Task<Models.HttpsApiRestShApiUDR> DeleteUser(Models.HttpsApiRestShApiUD body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiUD();
string contentType = "Content-Type";

Models.HttpsApiRestShApiUDR result = await userManagement.DeleteUser(body, contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.LoginAndRegistration") LoginAndRegistration

### Get singleton instance

The singleton instance of the ``` LoginAndRegistration ``` class can be accessed from the API Client.

```csharp
ILoginAndRegistration loginAndRegistration = client.LoginAndRegistration;
```

### <a name="user_registration"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.LoginAndRegistration.UserRegistration") UserRegistration

> User Registration API


```csharp
Task<Models.HttpsApiRestShApiAURR> UserRegistration(
        string key,
        string uid,
        string user,
        string password,
        string name,
        string email,
        int phone,
        int countrycode,
        string address,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string user = "user";
string password = "password";
string name = "name";
string email = "email";
int phone = 202;
int countrycode = 202;
string address = "address";
string contentType = "Content-Type";

Models.HttpsApiRestShApiAURR result = await loginAndRegistration.UserRegistration(key, uid, user, password, name, email, phone, countrycode, address, contentType);

```


### <a name="user_registration"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.LoginAndRegistration.UserRegistration") UserRegistration

> User Registration API


```csharp
Task<Models.HttpsApiRestShApiAURR> UserRegistration(Models.HttpsApiRestShApiAUR body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiAUR();
string contentType = "Content-Type";

Models.HttpsApiRestShApiAURR result = await loginAndRegistration.UserRegistration(body, contentType);

```


### <a name="user_authentication"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.LoginAndRegistration.UserAuthentication") UserAuthentication

> User Authentication API


```csharp
Task<Models.HttpsApiRestShApiAULR> UserAuthentication(
        string key,
        string uid,
        string user,
        string password,
        string contentType)
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

```csharp
string key = "key";
string uid = "uid";
string user = "user";
string password = "password";
string contentType = "Content-Type";

Models.HttpsApiRestShApiAULR result = await loginAndRegistration.UserAuthentication(key, uid, user, password, contentType);

```


### <a name="user_authentication"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.LoginAndRegistration.UserAuthentication") UserAuthentication

> User Authentication API


```csharp
Task<Models.HttpsApiRestShApiAULR> UserAuthentication(Models.HttpsApiRestShApiAUL body, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new Models.HttpsApiRestShApiAUL();
string contentType = "Content-Type";

Models.HttpsApiRestShApiAULR result = await loginAndRegistration.UserAuthentication(body, contentType);

```


[Back to List of Controllers](#list_of_controllers)



