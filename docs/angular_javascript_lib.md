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
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSecurityLoggingInfoRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSecurityLoggingRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiDataRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVerifyAddressRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSecurityWafConfigureRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSecurityWafRequestModel.js"></script>
    <script src="scripts/SMASH/Models/Info17Model.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSecurityEncryptionResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSecurityEncryptionRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiServiceCdnPushRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiServiceCdnPullRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUserUpdateRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiServiceDnsConfigureRequestModel.js"></script>
    <script src="scripts/SMASH/Models/DataModel.js"></script>
    <script src="scripts/SMASH/Models/LogModel.js"></script>
    <script src="scripts/SMASH/Models/NameserversModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiServiceHostingResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSecurityWafConfigureResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiAuthUserRegisterRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSecurityWafResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiServiceObfuscationResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiServiceHostingRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiDataResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiServiceObfuscationRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiImageResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiImageRequestModel.js"></script>
    <script src="scripts/SMASH/Models/InfoModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApi2faTokenRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApi2faResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVerifyUserRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiServiceCdnPushResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiServiceCdnPullResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVerifyResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUserDeleteRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiServiceDnsConfigureResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUserInfoResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiServiceDnsAddResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUserInfoRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiServiceDnsAddRequestModel.js"></script>
    <script src="scripts/SMASH/Models/Info12Model.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUserUpdateResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApi2faTokenResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApi2faRequestModel.js"></script>
    <script src="scripts/SMASH/Models/Info7Model.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVerifyAddressResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiAuthUserRegisterResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVerifyUserResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiAuthUserLoginResponseModel.js"></script>
    <script src="scripts/SMASH/Models/MMDDYYYYHHMMSSModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiAuthUserLoginRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSecurityLoggingInfoResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiVerifyRequestModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiSecurityLoggingResponseModel.js"></script>
    <script src="scripts/SMASH/Models/HttpsApiRestShApiUserDeleteResponseModel.js"></script>

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
	app.controller("testController", function($scope, AdvancedLoggingController, HttpsApiRestShApiSecurityLoggingInfoResponseModel, HttpsApiRestShApiSecurityLoggingResponseModel){
	});
```

### <a name="get_https_api_rest_sh_api_security_logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSecurityLoggingInfo") getHttpsApiRestShApiSecurityLoggingInfo

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```javascript
function getHttpsApiRestShApiSecurityLoggingInfo(input)
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


	app.controller("testController", function($scope, AdvancedLoggingController, HttpsApiRestShApiSecurityLoggingInfoResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['name'] = 'name';
        input['origin'] = 'origin';
        input['time'] = 'time';
        input['contentType'] = 'Content-Type';


		var result = AdvancedLoggingController.getHttpsApiRestShApiSecurityLoggingInfo(input);
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



### <a name="get_https_api_rest_sh_api_security_logging"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.getHttpsApiRestShApiSecurityLogging") getHttpsApiRestShApiSecurityLogging

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```javascript
function getHttpsApiRestShApiSecurityLogging(input)
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


	app.controller("testController", function($scope, AdvancedLoggingController, HttpsApiRestShApiSecurityLoggingResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['name'] = 'name';
        input['origin'] = 'origin';
        input['activate'] = true;
        input['contentType'] = 'Content-Type';


		var result = AdvancedLoggingController.getHttpsApiRestShApiSecurityLogging(input);
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



### <a name="create_https_api_rest_sh_api_security_logging_info"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSecurityLoggingInfo") createHttpsApiRestShApiSecurityLoggingInfo

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info


```javascript
function createHttpsApiRestShApiSecurityLoggingInfo(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, AdvancedLoggingController, HttpsApiRestShApiSecurityLoggingInfoResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSecurityLoggingInfoRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = AdvancedLoggingController.createHttpsApiRestShApiSecurityLoggingInfo(input);
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



### <a name="create_https_api_rest_sh_api_security_logging"></a>![Method: ](https://apidocs.io/img/method.png ".AdvancedLoggingController.createHttpsApiRestShApiSecurityLogging") createHttpsApiRestShApiSecurityLogging

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup


```javascript
function createHttpsApiRestShApiSecurityLogging(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, AdvancedLoggingController, HttpsApiRestShApiSecurityLoggingResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSecurityLoggingRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = AdvancedLoggingController.createHttpsApiRestShApiSecurityLogging(input);
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
	app.controller("testController", function($scope, WAFDDOSProtectionController, HttpsApiRestShApiSecurityWafConfigureResponseModel, HttpsApiRestShApiSecurityWafResponseModel){
	});
```

### <a name="get_https_api_rest_sh_api_security_waf_configure"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSecurityWafConfigure") getHttpsApiRestShApiSecurityWafConfigure

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function getHttpsApiRestShApiSecurityWafConfigure(input)
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


	app.controller("testController", function($scope, WAFDDOSProtectionController, HttpsApiRestShApiSecurityWafConfigureResponseModel){
        var input = [];
        input['key'] = 'API';
        input['uid'] = 'UID';
        input['name'] = 'origin-name';
        input['origin'] = 'origin.yourdomain.tld';
        input['rule'] = 'header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does';
        input['contentType'] = 'application/json';


		var result = WAFDDOSProtectionController.getHttpsApiRestShApiSecurityWafConfigure(input);
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



### <a name="get_https_api_rest_sh_api_security_waf"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.getHttpsApiRestShApiSecurityWaf") getHttpsApiRestShApiSecurityWaf

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function getHttpsApiRestShApiSecurityWaf(input)
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


	app.controller("testController", function($scope, WAFDDOSProtectionController, HttpsApiRestShApiSecurityWafResponseModel){
        var input = [];
        input['key'] = 'API';
        input['uid'] = 'UID';
        input['origin'] = 'origin.yourdomain.tld';
        input['cname'] = 'yourdomain.tld,www.yourdomain.tld';
        input['contentType'] = 'application/json';


		var result = WAFDDOSProtectionController.getHttpsApiRestShApiSecurityWaf(input);
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



### <a name="create_https_api_rest_sh_api_security_waf_configure"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSecurityWafConfigure") createHttpsApiRestShApiSecurityWafConfigure

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function createHttpsApiRestShApiSecurityWafConfigure(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, WAFDDOSProtectionController, HttpsApiRestShApiSecurityWafConfigureResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSecurityWafConfigureRequestModel({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "name": "WHAT YOU WISH TO NAME YOUR WAF",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
});
        input['contentType'] = 'application/json';


		var result = WAFDDOSProtectionController.createHttpsApiRestShApiSecurityWafConfigure(input);
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



### <a name="create_https_api_rest_sh_api_security_waf"></a>![Method: ](https://apidocs.io/img/method.png ".WAFDDOSProtectionController.createHttpsApiRestShApiSecurityWaf") createHttpsApiRestShApiSecurityWaf

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function createHttpsApiRestShApiSecurityWaf(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, WAFDDOSProtectionController, HttpsApiRestShApiSecurityWafResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSecurityWafRequestModel({
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
});
        input['contentType'] = 'application/json';


		var result = WAFDDOSProtectionController.createHttpsApiRestShApiSecurityWaf(input);
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
	app.controller("testController", function($scope, EncryptionController, HttpsApiRestShApiSecurityEncryptionResponseModel){
	});
```

### <a name="get_https_api_rest_sh_api_security_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.getHttpsApiRestShApiSecurityEncryption") getHttpsApiRestShApiSecurityEncryption

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```javascript
function getHttpsApiRestShApiSecurityEncryption(input)
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


	app.controller("testController", function($scope, EncryptionController, HttpsApiRestShApiSecurityEncryptionResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['data'] = 'data';
        input['method'] = 'method';
        input['bit'] = 129;
        input['contentType'] = 'Content-Type';


		var result = EncryptionController.getHttpsApiRestShApiSecurityEncryption(input);
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



### <a name="create_https_api_rest_sh_api_security_encryption"></a>![Method: ](https://apidocs.io/img/method.png ".EncryptionController.createHttpsApiRestShApiSecurityEncryption") createHttpsApiRestShApiSecurityEncryption

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API


```javascript
function createHttpsApiRestShApiSecurityEncryption(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, EncryptionController, HttpsApiRestShApiSecurityEncryptionResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiSecurityEncryptionRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = EncryptionController.createHttpsApiRestShApiSecurityEncryption(input);
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
	app.controller("testController", function($scope, CDNController, HttpsApiRestShApiServiceCdnPushResponseModel, HttpsApiRestShApiServiceCdnPullResponseModel){
	});
```

### <a name="get_https_api_rest_sh_api_service_cdn_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiServiceCdnPush") getHttpsApiRestShApiServiceCdnPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```javascript
function getHttpsApiRestShApiServiceCdnPush(input)
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


	app.controller("testController", function($scope, CDNController, HttpsApiRestShApiServiceCdnPushResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['cname'] = 'cname';
        input['file'] = 'file';
        input['contentType'] = 'Content-Type';


		var result = CDNController.getHttpsApiRestShApiServiceCdnPush(input);
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



### <a name="get_https_api_rest_sh_api_service_cdn_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.getHttpsApiRestShApiServiceCdnPull") getHttpsApiRestShApiServiceCdnPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```javascript
function getHttpsApiRestShApiServiceCdnPull(input)
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


	app.controller("testController", function($scope, CDNController, HttpsApiRestShApiServiceCdnPullResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['origin'] = 'origin';
        input['cname'] = 'cname';
        input['contentType'] = 'Content-Type';


		var result = CDNController.getHttpsApiRestShApiServiceCdnPull(input);
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



### <a name="create_https_api_rest_sh_api_service_cdn_push"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiServiceCdnPush") createHttpsApiRestShApiServiceCdnPush

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API


```javascript
function createHttpsApiRestShApiServiceCdnPush(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CDNController, HttpsApiRestShApiServiceCdnPushResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiServiceCdnPushRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = CDNController.createHttpsApiRestShApiServiceCdnPush(input);
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



### <a name="create_https_api_rest_sh_api_service_cdn_pull"></a>![Method: ](https://apidocs.io/img/method.png ".CDNController.createHttpsApiRestShApiServiceCdnPull") createHttpsApiRestShApiServiceCdnPull

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API


```javascript
function createHttpsApiRestShApiServiceCdnPull(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CDNController, HttpsApiRestShApiServiceCdnPullResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiServiceCdnPullRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = CDNController.createHttpsApiRestShApiServiceCdnPull(input);
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
	app.controller("testController", function($scope, DNSController, HttpsApiRestShApiServiceDnsConfigureResponseModel, HttpsApiRestShApiServiceDnsAddResponseModel){
	});
```

### <a name="get_https_api_rest_sh_api_service_dns_configure"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiServiceDnsConfigure") getHttpsApiRestShApiServiceDnsConfigure

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```javascript
function getHttpsApiRestShApiServiceDnsConfigure(input)
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


	app.controller("testController", function($scope, DNSController, HttpsApiRestShApiServiceDnsConfigureResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['domain'] = 'domain';
        input['records'] = 'records';
        input['contentType'] = 'Content-Type';


		var result = DNSController.getHttpsApiRestShApiServiceDnsConfigure(input);
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



### <a name="create_https_api_rest_sh_api_service_dns_configure"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiServiceDnsConfigure") createHttpsApiRestShApiServiceDnsConfigure

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API


```javascript
function createHttpsApiRestShApiServiceDnsConfigure(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DNSController, HttpsApiRestShApiServiceDnsConfigureResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiServiceDnsConfigureRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = DNSController.createHttpsApiRestShApiServiceDnsConfigure(input);
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



### <a name="get_https_api_rest_sh_api_service_dns_add"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.getHttpsApiRestShApiServiceDnsAdd") getHttpsApiRestShApiServiceDnsAdd

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```javascript
function getHttpsApiRestShApiServiceDnsAdd(input)
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


	app.controller("testController", function($scope, DNSController, HttpsApiRestShApiServiceDnsAddResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['domain'] = 'domain';
        input['contentType'] = 'Content-Type';


		var result = DNSController.getHttpsApiRestShApiServiceDnsAdd(input);
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



### <a name="create_https_api_rest_sh_api_service_dns_add"></a>![Method: ](https://apidocs.io/img/method.png ".DNSController.createHttpsApiRestShApiServiceDnsAdd") createHttpsApiRestShApiServiceDnsAdd

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API


```javascript
function createHttpsApiRestShApiServiceDnsAdd(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DNSController, HttpsApiRestShApiServiceDnsAddResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiServiceDnsAddRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = DNSController.createHttpsApiRestShApiServiceDnsAdd(input);
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
	app.controller("testController", function($scope, CodeObfuscationController, HttpsApiRestShApiServiceObfuscationResponseModel){
	});
```

### <a name="get_https_api_rest_sh_api_service_obfuscation"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.getHttpsApiRestShApiServiceObfuscation") getHttpsApiRestShApiServiceObfuscation

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```javascript
function getHttpsApiRestShApiServiceObfuscation(input)
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


	app.controller("testController", function($scope, CodeObfuscationController, HttpsApiRestShApiServiceObfuscationResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['app'] = 'app';
        input['contentType'] = 'Content-Type';


		var result = CodeObfuscationController.getHttpsApiRestShApiServiceObfuscation(input);
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



### <a name="create_https_api_rest_sh_api_service_obfuscation"></a>![Method: ](https://apidocs.io/img/method.png ".CodeObfuscationController.createHttpsApiRestShApiServiceObfuscation") createHttpsApiRestShApiServiceObfuscation

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API


```javascript
function createHttpsApiRestShApiServiceObfuscation(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CodeObfuscationController, HttpsApiRestShApiServiceObfuscationResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiServiceObfuscationRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = CodeObfuscationController.createHttpsApiRestShApiServiceObfuscation(input);
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
	app.controller("testController", function($scope, HostingController, HttpsApiRestShApiServiceHostingResponseModel){
	});
```

### <a name="get_https_api_rest_sh_api_service_hosting"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.getHttpsApiRestShApiServiceHosting") getHttpsApiRestShApiServiceHosting

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```javascript
function getHttpsApiRestShApiServiceHosting(input)
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


	app.controller("testController", function($scope, HostingController, HttpsApiRestShApiServiceHostingResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['app'] = 'app';
        input['domain'] = 'domain';
        input['contentType'] = 'Content-Type';


		var result = HostingController.getHttpsApiRestShApiServiceHosting(input);
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



### <a name="create_https_api_rest_sh_api_service_hosting"></a>![Method: ](https://apidocs.io/img/method.png ".HostingController.createHttpsApiRestShApiServiceHosting") createHttpsApiRestShApiServiceHosting

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting


```javascript
function createHttpsApiRestShApiServiceHosting(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, HostingController, HttpsApiRestShApiServiceHostingResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiServiceHostingRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = HostingController.createHttpsApiRestShApiServiceHosting(input);
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
	app.controller("testController", function($scope, DataManipulationConversionSortingAndCompressionAPIController, HttpsApiRestShApiDataResponseModel){
	});
```

### <a name="get_https_api_rest_sh_api_data"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.getHttpsApiRestShApiData") getHttpsApiRestShApiData

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function getHttpsApiRestShApiData(input)
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


	app.controller("testController", function($scope, DataManipulationConversionSortingAndCompressionAPIController, HttpsApiRestShApiDataResponseModel){
        var input = [];
        input['key'] = 'API';
        input['uid'] = 'UID';
        input['user'] = 'UID';
        input['apiuid'] = 'apiUID';
        input['data'] = 'https://static.yourcdn.com/data.file';
        input['contentType'] = 'application/json';


		var result = DataManipulationConversionSortingAndCompressionAPIController.getHttpsApiRestShApiData(input);
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



### <a name="create_https_api_rest_sh_api_data"></a>![Method: ](https://apidocs.io/img/method.png ".DataManipulationConversionSortingAndCompressionAPIController.createHttpsApiRestShApiData") createHttpsApiRestShApiData

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description


```javascript
function createHttpsApiRestShApiData(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DataManipulationConversionSortingAndCompressionAPIController, HttpsApiRestShApiDataResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiDataRequestModel({
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


		var result = DataManipulationConversionSortingAndCompressionAPIController.createHttpsApiRestShApiData(input);
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
	app.controller("testController", function($scope, ImageManipulationAndModerationAPIController, HttpsApiRestShApiImageResponseModel){
	});
```

### <a name="get_https_api_rest_sh_api_image"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.getHttpsApiRestShApiImage") getHttpsApiRestShApiImage

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```javascript
function getHttpsApiRestShApiImage(input)
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


	app.controller("testController", function($scope, ImageManipulationAndModerationAPIController, HttpsApiRestShApiImageResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['image'] = 'image';
        input['transform'] = 'transform';
        input['contentType'] = 'Content-Type';


		var result = ImageManipulationAndModerationAPIController.getHttpsApiRestShApiImage(input);
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



### <a name="create_https_api_rest_sh_api_image"></a>![Method: ](https://apidocs.io/img/method.png ".ImageManipulationAndModerationAPIController.createHttpsApiRestShApiImage") createHttpsApiRestShApiImage

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API


```javascript
function createHttpsApiRestShApiImage(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ImageManipulationAndModerationAPIController, HttpsApiRestShApiImageResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiImageRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = ImageManipulationAndModerationAPIController.createHttpsApiRestShApiImage(input);
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
	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVerifyAddressResponseModel, HttpsApiRestShApiVerifyUserResponseModel, HttpsApiRestShApiVerifyResponseModel){
	});
```

### <a name="get_https_api_rest_sh_api_verify_address"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVerifyAddress") getHttpsApiRestShApiVerifyAddress

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```javascript
function getHttpsApiRestShApiVerifyAddress(input)
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


	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVerifyAddressResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['a'] = 'a';
        input['sa'] = 'sa';
        input['c'] = 'c';
        input['s'] = 's';
        input['z'] = 87;
        input['contentType'] = 'Content-Type';


		var result = VerificationController.getHttpsApiRestShApiVerifyAddress(input);
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



### <a name="create_https_api_rest_sh_api_verify_address"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVerifyAddress") createHttpsApiRestShApiVerifyAddress

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API


```javascript
function createHttpsApiRestShApiVerifyAddress(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVerifyAddressResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiVerifyAddressRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = VerificationController.createHttpsApiRestShApiVerifyAddress(input);
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



### <a name="get_https_api_rest_sh_api_verify_user"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVerifyUser") getHttpsApiRestShApiVerifyUser

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```javascript
function getHttpsApiRestShApiVerifyUser(input)
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


	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVerifyUserResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['code'] = 'code';
        input['contentType'] = 'Content-Type';


		var result = VerificationController.getHttpsApiRestShApiVerifyUser(input);
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



### <a name="create_https_api_rest_sh_api_verify_user"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVerifyUser") createHttpsApiRestShApiVerifyUser

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API


```javascript
function createHttpsApiRestShApiVerifyUser(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVerifyUserResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiVerifyUserRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = VerificationController.createHttpsApiRestShApiVerifyUser(input);
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



### <a name="get_https_api_rest_sh_api_verify"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.getHttpsApiRestShApiVerify") getHttpsApiRestShApiVerify

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```javascript
function getHttpsApiRestShApiVerify(input)
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


	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVerifyResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['to'] = 'to';
        input['contentType'] = 'Content-Type';


		var result = VerificationController.getHttpsApiRestShApiVerify(input);
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



### <a name="create_https_api_rest_sh_api_verify"></a>![Method: ](https://apidocs.io/img/method.png ".VerificationController.createHttpsApiRestShApiVerify") createHttpsApiRestShApiVerify

> *Tags:*  ``` Skips Authentication ``` 

> Verification API


```javascript
function createHttpsApiRestShApiVerify(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, VerificationController, HttpsApiRestShApiVerifyResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiVerifyRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = VerificationController.createHttpsApiRestShApiVerify(input);
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
	app.controller("testController", function($scope, TwoFactorAuthenticationAPIController, HttpsApiRestShApi2faTokenResponseModel, HttpsApiRestShApi2faResponseModel){
	});
```

### <a name="get_https_api_rest_sh_api2fa_token"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2faToken") getHttpsApiRestShApi2faToken

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```javascript
function getHttpsApiRestShApi2faToken(input)
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


	app.controller("testController", function($scope, TwoFactorAuthenticationAPIController, HttpsApiRestShApi2faTokenResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['code'] = 'code';
        input['contentType'] = 'Content-Type';


		var result = TwoFactorAuthenticationAPIController.getHttpsApiRestShApi2faToken(input);
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



### <a name="create_https_api_rest_sh_api2fa_token"></a>![Method: ](https://apidocs.io/img/method.png ".TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2faToken") createHttpsApiRestShApi2faToken

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply


```javascript
function createHttpsApiRestShApi2faToken(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, TwoFactorAuthenticationAPIController, HttpsApiRestShApi2faTokenResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApi2faTokenRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = TwoFactorAuthenticationAPIController.createHttpsApiRestShApi2faToken(input);
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


	app.controller("testController", function($scope, TwoFactorAuthenticationAPIController, HttpsApiRestShApi2faResponseModel){
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


	app.controller("testController", function($scope, TwoFactorAuthenticationAPIController, HttpsApiRestShApi2faResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApi2faRequestModel({"key":"value"});
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
	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUserInfoResponseModel, HttpsApiRestShApiUserUpdateResponseModel, HttpsApiRestShApiUserDeleteResponseModel){
	});
```

### <a name="get_https_api_rest_sh_api_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUserInfo") getHttpsApiRestShApiUserInfo

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```javascript
function getHttpsApiRestShApiUserInfo(input)
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


	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUserInfoResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['apiuid'] = 'apiuid';
        input['contentType'] = 'Content-Type';


		var result = UserManagementController.getHttpsApiRestShApiUserInfo(input);
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



### <a name="create_https_api_rest_sh_api_user_info"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUserInfo") createHttpsApiRestShApiUserInfo

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API


```javascript
function createHttpsApiRestShApiUserInfo(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUserInfoResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiUserInfoRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = UserManagementController.createHttpsApiRestShApiUserInfo(input);
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



### <a name="get_https_api_rest_sh_api_user_update"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUserUpdate") getHttpsApiRestShApiUserUpdate

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```javascript
function getHttpsApiRestShApiUserUpdate(input)
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


	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUserUpdateResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['apiuid'] = 'apiuid';
        input['avatar'] = 'avatar';
        input['customInput'] = custom input;
        input['contentType'] = 'Content-Type';


		var result = UserManagementController.getHttpsApiRestShApiUserUpdate(input);
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



### <a name="create_https_api_rest_sh_api_user_update"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUserUpdate") createHttpsApiRestShApiUserUpdate

> *Tags:*  ``` Skips Authentication ``` 

> Update User API


```javascript
function createHttpsApiRestShApiUserUpdate(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUserUpdateResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiUserUpdateRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = UserManagementController.createHttpsApiRestShApiUserUpdate(input);
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



### <a name="get_https_api_rest_sh_api_user_delete"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.getHttpsApiRestShApiUserDelete") getHttpsApiRestShApiUserDelete

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```javascript
function getHttpsApiRestShApiUserDelete(input)
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


	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUserDeleteResponseModel){
        var input = [];
        input['api'] = 'api';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['apiuid'] = 'apiuid';
        input['contentType'] = 'Content-Type';


		var result = UserManagementController.getHttpsApiRestShApiUserDelete(input);
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



### <a name="create_https_api_rest_sh_api_user_delete"></a>![Method: ](https://apidocs.io/img/method.png ".UserManagementController.createHttpsApiRestShApiUserDelete") createHttpsApiRestShApiUserDelete

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API


```javascript
function createHttpsApiRestShApiUserDelete(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserManagementController, HttpsApiRestShApiUserDeleteResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiUserDeleteRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = UserManagementController.createHttpsApiRestShApiUserDelete(input);
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
	app.controller("testController", function($scope, LoginAndRegistrationController, HttpsApiRestShApiAuthUserRegisterResponseModel, HttpsApiRestShApiAuthUserLoginResponseModel){
	});
```

### <a name="get_https_api_rest_sh_api_auth_user_register"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAuthUserRegister") getHttpsApiRestShApiAuthUserRegister

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```javascript
function getHttpsApiRestShApiAuthUserRegister(input)
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


	app.controller("testController", function($scope, LoginAndRegistrationController, HttpsApiRestShApiAuthUserRegisterResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['password'] = 'password';
        input['name'] = 'name';
        input['email'] = 'email';
        input['phone'] = 87;
        input['countrycode'] = 87;
        input['address'] = 'address';
        input['contentType'] = 'Content-Type';


		var result = LoginAndRegistrationController.getHttpsApiRestShApiAuthUserRegister(input);
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



### <a name="create_https_api_rest_sh_api_auth_user_register"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAuthUserRegister") createHttpsApiRestShApiAuthUserRegister

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API


```javascript
function createHttpsApiRestShApiAuthUserRegister(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, LoginAndRegistrationController, HttpsApiRestShApiAuthUserRegisterResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiAuthUserRegisterRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = LoginAndRegistrationController.createHttpsApiRestShApiAuthUserRegister(input);
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



### <a name="get_https_api_rest_sh_api_auth_user_login"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.getHttpsApiRestShApiAuthUserLogin") getHttpsApiRestShApiAuthUserLogin

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```javascript
function getHttpsApiRestShApiAuthUserLogin(input)
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


	app.controller("testController", function($scope, LoginAndRegistrationController, HttpsApiRestShApiAuthUserLoginResponseModel){
        var input = [];
        input['key'] = 'key';
        input['uid'] = 'uid';
        input['user'] = 'user';
        input['password'] = 'password';
        input['contentType'] = 'Content-Type';


		var result = LoginAndRegistrationController.getHttpsApiRestShApiAuthUserLogin(input);
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



### <a name="create_https_api_rest_sh_api_auth_user_login"></a>![Method: ](https://apidocs.io/img/method.png ".LoginAndRegistrationController.createHttpsApiRestShApiAuthUserLogin") createHttpsApiRestShApiAuthUserLogin

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API


```javascript
function createHttpsApiRestShApiAuthUserLogin(input)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, LoginAndRegistrationController, HttpsApiRestShApiAuthUserLoginResponseModel){
        var input = [];
        input['body'] = new HttpsApiRestShApiAuthUserLoginRequestModel({"key":"value"});
        input['contentType'] = 'Content-Type';


		var result = LoginAndRegistrationController.createHttpsApiRestShApiAuthUserLogin(input);
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



