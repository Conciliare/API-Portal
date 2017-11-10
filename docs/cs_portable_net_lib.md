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

### <a name="get_https_api_rest_sh_api_sli"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLoggingController.GetHttpsApiRestShApiSLI") GetHttpsApiRestShApiSLI

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```csharp
Task<Models.HttpsApiRestShApiSLIRModel> GetHttpsApiRestShApiSLI(Models.GetHttpsApiRestShApiSLIInput input)
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
GetHttpsApiRestShApiSLIInput collect = new GetHttpsApiRestShApiSLIInput();

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


Models.HttpsApiRestShApiSLIRModel result = await advancedLogging.GetHttpsApiRestShApiSLI(collect);

```


### <a name="get_https_api_rest_sh_api_sl"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLoggingController.GetHttpsApiRestShApiSL") GetHttpsApiRestShApiSL

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```csharp
Task<Models.HttpsApiRestShApiSLRModel> GetHttpsApiRestShApiSL(Models.GetHttpsApiRestShApiSLInput input)
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
GetHttpsApiRestShApiSLInput collect = new GetHttpsApiRestShApiSLInput();

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


Models.HttpsApiRestShApiSLRModel result = await advancedLogging.GetHttpsApiRestShApiSL(collect);

```


### <a name="create_https_api_rest_sh_api_sli"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLoggingController.CreateHttpsApiRestShApiSLI") CreateHttpsApiRestShApiSLI

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```csharp
Task<Models.HttpsApiRestShApiSLIRModel> CreateHttpsApiRestShApiSLI(Models.CreateHttpsApiRestShApiSLIInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSLIInput collect = new CreateHttpsApiRestShApiSLIInput();

var body = new Models.HttpsApiRestShApiSLIModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSLIRModel result = await advancedLogging.CreateHttpsApiRestShApiSLI(collect);

```


### <a name="create_https_api_rest_sh_api_sl"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLoggingController.CreateHttpsApiRestShApiSL") CreateHttpsApiRestShApiSL

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```csharp
Task<Models.HttpsApiRestShApiSLRModel> CreateHttpsApiRestShApiSL(Models.CreateHttpsApiRestShApiSLInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSLInput collect = new CreateHttpsApiRestShApiSLInput();

var body = new Models.HttpsApiRestShApiSLModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSLRModel result = await advancedLogging.CreateHttpsApiRestShApiSL(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.WAFDDOSProtectionController") WAFDDOSProtectionController

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtectionController ``` class can be accessed from the API Client.

```csharp
IWAFDDOSProtectionController wAFDDOSProtection = client.WAFDDOSProtection;
```

### <a name="get_https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFDDOSProtectionController.GetHttpsApiRestShApiSWC") GetHttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiSWCRModel> GetHttpsApiRestShApiSWC(Models.GetHttpsApiRestShApiSWCInput input)
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
GetHttpsApiRestShApiSWCInput collect = new GetHttpsApiRestShApiSWCInput();

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


Models.HttpsApiRestShApiSWCRModel result = await wAFDDOSProtection.GetHttpsApiRestShApiSWC(collect);

```


### <a name="get_https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFDDOSProtectionController.GetHttpsApiRestShApiSW") GetHttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiSWRModel> GetHttpsApiRestShApiSW(Models.GetHttpsApiRestShApiSWInput input)
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
GetHttpsApiRestShApiSWInput collect = new GetHttpsApiRestShApiSWInput();

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


Models.HttpsApiRestShApiSWRModel result = await wAFDDOSProtection.GetHttpsApiRestShApiSW(collect);

```


### <a name="create_https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFDDOSProtectionController.CreateHttpsApiRestShApiSWC") CreateHttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiSWCRModel> CreateHttpsApiRestShApiSWC(Models.CreateHttpsApiRestShApiSWCInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSWCInput collect = new CreateHttpsApiRestShApiSWCInput();

string bodyValue = "{\n  \"key\": \"YOUR API KEY\",\n  \"uid\": \"YOUR USER ID\",\n  \"name\": \"WHAT YOU WISH TO NAME YOUR WAF\",\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\n}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<Models.HttpsApiRestShApiSWCModel>(bodyValue);
collect.Body = body;

string contentType = "application/json";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSWCRModel result = await wAFDDOSProtection.CreateHttpsApiRestShApiSWC(collect);

```


### <a name="create_https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFDDOSProtectionController.CreateHttpsApiRestShApiSW") CreateHttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiSWRModel> CreateHttpsApiRestShApiSW(Models.CreateHttpsApiRestShApiSWInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSWInput collect = new CreateHttpsApiRestShApiSWInput();

string bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"origin\": \"ORIGIN YOU WISH TO PROTECT\",\r\n  \"cname\": \"CNAMES YOU WISH TO USE WITH YOUR WAF\"\r\n}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<Models.HttpsApiRestShApiSWModel>(bodyValue);
collect.Body = body;

string contentType = "application/json";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSWRModel result = await wAFDDOSProtection.CreateHttpsApiRestShApiSW(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="encryption_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.EncryptionController") EncryptionController

### Get singleton instance

The singleton instance of the ``` EncryptionController ``` class can be accessed from the API Client.

```csharp
IEncryptionController encryption = client.Encryption;
```

### <a name="get_https_api_rest_sh_api_se"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.EncryptionController.GetHttpsApiRestShApiSE") GetHttpsApiRestShApiSE

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```csharp
Task<Models.HttpsApiRestShApiSERModel> GetHttpsApiRestShApiSE(Models.GetHttpsApiRestShApiSEInput input)
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
GetHttpsApiRestShApiSEInput collect = new GetHttpsApiRestShApiSEInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string data = "data";
collect.Data = data;

string method = "method";
collect.Method = method;

int bit = 112;
collect.Bit = bit;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSERModel result = await encryption.GetHttpsApiRestShApiSE(collect);

```


### <a name="create_https_api_rest_sh_api_se"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.EncryptionController.CreateHttpsApiRestShApiSE") CreateHttpsApiRestShApiSE

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```csharp
Task<Models.HttpsApiRestShApiSERModel> CreateHttpsApiRestShApiSE(Models.CreateHttpsApiRestShApiSEInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSEInput collect = new CreateHttpsApiRestShApiSEInput();

var body = new Models.HttpsApiRestShApiSEModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSERModel result = await encryption.CreateHttpsApiRestShApiSE(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cdn_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.CDNController") CDNController

### Get singleton instance

The singleton instance of the ``` CDNController ``` class can be accessed from the API Client.

```csharp
ICDNController cDN = client.CDN;
```

### <a name="get_https_api_rest_sh_api_sc_push"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CDNController.GetHttpsApiRestShApiSCPush") GetHttpsApiRestShApiSCPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```csharp
Task<Models.HttpsApiRestShApiSCPushRModel> GetHttpsApiRestShApiSCPush(Models.GetHttpsApiRestShApiSCPushInput input)
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
GetHttpsApiRestShApiSCPushInput collect = new GetHttpsApiRestShApiSCPushInput();

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


Models.HttpsApiRestShApiSCPushRModel result = await cDN.GetHttpsApiRestShApiSCPush(collect);

```


### <a name="get_https_api_rest_sh_api_sc_pull"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CDNController.GetHttpsApiRestShApiSCPull") GetHttpsApiRestShApiSCPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```csharp
Task<Models.HttpsApiRestShApiSCPullRModel> GetHttpsApiRestShApiSCPull(Models.GetHttpsApiRestShApiSCPullInput input)
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
GetHttpsApiRestShApiSCPullInput collect = new GetHttpsApiRestShApiSCPullInput();

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


Models.HttpsApiRestShApiSCPullRModel result = await cDN.GetHttpsApiRestShApiSCPull(collect);

```


### <a name="create_https_api_rest_sh_api_sc_push"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CDNController.CreateHttpsApiRestShApiSCPush") CreateHttpsApiRestShApiSCPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```csharp
Task<Models.HttpsApiRestShApiSCPushRModel> CreateHttpsApiRestShApiSCPush(Models.CreateHttpsApiRestShApiSCPushInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSCPushInput collect = new CreateHttpsApiRestShApiSCPushInput();

var body = new Models.HttpsApiRestShApiSCPushModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSCPushRModel result = await cDN.CreateHttpsApiRestShApiSCPush(collect);

```


### <a name="create_https_api_rest_sh_api_sc_pull"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CDNController.CreateHttpsApiRestShApiSCPull") CreateHttpsApiRestShApiSCPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```csharp
Task<Models.HttpsApiRestShApiSCPullRModel> CreateHttpsApiRestShApiSCPull(Models.CreateHttpsApiRestShApiSCPullInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSCPullInput collect = new CreateHttpsApiRestShApiSCPullInput();

var body = new Models.HttpsApiRestShApiSCPullModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSCPullRModel result = await cDN.CreateHttpsApiRestShApiSCPull(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="dns_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.DNSController") DNSController

### Get singleton instance

The singleton instance of the ``` DNSController ``` class can be accessed from the API Client.

```csharp
IDNSController dNS = client.DNS;
```

### <a name="get_https_api_rest_sh_api_sdc"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DNSController.GetHttpsApiRestShApiSDC") GetHttpsApiRestShApiSDC

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```csharp
Task<Models.HttpsApiRestShApiSDCRModel> GetHttpsApiRestShApiSDC(Models.GetHttpsApiRestShApiSDCInput input)
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
GetHttpsApiRestShApiSDCInput collect = new GetHttpsApiRestShApiSDCInput();

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


Models.HttpsApiRestShApiSDCRModel result = await dNS.GetHttpsApiRestShApiSDC(collect);

```


### <a name="create_https_api_rest_sh_api_sdc"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DNSController.CreateHttpsApiRestShApiSDC") CreateHttpsApiRestShApiSDC

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```csharp
Task<Models.HttpsApiRestShApiSDCRModel> CreateHttpsApiRestShApiSDC(Models.CreateHttpsApiRestShApiSDCInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSDCInput collect = new CreateHttpsApiRestShApiSDCInput();

var body = new Models.HttpsApiRestShApiSDCModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSDCRModel result = await dNS.CreateHttpsApiRestShApiSDC(collect);

```


### <a name="get_https_api_rest_sh_api_sda"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DNSController.GetHttpsApiRestShApiSDA") GetHttpsApiRestShApiSDA

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```csharp
Task<Models.HttpsApiRestShApiSDARModel> GetHttpsApiRestShApiSDA(Models.GetHttpsApiRestShApiSDAInput input)
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
GetHttpsApiRestShApiSDAInput collect = new GetHttpsApiRestShApiSDAInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string domain = "domain";
collect.Domain = domain;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSDARModel result = await dNS.GetHttpsApiRestShApiSDA(collect);

```


### <a name="create_https_api_rest_sh_api_sda"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DNSController.CreateHttpsApiRestShApiSDA") CreateHttpsApiRestShApiSDA

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```csharp
Task<Models.HttpsApiRestShApiSDARModel> CreateHttpsApiRestShApiSDA(Models.CreateHttpsApiRestShApiSDAInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSDAInput collect = new CreateHttpsApiRestShApiSDAInput();

var body = new Models.HttpsApiRestShApiSDAModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSDARModel result = await dNS.CreateHttpsApiRestShApiSDA(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.CodeObfuscationController") CodeObfuscationController

### Get singleton instance

The singleton instance of the ``` CodeObfuscationController ``` class can be accessed from the API Client.

```csharp
ICodeObfuscationController codeObfuscation = client.CodeObfuscation;
```

### <a name="get_https_api_rest_sh_api_so"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CodeObfuscationController.GetHttpsApiRestShApiSO") GetHttpsApiRestShApiSO

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```csharp
Task<Models.HttpsApiRestShApiSORModel> GetHttpsApiRestShApiSO(Models.GetHttpsApiRestShApiSOInput input)
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
GetHttpsApiRestShApiSOInput collect = new GetHttpsApiRestShApiSOInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string app = "app";
collect.App = app;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSORModel result = await codeObfuscation.GetHttpsApiRestShApiSO(collect);

```


### <a name="create_https_api_rest_sh_api_so"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CodeObfuscationController.CreateHttpsApiRestShApiSO") CreateHttpsApiRestShApiSO

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```csharp
Task<Models.HttpsApiRestShApiSORModel> CreateHttpsApiRestShApiSO(Models.CreateHttpsApiRestShApiSOInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSOInput collect = new CreateHttpsApiRestShApiSOInput();

var body = new Models.HttpsApiRestShApiSOModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSORModel result = await codeObfuscation.CreateHttpsApiRestShApiSO(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="hosting_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.HostingController") HostingController

### Get singleton instance

The singleton instance of the ``` HostingController ``` class can be accessed from the API Client.

```csharp
IHostingController hosting = client.Hosting;
```

### <a name="get_https_api_rest_sh_api_sh"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.HostingController.GetHttpsApiRestShApiSH") GetHttpsApiRestShApiSH

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```csharp
Task<Models.HttpsApiRestShApiSHRModel> GetHttpsApiRestShApiSH(Models.GetHttpsApiRestShApiSHInput input)
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
GetHttpsApiRestShApiSHInput collect = new GetHttpsApiRestShApiSHInput();

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


Models.HttpsApiRestShApiSHRModel result = await hosting.GetHttpsApiRestShApiSH(collect);

```


### <a name="create_https_api_rest_sh_api_sh"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.HostingController.CreateHttpsApiRestShApiSH") CreateHttpsApiRestShApiSH

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```csharp
Task<Models.HttpsApiRestShApiSHRModel> CreateHttpsApiRestShApiSH(Models.CreateHttpsApiRestShApiSHInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiSHInput collect = new CreateHttpsApiRestShApiSHInput();

var body = new Models.HttpsApiRestShApiSHModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiSHRModel result = await hosting.CreateHttpsApiRestShApiSH(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.DataManipulationConversionSortingAndCompressionAPIController") DataManipulationConversionSortingAndCompressionAPIController

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPIController ``` class can be accessed from the API Client.

```csharp
IDataManipulationConversionSortingAndCompressionAPIController dataManipulationConversionSortingAndCompressionAPI = client.DataManipulationConversionSortingAndCompressionAPI;
```

### <a name="get_https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DataManipulationConversionSortingAndCompressionAPIController.GetHttpsApiRestShApiD") GetHttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiDRModel> GetHttpsApiRestShApiD(Models.GetHttpsApiRestShApiDInput input)
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
GetHttpsApiRestShApiDInput collect = new GetHttpsApiRestShApiDInput();

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


Models.HttpsApiRestShApiDRModel result = await dataManipulationConversionSortingAndCompressionAPI.GetHttpsApiRestShApiD(collect);

```


### <a name="create_https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DataManipulationConversionSortingAndCompressionAPIController.CreateHttpsApiRestShApiD") CreateHttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```csharp
Task<Models.HttpsApiRestShApiDRModel> CreateHttpsApiRestShApiD(Models.CreateHttpsApiRestShApiDInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiDInput collect = new CreateHttpsApiRestShApiDInput();

string bodyValue = "{\r\n  \"key\": \"YOUR API KEY\",\r\n  \"uid\": \"YOUR USER ID\",\r\n  \"user\": \"USERS EMAIL OR USERNAME\",\r\n  \"apiuid\": \"USERS API SIDE USER ID\",\r\n  \"url\": \"DATA URL OR DIRECT FILE UPLOAD FROM CLIENT\",\r\n  \"manipulation\": \"DATA MANIPULATION DIRECTIVES\",\r\n  \"conversion\": \"CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)\",\r\n  \"sorting\": \"SORT BY (NAME, DATE, TYPE, SIZE)\",\r\n  \"compression\": \"COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)\"\r\n}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<Models.HttpsApiRestShApiDModel>(bodyValue);
collect.Body = body;

string contentType = "application/json";
collect.ContentType = contentType;


Models.HttpsApiRestShApiDRModel result = await dataManipulationConversionSortingAndCompressionAPI.CreateHttpsApiRestShApiD(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.ImageManipulationAndModerationAPIController") ImageManipulationAndModerationAPIController

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPIController ``` class can be accessed from the API Client.

```csharp
IImageManipulationAndModerationAPIController imageManipulationAndModerationAPI = client.ImageManipulationAndModerationAPI;
```

### <a name="get_https_api_rest_sh_api_i"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.ImageManipulationAndModerationAPIController.GetHttpsApiRestShApiI") GetHttpsApiRestShApiI

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```csharp
Task<Models.HttpsApiRestShApiIRModel> GetHttpsApiRestShApiI(Models.GetHttpsApiRestShApiIInput input)
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
GetHttpsApiRestShApiIInput collect = new GetHttpsApiRestShApiIInput();

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


Models.HttpsApiRestShApiIRModel result = await imageManipulationAndModerationAPI.GetHttpsApiRestShApiI(collect);

```


### <a name="create_https_api_rest_sh_api_i"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.ImageManipulationAndModerationAPIController.CreateHttpsApiRestShApiI") CreateHttpsApiRestShApiI

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```csharp
Task<Models.HttpsApiRestShApiIRModel> CreateHttpsApiRestShApiI(Models.CreateHttpsApiRestShApiIInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiIInput collect = new CreateHttpsApiRestShApiIInput();

var body = new Models.HttpsApiRestShApiIModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiIRModel result = await imageManipulationAndModerationAPI.CreateHttpsApiRestShApiI(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="verification_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.VerificationController") VerificationController

### Get singleton instance

The singleton instance of the ``` VerificationController ``` class can be accessed from the API Client.

```csharp
IVerificationController verification = client.Verification;
```

### <a name="get_https_api_rest_sh_api_va"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.VerificationController.GetHttpsApiRestShApiVA") GetHttpsApiRestShApiVA

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```csharp
Task<Models.HttpsApiRestShApiVARModel> GetHttpsApiRestShApiVA(Models.GetHttpsApiRestShApiVAInput input)
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
GetHttpsApiRestShApiVAInput collect = new GetHttpsApiRestShApiVAInput();

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

int z = 70;
collect.Z = z;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiVARModel result = await verification.GetHttpsApiRestShApiVA(collect);

```


### <a name="create_https_api_rest_sh_api_va"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.VerificationController.CreateHttpsApiRestShApiVA") CreateHttpsApiRestShApiVA

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```csharp
Task<Models.HttpsApiRestShApiVARModel> CreateHttpsApiRestShApiVA(Models.CreateHttpsApiRestShApiVAInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiVAInput collect = new CreateHttpsApiRestShApiVAInput();

var body = new Models.HttpsApiRestShApiVAModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiVARModel result = await verification.CreateHttpsApiRestShApiVA(collect);

```


### <a name="get_https_api_rest_sh_api_vu"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.VerificationController.GetHttpsApiRestShApiVU") GetHttpsApiRestShApiVU

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```csharp
Task<Models.HttpsApiRestShApiVURModel> GetHttpsApiRestShApiVU(Models.GetHttpsApiRestShApiVUInput input)
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
GetHttpsApiRestShApiVUInput collect = new GetHttpsApiRestShApiVUInput();

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


Models.HttpsApiRestShApiVURModel result = await verification.GetHttpsApiRestShApiVU(collect);

```


### <a name="create_https_api_rest_sh_api_vu"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.VerificationController.CreateHttpsApiRestShApiVU") CreateHttpsApiRestShApiVU

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```csharp
Task<Models.HttpsApiRestShApiVURModel> CreateHttpsApiRestShApiVU(Models.CreateHttpsApiRestShApiVUInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiVUInput collect = new CreateHttpsApiRestShApiVUInput();

var body = new Models.HttpsApiRestShApiVUModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiVURModel result = await verification.CreateHttpsApiRestShApiVU(collect);

```


### <a name="get_https_api_rest_sh_api_v"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.VerificationController.GetHttpsApiRestShApiV") GetHttpsApiRestShApiV

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```csharp
Task<Models.HttpsApiRestShApiVRModel> GetHttpsApiRestShApiV(Models.GetHttpsApiRestShApiVInput input)
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
GetHttpsApiRestShApiVInput collect = new GetHttpsApiRestShApiVInput();

string key = "key";
collect.Key = key;

string uid = "uid";
collect.Uid = uid;

string to = "to";
collect.To = to;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiVRModel result = await verification.GetHttpsApiRestShApiV(collect);

```


### <a name="create_https_api_rest_sh_api_v"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.VerificationController.CreateHttpsApiRestShApiV") CreateHttpsApiRestShApiV

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```csharp
Task<Models.HttpsApiRestShApiVRModel> CreateHttpsApiRestShApiV(Models.CreateHttpsApiRestShApiVInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiVInput collect = new CreateHttpsApiRestShApiVInput();

var body = new Models.HttpsApiRestShApiVModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiVRModel result = await verification.CreateHttpsApiRestShApiV(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.TwoFactorAuthenticationAPIController") TwoFactorAuthenticationAPIController

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPIController ``` class can be accessed from the API Client.

```csharp
ITwoFactorAuthenticationAPIController twoFactorAuthenticationAPI = client.TwoFactorAuthenticationAPI;
```

### <a name="get_https_api_rest_sh_api2fa_t"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.TwoFactorAuthenticationAPIController.GetHttpsApiRestShApi2faT") GetHttpsApiRestShApi2faT

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```csharp
Task<Models.HttpsApiRestShApi2faTRModel> GetHttpsApiRestShApi2faT(Models.GetHttpsApiRestShApi2faTInput input)
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
GetHttpsApiRestShApi2faTInput collect = new GetHttpsApiRestShApi2faTInput();

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


Models.HttpsApiRestShApi2faTRModel result = await twoFactorAuthenticationAPI.GetHttpsApiRestShApi2faT(collect);

```


### <a name="create_https_api_rest_sh_api2fa_t"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.TwoFactorAuthenticationAPIController.CreateHttpsApiRestShApi2faT") CreateHttpsApiRestShApi2faT

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```csharp
Task<Models.HttpsApiRestShApi2faTRModel> CreateHttpsApiRestShApi2faT(Models.CreateHttpsApiRestShApi2faTInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApi2faTInput collect = new CreateHttpsApiRestShApi2faTInput();

var body = new Models.HttpsApiRestShApi2faTModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApi2faTRModel result = await twoFactorAuthenticationAPI.CreateHttpsApiRestShApi2faT(collect);

```


### <a name="get_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.TwoFactorAuthenticationAPIController.GetHttpsApiRestShApi2fa") GetHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```csharp
Task<Models.HttpsApiRestShApi2faRModel> GetHttpsApiRestShApi2fa(Models.GetHttpsApiRestShApi2faInput input)
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


Models.HttpsApiRestShApi2faRModel result = await twoFactorAuthenticationAPI.GetHttpsApiRestShApi2fa(collect);

```


### <a name="create_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.TwoFactorAuthenticationAPIController.CreateHttpsApiRestShApi2fa") CreateHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```csharp
Task<Models.HttpsApiRestShApi2faRModel> CreateHttpsApiRestShApi2fa(Models.CreateHttpsApiRestShApi2faInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApi2faInput collect = new CreateHttpsApiRestShApi2faInput();

var body = new Models.HttpsApiRestShApi2faModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApi2faRModel result = await twoFactorAuthenticationAPI.CreateHttpsApiRestShApi2fa(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_management_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.UserManagementController") UserManagementController

### Get singleton instance

The singleton instance of the ``` UserManagementController ``` class can be accessed from the API Client.

```csharp
IUserManagementController userManagement = client.UserManagement;
```

### <a name="get_https_api_rest_sh_api_ui"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagementController.GetHttpsApiRestShApiUI") GetHttpsApiRestShApiUI

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```csharp
Task<Models.HttpsApiRestShApiUIRModel> GetHttpsApiRestShApiUI(Models.GetHttpsApiRestShApiUIInput input)
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
GetHttpsApiRestShApiUIInput collect = new GetHttpsApiRestShApiUIInput();

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


Models.HttpsApiRestShApiUIRModel result = await userManagement.GetHttpsApiRestShApiUI(collect);

```


### <a name="create_https_api_rest_sh_api_ui"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagementController.CreateHttpsApiRestShApiUI") CreateHttpsApiRestShApiUI

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```csharp
Task<Models.HttpsApiRestShApiUIRModel> CreateHttpsApiRestShApiUI(Models.CreateHttpsApiRestShApiUIInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiUIInput collect = new CreateHttpsApiRestShApiUIInput();

var body = new Models.HttpsApiRestShApiUIModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiUIRModel result = await userManagement.CreateHttpsApiRestShApiUI(collect);

```


### <a name="get_https_api_rest_sh_api_uu"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagementController.GetHttpsApiRestShApiUU") GetHttpsApiRestShApiUU

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```csharp
Task<Models.HttpsApiRestShApiUURModel> GetHttpsApiRestShApiUU(Models.GetHttpsApiRestShApiUUInput input)
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
GetHttpsApiRestShApiUUInput collect = new GetHttpsApiRestShApiUUInput();

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


Models.HttpsApiRestShApiUURModel result = await userManagement.GetHttpsApiRestShApiUU(collect);

```


### <a name="create_https_api_rest_sh_api_uu"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagementController.CreateHttpsApiRestShApiUU") CreateHttpsApiRestShApiUU

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```csharp
Task<Models.HttpsApiRestShApiUURModel> CreateHttpsApiRestShApiUU(Models.CreateHttpsApiRestShApiUUInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiUUInput collect = new CreateHttpsApiRestShApiUUInput();

var body = new Models.HttpsApiRestShApiUUModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiUURModel result = await userManagement.CreateHttpsApiRestShApiUU(collect);

```


### <a name="get_https_api_rest_sh_api_ud"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagementController.GetHttpsApiRestShApiUD") GetHttpsApiRestShApiUD

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```csharp
Task<Models.HttpsApiRestShApiUDRModel> GetHttpsApiRestShApiUD(Models.GetHttpsApiRestShApiUDInput input)
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
GetHttpsApiRestShApiUDInput collect = new GetHttpsApiRestShApiUDInput();

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


Models.HttpsApiRestShApiUDRModel result = await userManagement.GetHttpsApiRestShApiUD(collect);

```


### <a name="create_https_api_rest_sh_api_ud"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagementController.CreateHttpsApiRestShApiUD") CreateHttpsApiRestShApiUD

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```csharp
Task<Models.HttpsApiRestShApiUDRModel> CreateHttpsApiRestShApiUD(Models.CreateHttpsApiRestShApiUDInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiUDInput collect = new CreateHttpsApiRestShApiUDInput();

var body = new Models.HttpsApiRestShApiUDModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiUDRModel result = await userManagement.CreateHttpsApiRestShApiUD(collect);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration_controller"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.LoginAndRegistrationController") LoginAndRegistrationController

### Get singleton instance

The singleton instance of the ``` LoginAndRegistrationController ``` class can be accessed from the API Client.

```csharp
ILoginAndRegistrationController loginAndRegistration = client.LoginAndRegistration;
```

### <a name="get_https_api_rest_sh_api_aur"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.LoginAndRegistrationController.GetHttpsApiRestShApiAUR") GetHttpsApiRestShApiAUR

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```csharp
Task<Models.HttpsApiRestShApiAURRModel> GetHttpsApiRestShApiAUR(Models.GetHttpsApiRestShApiAURInput input)
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
GetHttpsApiRestShApiAURInput collect = new GetHttpsApiRestShApiAURInput();

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

int phone = 70;
collect.Phone = phone;

int countrycode = 70;
collect.Countrycode = countrycode;

string address = "address";
collect.Address = address;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiAURRModel result = await loginAndRegistration.GetHttpsApiRestShApiAUR(collect);

```


### <a name="create_https_api_rest_sh_api_aur"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.LoginAndRegistrationController.CreateHttpsApiRestShApiAUR") CreateHttpsApiRestShApiAUR

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```csharp
Task<Models.HttpsApiRestShApiAURRModel> CreateHttpsApiRestShApiAUR(Models.CreateHttpsApiRestShApiAURInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiAURInput collect = new CreateHttpsApiRestShApiAURInput();

var body = new Models.HttpsApiRestShApiAURModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiAURRModel result = await loginAndRegistration.CreateHttpsApiRestShApiAUR(collect);

```


### <a name="get_https_api_rest_sh_api_aul"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.LoginAndRegistrationController.GetHttpsApiRestShApiAUL") GetHttpsApiRestShApiAUL

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```csharp
Task<Models.HttpsApiRestShApiAULRModel> GetHttpsApiRestShApiAUL(Models.GetHttpsApiRestShApiAULInput input)
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
GetHttpsApiRestShApiAULInput collect = new GetHttpsApiRestShApiAULInput();

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


Models.HttpsApiRestShApiAULRModel result = await loginAndRegistration.GetHttpsApiRestShApiAUL(collect);

```


### <a name="create_https_api_rest_sh_api_aul"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.LoginAndRegistrationController.CreateHttpsApiRestShApiAUL") CreateHttpsApiRestShApiAUL

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```csharp
Task<Models.HttpsApiRestShApiAULRModel> CreateHttpsApiRestShApiAUL(Models.CreateHttpsApiRestShApiAULInput input)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
CreateHttpsApiRestShApiAULInput collect = new CreateHttpsApiRestShApiAULInput();

var body = new Models.HttpsApiRestShApiAULModel();
collect.Body = body;

string contentType = "Content-Type";
collect.ContentType = contentType;


Models.HttpsApiRestShApiAULRModel result = await loginAndRegistration.CreateHttpsApiRestShApiAUL(collect);

```


[Back to List of Controllers](#list_of_controllers)



