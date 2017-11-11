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
    * WAF and DDOS Protection (Web Application Firewall)
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
| uid | Your user ID |
| secret | Your Private API Key |
| key | Your Public API Key |



API client can be initialized as following.

```csharp
// Configuration parameters and credentials
string uid = "UID"; // Your user ID
string secret = "SECRET"; // Your Private API Key
string key = "KEY"; // Your Public API Key

SMASHClient client = new SMASHClient(uid, secret, key);
```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [AdvancedLogging](#advanced_logging)
* [WAFAndDDOSProtection](#waf_and_ddos_protection)
* [Encryption](#encryption)
* [CDN](#cdn)
* [DNS](#dns)
* [CodeObfuscation](#code_obfuscation)
* [Hosting](#hosting)
* [DataManipulation](#data_manipulation)
* [ImageManipulation](#image_manipulation)
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

### <a name="logging_configuration"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLogging.LoggingConfiguration") LoggingConfiguration

> WAF Log Configuration


```csharp
Task<Models.HttpsApiRestShApiSLR> LoggingConfiguration(string name, string origin, string activate)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| name |  ``` Required ```  | Name of the WAF zone |
| origin |  ``` Required ```  | IP Address of the Web Application you wish to configure logging on |
| activate |  ``` Required ```  | Activate or Disable |


#### Example Usage

```csharp
string name = "name";
string origin = "origin";
string activate = "activate";

Models.HttpsApiRestShApiSLR result = await advancedLogging.LoggingConfiguration(name, origin, activate);

```


### <a name="logging_info"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.AdvancedLogging.LoggingInfo") LoggingInfo

> WAF Log Info


```csharp
Task<Models.HttpsApiRestShApiSLIR> LoggingInfo(string name, string origin, string time = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| name |  ``` Required ```  | Name of your WAF zone |
| origin |  ``` Required ```  | IP Address of the Web Application |
| time |  ``` Optional ```  | Specific times or dates to lookup separated by a comma in MMDDYYHHMMSS Format ( Month Month Day Day Year Year Year Hour Hour Minute Minute Second Second [01/01/0101;24:59:01]) |


#### Example Usage

```csharp
string name = "name";
string origin = "origin";
string time = "time";

Models.HttpsApiRestShApiSLIR result = await advancedLogging.LoggingInfo(name, origin, time);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="waf_and_ddos_protection"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.WAFAndDDOSProtection") WAFAndDDOSProtection

### Get singleton instance

The singleton instance of the ``` WAFAndDDOSProtection ``` class can be accessed from the API Client.

```csharp
IWAFAndDDOSProtection wAFAndDDOSProtection = client.WAFAndDDOSProtection;
```

### <a name="https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFAndDDOSProtection.HttpsApiRestShApiSWC") HttpsApiRestShApiSWC

> WAF and DDOS Configuration


```csharp
Task<Models.HttpsApiRestShApiSWCR> HttpsApiRestShApiSWC(string name, string rule)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| name |  ``` Required ```  | Name of your WAF zone |
| rule |  ``` Required ```  | Rule or rules to add or update separated by a comma |


#### Example Usage

```csharp
string name = "name";
string rule = "rule";

Models.HttpsApiRestShApiSWCR result = await wAFAndDDOSProtection.HttpsApiRestShApiSWC(name, rule);

```


### <a name="https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.WAFAndDDOSProtection.HttpsApiRestShApiSW") HttpsApiRestShApiSW

> WAF and DDOS Creation


```csharp
Task<Models.HttpsApiRestShApiSWR> HttpsApiRestShApiSW(string origin, string cname)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| origin |  ``` Required ```  | IP of the Web server you wish to protect |
| cname |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access |


#### Example Usage

```csharp
string origin = "origin";
string cname = "cname";

Models.HttpsApiRestShApiSWR result = await wAFAndDDOSProtection.HttpsApiRestShApiSW(origin, cname);

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
Task<Models.HttpsApiRestShApiSER> DataAndFileEncryption(string data, string method, int bit)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Required ```  | GIT URL, file URL, direct upload of file, or data as a query string |
| method |  ``` Required ```  | Single or multiple encryption types to apply to data or files separated by a comma (DES, RSA, BLOWFISH, TWOFISH, AES, IDEA, PGP) |
| bit |  ``` Required ```  | Encryption key size (4096) |


#### Example Usage

```csharp
string data = "data";
string method = "method";
int bit = 70;

Models.HttpsApiRestShApiSER result = await encryption.DataAndFileEncryption(data, method, bit);

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
Task<Models.HttpsApiRestShApiSCPushR> CDNPushZone(string cname, string file)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| cname |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access |
| file |  ``` Required ```  | GIT URL, file URL, or direct upload of file |


#### Example Usage

```csharp
string cname = "cname";
string file = "file";

Models.HttpsApiRestShApiSCPushR result = await cDN.CDNPushZone(cname, file);

```


### <a name="cdn_pull_zone"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.CDN.CDNPullZone") CDNPullZone

> CDN Pull Zone API


```csharp
Task<Models.HttpsApiRestShApiSCPullR> CDNPullZone(string origin, string cname)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| origin |  ``` Required ```  | Domain or domain names separated by a comma |
| cname |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access |


#### Example Usage

```csharp
string origin = "origin";
string cname = "cname";

Models.HttpsApiRestShApiSCPullR result = await cDN.CDNPullZone(origin, cname);

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
Task<Models.HttpsApiRestShApiSDCR> DNSConfiguration(string domain, string records)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| domain |  ``` Required ```  | Domain or domain names separated by a comma |
| records |  ``` Required ```  | Records to append to domain separated by a comma (a;www.mydomain.com;127.0.0.0,cname;mydomain.com;otherdomain.com) |


#### Example Usage

```csharp
string domain = "domain";
string records = "records";

Models.HttpsApiRestShApiSDCR result = await dNS.DNSConfiguration(domain, records);

```


### <a name="dns_creation"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DNS.DNSCreation") DNSCreation

> DNS Creation API


```csharp
Task<Models.HttpsApiRestShApiSDAR> DNSCreation(string domain)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| domain |  ``` Required ```  | Domain or domain names separated by a comma |


#### Example Usage

```csharp
string domain = "domain";

Models.HttpsApiRestShApiSDAR result = await dNS.DNSCreation(domain);

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
Task<Models.HttpsApiRestShApiSOR> ObfuscationAndAntiTampering(string app)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| app |  ``` Required ```  | GIT URL or ZIP package containing your APP |


#### Example Usage

```csharp
string app = "app";

Models.HttpsApiRestShApiSOR result = await codeObfuscation.ObfuscationAndAntiTampering(app);

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
Task<Models.HttpsApiRestShApiSHR> HostingSetup(string app, string domain)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| app |  ``` Required ```  | GIT URL or ZIP package containing your APP |
| domain |  ``` Required ```  | Domain or domain names separated by a comma |


#### Example Usage

```csharp
string app = "app";
string domain = "domain";

Models.HttpsApiRestShApiSHR result = await hosting.HostingSetup(app, domain);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.DataManipulation") DataManipulation

### Get singleton instance

The singleton instance of the ``` DataManipulation ``` class can be accessed from the API Client.

```csharp
IDataManipulation dataManipulation = client.DataManipulation;
```

### <a name="https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.DataManipulation.HttpsApiRestShApiD") HttpsApiRestShApiD

> Data Manipulation API


```csharp
Task<Models.HttpsApiRestShApiDR> HttpsApiRestShApiD(string data, string transform)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Required ```  | Data URL, data as a query string, or direct upload |
| transform |  ``` Required ```  | Transformations to perform |


#### Example Usage

```csharp
string data = "data";
string transform = "transform";

Models.HttpsApiRestShApiDR result = await dataManipulation.HttpsApiRestShApiD(data, transform);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation"></a>![Class: ](https://apidocs.io/img/class.png "SMASH.Controllers.ImageManipulation") ImageManipulation

### Get singleton instance

The singleton instance of the ``` ImageManipulation ``` class can be accessed from the API Client.

```csharp
IImageManipulation imageManipulation = client.ImageManipulation;
```

### <a name="image_manipulation"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.ImageManipulation.ImageManipulation") ImageManipulation

> Image Manipulation API


```csharp
Task<Models.HttpsApiRestShApiIR> ImageManipulation(string image, string transform)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| image |  ``` Required ```  | Image URL or direct upload |
| transform |  ``` Required ```  | Transformations to perform |


#### Example Usage

```csharp
string image = "image";
string transform = "transform";

Models.HttpsApiRestShApiIR result = await imageManipulation.ImageManipulation(image, transform);

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
        string user,
        string a,
        string sa,
        string c,
        string s,
        int z,
        string address = null)
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

```csharp
string user = "user";
string a = "a";
string sa = "sa";
string c = "c";
string s = "s";
int z = 70;
string address = "address";

Models.HttpsApiRestShApiVAR result = await verification.UserAddressVerification(user, a, sa, c, s, z, address);

```


### <a name="user_verification_response"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.Verification.UserVerificationResponse") UserVerificationResponse

> Users Verification Response API


```csharp
Task<Models.HttpsApiRestShApiVUR> UserVerificationResponse(string user, string code)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |
| code |  ``` Required ```  | Verification code entered by the user |


#### Example Usage

```csharp
string user = "user";
string code = "code";

Models.HttpsApiRestShApiVUR result = await verification.UserVerificationResponse(user, code);

```


### <a name="user_verification"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.Verification.UserVerification") UserVerification

> User Verification API


```csharp
Task<Models.HttpsApiRestShApiVR> UserVerification(string user)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |


#### Example Usage

```csharp
string user = "user";

Models.HttpsApiRestShApiVR result = await verification.UserVerification(user);

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
Task<Models.HttpsApiRestShApi2faTR> M2FATokenResponse(string user, string code)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username or Email |
| code |  ``` Required ```  | Response From User Containing 2FA Code |


#### Example Usage

```csharp
string user = "user";
string code = "code";

Models.HttpsApiRestShApi2faTR result = await twoFactorAuthenticationAPI.M2FATokenResponse(user, code);

```


### <a name="two_factor_authentication"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.TwoFactorAuthenticationAPI.TwoFactorAuthentication") TwoFactorAuthentication

> Two Factor Authentication API


```csharp
Task<Models.HttpsApiRestShApi2faR> TwoFactorAuthentication(string to)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| to |  ``` Required ```  | Users UID, Username, Email, Or Cellphone number |


#### Example Usage

```csharp
string to = "to";

Models.HttpsApiRestShApi2faR result = await twoFactorAuthenticationAPI.TwoFactorAuthentication(to);

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
Task<Models.HttpsApiRestShApiUIR> GetUserInfo(string user)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users User ID |


#### Example Usage

```csharp
string user = "user";

Models.HttpsApiRestShApiUIR result = await userManagement.GetUserInfo(user);

```


### <a name="update_user"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagement.UpdateUser") UpdateUser

> Update User API


```csharp
Task<Models.HttpsApiRestShApiUUR> UpdateUser(
        string user,
        string avatar,
        string customInput,
        Dictionary<string, object> queryParameters = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |
| avatar |  ``` Required ```  | Avatar Image URL |
| customInput |  ``` Required ```  | Custom input variable for users profile |
| queryParameters | ``` Optional ``` | Additional optional query parameters are supported by this method |


#### Example Usage

```csharp
string user = "user";
string avatar = "avatar";
string customInput = "custom input";
// key-value map for optional query parameters
var queryParams = new Dictionary<string, object>();


Models.HttpsApiRestShApiUUR result = await userManagement.UpdateUser(user, avatar, customInput, queryParams);

```


### <a name="delete_user"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.UserManagement.DeleteUser") DeleteUser

> Delete User API


```csharp
Task<Models.HttpsApiRestShApiUDR> DeleteUser(string user)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, or Email |


#### Example Usage

```csharp
string user = "user";

Models.HttpsApiRestShApiUDR result = await userManagement.DeleteUser(user);

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
        string email,
        string user,
        string password,
        string name = null,
        int? phone = null,
        int? countrycode = null,
        string address = null,
        Dictionary<string, object> queryParameters = null)
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
| queryParameters | ``` Optional ``` | Additional optional query parameters are supported by this method |


#### Example Usage

```csharp
string email = "email";
string user = "user";
string password = "password";
string name = "name";
int? phone = 28;
int? countrycode = 28;
string address = "address";
// key-value map for optional query parameters
var queryParams = new Dictionary<string, object>();


Models.HttpsApiRestShApiAURR result = await loginAndRegistration.UserRegistration(email, user, password, name, phone, countrycode, address, queryParams);

```


### <a name="user_authentication"></a>![Method: ](https://apidocs.io/img/method.png "SMASH.Controllers.LoginAndRegistration.UserAuthentication") UserAuthentication

> User Authentication API


```csharp
Task<Models.HttpsApiRestShApiAULR> UserAuthentication(string user, string password)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users Username or Email |
| password |  ``` Required ```  | Users Password |


#### Example Usage

```csharp
string user = "user";
string password = "password";

Models.HttpsApiRestShApiAULR result = await loginAndRegistration.UserAuthentication(user, password);

```


[Back to List of Controllers](#list_of_controllers)



