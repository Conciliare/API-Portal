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
| basicAuthUserName | The username to use with basic authentication |
| basicAuthPassword | The password to use with basic authentication |



```JavaScript
var app = angular.module('myApp', [SMASH]);
app.factory('config', function($scope, Configuration) 
{
    return {
        setConfigVars: function() {
            // Configuration parameters and credentials
            Configuration.basicAuthUserName = 'basicAuthUserName'; // The username to use with basic authentication
            Configuration.basicAuthPassword = 'basicAuthPassword'; // The password to use with basic authentication
            
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

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```javascript
function loggingInfo(key, uid, name, origin, time, contentType)
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

```javascript


	app.controller("testController", function($scope, AdvancedLogging, HttpsApiRestShApiSLIR){
        var key = 'key';
        var uid = 'uid';
        var name = 'name';
        var origin = 'origin';
        var time = 'time';
        var contentType = 'Content-Type';


		var result = AdvancedLogging.loggingInfo(key, uid, name, origin, time, contentType);
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



### <a name="logging_setup"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingSetup") loggingSetup

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```javascript
function loggingSetup(key, uid, name, origin, activate, contentType)
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

```javascript


	app.controller("testController", function($scope, AdvancedLogging, HttpsApiRestShApiSLR){
        var key = 'key';
        var uid = 'uid';
        var name = 'name';
        var origin = 'origin';
        var activate = false;
        var contentType = 'Content-Type';


		var result = AdvancedLogging.loggingSetup(key, uid, name, origin, activate, contentType);
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



### <a name="logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingInfo") loggingInfo

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```javascript
function loggingInfo(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, AdvancedLogging, HttpsApiRestShApiSLIR){
        var body = new HttpsApiRestShApiSLI({"key":"value"});
        var contentType = 'Content-Type';


		var result = AdvancedLogging.loggingInfo(body, contentType);
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



### <a name="logging_setup"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLogging.loggingSetup") loggingSetup

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```javascript
function loggingSetup(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, AdvancedLogging, HttpsApiRestShApiSLR){
        var body = new HttpsApiRestShApiSL({"key":"value"});
        var contentType = 'Content-Type';


		var result = AdvancedLogging.loggingSetup(body, contentType);
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

### <a name="data_and_file_encryption_api"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.dataAndFileEncryptionAPI") dataAndFileEncryptionAPI

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```javascript
function dataAndFileEncryptionAPI(key, uid, data, method, bit, contentType)
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

```javascript


	app.controller("testController", function($scope, Encryption, HttpsApiRestShApiSER){
        var key = 'key';
        var uid = 'uid';
        var data = 'data';
        var method = 'method';
        var bit = 59;
        var contentType = 'Content-Type';


		var result = Encryption.dataAndFileEncryptionAPI(key, uid, data, method, bit, contentType);
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



### <a name="data_and_file_encryption_api"></a>![Method: ](https://apidocs.io/img/method.png ".Encryption.dataAndFileEncryptionAPI") dataAndFileEncryptionAPI

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```javascript
function dataAndFileEncryptionAPI(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, Encryption, HttpsApiRestShApiSER){
        var body = new HttpsApiRestShApiSE({"key":"value"});
        var contentType = 'Content-Type';


		var result = Encryption.dataAndFileEncryptionAPI(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```javascript
function cDNPushZone(key, uid, cname, file, contentType)
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

```javascript


	app.controller("testController", function($scope, CDN, HttpsApiRestShApiSCPushR){
        var key = 'key';
        var uid = 'uid';
        var cname = 'cname';
        var file = 'file';
        var contentType = 'Content-Type';


		var result = CDN.cDNPushZone(key, uid, cname, file, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```javascript
function cDNPullZone(key, uid, origin, cname, contentType)
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


	app.controller("testController", function($scope, CDN, HttpsApiRestShApiSCPullR){
        var key = 'key';
        var uid = 'uid';
        var origin = 'origin';
        var cname = 'cname';
        var contentType = 'Content-Type';


		var result = CDN.cDNPullZone(key, uid, origin, cname, contentType);
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



### <a name="c_dn_push_zone"></a>![Method: ](https://apidocs.io/img/method.png ".CDN.cDNPushZone") cDNPushZone

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```javascript
function cDNPushZone(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CDN, HttpsApiRestShApiSCPushR){
        var body = new HttpsApiRestShApiSCPush({"key":"value"});
        var contentType = 'Content-Type';


		var result = CDN.cDNPushZone(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```javascript
function cDNPullZone(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CDN, HttpsApiRestShApiSCPullR){
        var body = new HttpsApiRestShApiSCPull({"key":"value"});
        var contentType = 'Content-Type';


		var result = CDN.cDNPullZone(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```javascript
function dNSConfiguration(key, uid, domain, records, contentType)
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

```javascript


	app.controller("testController", function($scope, DNS, HttpsApiRestShApiSDCR){
        var key = 'key';
        var uid = 'uid';
        var domain = 'domain';
        var records = 'records';
        var contentType = 'Content-Type';


		var result = DNS.dNSConfiguration(key, uid, domain, records, contentType);
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



### <a name="d_ns_configuration"></a>![Method: ](https://apidocs.io/img/method.png ".DNS.dNSConfiguration") dNSConfiguration

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```javascript
function dNSConfiguration(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DNS, HttpsApiRestShApiSDCR){
        var body = new HttpsApiRestShApiSDC({"key":"value"});
        var contentType = 'Content-Type';


		var result = DNS.dNSConfiguration(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```javascript
function dNSCreation(key, uid, domain, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| domain |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DNS, HttpsApiRestShApiSDAR){
        var key = 'key';
        var uid = 'uid';
        var domain = 'domain';
        var contentType = 'Content-Type';


		var result = DNS.dNSCreation(key, uid, domain, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```javascript
function dNSCreation(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DNS, HttpsApiRestShApiSDAR){
        var body = new HttpsApiRestShApiSDA({"key":"value"});
        var contentType = 'Content-Type';


		var result = DNS.dNSCreation(body, contentType);
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

### <a name="code_application_obfuscation_and_anti_tampering"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.codeApplicationObfuscationAndAntiTampering") codeApplicationObfuscationAndAntiTampering

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```javascript
function codeApplicationObfuscationAndAntiTampering(key, uid, app, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| app |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CodeObfuscation, HttpsApiRestShApiSOR){
        var key = 'key';
        var uid = 'uid';
        var app = 'app';
        var contentType = 'Content-Type';


		var result = CodeObfuscation.codeApplicationObfuscationAndAntiTampering(key, uid, app, contentType);
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



### <a name="code_application_obfuscation_and_anti_tampering"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscation.codeApplicationObfuscationAndAntiTampering") codeApplicationObfuscationAndAntiTampering

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```javascript
function codeApplicationObfuscationAndAntiTampering(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CodeObfuscation, HttpsApiRestShApiSOR){
        var body = new HttpsApiRestShApiSO({"key":"value"});
        var contentType = 'Content-Type';


		var result = CodeObfuscation.codeApplicationObfuscationAndAntiTampering(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```javascript
function hostingSetup(key, uid, app, domain, contentType)
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

```javascript


	app.controller("testController", function($scope, Hosting, HttpsApiRestShApiSHR){
        var key = 'key';
        var uid = 'uid';
        var app = 'app';
        var domain = 'domain';
        var contentType = 'Content-Type';


		var result = Hosting.hostingSetup(key, uid, app, domain, contentType);
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



### <a name="hosting_setup"></a>![Method: ](https://apidocs.io/img/method.png ".Hosting.hostingSetup") hostingSetup

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```javascript
function hostingSetup(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, Hosting, HttpsApiRestShApiSHR){
        var body = new HttpsApiRestShApiSH({"key":"value"});
        var contentType = 'Content-Type';


		var result = Hosting.hostingSetup(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```javascript
function imageManipulation(key, uid, image, transform, contentType)
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

```javascript


	app.controller("testController", function($scope, ImageManipulationAndModerationAPI, HttpsApiRestShApiIR){
        var key = 'key';
        var uid = 'uid';
        var image = 'image';
        var transform = 'transform';
        var contentType = 'Content-Type';


		var result = ImageManipulationAndModerationAPI.imageManipulation(key, uid, image, transform, contentType);
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



### <a name="image_manipulation"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPI.imageManipulation") imageManipulation

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```javascript
function imageManipulation(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ImageManipulationAndModerationAPI, HttpsApiRestShApiIR){
        var body = new HttpsApiRestShApiI({"key":"value"});
        var contentType = 'Content-Type';


		var result = ImageManipulationAndModerationAPI.imageManipulation(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```javascript
function userAddressVerification(key, uid, user, a, sa, c, s, z, contentType)
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

```javascript


	app.controller("testController", function($scope, Verification, HttpsApiRestShApiVAR){
        var key = 'key';
        var uid = 'uid';
        var user = 'user';
        var a = 'a';
        var sa = 'sa';
        var c = 'c';
        var s = 's';
        var z = 59;
        var contentType = 'Content-Type';


		var result = Verification.userAddressVerification(key, uid, user, a, sa, c, s, z, contentType);
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



### <a name="user_address_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.userAddressVerification") userAddressVerification

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```javascript
function userAddressVerification(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, Verification, HttpsApiRestShApiVAR){
        var body = new HttpsApiRestShApiVA({"key":"value"});
        var contentType = 'Content-Type';


		var result = Verification.userAddressVerification(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```javascript
function userVerification(key, uid, user, code, contentType)
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

```javascript


	app.controller("testController", function($scope, Verification, HttpsApiRestShApiVUR){
        var key = 'key';
        var uid = 'uid';
        var user = 'user';
        var code = 'code';
        var contentType = 'Content-Type';


		var result = Verification.userVerification(key, uid, user, code, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```javascript
function userVerification(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, Verification, HttpsApiRestShApiVUR){
        var body = new HttpsApiRestShApiVU({"key":"value"});
        var contentType = 'Content-Type';


		var result = Verification.userVerification(body, contentType);
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



### <a name="cellphone_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.cellphoneVerification") cellphoneVerification

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```javascript
function cellphoneVerification(key, uid, to, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, Verification, HttpsApiRestShApiVR){
        var key = 'key';
        var uid = 'uid';
        var to = 'to';
        var contentType = 'Content-Type';


		var result = Verification.cellphoneVerification(key, uid, to, contentType);
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



### <a name="cellphone_verification"></a>![Method: ](https://apidocs.io/img/method.png ".Verification.cellphoneVerification") cellphoneVerification

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```javascript
function cellphoneVerification(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, Verification, HttpsApiRestShApiVR){
        var body = new HttpsApiRestShApiV({"key":"value"});
        var contentType = 'Content-Type';


		var result = Verification.cellphoneVerification(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```javascript
function m2FATokenResponse(key, uid, user, code, contentType)
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

```javascript


	app.controller("testController", function($scope, TwoFactorAuthenticationAPI, HttpsApiRestShApi2faTR){
        var key = 'key';
        var uid = 'uid';
        var user = 'user';
        var code = 'code';
        var contentType = 'Content-Type';


		var result = TwoFactorAuthenticationAPI.m2FATokenResponse(key, uid, user, code, contentType);
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



### <a name="m2_fa_token_response"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPI.m2FATokenResponse") m2FATokenResponse

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```javascript
function m2FATokenResponse(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, TwoFactorAuthenticationAPI, HttpsApiRestShApi2faTR){
        var body = new HttpsApiRestShApi2faT({"key":"value"});
        var contentType = 'Content-Type';


		var result = TwoFactorAuthenticationAPI.m2FATokenResponse(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```javascript
function twoFactorAuthentication(key, uid, to, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| key |  ``` Required ```  | TODO: Add a parameter description |
| uid |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, TwoFactorAuthenticationAPI, HttpsApiRestShApi2faR){
        var key = 'key';
        var uid = 'uid';
        var to = 'to';
        var contentType = 'Content-Type';


		var result = TwoFactorAuthenticationAPI.twoFactorAuthentication(key, uid, to, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```javascript
function twoFactorAuthentication(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, TwoFactorAuthenticationAPI, HttpsApiRestShApi2faR){
        var body = new HttpsApiRestShApi2fa({"key":"value"});
        var contentType = 'Content-Type';


		var result = TwoFactorAuthenticationAPI.twoFactorAuthentication(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```javascript
function getUserInfo(key, uid, user, apiuid, contentType)
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

```javascript


	app.controller("testController", function($scope, UserManagement, HttpsApiRestShApiUIR){
        var key = 'key';
        var uid = 'uid';
        var user = 'user';
        var apiuid = 'apiuid';
        var contentType = 'Content-Type';


		var result = UserManagement.getUserInfo(key, uid, user, apiuid, contentType);
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



### <a name="get_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagement.getUserInfo") getUserInfo

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```javascript
function getUserInfo(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserManagement, HttpsApiRestShApiUIR){
        var body = new HttpsApiRestShApiUI({"key":"value"});
        var contentType = 'Content-Type';


		var result = UserManagement.getUserInfo(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```javascript
function updateUser(key, uid, user, apiuid, avatar, customInput, contentType)
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

```javascript


	app.controller("testController", function($scope, UserManagement, HttpsApiRestShApiUUR){
        var key = 'key';
        var uid = 'uid';
        var user = 'user';
        var apiuid = 'apiuid';
        var avatar = 'avatar';
        var customInput = custom input;
        var contentType = 'Content-Type';


		var result = UserManagement.updateUser(key, uid, user, apiuid, avatar, customInput, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```javascript
function updateUser(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserManagement, HttpsApiRestShApiUUR){
        var body = new HttpsApiRestShApiUU({"key":"value"});
        var contentType = 'Content-Type';


		var result = UserManagement.updateUser(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```javascript
function deleteUser(api, uid, user, apiuid, contentType)
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

```javascript


	app.controller("testController", function($scope, UserManagement, HttpsApiRestShApiUDR){
        var api = 'api';
        var uid = 'uid';
        var user = 'user';
        var apiuid = 'apiuid';
        var contentType = 'Content-Type';


		var result = UserManagement.deleteUser(api, uid, user, apiuid, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```javascript
function deleteUser(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserManagement, HttpsApiRestShApiUDR){
        var body = new HttpsApiRestShApiUD({"key":"value"});
        var contentType = 'Content-Type';


		var result = UserManagement.deleteUser(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```javascript
function userRegistration(key, uid, user, password, name, email, phone, countrycode, address, contentType)
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

```javascript


	app.controller("testController", function($scope, LoginAndRegistration, HttpsApiRestShApiAURR){
        var key = 'key';
        var uid = 'uid';
        var user = 'user';
        var password = 'password';
        var name = 'name';
        var email = 'email';
        var phone = 59;
        var countrycode = 59;
        var address = 'address';
        var contentType = 'Content-Type';


		var result = LoginAndRegistration.userRegistration(key, uid, user, password, name, email, phone, countrycode, address, contentType);
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



### <a name="user_registration"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistration.userRegistration") userRegistration

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```javascript
function userRegistration(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, LoginAndRegistration, HttpsApiRestShApiAURR){
        var body = new HttpsApiRestShApiAUR({"key":"value"});
        var contentType = 'Content-Type';


		var result = LoginAndRegistration.userRegistration(body, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```javascript
function userAuthentication(key, uid, user, password, contentType)
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

```javascript


	app.controller("testController", function($scope, LoginAndRegistration, HttpsApiRestShApiAULR){
        var key = 'key';
        var uid = 'uid';
        var user = 'user';
        var password = 'password';
        var contentType = 'Content-Type';


		var result = LoginAndRegistration.userAuthentication(key, uid, user, password, contentType);
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

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```javascript
function userAuthentication(body, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, LoginAndRegistration, HttpsApiRestShApiAULR){
        var body = new HttpsApiRestShApiAUL({"key":"value"});
        var contentType = 'Content-Type';


		var result = LoginAndRegistration.userAuthentication(body, contentType);
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



