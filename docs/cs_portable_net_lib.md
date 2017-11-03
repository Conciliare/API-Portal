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
| key | Your API Key |
| uid | Your User ID |



API client can be initialized as following.

```csharp
// Configuration parameters and credentials
string key = "API"; // Your API Key
string uid = "UID"; // Your User ID

SMASHClient client = new SMASHClient(key, uid);
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

## <a name="advanced_logging_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.AdvancedLoggingController") AdvancedLoggingController

### Get singleton instance

The singleton instance of the ``` AdvancedLoggingController ``` class can be accessed from the API Client.

```csharp
IAdvancedLoggingController advancedLogging = client.AdvancedLogging;
```

### <a name="get_https_api_rest_sh_api_security_logging_info"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLoggingController.GetHttpsApiRestShApiSecurityLoggingInfo") GetHttpsApiRestShApiSecurityLoggingInfo

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```csharp
Task<Models.HttpsApiRestShApiSecurityLoggingInfoResponseModel> GetHttpsApiRestShApiSecurityLoggingInfo(Models.GetHttpsApiRestShApiSecurityLoggingInfoInput input)
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
GetHttpsApiRestShApiSecurityLoggingInfoInput collect = new GetHttpsApiRestShApiSecurityLoggingInfoInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string name = "name";
collect.Name = name;

string origin = "origin";
collect.Origin = origin;

string time = "time";
collect.Time = time;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSecurityLoggingInfoResponseModel result = await advancedLogging.GetHttpsApiRestShApiSecurityLoggingInfo(collect);

```


### <a name="get_https_api_rest_sh_api_security_logging"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLoggingController.GetHttpsApiRestShApiSecurityLogging") GetHttpsApiRestShApiSecurityLogging

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```csharp
Task<Models.HttpsApiRestShApiSecurityLoggingResponseModel> GetHttpsApiRestShApiSecurityLogging(Models.GetHttpsApiRestShApiSecurityLoggingInput input)
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
GetHttpsApiRestShApiSecurityLoggingInput collect = new GetHttpsApiRestShApiSecurityLoggingInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string name = "name";
collect.Name = name;

string origin = "origin";
collect.Origin = origin;

bool activate = false;
collect.Activate = activate;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSecurityLoggingResponseModel result = await advancedLogging.GetHttpsApiRestShApiSecurityLogging(collect);

```


### <a name="create_https_api_rest_sh_api_security_logging_info"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLoggingController.CreateHttpsApiRestShApiSecurityLoggingInfo") CreateHttpsApiRestShApiSecurityLoggingInfo

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```csharp
Task<Models.HttpsApiRestShApiSecurityLoggingInfoResponseModel> CreateHttpsApiRestShApiSecurityLoggingInfo(Models.CreateHttpsApiRestShApiSecurityLoggingInfoInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSecurityLoggingInfoInput collect = new CreateHttpsApiRestShApiSecurityLoggingInfoInput();

var body = new Models.HttpsApiRestShApiSecurityLoggingInfoRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSecurityLoggingInfoResponseModel result = await advancedLogging.CreateHttpsApiRestShApiSecurityLoggingInfo(collect);

```


### <a name="create_https_api_rest_sh_api_security_logging"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLoggingController.CreateHttpsApiRestShApiSecurityLogging") CreateHttpsApiRestShApiSecurityLogging

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```csharp
Task<Models.HttpsApiRestShApiSecurityLoggingResponseModel> CreateHttpsApiRestShApiSecurityLogging(Models.CreateHttpsApiRestShApiSecurityLoggingInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSecurityLoggingInput collect = new CreateHttpsApiRestShApiSecurityLoggingInput();

var body = new Models.HttpsApiRestShApiSecurityLoggingRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSecurityLoggingResponseModel result = await advancedLogging.CreateHttpsApiRestShApiSecurityLogging(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.WAFDDOSProtectionController") WAFDDOSProtectionController

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtectionController ``` class can be accessed from the API Client.

```csharp
IWAFDDOSProtectionController wAFDDOSProtection = client.WAFDDOSProtection;
```

### <a name="get_https_api_rest_sh_api_security_waf_configure"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFDDOSProtectionController.GetHttpsApiRestShApiSecurityWafConfigure") GetHttpsApiRestShApiSecurityWafConfigure

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiSecurityWafConfigureResponseModel> GetHttpsApiRestShApiSecurityWafConfigure(Models.GetHttpsApiRestShApiSecurityWafConfigureInput input)
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
GetHttpsApiRestShApiSecurityWafConfigureInput collect = new GetHttpsApiRestShApiSecurityWafConfigureInput();

string key = "API";
collect.Key = key;

string uid = "UID";
collect.Uid = uid;

string name = "origin-name";
collect.Name = name;

string origin = "origin.yourdomain.tld";
collect.Origin = origin;

string rule = "header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does";
collect.Rule = rule;

string contentType = "application/json";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSecurityWafConfigureResponseModel result = await wAFDDOSProtection.GetHttpsApiRestShApiSecurityWafConfigure(collect);

```


### <a name="get_https_api_rest_sh_api_security_waf"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFDDOSProtectionController.GetHttpsApiRestShApiSecurityWaf") GetHttpsApiRestShApiSecurityWaf

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiSecurityWafResponseModel> GetHttpsApiRestShApiSecurityWaf(Models.GetHttpsApiRestShApiSecurityWafInput input)
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
GetHttpsApiRestShApiSecurityWafInput collect = new GetHttpsApiRestShApiSecurityWafInput();

string key = "API";
collect.Key = key;

string uid = "UID";
collect.Uid = uid;

string origin = "origin.yourdomain.tld";
collect.Origin = origin;

string cname = "yourdomain.tld,www.yourdomain.tld";
collect.Cname = cname;

string contentType = "application/json";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSecurityWafResponseModel result = await wAFDDOSProtection.GetHttpsApiRestShApiSecurityWaf(collect);

```


### <a name="create_https_api_rest_sh_api_security_waf_configure"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFDDOSProtectionController.CreateHttpsApiRestShApiSecurityWafConfigure") CreateHttpsApiRestShApiSecurityWafConfigure

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiSecurityWafConfigureResponseModel> CreateHttpsApiRestShApiSecurityWafConfigure(Models.CreateHttpsApiRestShApiSecurityWafConfigureInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSecurityWafConfigureInput collect = new CreateHttpsApiRestShApiSecurityWafConfigureInput();

string bodyValue = "{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<Models.HttpsApiRestShApiSecurityWafConfigureRequestModel>(bodyValue);
collect.Body = body;

string contentType = "application/json";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSecurityWafConfigureResponseModel result = await wAFDDOSProtection.CreateHttpsApiRestShApiSecurityWafConfigure(collect);

```


### <a name="create_https_api_rest_sh_api_security_waf"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFDDOSProtectionController.CreateHttpsApiRestShApiSecurityWaf") CreateHttpsApiRestShApiSecurityWaf

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiSecurityWafResponseModel> CreateHttpsApiRestShApiSecurityWaf(Models.CreateHttpsApiRestShApiSecurityWafInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSecurityWafInput collect = new CreateHttpsApiRestShApiSecurityWafInput();

string bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<Models.HttpsApiRestShApiSecurityWafRequestModel>(bodyValue);
collect.Body = body;

string contentType = "application/json";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSecurityWafResponseModel result = await wAFDDOSProtection.CreateHttpsApiRestShApiSecurityWaf(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.EncryptionController") EncryptionController

### Get singleton instance

The singleton instance of the ``` EncryptionController ``` class can be accessed from the API Client.

```csharp
IEncryptionController encryption = client.Encryption;
```

### <a name="get_https_api_rest_sh_api_security_encryption"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.EncryptionController.GetHttpsApiRestShApiSecurityEncryption") GetHttpsApiRestShApiSecurityEncryption

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```csharp
Task<Models.HttpsApiRestShApiSecurityEncryptionResponseModel> GetHttpsApiRestShApiSecurityEncryption(Models.GetHttpsApiRestShApiSecurityEncryptionInput input)
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
GetHttpsApiRestShApiSecurityEncryptionInput collect = new GetHttpsApiRestShApiSecurityEncryptionInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string data = "data";
collect.Data = data;

string method = "method";
collect.Method = method;

int bit = 65;
collect.Bit = bit;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSecurityEncryptionResponseModel result = await encryption.GetHttpsApiRestShApiSecurityEncryption(collect);

```


### <a name="create_https_api_rest_sh_api_security_encryption"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.EncryptionController.CreateHttpsApiRestShApiSecurityEncryption") CreateHttpsApiRestShApiSecurityEncryption

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```csharp
Task<Models.HttpsApiRestShApiSecurityEncryptionResponseModel> CreateHttpsApiRestShApiSecurityEncryption(Models.CreateHttpsApiRestShApiSecurityEncryptionInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSecurityEncryptionInput collect = new CreateHttpsApiRestShApiSecurityEncryptionInput();

var body = new Models.HttpsApiRestShApiSecurityEncryptionRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSecurityEncryptionResponseModel result = await encryption.CreateHttpsApiRestShApiSecurityEncryption(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.CDNController") CDNController

### Get singleton instance

The singleton instance of the ``` CDNController ``` class can be accessed from the API Client.

```csharp
ICDNController cDN = client.CDN;
```

### <a name="get_https_api_rest_sh_api_service_cdn_push"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CDNController.GetHttpsApiRestShApiServiceCdnPush") GetHttpsApiRestShApiServiceCdnPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```csharp
Task<Models.HttpsApiRestShApiServiceCdnPushResponseModel> GetHttpsApiRestShApiServiceCdnPush(Models.GetHttpsApiRestShApiServiceCdnPushInput input)
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
GetHttpsApiRestShApiServiceCdnPushInput collect = new GetHttpsApiRestShApiServiceCdnPushInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string cname = "cname";
collect.Cname = cname;

string file = "file";
collect.File = file;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiServiceCdnPushResponseModel result = await cDN.GetHttpsApiRestShApiServiceCdnPush(collect);

```


### <a name="get_https_api_rest_sh_api_service_cdn_pull"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CDNController.GetHttpsApiRestShApiServiceCdnPull") GetHttpsApiRestShApiServiceCdnPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```csharp
Task<Models.HttpsApiRestShApiServiceCdnPullResponseModel> GetHttpsApiRestShApiServiceCdnPull(Models.GetHttpsApiRestShApiServiceCdnPullInput input)
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
GetHttpsApiRestShApiServiceCdnPullInput collect = new GetHttpsApiRestShApiServiceCdnPullInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string origin = "origin";
collect.Origin = origin;

string cname = "cname";
collect.Cname = cname;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiServiceCdnPullResponseModel result = await cDN.GetHttpsApiRestShApiServiceCdnPull(collect);

```


### <a name="create_https_api_rest_sh_api_service_cdn_push"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CDNController.CreateHttpsApiRestShApiServiceCdnPush") CreateHttpsApiRestShApiServiceCdnPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```csharp
Task<Models.HttpsApiRestShApiServiceCdnPushResponseModel> CreateHttpsApiRestShApiServiceCdnPush(Models.CreateHttpsApiRestShApiServiceCdnPushInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiServiceCdnPushInput collect = new CreateHttpsApiRestShApiServiceCdnPushInput();

var body = new Models.HttpsApiRestShApiServiceCdnPushRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiServiceCdnPushResponseModel result = await cDN.CreateHttpsApiRestShApiServiceCdnPush(collect);

```


### <a name="create_https_api_rest_sh_api_service_cdn_pull"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CDNController.CreateHttpsApiRestShApiServiceCdnPull") CreateHttpsApiRestShApiServiceCdnPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```csharp
Task<Models.HttpsApiRestShApiServiceCdnPullResponseModel> CreateHttpsApiRestShApiServiceCdnPull(Models.CreateHttpsApiRestShApiServiceCdnPullInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiServiceCdnPullInput collect = new CreateHttpsApiRestShApiServiceCdnPullInput();

var body = new Models.HttpsApiRestShApiServiceCdnPullRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiServiceCdnPullResponseModel result = await cDN.CreateHttpsApiRestShApiServiceCdnPull(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.DNSController") DNSController

### Get singleton instance

The singleton instance of the ``` DNSController ``` class can be accessed from the API Client.

```csharp
IDNSController dNS = client.DNS;
```

### <a name="get_https_api_rest_sh_api_service_dns_configure"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DNSController.GetHttpsApiRestShApiServiceDnsConfigure") GetHttpsApiRestShApiServiceDnsConfigure

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```csharp
Task<Models.HttpsApiRestShApiServiceDnsConfigureResponseModel> GetHttpsApiRestShApiServiceDnsConfigure(Models.GetHttpsApiRestShApiServiceDnsConfigureInput input)
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
GetHttpsApiRestShApiServiceDnsConfigureInput collect = new GetHttpsApiRestShApiServiceDnsConfigureInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string domain = "domain";
collect.Domain = domain;

string records = "records";
collect.Records = records;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiServiceDnsConfigureResponseModel result = await dNS.GetHttpsApiRestShApiServiceDnsConfigure(collect);

```


### <a name="create_https_api_rest_sh_api_service_dns_configure"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DNSController.CreateHttpsApiRestShApiServiceDnsConfigure") CreateHttpsApiRestShApiServiceDnsConfigure

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```csharp
Task<Models.HttpsApiRestShApiServiceDnsConfigureResponseModel> CreateHttpsApiRestShApiServiceDnsConfigure(Models.CreateHttpsApiRestShApiServiceDnsConfigureInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiServiceDnsConfigureInput collect = new CreateHttpsApiRestShApiServiceDnsConfigureInput();

var body = new Models.HttpsApiRestShApiServiceDnsConfigureRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiServiceDnsConfigureResponseModel result = await dNS.CreateHttpsApiRestShApiServiceDnsConfigure(collect);

```


### <a name="get_https_api_rest_sh_api_service_dns_add"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DNSController.GetHttpsApiRestShApiServiceDnsAdd") GetHttpsApiRestShApiServiceDnsAdd

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```csharp
Task<Models.HttpsApiRestShApiServiceDnsAddResponseModel> GetHttpsApiRestShApiServiceDnsAdd(Models.GetHttpsApiRestShApiServiceDnsAddInput input)
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
GetHttpsApiRestShApiServiceDnsAddInput collect = new GetHttpsApiRestShApiServiceDnsAddInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string domain = "domain";
collect.Domain = domain;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiServiceDnsAddResponseModel result = await dNS.GetHttpsApiRestShApiServiceDnsAdd(collect);

```


### <a name="create_https_api_rest_sh_api_service_dns_add"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DNSController.CreateHttpsApiRestShApiServiceDnsAdd") CreateHttpsApiRestShApiServiceDnsAdd

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```csharp
Task<Models.HttpsApiRestShApiServiceDnsAddResponseModel> CreateHttpsApiRestShApiServiceDnsAdd(Models.CreateHttpsApiRestShApiServiceDnsAddInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiServiceDnsAddInput collect = new CreateHttpsApiRestShApiServiceDnsAddInput();

var body = new Models.HttpsApiRestShApiServiceDnsAddRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiServiceDnsAddResponseModel result = await dNS.CreateHttpsApiRestShApiServiceDnsAdd(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.CodeObfuscationController") CodeObfuscationController

### Get singleton instance

The singleton instance of the ``` CodeObfuscationController ``` class can be accessed from the API Client.

```csharp
ICodeObfuscationController codeObfuscation = client.CodeObfuscation;
```

### <a name="get_https_api_rest_sh_api_service_obfuscation"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CodeObfuscationController.GetHttpsApiRestShApiServiceObfuscation") GetHttpsApiRestShApiServiceObfuscation

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```csharp
Task<Models.HttpsApiRestShApiServiceObfuscationResponseModel> GetHttpsApiRestShApiServiceObfuscation(Models.GetHttpsApiRestShApiServiceObfuscationInput input)
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
GetHttpsApiRestShApiServiceObfuscationInput collect = new GetHttpsApiRestShApiServiceObfuscationInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string app = "app";
collect.App = app;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiServiceObfuscationResponseModel result = await codeObfuscation.GetHttpsApiRestShApiServiceObfuscation(collect);

```


### <a name="create_https_api_rest_sh_api_service_obfuscation"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CodeObfuscationController.CreateHttpsApiRestShApiServiceObfuscation") CreateHttpsApiRestShApiServiceObfuscation

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```csharp
Task<Models.HttpsApiRestShApiServiceObfuscationResponseModel> CreateHttpsApiRestShApiServiceObfuscation(Models.CreateHttpsApiRestShApiServiceObfuscationInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiServiceObfuscationInput collect = new CreateHttpsApiRestShApiServiceObfuscationInput();

var body = new Models.HttpsApiRestShApiServiceObfuscationRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiServiceObfuscationResponseModel result = await codeObfuscation.CreateHttpsApiRestShApiServiceObfuscation(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.HostingController") HostingController

### Get singleton instance

The singleton instance of the ``` HostingController ``` class can be accessed from the API Client.

```csharp
IHostingController hosting = client.Hosting;
```

### <a name="get_https_api_rest_sh_api_service_hosting"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.HostingController.GetHttpsApiRestShApiServiceHosting") GetHttpsApiRestShApiServiceHosting

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```csharp
Task<Models.HttpsApiRestShApiServiceHostingResponseModel> GetHttpsApiRestShApiServiceHosting(Models.GetHttpsApiRestShApiServiceHostingInput input)
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
GetHttpsApiRestShApiServiceHostingInput collect = new GetHttpsApiRestShApiServiceHostingInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string app = "app";
collect.App = app;

string domain = "domain";
collect.Domain = domain;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiServiceHostingResponseModel result = await hosting.GetHttpsApiRestShApiServiceHosting(collect);

```


### <a name="create_https_api_rest_sh_api_service_hosting"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.HostingController.CreateHttpsApiRestShApiServiceHosting") CreateHttpsApiRestShApiServiceHosting

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```csharp
Task<Models.HttpsApiRestShApiServiceHostingResponseModel> CreateHttpsApiRestShApiServiceHosting(Models.CreateHttpsApiRestShApiServiceHostingInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiServiceHostingInput collect = new CreateHttpsApiRestShApiServiceHostingInput();

var body = new Models.HttpsApiRestShApiServiceHostingRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiServiceHostingResponseModel result = await hosting.CreateHttpsApiRestShApiServiceHosting(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.DataManipulationConversionSortingAndCompressionAPIController") DataManipulationConversionSortingAndCompressionAPIController

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPIController ``` class can be accessed from the API Client.

```csharp
IDataManipulationConversionSortingAndCompressionAPIController dataManipulationConversionSortingAndCompressionAPI = client.DataManipulationConversionSortingAndCompressionAPI;
```

### <a name="get_https_api_rest_sh_api_data"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DataManipulationConversionSortingAndCompressionAPIController.GetHttpsApiRestShApiData") GetHttpsApiRestShApiData

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiDataResponseModel> GetHttpsApiRestShApiData(Models.GetHttpsApiRestShApiDataInput input)
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
GetHttpsApiRestShApiDataInput collect = new GetHttpsApiRestShApiDataInput();

string key = "API";
collect.Key = key;

string uid = "UID";
collect.Uid = uid;

string user = "UID";
collect.User = user;

string apiuid = "apiUID";
collect.Apiuid = apiuid;

string data = "https://static.yourcdn.com/data.file";
collect.Data = data;

string contentType = "application/json";
collect.ContentType = contentType;


Models.HttpsApiRestShApiDataResponseModel result = await dataManipulationConversionSortingAndCompressionAPI.GetHttpsApiRestShApiData(collect);

```


### <a name="create_https_api_rest_sh_api_data"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DataManipulationConversionSortingAndCompressionAPIController.CreateHttpsApiRestShApiData") CreateHttpsApiRestShApiData

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiDataResponseModel> CreateHttpsApiRestShApiData(Models.CreateHttpsApiRestShApiDataInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiDataInput collect = new CreateHttpsApiRestShApiDataInput();

string bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<Models.HttpsApiRestShApiDataRequestModel>(bodyValue);
collect.Body = body;

string contentType = "application/json";
collect.ContentType = contentType;


Models.HttpsApiRestShApiDataResponseModel result = await dataManipulationConversionSortingAndCompressionAPI.CreateHttpsApiRestShApiData(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.ImageManipulationAndModerationAPIController") ImageManipulationAndModerationAPIController

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPIController ``` class can be accessed from the API Client.

```csharp
IImageManipulationAndModerationAPIController imageManipulationAndModerationAPI = client.ImageManipulationAndModerationAPI;
```

### <a name="get_https_api_rest_sh_api_image"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.ImageManipulationAndModerationAPIController.GetHttpsApiRestShApiImage") GetHttpsApiRestShApiImage

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```csharp
Task<Models.HttpsApiRestShApiImageResponseModel> GetHttpsApiRestShApiImage(Models.GetHttpsApiRestShApiImageInput input)
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
GetHttpsApiRestShApiImageInput collect = new GetHttpsApiRestShApiImageInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string image = "image";
collect.Image = image;

string transform = "transform";
collect.Transform = transform;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiImageResponseModel result = await imageManipulationAndModerationAPI.GetHttpsApiRestShApiImage(collect);

```


### <a name="create_https_api_rest_sh_api_image"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.ImageManipulationAndModerationAPIController.CreateHttpsApiRestShApiImage") CreateHttpsApiRestShApiImage

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```csharp
Task<Models.HttpsApiRestShApiImageResponseModel> CreateHttpsApiRestShApiImage(Models.CreateHttpsApiRestShApiImageInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiImageInput collect = new CreateHttpsApiRestShApiImageInput();

var body = new Models.HttpsApiRestShApiImageRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiImageResponseModel result = await imageManipulationAndModerationAPI.CreateHttpsApiRestShApiImage(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.VerificationController") VerificationController

### Get singleton instance

The singleton instance of the ``` VerificationController ``` class can be accessed from the API Client.

```csharp
IVerificationController verification = client.Verification;
```

### <a name="get_https_api_rest_sh_api_verify_address"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.VerificationController.GetHttpsApiRestShApiVerifyAddress") GetHttpsApiRestShApiVerifyAddress

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```csharp
Task<Models.HttpsApiRestShApiVerifyAddressResponseModel> GetHttpsApiRestShApiVerifyAddress(Models.GetHttpsApiRestShApiVerifyAddressInput input)
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
GetHttpsApiRestShApiVerifyAddressInput collect = new GetHttpsApiRestShApiVerifyAddressInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string user = "user";
collect.User = user;

string a = "a";
collect.A = a;

string sa = "sa";
collect.Sa = sa;

string c = "c";
collect.C = c;

string s = "s";
collect.S = s;

int z = 23;
collect.Z = z;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiVerifyAddressResponseModel result = await verification.GetHttpsApiRestShApiVerifyAddress(collect);

```


### <a name="create_https_api_rest_sh_api_verify_address"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.VerificationController.CreateHttpsApiRestShApiVerifyAddress") CreateHttpsApiRestShApiVerifyAddress

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```csharp
Task<Models.HttpsApiRestShApiVerifyAddressResponseModel> CreateHttpsApiRestShApiVerifyAddress(Models.CreateHttpsApiRestShApiVerifyAddressInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiVerifyAddressInput collect = new CreateHttpsApiRestShApiVerifyAddressInput();

var body = new Models.HttpsApiRestShApiVerifyAddressRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiVerifyAddressResponseModel result = await verification.CreateHttpsApiRestShApiVerifyAddress(collect);

```


### <a name="get_https_api_rest_sh_api_verify_user"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.VerificationController.GetHttpsApiRestShApiVerifyUser") GetHttpsApiRestShApiVerifyUser

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```csharp
Task<Models.HttpsApiRestShApiVerifyUserResponseModel> GetHttpsApiRestShApiVerifyUser(Models.GetHttpsApiRestShApiVerifyUserInput input)
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
GetHttpsApiRestShApiVerifyUserInput collect = new GetHttpsApiRestShApiVerifyUserInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string user = "user";
collect.User = user;

string code = "code";
collect.Code = code;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiVerifyUserResponseModel result = await verification.GetHttpsApiRestShApiVerifyUser(collect);

```


### <a name="create_https_api_rest_sh_api_verify_user"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.VerificationController.CreateHttpsApiRestShApiVerifyUser") CreateHttpsApiRestShApiVerifyUser

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```csharp
Task<Models.HttpsApiRestShApiVerifyUserResponseModel> CreateHttpsApiRestShApiVerifyUser(Models.CreateHttpsApiRestShApiVerifyUserInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiVerifyUserInput collect = new CreateHttpsApiRestShApiVerifyUserInput();

var body = new Models.HttpsApiRestShApiVerifyUserRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiVerifyUserResponseModel result = await verification.CreateHttpsApiRestShApiVerifyUser(collect);

```


### <a name="get_https_api_rest_sh_api_verify"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.VerificationController.GetHttpsApiRestShApiVerify") GetHttpsApiRestShApiVerify

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```csharp
Task<Models.HttpsApiRestShApiVerifyResponseModel> GetHttpsApiRestShApiVerify(Models.GetHttpsApiRestShApiVerifyInput input)
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
GetHttpsApiRestShApiVerifyInput collect = new GetHttpsApiRestShApiVerifyInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string to = "to";
collect.To = to;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiVerifyResponseModel result = await verification.GetHttpsApiRestShApiVerify(collect);

```


### <a name="create_https_api_rest_sh_api_verify"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.VerificationController.CreateHttpsApiRestShApiVerify") CreateHttpsApiRestShApiVerify

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```csharp
Task<Models.HttpsApiRestShApiVerifyResponseModel> CreateHttpsApiRestShApiVerify(Models.CreateHttpsApiRestShApiVerifyInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiVerifyInput collect = new CreateHttpsApiRestShApiVerifyInput();

var body = new Models.HttpsApiRestShApiVerifyRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiVerifyResponseModel result = await verification.CreateHttpsApiRestShApiVerify(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.TwoFactorAuthenticationAPIController") TwoFactorAuthenticationAPIController

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPIController ``` class can be accessed from the API Client.

```csharp
ITwoFactorAuthenticationAPIController twoFactorAuthenticationAPI = client.TwoFactorAuthenticationAPI;
```

### <a name="get_https_api_rest_sh_api2fa_token"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.TwoFactorAuthenticationAPIController.GetHttpsApiRestShApi2faToken") GetHttpsApiRestShApi2faToken

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```csharp
Task<Models.HttpsApiRestShApi2faTokenResponseModel> GetHttpsApiRestShApi2faToken(Models.GetHttpsApiRestShApi2faTokenInput input)
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
GetHttpsApiRestShApi2faTokenInput collect = new GetHttpsApiRestShApi2faTokenInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string user = "user";
collect.User = user;

string code = "code";
collect.Code = code;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApi2faTokenResponseModel result = await twoFactorAuthenticationAPI.GetHttpsApiRestShApi2faToken(collect);

```


### <a name="create_https_api_rest_sh_api2fa_token"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.TwoFactorAuthenticationAPIController.CreateHttpsApiRestShApi2faToken") CreateHttpsApiRestShApi2faToken

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```csharp
Task<Models.HttpsApiRestShApi2faTokenResponseModel> CreateHttpsApiRestShApi2faToken(Models.CreateHttpsApiRestShApi2faTokenInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApi2faTokenInput collect = new CreateHttpsApiRestShApi2faTokenInput();

var body = new Models.HttpsApiRestShApi2faTokenRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApi2faTokenResponseModel result = await twoFactorAuthenticationAPI.CreateHttpsApiRestShApi2faToken(collect);

```


### <a name="get_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.TwoFactorAuthenticationAPIController.GetHttpsApiRestShApi2fa") GetHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```csharp
Task<Models.HttpsApiRestShApi2faResponseModel> GetHttpsApiRestShApi2fa(Models.GetHttpsApiRestShApi2faInput input)
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
GetHttpsApiRestShApi2faInput collect = new GetHttpsApiRestShApi2faInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string to = "to";
collect.To = to;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApi2faResponseModel result = await twoFactorAuthenticationAPI.GetHttpsApiRestShApi2fa(collect);

```


### <a name="create_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.TwoFactorAuthenticationAPIController.CreateHttpsApiRestShApi2fa") CreateHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```csharp
Task<Models.HttpsApiRestShApi2faResponseModel> CreateHttpsApiRestShApi2fa(Models.CreateHttpsApiRestShApi2faInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApi2faInput collect = new CreateHttpsApiRestShApi2faInput();

var body = new Models.HttpsApiRestShApi2faRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApi2faResponseModel result = await twoFactorAuthenticationAPI.CreateHttpsApiRestShApi2fa(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.UserManagementController") UserManagementController

### Get singleton instance

The singleton instance of the ``` UserManagementController ``` class can be accessed from the API Client.

```csharp
IUserManagementController userManagement = client.UserManagement;
```

### <a name="get_https_api_rest_sh_api_user_info"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagementController.GetHttpsApiRestShApiUserInfo") GetHttpsApiRestShApiUserInfo

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```csharp
Task<Models.HttpsApiRestShApiUserInfoResponseModel> GetHttpsApiRestShApiUserInfo(Models.GetHttpsApiRestShApiUserInfoInput input)
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
GetHttpsApiRestShApiUserInfoInput collect = new GetHttpsApiRestShApiUserInfoInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string user = "user";
collect.User = user;

string apiuid = "apiuid";
collect.Apiuid = apiuid;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiUserInfoResponseModel result = await userManagement.GetHttpsApiRestShApiUserInfo(collect);

```


### <a name="create_https_api_rest_sh_api_user_info"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagementController.CreateHttpsApiRestShApiUserInfo") CreateHttpsApiRestShApiUserInfo

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```csharp
Task<Models.HttpsApiRestShApiUserInfoResponseModel> CreateHttpsApiRestShApiUserInfo(Models.CreateHttpsApiRestShApiUserInfoInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiUserInfoInput collect = new CreateHttpsApiRestShApiUserInfoInput();

var body = new Models.HttpsApiRestShApiUserInfoRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiUserInfoResponseModel result = await userManagement.CreateHttpsApiRestShApiUserInfo(collect);

```


### <a name="get_https_api_rest_sh_api_user_update"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagementController.GetHttpsApiRestShApiUserUpdate") GetHttpsApiRestShApiUserUpdate

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```csharp
Task<Models.HttpsApiRestShApiUserUpdateResponseModel> GetHttpsApiRestShApiUserUpdate(Models.GetHttpsApiRestShApiUserUpdateInput input)
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
GetHttpsApiRestShApiUserUpdateInput collect = new GetHttpsApiRestShApiUserUpdateInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string user = "user";
collect.User = user;

string apiuid = "apiuid";
collect.Apiuid = apiuid;

string avatar = "avatar";
collect.Avatar = avatar;

string customInput = "custom input";
collect.CustomInput = customInput;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiUserUpdateResponseModel result = await userManagement.GetHttpsApiRestShApiUserUpdate(collect);

```


### <a name="create_https_api_rest_sh_api_user_update"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagementController.CreateHttpsApiRestShApiUserUpdate") CreateHttpsApiRestShApiUserUpdate

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```csharp
Task<Models.HttpsApiRestShApiUserUpdateResponseModel> CreateHttpsApiRestShApiUserUpdate(Models.CreateHttpsApiRestShApiUserUpdateInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiUserUpdateInput collect = new CreateHttpsApiRestShApiUserUpdateInput();

var body = new Models.HttpsApiRestShApiUserUpdateRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiUserUpdateResponseModel result = await userManagement.CreateHttpsApiRestShApiUserUpdate(collect);

```


### <a name="get_https_api_rest_sh_api_user_delete"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagementController.GetHttpsApiRestShApiUserDelete") GetHttpsApiRestShApiUserDelete

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```csharp
Task<Models.HttpsApiRestShApiUserDeleteResponseModel> GetHttpsApiRestShApiUserDelete(Models.GetHttpsApiRestShApiUserDeleteInput input)
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
GetHttpsApiRestShApiUserDeleteInput collect = new GetHttpsApiRestShApiUserDeleteInput();

string api = "api";
collect.Api = api;

string uid = "uid";
collect.Uid = uid;

string user = "user";
collect.User = user;

string apiuid = "apiuid";
collect.Apiuid = apiuid;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiUserDeleteResponseModel result = await userManagement.GetHttpsApiRestShApiUserDelete(collect);

```


### <a name="create_https_api_rest_sh_api_user_delete"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagementController.CreateHttpsApiRestShApiUserDelete") CreateHttpsApiRestShApiUserDelete

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```csharp
Task<Models.HttpsApiRestShApiUserDeleteResponseModel> CreateHttpsApiRestShApiUserDelete(Models.CreateHttpsApiRestShApiUserDeleteInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiUserDeleteInput collect = new CreateHttpsApiRestShApiUserDeleteInput();

var body = new Models.HttpsApiRestShApiUserDeleteRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiUserDeleteResponseModel result = await userManagement.CreateHttpsApiRestShApiUserDelete(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.LoginAndRegistrationController") LoginAndRegistrationController

### Get singleton instance

The singleton instance of the ``` LoginAndRegistrationController ``` class can be accessed from the API Client.

```csharp
ILoginAndRegistrationController loginAndRegistration = client.LoginAndRegistration;
```

### <a name="get_https_api_rest_sh_api_auth_user_register"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.LoginAndRegistrationController.GetHttpsApiRestShApiAuthUserRegister") GetHttpsApiRestShApiAuthUserRegister

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```csharp
Task<Models.HttpsApiRestShApiAuthUserRegisterResponseModel> GetHttpsApiRestShApiAuthUserRegister(Models.GetHttpsApiRestShApiAuthUserRegisterInput input)
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
GetHttpsApiRestShApiAuthUserRegisterInput collect = new GetHttpsApiRestShApiAuthUserRegisterInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string user = "user";
collect.User = user;

string password = "password";
collect.Password = password;

string name = "name";
collect.Name = name;

string email = "email";
collect.Email = email;

int phone = 23;
collect.Phone = phone;

int countrycode = 23;
collect.Countrycode = countrycode;

string address = "address";
collect.Address = address;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiAuthUserRegisterResponseModel result = await loginAndRegistration.GetHttpsApiRestShApiAuthUserRegister(collect);

```


### <a name="create_https_api_rest_sh_api_auth_user_register"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.LoginAndRegistrationController.CreateHttpsApiRestShApiAuthUserRegister") CreateHttpsApiRestShApiAuthUserRegister

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```csharp
Task<Models.HttpsApiRestShApiAuthUserRegisterResponseModel> CreateHttpsApiRestShApiAuthUserRegister(Models.CreateHttpsApiRestShApiAuthUserRegisterInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiAuthUserRegisterInput collect = new CreateHttpsApiRestShApiAuthUserRegisterInput();

var body = new Models.HttpsApiRestShApiAuthUserRegisterRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiAuthUserRegisterResponseModel result = await loginAndRegistration.CreateHttpsApiRestShApiAuthUserRegister(collect);

```


### <a name="get_https_api_rest_sh_api_auth_user_login"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.LoginAndRegistrationController.GetHttpsApiRestShApiAuthUserLogin") GetHttpsApiRestShApiAuthUserLogin

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```csharp
Task<Models.HttpsApiRestShApiAuthUserLoginResponseModel> GetHttpsApiRestShApiAuthUserLogin(Models.GetHttpsApiRestShApiAuthUserLoginInput input)
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
GetHttpsApiRestShApiAuthUserLoginInput collect = new GetHttpsApiRestShApiAuthUserLoginInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string user = "user";
collect.User = user;

string password = "password";
collect.Password = password;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiAuthUserLoginResponseModel result = await loginAndRegistration.GetHttpsApiRestShApiAuthUserLogin(collect);

```


### <a name="create_https_api_rest_sh_api_auth_user_login"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.LoginAndRegistrationController.CreateHttpsApiRestShApiAuthUserLogin") CreateHttpsApiRestShApiAuthUserLogin

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```csharp
Task<Models.HttpsApiRestShApiAuthUserLoginResponseModel> CreateHttpsApiRestShApiAuthUserLogin(Models.CreateHttpsApiRestShApiAuthUserLoginInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiAuthUserLoginInput collect = new CreateHttpsApiRestShApiAuthUserLoginInput();

var body = new Models.HttpsApiRestShApiAuthUserLoginRequestModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiAuthUserLoginResponseModel result = await loginAndRegistration.CreateHttpsApiRestShApiAuthUserLogin(collect);

```


[Back to List of Controllers](#list_of_controllers)



