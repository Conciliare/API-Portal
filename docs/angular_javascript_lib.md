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

The generated SDK requires AngularJS framework to work. If you do not already have angular downloaded, please go ahead and do it from [here](https://angularjs.org/).
If any of your models have `Date` or `Datetime` type fields or your endpoints have `Date`/`Datetime` type response, you will need to download and link [angular-moment](https://cdnjs.cloudflare.com/ajax/libs/angular-moment/1.0.1/angular-moment.min.js) and [moment.js](https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.17.1/moment.min.js) with your project.

## How to Use

The following section describes how to use the generated SDK in an existing/new project.

### 1. Configure Angular and Generated SDK
Perform the following steps to configure angular and the SDK:
+ Make a `scripts` folder inside the root folder of the project. If you already have a `scripts` folder, skip to the next step.
+ Move the `angular.min.js` file inside the scripts folder. 
+ Move the `SMASH` folder inside the scripts folder.
+ If any of the Custom Types in your API have `Date`/`Datetime` type fields or any endpoint has `Date`/`Datetime` response, you will need to download angular-moment and moment.js. Move these 2 files into the `scripts` folder as well.

![folder-structure-image](https://apidocs.io/illustration/angularjs?step=folderStructure&workspaceFolder=SMASH-Angular&projectName=SMASH)

### 2. Open Project Folder
Open an IDE/Text Editor for JavaScript like Sublime Text. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.  
Click on `File` and select `Open Folder`

Select the folder of your SDK and click on `Select Folder` to open it up in Sublime Text. The folder will become visible in the bar on the left.

![open-folder-image](https://apidocs.io/illustration/angularjs?step=openFolder&workspaceFolder=SMASH-Angular)

### 3. Create an Angular Application
Since Angular JS is used for client-side web development, in order to use the generated library, you will have to develop an application first.
If you already have an angular application, [skip to Step 6](#6-include-sdk-references-in-html-file). Otherwise, follow these steps to create one:

+ In the IDE, click on `File` and choose `New File` to create a new file.
+ Add the following starting code in the file:
```js
var app = angular.module('myApp', []);
app.controller('testController', function($scope) 
{

});
```
+ Save it with the name `app.js` in the `scripts` folder.


### 4. Create HTML File
Skip to the next step if you are working with an existing project and already have an html file. Otherwise follow the steps to create one:
+ Inside the IDE, right click on the project folder name and select the `New File` option to create a new test file.
+ Save it with an appropriate name such as `index.html` in the root of your project folder.
`index.html` should look like this:
```html
<!DOCTYPE html>
<html>
<head>
	<title>Angular Project</title>
	<script></script>
</head>

<body>
</body>

</html>
```

![initial-html-code-image](https://apidocs.io/illustration/angularjs?step=initialCode&workspaceFolder=SMASH-Angular)

### 5. Including links to Angular in HTML file
Your HTML file needs to have a link to `angular.min.js` file to use Angular-JS. Add the link using `script` tags inside the `head` section of `index.html` like:
```html
<script src="scripts/angular.min.js" ></script>
```
If any of the Custom Types that you have defined have `Date`/`Datetime` type fields or any endpoint has `Date`/`Datetime` response, you will also need to link to angular-moment and moment.js like:
```html
<script src="scripts/angular.min.js" ></script>
<script src="scripts/moment.min.js" ></script>
<script src="scripts/angular-moment.min.js" ></script>
```

### 6. Include SDK references in HTML file
Import the reference to the generated SDK files inside your html file like:
```html
<head>
    ...
    <!-- Helper files -->
    <script src="scripts/SMASH/Module.js"></script>
    <script src="scripts/SMASH/Configuration.js"></script>
    <script src="scripts/SMASH/ModelFactory.js"></script>
    <script src="scripts/SMASH/ObjectMapper.js"></script>
    <script src="scripts/SMASH/APIHelper.js"></script>
    <script src="scripts/SMASH/Http/Client/HttpContext.js"></script>
    <script src="scripts/SMASH/Http/Client/RequestClient.js"></script>
    <script src="scripts/SMASH/Http/Request/HttpRequest.js"></script>
    <script src="scripts/SMASH/Http/Response/HttpResponse.js"></script>

    <!-- API Controllers -->
    <script src="scripts/SMASH/Controllers/BaseController.js"></script>
    <script src="scripts/SMASH/Controllers/AdvancedLogging.js"></script>
    <script src="scripts/SMASH/Controllers/WAFDDOSProtection.js"></script>
    <script src="scripts/SMASH/Controllers/Encryption.js"></script>
    <script src="scripts/SMASH/Controllers/CDN.js"></script>
    <script src="scripts/SMASH/Controllers/DNS.js"></script>
    <script src="scripts/SMASH/Controllers/CodeObfuscation.js"></script>
    <script src="scripts/SMASH/Controllers/Hosting.js"></script>
    <script src="scripts/SMASH/Controllers/DataManipulationConversionSortingAndCompressionAPI.js"></script>
    <script src="scripts/SMASH/Controllers/ImageManipulationAndModerationAPI.js"></script>
    <script src="scripts/SMASH/Controllers/Verification.js"></script>
    <script src="scripts/SMASH/Controllers/TwoFactorAuthenticationAPI.js"></script>
    <script src="scripts/SMASH/Controllers/UserManagement.js"></script>
    <script src="scripts/SMASH/Controllers/LoginAndRegistration.js"></script>


    <!-- Models -->
    <script src="scripts/SMASH/Models/BaseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSLR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSLIR.js"></script>
    <script src="scripts/SMASH/Models/MMDDYYYYHHMMSS.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiAUL.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiAULR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiAURR.js"></script>
    <script src="scripts/SMASH/Models/Info7.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUUR.js"></script>
    <script src="scripts/SMASH/Models/Info12.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUI.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUIR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUD.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVU.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApi2fa.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApi2faT.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiI.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiIR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiDR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSH.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSHR.js"></script>
    <script src="scripts/SMASH/Models/Nameservers.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSDC.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSCPull.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSCPush.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSE.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSER.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSW.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSWC.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSL.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSLI.js"></script>
    <script src="scripts/SMASH/Models/Info.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiAUR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUU.js"></script>
    <script src="scripts/SMASH/Models/Info17.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVA.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiD.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUDR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiV.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVUR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVAR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApi2faR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApi2faTR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSDA.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSDAR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSDCR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSCPullR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSCPushR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSO.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSOR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSWR.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSWCR.js"></script>
    <script src="scripts/SMASH/Models/Log.js"></script>
    <script src="scripts/SMASH/Models/Data.js"></script>

    ...
</head>
```
> The `Module.js` file should be imported before the other files. After `Module.js`, `Configuration.js` should be imported.
> The `ModelFactory.js` file is needed by `ObjectMapper.js` file. The `ObjectMapper` in turn, is needed by `BaseController.js`.

### 7. Including link to `app.js` in HTML file
Link your `app.js` file to your `index.html` file like:
```html
<head>
	...
	<script src="scripts/app.js"></script>
</head>
```
> The link to app.js needs to be included at the very end of the head tag, after the SDK references have been added

### 8. Initializing the Angular App
You need to initialize your app and the controller associated with your view inside your `index.html` file. Do so like:
+ Add ng-app directive to initialize your app inside the `body` tag.
```html
<body ng-app="myApp">
```
+ Add ng-controller directive to initialize your controller and bind it with your view (`index.html` file).
```html
...
<body ng-app="myApp">
	<div ng-controller="testController">
		...
	</div>
	...
</body>
...
```

### 9. Consuming the SDK 
In order to use the generated SDK's modules, controllers and factories, the project needs to be added as a dependency in your angular app's module. This will be done inside the `app.js` file.
Add the dependency like this:

```js
var app = angular.module('myApp', ['SMASH']);
```
At this point, the SDK has been successfully included in your project. Further steps include using a service/factory from the generated SDK. To see working example of this, please head on [over here](#list-of-controllers) and choose any class to see its functions and example usage.  

### 10. Running The App
To run the app, simply open up the `index.html` file in a browser.

![app-running](https://apidocs.io/illustration/angularjs?step=appRunning)

## Initialization


The Angular Application can be initialized as following:
```JavaScript
var app = angular.module('myApp', [SMASH]);
// now controllers/services can be created which import
// the factories provided by the sdk
```
### Authentication
In order to setup authentication and initialization of the Angular App, you need the following information.

| Parameter | Description |
|-----------|-------------|
| uid | Your user ID |
| secret | Your Private API Key |
| key | Your Public API Key |



```JavaScript
var app = angular.module('myApp', [SMASH]);
app.factory('config', function($scope, Configuration) 
{
    return {
        setConfigVars: function() {
            // Configuration parameters and credentials
            Configuration.uid = 'UID'; // Your user ID
            Configuration.secret = 'SECRET'; // Your Private API Key
            Configuration.key = 'KEY'; // Your Public API Key
            
        }
    };
});
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

### Get singleton instance

The singleton instance of the ``` AdvancedLogging ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, AdvancedLogging, HttpsApiRestShApiSLIR, HttpsApiRestShApiSLR){
	});
```

### <a name="logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingInfo") loggingInfo

> WAF Log Info


```javascript
function loggingInfo(name, origin, time)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| name |  ``` Required ```  | Name of your WAF zone |
| origin |  ``` Required ```  | IP Address of the Web Application |
| time |  ``` Optional ```  | Specific times or dates to lookup separated by a comma in MMDDYYHHMMSS Format ( Month Month Day Day Year Year Year Hour Hour Minute Minute Second Second [01012017120059]) |



#### Example Usage

```javascript


	app.controller("testController", function($scope, AdvancedLogging, HttpsApiRestShApiSLIR){
        var name = 'name';
        var origin = 'origin';
        var time = 'time';


		var result = AdvancedLogging.loggingInfo(name, origin, time);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="logging_configuration"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingConfiguration") loggingConfiguration

> WAF Log Configuration


```javascript
function loggingConfiguration(name, origin, activate)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| name |  ``` Required ```  | Name of the WAF zone |
| origin |  ``` Required ```  | IP Address of the Web Application you wish to configure logging on |
| activate |  ``` Required ```  | True or False |



#### Example Usage

```javascript


	app.controller("testController", function($scope, AdvancedLogging, HttpsApiRestShApiSLR){
        var name = 'name';
        var origin = 'origin';
        var activate = 'activate';


		var result = AdvancedLogging.loggingConfiguration(name, origin, activate);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="wafddos_protection"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtection") WAFDDOSProtection

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtection ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, WAFDDOSProtection, HttpsApiRestShApiSWCR, HttpsApiRestShApiSWR){
	});
```

### <a name="https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSWC") httpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function httpsApiRestShApiSWC(key, uid, name, origin, rule, contentType)
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

```javascript


	app.controller("testController", function($scope, WAFDDOSProtection, HttpsApiRestShApiSWCR){
        var key = 'API';
        var uid = 'UID';
        var name = 'origin-name';
        var origin = 'origin.yourdomain.tld';
        var rule = 'header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does';
        var contentType = 'application/json';


		var result = WAFDDOSProtection.httpsApiRestShApiSWC(key, uid, name, origin, rule, contentType);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSW") httpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function httpsApiRestShApiSW(key, uid, origin, cname, contentType)
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

```javascript


	app.controller("testController", function($scope, WAFDDOSProtection, HttpsApiRestShApiSWR){
        var key = 'API';
        var uid = 'UID';
        var origin = 'origin.yourdomain.tld';
        var cname = 'yourdomain.tld,www.yourdomain.tld';
        var contentType = 'application/json';


		var result = WAFDDOSProtection.httpsApiRestShApiSW(key, uid, origin, cname, contentType);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSWC") httpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function httpsApiRestShApiSWC(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, WAFDDOSProtection, HttpsApiRestShApiSWCR){
        var body = new HttpsApiRestShApiSWC({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "name": "WHAT YOU WISH TO NAME YOUR WAF",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
});
        var contentType = 'application/json';


		var result = WAFDDOSProtection.httpsApiRestShApiSWC(body, contentType);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtection.httpsApiRestShApiSW") httpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function httpsApiRestShApiSW(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, WAFDDOSProtection, HttpsApiRestShApiSWR){
        var body = new HttpsApiRestShApiSW({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
});
        var contentType = 'application/json';


		var result = WAFDDOSProtection.httpsApiRestShApiSW(body, contentType);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="encryption"></a>![Class: ](https://apidocs.io/img/class.png ".Encryption") Encryption

### Get singleton instance

The singleton instance of the ``` Encryption ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, Encryption, HttpsApiRestShApiSER){
	});
```

### <a name="data_and_file_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.dataAndFileEncryption") dataAndFileEncryption

> Data and File Encryption API


```javascript
function dataAndFileEncryption(data, method, bit)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| data |  ``` Required ```  | GIT URL, file URL, direct upload of file, or data as a query string |
| method |  ``` Required ```  | Single or multiple encryption types to apply to data or files separated by a comma (DES, RSA, BLOWFISH, TWOFISH, AES, IDEA, PGP) |
| bit |  ``` Required ```  | Encryption key size (4096) |



#### Example Usage

```javascript


	app.controller("testController", function($scope, Encryption, HttpsApiRestShApiSER){
        var data = 'data';
        var method = 'method';
        var bit = 99;


		var result = Encryption.dataAndFileEncryption(data, method, bit);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="cdn"></a>![Class: ](https://apidocs.io/img/class.png ".CDN") CDN

### Get singleton instance

The singleton instance of the ``` CDN ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, CDN, HttpsApiRestShApiSCPushR, HttpsApiRestShApiSCPullR){
	});
```

### <a name="c_dn_push_zone"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPushZone") cDNPushZone

> CDN Push Zone API


```javascript
function cDNPushZone(cname, file)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| cname |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access |
| file |  ``` Required ```  | GIT URL, file URL, or direct upload of file |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CDN, HttpsApiRestShApiSCPushR){
        var cname = 'cname';
        var file = 'file';


		var result = CDN.cDNPushZone(cname, file);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="c_dn_pull_zone"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPullZone") cDNPullZone

> CDN Pull Zone API


```javascript
function cDNPullZone(origin, cname)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| origin |  ``` Required ```  | Domain or domain names separated by a comma |
| cname |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CDN, HttpsApiRestShApiSCPullR){
        var origin = 'origin';
        var cname = 'cname';


		var result = CDN.cDNPullZone(origin, cname);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="dns"></a>![Class: ](https://apidocs.io/img/class.png ".DNS") DNS

### Get singleton instance

The singleton instance of the ``` DNS ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, DNS, HttpsApiRestShApiSDCR, HttpsApiRestShApiSDAR){
	});
```

### <a name="d_ns_configuration"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSConfiguration") dNSConfiguration

> DNS Configuration API


```javascript
function dNSConfiguration(domain, records)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| domain |  ``` Required ```  | Domain or domain names separated by a comma |
| records |  ``` Required ```  | Records to append to domain separated by a comma (a;www.mydomain.com;127.0.0.0,cname;mydomain.com;otherdomain.com) |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DNS, HttpsApiRestShApiSDCR){
        var domain = 'domain';
        var records = 'records';


		var result = DNS.dNSConfiguration(domain, records);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="d_ns_creation"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSCreation") dNSCreation

> DNS Creation API


```javascript
function dNSCreation(domain)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| domain |  ``` Required ```  | Domain or domain names separated by a comma |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DNS, HttpsApiRestShApiSDAR){
        var domain = 'domain';


		var result = DNS.dNSCreation(domain);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="code_obfuscation"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscation") CodeObfuscation

### Get singleton instance

The singleton instance of the ``` CodeObfuscation ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, CodeObfuscation, HttpsApiRestShApiSOR){
	});
```

### <a name="obfuscation_and_anti_tampering"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.obfuscationAndAntiTampering") obfuscationAndAntiTampering

> Javascript and Node.JS Obfuscation and Anti-Tampering API


```javascript
function obfuscationAndAntiTampering(app)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| app |  ``` Required ```  | GIT URL or ZIP package containing your APP |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CodeObfuscation, HttpsApiRestShApiSOR){
        var app = 'app';


		var result = CodeObfuscation.obfuscationAndAntiTampering(app);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="hosting"></a>![Class: ](https://apidocs.io/img/class.png ".Hosting") Hosting

### Get singleton instance

The singleton instance of the ``` Hosting ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, Hosting, HttpsApiRestShApiSHR){
	});
```

### <a name="hosting_setup"></a>![Method: ](https://apidocs.io/img/method.png ".Hosting.hostingSetup") hostingSetup

> Node.JS and Static Web APP Hosting


```javascript
function hostingSetup(app, domain)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| app |  ``` Required ```  | GIT URL or ZIP package containing your APP |
| domain |  ``` Required ```  | Domain or domain names separated by a comma |



#### Example Usage

```javascript


	app.controller("testController", function($scope, Hosting, HttpsApiRestShApiSHR){
        var app = 'app';
        var domain = 'domain';


		var result = Hosting.hostingSetup(app, domain);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="data_manipulation_conversion_sorting_and_compression_api"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPI") DataManipulationConversionSortingAndCompressionAPI

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPI ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, DataManipulationConversionSortingAndCompressionAPI, HttpsApiRestShApiDR){
	});
```

### <a name="https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiD") httpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function httpsApiRestShApiD(key, uid, user, apiuid, data, contentType)
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

```javascript


	app.controller("testController", function($scope, DataManipulationConversionSortingAndCompressionAPI, HttpsApiRestShApiDR){
        var key = 'API';
        var uid = 'UID';
        var user = 'UID';
        var apiuid = 'apiUID';
        var data = 'https://static.yourcdn.com/data.file';
        var contentType = 'application/json';


		var result = DataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiD(key, uid, user, apiuid, data, contentType);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiD") httpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function httpsApiRestShApiD(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DataManipulationConversionSortingAndCompressionAPI, HttpsApiRestShApiDR){
        var body = new HttpsApiRestShApiD({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "apiuid": "USERS API SIDE USER ID",
  "url": "DATA URL OR DIRECT FILE UPLOAD FROM CLIENT",
  "manipulation": "DATA MANIPULATION DIRECTIVES",
  "conversion": "CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)",
  "sorting": "SORT BY (NAME, DATE, TYPE, SIZE)",
  "compression": "COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)"
});
        var contentType = 'application/json';


		var result = DataManipulationConversionSortingAndCompressionAPI.httpsApiRestShApiD(body, contentType);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="image_manipulation_and_moderation_api"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPI") ImageManipulationAndModerationAPI

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPI ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, ImageManipulationAndModerationAPI, HttpsApiRestShApiIR){
	});
```

### <a name="image_manipulation"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPI.imageManipulation") imageManipulation

> Image Manipulation API


```javascript
function imageManipulation(image, transform)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| image |  ``` Required ```  | Image URL or direct upload |
| transform |  ``` Required ```  | Transformations to perform |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ImageManipulationAndModerationAPI, HttpsApiRestShApiIR){
        var image = 'image';
        var transform = 'transform';


		var result = ImageManipulationAndModerationAPI.imageManipulation(image, transform);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="verification"></a>![Class: ](https://apidocs.io/img/class.png ".Verification") Verification

### Get singleton instance

The singleton instance of the ``` Verification ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, Verification, HttpsApiRestShApiVAR, HttpsApiRestShApiVUR, HttpsApiRestShApiVR){
	});
```

### <a name="user_address_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userAddressVerification") userAddressVerification

> User Address Verification API


```javascript
function userAddressVerification(user, a, sa, c, s, z, address)
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

```javascript


	app.controller("testController", function($scope, Verification, HttpsApiRestShApiVAR){
        var user = 'user';
        var a = 'a';
        var sa = 'sa';
        var c = 'c';
        var s = 's';
        var z = 99;
        var address = 'address';


		var result = Verification.userAddressVerification(user, a, sa, c, s, z, address);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="user_verification_response"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userVerificationResponse") userVerificationResponse

> Users Verification Response API


```javascript
function userVerificationResponse(user, code)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |
| code |  ``` Required ```  | Verification code entered by the user |



#### Example Usage

```javascript


	app.controller("testController", function($scope, Verification, HttpsApiRestShApiVUR){
        var user = 'user';
        var code = 'code';


		var result = Verification.userVerificationResponse(user, code);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="user_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userVerification") userVerification

> User Verification API


```javascript
function userVerification(user)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |



#### Example Usage

```javascript


	app.controller("testController", function($scope, Verification, HttpsApiRestShApiVR){
        var user = 'user';


		var result = Verification.userVerification(user);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="two_factor_authentication_api"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPI") TwoFactorAuthenticationAPI

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPI ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, TwoFactorAuthenticationAPI, HttpsApiRestShApi2faTR, HttpsApiRestShApi2faR){
	});
```

### <a name="m2_fa_token_response"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.m2FATokenResponse") m2FATokenResponse

> Two Factor Authentication Token Reply


```javascript
function m2FATokenResponse(user, code)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username or Email |
| code |  ``` Required ```  | Response From User Containing 2FA Code |



#### Example Usage

```javascript


	app.controller("testController", function($scope, TwoFactorAuthenticationAPI, HttpsApiRestShApi2faTR){
        var user = 'user';
        var code = 'code';


		var result = TwoFactorAuthenticationAPI.m2FATokenResponse(user, code);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="two_factor_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.twoFactorAuthentication") twoFactorAuthentication

> Two Factor Authentication API


```javascript
function twoFactorAuthentication(to)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| to |  ``` Required ```  | Users UID, Username, Email, Or Cellphone number |



#### Example Usage

```javascript


	app.controller("testController", function($scope, TwoFactorAuthenticationAPI, HttpsApiRestShApi2faR){
        var to = 'to';


		var result = TwoFactorAuthenticationAPI.twoFactorAuthentication(to);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="user_management"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagement") UserManagement

### Get singleton instance

The singleton instance of the ``` UserManagement ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, UserManagement, HttpsApiRestShApiUIR, HttpsApiRestShApiUUR, HttpsApiRestShApiUDR){
	});
```

### <a name="get_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.getUserInfo") getUserInfo

> Get User Info API


```javascript
function getUserInfo(user)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users User ID |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserManagement, HttpsApiRestShApiUIR){
        var user = 'user';


		var result = UserManagement.getUserInfo(user);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="update_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.updateUser") updateUser

> Update User API


```javascript
function updateUser(user, avatar, customInput, queryParameters)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, Or Email |
| avatar |  ``` Required ```  | Avatar Image URL |
| customInput |  ``` Required ```  | Custom input variable for users profile |
| queryParameters | ``` Optional ``` | Additional optional query parameters are supported by this method |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserManagement, HttpsApiRestShApiUUR){
        var user = 'user';
        var avatar = 'avatar';
        var customInput = custom input;

        // key-value map for optional query parameters
        var queryParameters = [];


		var result = UserManagement.updateUser(user, avatar, customInput, queryParameters);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="delete_user"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.deleteUser") deleteUser

> Delete User API


```javascript
function deleteUser(user)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users UID, Username, or Email |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserManagement, HttpsApiRestShApiUDR){
        var user = 'user';


		var result = UserManagement.deleteUser(user);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="login_and_registration"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistration") LoginAndRegistration

### Get singleton instance

The singleton instance of the ``` LoginAndRegistration ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, LoginAndRegistration, HttpsApiRestShApiAURR, HttpsApiRestShApiAULR){
	});
```

### <a name="user_registration"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userRegistration") userRegistration

> User Registration API


```javascript
function userRegistration(email, user, password, name, phone, countrycode, address, queryParameters)
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

```javascript


	app.controller("testController", function($scope, LoginAndRegistration, HttpsApiRestShApiAURR){
        var email = 'email';
        var user = 'user';
        var password = 'password';
        var name = 'name';
        var phone = 99;
        var countrycode = 99;
        var address = 'address';

        // key-value map for optional query parameters
        var queryParameters = [];


		var result = LoginAndRegistration.userRegistration(email, user, password, name, phone, countrycode, address, queryParameters);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="user_authentication"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userAuthentication") userAuthentication

> User Authentication API


```javascript
function userAuthentication(user, password)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| user |  ``` Required ```  | Users Username or Email |
| password |  ``` Required ```  | Users Password |



#### Example Usage

```javascript


	app.controller("testController", function($scope, LoginAndRegistration, HttpsApiRestShApiAULR){
        var user = 'user';
        var password = 'password';


		var result = LoginAndRegistration.userAuthentication(user, password);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)



