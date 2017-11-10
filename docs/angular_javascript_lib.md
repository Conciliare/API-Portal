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
    <script src="scripts/SMASH/Controllers/AdvancedLoggingController.js"></script>
    <script src="scripts/SMASH/Controllers/WAFDDOSProtectionController.js"></script>
    <script src="scripts/SMASH/Controllers/EncryptionController.js"></script>
    <script src="scripts/SMASH/Controllers/CDNController.js"></script>
    <script src="scripts/SMASH/Controllers/DNSController.js"></script>
    <script src="scripts/SMASH/Controllers/CodeObfuscationController.js"></script>
    <script src="scripts/SMASH/Controllers/HostingController.js"></script>
    <script src="scripts/SMASH/Controllers/DataManipulationConversionSortingAndCompressionAPIController.js"></script>
    <script src="scripts/SMASH/Controllers/ImageManipulationAndModerationAPIController.js"></script>
    <script src="scripts/SMASH/Controllers/VerificationController.js"></script>
    <script src="scripts/SMASH/Controllers/TwoFactorAuthenticationAPIController.js"></script>
    <script src="scripts/SMASH/Controllers/UserManagementController.js"></script>
    <script src="scripts/SMASH/Controllers/LoginAndRegistrationController.js"></script>


    <!-- Models -->
    <script src="scripts/SMASH/Models/BaseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSLRModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSLIRModel.js"></script>
    <script src="scripts/SMASH/Models/MMDDYYYYHHMMSSModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiAULModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiAULRModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiAURRModel.js"></script>
    <script src="scripts/SMASH/Models/Info7Model.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUURModel.js"></script>
    <script src="scripts/SMASH/Models/Info12Model.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUIModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUIRModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUDModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVRModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVUModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApi2faModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApi2faTModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiIModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiIRModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiDRModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSHModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSHRModel.js"></script>
    <script src="scripts/SMASH/Models/NameserversModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSDCModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSCPullModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSCPushModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSEModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSERModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSWModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSWCModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSLModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSLIModel.js"></script>
    <script src="scripts/SMASH/Models/InfoModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiAURModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUUModel.js"></script>
    <script src="scripts/SMASH/Models/Info17Model.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVAModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiDModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUDRModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVURModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVARModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApi2faRModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApi2faTRModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSDAModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSDARModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSDCRModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSCPullRModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSCPushRModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSOModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSORModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSWRModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSWCRModel.js"></script>
    <script src="scripts/SMASH/Models/LogModel.js"></script>
    <script src="scripts/SMASH/Models/DataModel.js"></script>

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
| key | Your API Key |
| uid | Your User ID |



```JavaScript
var app = angular.module('myApp', [SMASH]);
app.factory('config', function($scope, Configuration) 
{
    return {
        setConfigVars: function() {
            // Configuration parameters and credentials
            Configuration.key = 'API'; // Your API Key
            Configuration.uid = 'UID'; // Your User ID
            
        }
    };
});
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

### Get singleton instance

The singleton instance of the ``` AdvancedLoggingController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, AdvancedLoggingController, HttpsApiRestShApiSLIRModel, HttpsApiRestShApiSLRModel){
	});
```

### <a name="get_https_api_rest_sh_api_sli"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSLI") getHttpsApiRestShApiSLI

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```javascript
function getHttpsApiRestShApiSLI(input)
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


	app.controller("testController", function($scope, AdvancedLoggingController, HttpsApiRestShApiSLIRModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['name'] = 'name';
        input['origin'] = 'origin';
        input['time'] = 'time';
        input['contentType'] = 'Content-Type';


		var result = AdvancedLoggingController.getHttpsApiRestShApiSLI(input);
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



### <a name="get_https_api_rest_sh_api_sl"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSL") getHttpsApiRestShApiSL

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```javascript
function getHttpsApiRestShApiSL(input)
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


	app.controller("testController", function($scope, AdvancedLoggingController, HttpsApiRestShApiSLRModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['name'] = 'name';
        input['origin'] = 'origin';
        input['activate'] = true;
        input['contentType'] = 'Content-Type';


		var result = AdvancedLoggingController.getHttpsApiRestShApiSL(input);
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



### <a name="create_https_api_rest_sh_api_sli"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSLI") createHttpsApiRestShApiSLI

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```javascript
function createHttpsApiRestShApiSLI(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, AdvancedLoggingController, HttpsApiRestShApiSLIRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSLIModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = AdvancedLoggingController.createHttpsApiRestShApiSLI(input);
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



### <a name="create_https_api_rest_sh_api_sl"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSL") createHttpsApiRestShApiSL

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```javascript
function createHttpsApiRestShApiSL(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, AdvancedLoggingController, HttpsApiRestShApiSLRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSLModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = AdvancedLoggingController.createHttpsApiRestShApiSL(input);
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

## <a name="wafddos_protection_controller"></a>![Class: ](https://apidocs.io/img/class.png ".WAFDDOSProtectionController") WAFDDOSProtectionController

### Get singleton instance

The singleton instance of the ``` WAFDDOSProtectionController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, WAFDDOSProtectionController, HttpsApiRestShApiSWCRModel, HttpsApiRestShApiSWRModel){
	});
```

### <a name="get_https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSWC") getHttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function getHttpsApiRestShApiSWC(input)
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


	app.controller("testController", function($scope, WAFDDOSProtectionController, HttpsApiRestShApiSWCRModel){
        var input = [];
        input['key'] = 'API';
        input['uid'] = 'UID';
        input['name'] = 'origin-name';
        input['origin'] = 'origin.yourdomain.tld';
        input['rule'] = 'header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does';
        input['contentType'] = 'application/json';


		var result = WAFDDOSProtectionController.getHttpsApiRestShApiSWC(input);
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



### <a name="get_https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSW") getHttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function getHttpsApiRestShApiSW(input)
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


	app.controller("testController", function($scope, WAFDDOSProtectionController, HttpsApiRestShApiSWRModel){
        var input = [];
        input['key'] = 'API';
        input['uid'] = 'UID';
        input['origin'] = 'origin.yourdomain.tld';
        input['cname'] = 'yourdomain.tld,www.yourdomain.tld';
        input['contentType'] = 'application/json';


		var result = WAFDDOSProtectionController.getHttpsApiRestShApiSW(input);
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



### <a name="create_https_api_rest_sh_api_swc"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSWC") createHttpsApiRestShApiSWC

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function createHttpsApiRestShApiSWC(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, WAFDDOSProtectionController, HttpsApiRestShApiSWCRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSWCModel({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "name": "WHAT YOU WISH TO NAME YOUR WAF",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
});
        input['contentType'] = 'application/json';


		var result = WAFDDOSProtectionController.createHttpsApiRestShApiSWC(input);
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



### <a name="create_https_api_rest_sh_api_sw"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSW") createHttpsApiRestShApiSW

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function createHttpsApiRestShApiSW(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, WAFDDOSProtectionController, HttpsApiRestShApiSWRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSWModel({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
});
        input['contentType'] = 'application/json';


		var result = WAFDDOSProtectionController.createHttpsApiRestShApiSW(input);
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

## <a name="encryption_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EncryptionController") EncryptionController

### Get singleton instance

The singleton instance of the ``` EncryptionController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, EncryptionController, HttpsApiRestShApiSERModel){
	});
```

### <a name="get_https_api_rest_sh_api_se"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.getHttpsApiRestShApiSE") getHttpsApiRestShApiSE

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```javascript
function getHttpsApiRestShApiSE(input)
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


	app.controller("testController", function($scope, EncryptionController, HttpsApiRestShApiSERModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['data'] = 'data';
        input['method'] = 'method';
        input['bit'] = 134;
        input['contentType'] = 'Content-Type';


		var result = EncryptionController.getHttpsApiRestShApiSE(input);
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



### <a name="create_https_api_rest_sh_api_se"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.createHttpsApiRestShApiSE") createHttpsApiRestShApiSE

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```javascript
function createHttpsApiRestShApiSE(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, EncryptionController, HttpsApiRestShApiSERModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSEModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = EncryptionController.createHttpsApiRestShApiSE(input);
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

## <a name="cdn_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CDNController") CDNController

### Get singleton instance

The singleton instance of the ``` CDNController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, CDNController, HttpsApiRestShApiSCPushRModel, HttpsApiRestShApiSCPullRModel){
	});
```

### <a name="get_https_api_rest_sh_api_sc_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiSCPush") getHttpsApiRestShApiSCPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```javascript
function getHttpsApiRestShApiSCPush(input)
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


	app.controller("testController", function($scope, CDNController, HttpsApiRestShApiSCPushRModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['cname'] = 'cname';
        input['file'] = 'file';
        input['contentType'] = 'Content-Type';


		var result = CDNController.getHttpsApiRestShApiSCPush(input);
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



### <a name="get_https_api_rest_sh_api_sc_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiSCPull") getHttpsApiRestShApiSCPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```javascript
function getHttpsApiRestShApiSCPull(input)
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


	app.controller("testController", function($scope, CDNController, HttpsApiRestShApiSCPullRModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['origin'] = 'origin';
        input['cname'] = 'cname';
        input['contentType'] = 'Content-Type';


		var result = CDNController.getHttpsApiRestShApiSCPull(input);
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



### <a name="create_https_api_rest_sh_api_sc_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiSCPush") createHttpsApiRestShApiSCPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```javascript
function createHttpsApiRestShApiSCPush(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CDNController, HttpsApiRestShApiSCPushRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSCPushModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = CDNController.createHttpsApiRestShApiSCPush(input);
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



### <a name="create_https_api_rest_sh_api_sc_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiSCPull") createHttpsApiRestShApiSCPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```javascript
function createHttpsApiRestShApiSCPull(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CDNController, HttpsApiRestShApiSCPullRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSCPullModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = CDNController.createHttpsApiRestShApiSCPull(input);
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

## <a name="dns_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DNSController") DNSController

### Get singleton instance

The singleton instance of the ``` DNSController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, DNSController, HttpsApiRestShApiSDCRModel, HttpsApiRestShApiSDARModel){
	});
```

### <a name="get_https_api_rest_sh_api_sdc"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiSDC") getHttpsApiRestShApiSDC

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```javascript
function getHttpsApiRestShApiSDC(input)
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


	app.controller("testController", function($scope, DNSController, HttpsApiRestShApiSDCRModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['domain'] = 'domain';
        input['records'] = 'records';
        input['contentType'] = 'Content-Type';


		var result = DNSController.getHttpsApiRestShApiSDC(input);
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



### <a name="create_https_api_rest_sh_api_sdc"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiSDC") createHttpsApiRestShApiSDC

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```javascript
function createHttpsApiRestShApiSDC(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DNSController, HttpsApiRestShApiSDCRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSDCModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = DNSController.createHttpsApiRestShApiSDC(input);
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



### <a name="get_https_api_rest_sh_api_sda"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiSDA") getHttpsApiRestShApiSDA

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```javascript
function getHttpsApiRestShApiSDA(input)
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


	app.controller("testController", function($scope, DNSController, HttpsApiRestShApiSDARModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['domain'] = 'domain';
        input['contentType'] = 'Content-Type';


		var result = DNSController.getHttpsApiRestShApiSDA(input);
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



### <a name="create_https_api_rest_sh_api_sda"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiSDA") createHttpsApiRestShApiSDA

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```javascript
function createHttpsApiRestShApiSDA(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DNSController, HttpsApiRestShApiSDARModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSDAModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = DNSController.createHttpsApiRestShApiSDA(input);
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

## <a name="code_obfuscation_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CodeObfuscationController") CodeObfuscationController

### Get singleton instance

The singleton instance of the ``` CodeObfuscationController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, CodeObfuscationController, HttpsApiRestShApiSORModel){
	});
```

### <a name="get_https_api_rest_sh_api_so"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.getHttpsApiRestShApiSO") getHttpsApiRestShApiSO

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```javascript
function getHttpsApiRestShApiSO(input)
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


	app.controller("testController", function($scope, CodeObfuscationController, HttpsApiRestShApiSORModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['app'] = 'app';
        input['contentType'] = 'Content-Type';


		var result = CodeObfuscationController.getHttpsApiRestShApiSO(input);
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



### <a name="create_https_api_rest_sh_api_so"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.createHttpsApiRestShApiSO") createHttpsApiRestShApiSO

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```javascript
function createHttpsApiRestShApiSO(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CodeObfuscationController, HttpsApiRestShApiSORModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSOModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = CodeObfuscationController.createHttpsApiRestShApiSO(input);
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

## <a name="hosting_controller"></a>![Class: ](https://apidocs.io/img/class.png ".HostingController") HostingController

### Get singleton instance

The singleton instance of the ``` HostingController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, HostingController, HttpsApiRestShApiSHRModel){
	});
```

### <a name="get_https_api_rest_sh_api_sh"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.getHttpsApiRestShApiSH") getHttpsApiRestShApiSH

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```javascript
function getHttpsApiRestShApiSH(input)
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


	app.controller("testController", function($scope, HostingController, HttpsApiRestShApiSHRModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['app'] = 'app';
        input['domain'] = 'domain';
        input['contentType'] = 'Content-Type';


		var result = HostingController.getHttpsApiRestShApiSH(input);
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



### <a name="create_https_api_rest_sh_api_sh"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.createHttpsApiRestShApiSH") createHttpsApiRestShApiSH

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```javascript
function createHttpsApiRestShApiSH(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, HostingController, HttpsApiRestShApiSHRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSHModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = HostingController.createHttpsApiRestShApiSH(input);
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

## <a name="data_manipulation_conversion_sorting_and_compression_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DataManipulationConversionSortingAndCompressionAPIController") DataManipulationConversionSortingAndCompressionAPIController

### Get singleton instance

The singleton instance of the ``` DataManipulationConversionSortingAndCompressionAPIController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, DataManipulationConversionSortingAndCompressionAPIController, HttpsApiRestShApiDRModel){
	});
```

### <a name="get_https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.getHttpsApiRestShApiD") getHttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function getHttpsApiRestShApiD(input)
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


	app.controller("testController", function($scope, DataManipulationConversionSortingAndCompressionAPIController, HttpsApiRestShApiDRModel){
        var input = [];
        input['key'] = 'API';
        input['uid'] = 'UID';
        input['user'] = 'UID';
        input['apiuid'] = 'apiUID';
        input['data'] = 'https://static.yourcdn.com/data.file';
        input['contentType'] = 'application/json';


		var result = DataManipulationConversionSortingAndCompressionAPIController.getHttpsApiRestShApiD(input);
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



### <a name="create_https_api_rest_sh_api_d"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.createHttpsApiRestShApiD") createHttpsApiRestShApiD

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function createHttpsApiRestShApiD(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DataManipulationConversionSortingAndCompressionAPIController, HttpsApiRestShApiDRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiDModel({
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
        input['contentType'] = 'application/json';


		var result = DataManipulationConversionSortingAndCompressionAPIController.createHttpsApiRestShApiD(input);
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

## <a name="image_manipulation_and_moderation_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ImageManipulationAndModerationAPIController") ImageManipulationAndModerationAPIController

### Get singleton instance

The singleton instance of the ``` ImageManipulationAndModerationAPIController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, ImageManipulationAndModerationAPIController, HttpsApiRestShApiIRModel){
	});
```

### <a name="get_https_api_rest_sh_api_i"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.getHttpsApiRestShApiI") getHttpsApiRestShApiI

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```javascript
function getHttpsApiRestShApiI(input)
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


	app.controller("testController", function($scope, ImageManipulationAndModerationAPIController, HttpsApiRestShApiIRModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['image'] = 'image';
        input['transform'] = 'transform';
        input['contentType'] = 'Content-Type';


		var result = ImageManipulationAndModerationAPIController.getHttpsApiRestShApiI(input);
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



### <a name="create_https_api_rest_sh_api_i"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.createHttpsApiRestShApiI") createHttpsApiRestShApiI

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```javascript
function createHttpsApiRestShApiI(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ImageManipulationAndModerationAPIController, HttpsApiRestShApiIRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiIModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = ImageManipulationAndModerationAPIController.createHttpsApiRestShApiI(input);
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

## <a name="verification_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VerificationController") VerificationController

### Get singleton instance

The singleton instance of the ``` VerificationController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVARModel, HttpsApiRestShApiVURModel, HttpsApiRestShApiVRModel){
	});
```

### <a name="get_https_api_rest_sh_api_va"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVA") getHttpsApiRestShApiVA

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```javascript
function getHttpsApiRestShApiVA(input)
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


	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVARModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['a'] = 'a';
        input['sa'] = 'sa';
        input['c'] = 'c';
        input['s'] = 's';
        input['z'] = 134;
        input['contentType'] = 'Content-Type';


		var result = VerificationController.getHttpsApiRestShApiVA(input);
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



### <a name="create_https_api_rest_sh_api_va"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVA") createHttpsApiRestShApiVA

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```javascript
function createHttpsApiRestShApiVA(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVARModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiVAModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = VerificationController.createHttpsApiRestShApiVA(input);
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



### <a name="get_https_api_rest_sh_api_vu"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVU") getHttpsApiRestShApiVU

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```javascript
function getHttpsApiRestShApiVU(input)
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


	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVURModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['code'] = 'code';
        input['contentType'] = 'Content-Type';


		var result = VerificationController.getHttpsApiRestShApiVU(input);
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



### <a name="create_https_api_rest_sh_api_vu"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVU") createHttpsApiRestShApiVU

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```javascript
function createHttpsApiRestShApiVU(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVURModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiVUModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = VerificationController.createHttpsApiRestShApiVU(input);
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



### <a name="get_https_api_rest_sh_api_v"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiV") getHttpsApiRestShApiV

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```javascript
function getHttpsApiRestShApiV(input)
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


	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVRModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['to'] = 'to';
        input['contentType'] = 'Content-Type';


		var result = VerificationController.getHttpsApiRestShApiV(input);
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



### <a name="create_https_api_rest_sh_api_v"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiV") createHttpsApiRestShApiV

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```javascript
function createHttpsApiRestShApiV(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiVModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = VerificationController.createHttpsApiRestShApiV(input);
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

## <a name="two_factor_authentication_api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TwoFactorAuthenticationAPIController") TwoFactorAuthenticationAPIController

### Get singleton instance

The singleton instance of the ``` TwoFactorAuthenticationAPIController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, TwoFactorAuthenticationAPIController, HttpsApiRestShApi2faTRModel, HttpsApiRestShApi2faRModel){
	});
```

### <a name="get_https_api_rest_sh_api2fa_t"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2faT") getHttpsApiRestShApi2faT

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```javascript
function getHttpsApiRestShApi2faT(input)
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


	app.controller("testController", function($scope, TwoFactorAuthenticationAPIController, HttpsApiRestShApi2faTRModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['code'] = 'code';
        input['contentType'] = 'Content-Type';


		var result = TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2faT(input);
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



### <a name="create_https_api_rest_sh_api2fa_t"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2faT") createHttpsApiRestShApi2faT

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```javascript
function createHttpsApiRestShApi2faT(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, TwoFactorAuthenticationAPIController, HttpsApiRestShApi2faTRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApi2faTModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2faT(input);
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



### <a name="get_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2fa") getHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```javascript
function getHttpsApiRestShApi2fa(input)
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


	app.controller("testController", function($scope, TwoFactorAuthenticationAPIController, HttpsApiRestShApi2faRModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['to'] = 'to';
        input['contentType'] = 'Content-Type';


		var result = TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2fa(input);
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



### <a name="create_https_api_rest_sh_api2fa"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2fa") createHttpsApiRestShApi2fa

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API


```javascript
function createHttpsApiRestShApi2fa(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, TwoFactorAuthenticationAPIController, HttpsApiRestShApi2faRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApi2faModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2fa(input);
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

## <a name="user_management_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UserManagementController") UserManagementController

### Get singleton instance

The singleton instance of the ``` UserManagementController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUIRModel, HttpsApiRestShApiUURModel, HttpsApiRestShApiUDRModel){
	});
```

### <a name="get_https_api_rest_sh_api_ui"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUI") getHttpsApiRestShApiUI

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```javascript
function getHttpsApiRestShApiUI(input)
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


	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUIRModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['apiuid'] = 'apiuid';
        input['contentType'] = 'Content-Type';


		var result = UserManagementController.getHttpsApiRestShApiUI(input);
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



### <a name="create_https_api_rest_sh_api_ui"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUI") createHttpsApiRestShApiUI

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```javascript
function createHttpsApiRestShApiUI(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUIRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiUIModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = UserManagementController.createHttpsApiRestShApiUI(input);
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



### <a name="get_https_api_rest_sh_api_uu"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUU") getHttpsApiRestShApiUU

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```javascript
function getHttpsApiRestShApiUU(input)
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


	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUURModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['apiuid'] = 'apiuid';
        input['avatar'] = 'avatar';
        input['customInput'] = custom input;
        input['contentType'] = 'Content-Type';


		var result = UserManagementController.getHttpsApiRestShApiUU(input);
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



### <a name="create_https_api_rest_sh_api_uu"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUU") createHttpsApiRestShApiUU

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```javascript
function createHttpsApiRestShApiUU(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUURModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiUUModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = UserManagementController.createHttpsApiRestShApiUU(input);
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



### <a name="get_https_api_rest_sh_api_ud"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUD") getHttpsApiRestShApiUD

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```javascript
function getHttpsApiRestShApiUD(input)
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


	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUDRModel){
        var input = [];
        input['api'] = 'api';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['apiuid'] = 'apiuid';
        input['contentType'] = 'Content-Type';


		var result = UserManagementController.getHttpsApiRestShApiUD(input);
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



### <a name="create_https_api_rest_sh_api_ud"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUD") createHttpsApiRestShApiUD

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```javascript
function createHttpsApiRestShApiUD(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUDRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiUDModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = UserManagementController.createHttpsApiRestShApiUD(input);
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

## <a name="login_and_registration_controller"></a>![Class: ](https://apidocs.io/img/class.png ".LoginAndRegistrationController") LoginAndRegistrationController

### Get singleton instance

The singleton instance of the ``` LoginAndRegistrationController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, LoginAndRegistrationController, HttpsApiRestShApiAURRModel, HttpsApiRestShApiAULRModel){
	});
```

### <a name="get_https_api_rest_sh_api_aur"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAUR") getHttpsApiRestShApiAUR

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```javascript
function getHttpsApiRestShApiAUR(input)
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


	app.controller("testController", function($scope, LoginAndRegistrationController, HttpsApiRestShApiAURRModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['password'] = 'password';
        input['name'] = 'name';
        input['email'] = 'email';
        input['phone'] = 226;
        input['countrycode'] = 226;
        input['address'] = 'address';
        input['contentType'] = 'Content-Type';


		var result = LoginAndRegistrationController.getHttpsApiRestShApiAUR(input);
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



### <a name="create_https_api_rest_sh_api_aur"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAUR") createHttpsApiRestShApiAUR

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```javascript
function createHttpsApiRestShApiAUR(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, LoginAndRegistrationController, HttpsApiRestShApiAURRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiAURModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = LoginAndRegistrationController.createHttpsApiRestShApiAUR(input);
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



### <a name="get_https_api_rest_sh_api_aul"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAUL") getHttpsApiRestShApiAUL

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```javascript
function getHttpsApiRestShApiAUL(input)
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


	app.controller("testController", function($scope, LoginAndRegistrationController, HttpsApiRestShApiAULRModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['password'] = 'password';
        input['contentType'] = 'Content-Type';


		var result = LoginAndRegistrationController.getHttpsApiRestShApiAUL(input);
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



### <a name="create_https_api_rest_sh_api_aul"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAUL") createHttpsApiRestShApiAUL

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```javascript
function createHttpsApiRestShApiAUL(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, LoginAndRegistrationController, HttpsApiRestShApiAULRModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiAULModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = LoginAndRegistrationController.createHttpsApiRestShApiAUL(input);
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



