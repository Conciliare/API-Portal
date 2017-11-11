# 

**`API Version:`** `1.19`

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



## Server Configuration for Base URLs

This section provides details on the environments available and lists down the servers in each of the environment. The default environment for this API is set to `Production` while the default server is set to `PATH`.
### Environments

An environment consists of a set of servers with base URL values. The environment can be changed programatically allowing rapid switching between different environments e.g.the user can specify a Production and Testing Environment.The available environments for this API are: 

#### Production
> Production Enviroment

This environment comprises of the following servers: 

| Name | Base URL | 
|-----------|-------------|
| PATH | https://api.rest.sh/api |

#### Sandbox
> Testing and Debugging

This environment comprises of the following servers: 

| Name | Base URL | 
|-----------|-------------|
| PATH | https://sb.rest.sh/api |

#### Beta
> Updated Nightly (May Contain Bugs)

This environment comprises of the following servers: 

| Name | Base URL | 
|-----------|-------------|
| PATH | https://b.rest.sh/api |




## Authentication
This API uses `custom authentication`.



### Authentication Parameters

The parameters required for authentication are listed below:

| Parameter | Description | Example | 
|-----------|-------------| ------- |
| uid | Your user ID | `"UID"` |
| secret | Your Private API Key | `"SECRET"` |
| key | Your Public API Key | `"KEY"` |



## Global API Errors
Global API errors are applied across all endpoints.

**400** 
> Bad Request


**401** 
> Incorrect Credentials


**403** 
> Forbidden


**406** 
> Not Acceptable Input


**409** 
> Data Conflict


**413** 
> Payload Too Large


**415** 
> Un-Supported Content Type


**451** 
> Un-Available For Legal Reasons


**500** 
> Internal API Error


**501** 
> Not Implemented


**503** 
> API Unavailable


**504** 
> Request Timeout


**511** 
> Authentication Required





# <a name="api_reference"></a>API Reference

* [Advanced Logging](#advanced_logging)
* [WAF and DDOS Protection](#waf_and_ddos_protection)
* [Encryption](#encryption)
* [CDN](#cdn)
* [DNS](#dns)
* [Code Obfuscation](#code_obfuscation)
* [Hosting](#hosting)
* [Data Manipulation](#data_manipulation)
* [Image Manipulation](#image_manipulation)
* [Verification](#verification)
* [Two Factor Authentication API](#two_factor_authentication_api)
* [User Management](#user_management)
* [Login and Registration](#login_and_registration)

## <a name="advanced_logging"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Advanced Logging") Advanced Logging


### <a name="logging_configuration"></a>![Endpoint: ](https://apidocs.io/img/method.png "Logging Configuration") Logging Configuration


**`GET`** `/s/l`

> WAF Log Configuration


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| name | string |  ``` Required ```  | Name of the WAF zone | `origin-name` | 
| origin | string |  ``` Required ```  | IP Address of the Web Application you wish to configure logging on | `origin.yourdomain.tld` | 
| activate | string |  ``` Required ```  | Activate or Disable | `"activate"` | 

#### Responses
**200** 


 *Example Body* (**[Logging Setup Model Response](#logging_setup_model_response)**) 

```
{
  "success": "RETURNS TRUE IF ADVANCED LOGGING IS ACTIVATED"
}
```


### <a name="logging_info"></a>![Endpoint: ](https://apidocs.io/img/method.png "Logging Info") Logging Info


**`GET`** `/s/l/i`

> WAF Log Info


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| name | string |  ``` Required ```  | Name of your WAF zone | `origin-name` | 
| origin | string |  ``` Required ```  | IP Address of the Web Application | `origin.yourdomain.tld` | 
| time | string |  ``` Optional ```  | Specific times or dates to lookup separated by a comma in MMDDYYHHMMSS Format ( Month Month Day Day Year Year Year Hour Hour Minute Minute Second Second [01/01/0101;24:59:01]) | `01/01/0101;24:59:01` | 

#### Responses
**200** 


 *Example Body* (**[Logging Logs Model Response](#logging_logs_model_response)**) 

```
{
  "log": {
    "01010101245901": {
      "data": {
        "result": "INFO",
        "content": "LOG: CONTENT AND ACTIONS PERFORMED",
        "id": "FUNCTION ID"
      }
    },
    "01010101245902": {
      "data": {
        "result": "ERROR",
        "content": "LOG: ERROR CONTENT AND ACTIONS PERFORMED",
        "id": "FUNCTION ID"
      }
    }
  }
}
```


[Back to API Reference](#api_reference)

## <a name="waf_and_ddos_protection"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "WAF and DDOS Protection") WAF and DDOS Protection


### <a name="waf_configuration"></a>![Endpoint: ](https://apidocs.io/img/method.png "WAF Configuration") WAF Configuration


**`GET`** `/s/w/c`

> WAF and DDOS Configuration


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| name | string |  ``` Required ```  | Name of your WAF zone | `origin-name` | 
| rule | string |  ``` Required ```  | Rule or rules to add or update separated by a comma | `header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does` | 

#### Responses
**200** 


 *Example Body* (**[WAF Configuration Model Response](#waf_configuration_model_response)**) 

```
{
  "success": "SHOWS TRUE WHEN THE WAF AND ORIGIN SHIELD (DDOS PROTECTION) IS DEPLOYED SUCCESSFULLY",
  "rule": "RULES APPLIED TO WAF"
}
```


### <a name="waf_creation"></a>![Endpoint: ](https://apidocs.io/img/method.png "WAF Creation") WAF Creation


**`GET`** `/s/w`

> WAF and DDOS Creation


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| origin | string |  ``` Required ```  | IP of the Web server you wish to protect | `origin.yourdomain.tld` | 
| cname | string |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access | `yourdomain.tld,www.yourdomain.tld` | 

#### Responses
**200** 


 *Example Body* (**[WAF Creation Model Response](#waf_creation_model_response)**) 

```
{
  "success": "SHOWS TRUE WHEN THE WAF AND ORIGIN SHIELD (DDOS PROTECTION) IS DEPLOYED SUCCESSFULLY",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```


[Back to API Reference](#api_reference)

## <a name="encryption"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Encryption") Encryption


### <a name="data_and_file_encryption"></a>![Endpoint: ](https://apidocs.io/img/method.png "Data and File Encryption") Data and File Encryption


**`GET`** `/s/e`

> Data and File Encryption API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| data | string |  ``` Required ```  | GIT URL, file URL, direct upload of file, or data as a query string | `DATA` | 
| method | string |  ``` Required ```  | Single or multiple encryption types to apply to data or files separated by a comma (DES, RSA, BLOWFISH, TWOFISH, AES, IDEA, PGP) | `DES,RSA` | 
| bit | number |  ``` Required ```  | Encryption key size (4096) | `4096` | 

#### Responses
**200** 


 *Example Body* (**[Encryption Model Response](#encryption_model_response)**) 

```
{
  "data": "RETURNED ENCRYPTED DATA URL",
  "file": "RETURNED ENCRYPTED FILE URL",
  "success": "SHOWS TRUE IF ENCRYPTION WAS SUCCESSFULL",
  "public": "PUBLIC ENCRYPTION KEY FOR YOUR DATA OR FILES",
  "private": "PRIVATE ENCRYPTION KEY FOR YOUR DATA OR FILES"
}
```


[Back to API Reference](#api_reference)

## <a name="cdn"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "CDN") CDN


### <a name="cdn_push_zone"></a>![Endpoint: ](https://apidocs.io/img/method.png "CDN Push Zone") CDN Push Zone


**`GET`** `/s/c/push`

> CDN Push Zone API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| cname | string |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access | `cdn.yourdomain.tld,cdn1.yourdomain.tld,cdn2.yourdomain.tld` | 
| file | string |  ``` Required ```  | GIT URL, file URL, or direct upload of file | `static.yourdomain.tld/file.type` | 

#### Responses
**200** 


 *Example Body* (**[CDN Push Model Response](#cdn_push_model_response)**) 

```
{
  "success": "SHOWS TRUE WHEN PUSH ZONE IS DEPLOYED SUCCESSFULLY",
  "upload": "LIST OF FILES UPLOADED TO YOUR PUSH ZONE",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```


### <a name="cdn_pull_zone"></a>![Endpoint: ](https://apidocs.io/img/method.png "CDN Pull Zone") CDN Pull Zone


**`GET`** `/s/c/pull`

> CDN Pull Zone API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| origin | string |  ``` Required ```  | Domain or domain names separated by a comma | `origin.yourdomain.tld` | 
| cname | string |  ``` Required ```  | Domain or domain names separated by a comma you wish to allow CNAME access | `cdn.yourdomain.tld,cdn1.yourdomain.tld,cdn2.yourdomain.tld` | 

#### Responses
**200** 


 *Example Body* (**[CDN Pull Model Response](#cdn_pull_model_response)**) 

```
{
  "success": "SHOWS TRUE WHEN PULL ZONE IS DEPLOYED SUCCESSFULLY",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```


[Back to API Reference](#api_reference)

## <a name="dns"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "DNS") DNS


### <a name="dns_configuration"></a>![Endpoint: ](https://apidocs.io/img/method.png "DNS Configuration") DNS Configuration


**`GET`** `/s/d/c`

> DNS Configuration API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| domain | string |  ``` Required ```  | Domain or domain names separated by a comma | `yourdomain.tld` | 
| records | string |  ``` Required ```  | Records to append to domain separated by a comma (a;www.mydomain.com;127.0.0.0,cname;mydomain.com;otherdomain.com) | `set:root:a:127.0.0.1,set:www:a:127.0.0.1,set:cdn:cname:cname.domain.com` | 

#### Responses
**200** 


 *Example Body* (**[DNS Configuration Model Response](#dns_configuration_model_response)**) 

```
{
  "success": "SHOWS TRUE IF RECORDS WERE SUCCESSFULLY SET",
  "domain": "DOMAIN",
  "records": "RECORDS SET TO DOMAIN"
}
```


### <a name="dns_creation"></a>![Endpoint: ](https://apidocs.io/img/method.png "DNS Creation") DNS Creation


**`GET`** `/s/d/a`

> DNS Creation API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| domain | string |  ``` Required ```  | Domain or domain names separated by a comma | `yourdomain.tld,seconddomain.tld` | 

#### Responses
**200** 


 *Example Body* (**[DNS Creation Model Response](#dns_creation_model_response)**) 

```
{
  "domain": "LIST OF DOMAINS ADDED",
  "nameservers": {
    "ns1": "NAME SERVER ONE TO POINT YOUR DOMAIN AT",
    "ns2": "NAME SERVER TWO TO POINT YOUR DOMAIN AT",
    "ns3": "NAME SERVER THREE TO POINT YOUR DOMAIN AT",
    "ns4": "NAME SERVER FOUR TO POINT YOUR DOMAIN AT"
  }
}
```


[Back to API Reference](#api_reference)

## <a name="code_obfuscation"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Code Obfuscation") Code Obfuscation


### <a name="obfuscation_and_anti_tampering"></a>![Endpoint: ](https://apidocs.io/img/method.png "Obfuscation and Anti-Tampering") Obfuscation and Anti-Tampering


**`GET`** `/s/o`

> Javascript and Node.JS Obfuscation and Anti-Tampering API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| app | string |  ``` Required ```  | GIT URL or ZIP package containing your APP | `git://app.git` | 

#### Responses
**200** 


 *Example Body* (**[Code Protection Model Response](#code_protection_model_response)**) 

```
{
  "success": "RETURNS TRUE IF APP WAS SUCCESSFULLY OBFUSCTATED AND PROTECTED",
  "app": "OBFUSCATED APP URL"
}
```


[Back to API Reference](#api_reference)

## <a name="hosting"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Hosting") Hosting


### <a name="hosting_setup"></a>![Endpoint: ](https://apidocs.io/img/method.png "Hosting Setup") Hosting Setup


**`GET`** `/s/h`

> Node.JS and Static Web APP Hosting


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| app | string |  ``` Required ```  | GIT URL or ZIP package containing your APP | `git://app.git` | 
| domain | string |  ``` Required ```  | Domain or domain names separated by a comma | `yourdomain.tld,seconddomain.tld` | 

#### Responses
**200** 


 *Example Body* (**[Hosting Model Response](#hosting_model_response)**) 

```
{
  "request": "REQUEST TYPE",
  "url": "RETURNED APP HOSTING URL",
  "success": "RETURNS TRUE IF APP WAS SUCCESSFULLY DEPLOYED",
  "id": "TRANSACTION ID"
}
```


[Back to API Reference](#api_reference)

## <a name="data_manipulation"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Data Manipulation") Data Manipulation


### <a name="https://api.rest.sh/api/d"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/d") https://api.rest.sh/api/d


**`GET`** `/d`

> Data Manipulation API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| data | string |  ``` Required ```  | Data URL, data as a query string, or direct upload | `https://static.yourcdn.com/data.file` | 
| transform | string |  ``` Required ```  | Transformations to perform | `"transform"` | 

#### Responses
**200** 


 *Example Body* (**[Data Manipulation Model Response](#data_manipulation_model_response)**) 

```
{
  "request": "REQUEST TYPE",
  "url": "RETURNED DATA URL",
  "success": "RETURNS TRUE IF DATA MANIPULATION WAS SUCCESSFULL",
  "id": "TRANSACTION ID"
}
```


[Back to API Reference](#api_reference)

## <a name="image_manipulation"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Image Manipulation") Image Manipulation


### <a name="image_manipulation"></a>![Endpoint: ](https://apidocs.io/img/method.png "Image Manipulation") Image Manipulation


**`GET`** `/i`

> Image Manipulation API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| image | string |  ``` Required ```  | Image URL or direct upload | `https://img.yourdomain.tld/image.type` | 
| transform | string |  ``` Required ```  | Transformations to perform | `x:flip,y:flip,grayscale:true,compress:true;80,convert:png` | 

#### Responses
**200** 


 *Example Body* (**[Image Manipulation Model Response](#image_manipulation_model_response)**) 

```
{
  "request": "REQUEST TYPE",
  "url": "RETURNED IMAGE URL AND DATA",
  "success": "RETURNS TRUE IF IMAGE MANIPULATION WAS SUCCESSFULL",
  "moderated": "RETURNS TRUE IF IMAGE CONTAINED GRAPHIC IMAGERY",
  "id": "TRANSACTION ID"
}
```


[Back to API Reference](#api_reference)

## <a name="verification"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Verification") Verification


### <a name="user_address_verification"></a>![Endpoint: ](https://apidocs.io/img/method.png "User Address Verification") User Address Verification


**`GET`** `/v/a`

> User Address Verification API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| user | string |  ``` Required ```  | Users UID, Username, or Email | `UID` | 
| a | string |  ``` Required ```  | Address Line One | `3301 South Greenfield Rd` | 
| sa | string |  ``` Required ```  | Address Line Two | `Address Line Two` | 
| c | string |  ``` Required ```  | Address City | `Gilbert` | 
| s | string |  ``` Required ```  | Address State or Province | `AZ` | 
| z | number |  ``` Required ```  | Address Zipcode | `85297` | 
| address | string |  ``` Optional ```  | Address as a one line input separated by commas | `"address"` | 

#### Responses
**200** 


 *Example Body* (**[Verify Address Response](#verify_address_response)**) 

```
{
  "request": "REQUEST TYPE",
  "active": "RETURNS TRUE, IF ADDRESS IS ACTIVE AND IF USER IS CURRENTLY THERE",
  "id": "TRANSACTION ID"
}
```


### <a name="user_verification_response"></a>![Endpoint: ](https://apidocs.io/img/method.png "User Verification Response") User Verification Response


**`GET`** `/v/u`

> Users Verification Response API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| user | string |  ``` Required ```  | Users UID, Username, Or Email | `UID` | 
| code | string |  ``` Required ```  | Verification code entered by the user | `CODE` | 

#### Responses
**200** 


 *Example Body* (**[Verify User Model Response](#verify_user_model_response)**) 

```
{
  "request": "REQUEST TYPE",
  "correct": "RETURNS IF 2FA TOKEN IS CORRECT",
  "id": "TRANSACTION ID"
}
```


### <a name="user_verification"></a>![Endpoint: ](https://apidocs.io/img/method.png "User Verification") User Verification


**`GET`** `/v`

> User Verification API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| user | string |  ``` Required ```  | Users UID, Username, Or Email | `UID` | 

#### Responses
**200** 


 *Example Body* (**[Verify Model Response](#verify_model_response)**) 

```
{
  "request": "REQUEST TYPE",
  "to": "USER BEING VERIFIED",
  "verified": "RETURNS TRUE OR FALSE",
  "id": "TRANSACTION ID"
}
```


[Back to API Reference](#api_reference)

## <a name="two_factor_authentication_api"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Two Factor Authentication API") Two Factor Authentication API


### <a name="2_fa_token_response"></a>![Endpoint: ](https://apidocs.io/img/method.png "2FA Token Response") 2FA Token Response


**`GET`** `/2fa/t`

> Two Factor Authentication Token Reply


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| user | string |  ``` Required ```  | Users UID, Username or Email | `UID` | 
| code | string |  ``` Required ```  | Response From User Containing 2FA Code | `CODE` | 

#### Responses
**200** 


 *Example Body* (**[Two Factor Authentication Token Model Response](#two_factor_authentication_token_model_response)**) 

```
{
  "request": "REQUEST TYPE",
  "correct": "RETURNS IF 2FA TOKEN IS CORRECT",
  "id": "TRANSACTION ID"
}
```


### <a name="two_factor_authentication"></a>![Endpoint: ](https://apidocs.io/img/method.png "Two Factor Authentication") Two Factor Authentication


**`GET`** `/2fa`

> Two Factor Authentication API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| to | string |  ``` Required ```  | Users UID, Username, Email, Or Cellphone number | `UID` | 

#### Responses
**200** 


 *Example Body* (**[Two Factor Authentication Model Response](#two_factor_authentication_model_response)**) 

```
{
  "request": "REQUEST TYPE",
  "to": "USER BEING VERIFIED",
  "verified": "RETURNS TRUE OR FALSE",
  "id": "TRANSACTION ID"
}
```


[Back to API Reference](#api_reference)

## <a name="user_management"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "User Management") User Management


### <a name="get_user_info"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get User Info") Get User Info


**`GET`** `/u/i`

> Get User Info API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| user | string |  ``` Required ```  | Users User ID | `UID` | 

#### Responses
**200** 


 *Example Body* (**[User Information Model Response](#user_information_model_response)**) 

```
{
  "request": "REQUEST TYPE",
  "uid": "Users UID",
  "apiuid": "API SIDE USER ID",
  "verified": "RETURNS TRUE IF USER IS VERIFIED",
  "id": "TRANSACTION ID",
  "info": {
    "realname": "USERS REAL NAME",
    "displayname": "USERS USERNAME",
    "avatar": "USER AVATAR URL",
    "email": "USERS EMAIL",
    "address": "USERS ADDRESS IN ONE LINE SEPERATED BY COMMAS",
    "address1": "USERS ADDRESS LINE ONE",
    "address2": "USERS ADDRESS LINE TWO",
    "city": "USERS ADDRESS CITY",
    "state": "USERS ADDRESS STATE",
    "zipcode": "USERS ADDRESS ZIPCODE",
    "phone": "USERS CELL PHONE NUMBER",
    "lastlogin": "USERS LAST LOGIN",
    "ip": "USERS IP",
    "2fa": "RETURNS TRUE IF 2FA IS ENABLED",
    "iplock": "RETURNS TRUE IF IP LOCK IS ENABLED"
  }
}
```


### <a name="update_user"></a>![Endpoint: ](https://apidocs.io/img/method.png "Update User") Update User


**`GET`** `/u/u`

> Update User API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
> Additional optional query parameters are allowed

| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| user | string |  ``` Required ```  | Users UID, Username, Or Email | `UID` | 
| avatar | string |  ``` Required ```  | Avatar Image URL | `https://img.cdnurl.com/UID/image` | 
| custom input | string |  ``` Required ```  | Custom input variable for users profile | `custom input` | 

#### Responses
**200** 


 *Example Body* (**[User Update Model Response](#user_update_model_response)**) 

```
{
  "request": "REQUEST TYPE",
  "updated": "RETURNS TRUE, IF USERS PROFILE WAS SUCCESSFULLY UPDATED",
  "id": "TRANSACTION ID",
  "info": {
    "uid": "USERS ID",
    "apiuid": "API SIDE USER ID",
    "avatar": "INPUTTED AVATAR URL",
    "custom-input": "CUSTOM INPUTTED PROFILE DATA"
  }
}
```


### <a name="delete_user"></a>![Endpoint: ](https://apidocs.io/img/method.png "Delete User") Delete User


**`GET`** `/u/d`

> Delete User API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| user | string |  ``` Required ```  | Users UID, Username, or Email | `UID` | 

#### Responses
**200** 


 *Example Body* (**[User Deletion Response Model](#user_deletion_response_model)**) 

```
{
  "request": "REQUEST TYPE",
  "deleted": "RETURNS TRUE, IF USERS ACCOUNT WAS SUCCESSFULLY DELETED",
  "id": "TRANSACTION ID"
}
```


[Back to API Reference](#api_reference)

## <a name="login_and_registration"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Login and Registration") Login and Registration


### <a name="user_registration"></a>![Endpoint: ](https://apidocs.io/img/method.png "User Registration") User Registration


**`GET`** `/a/u/r`

> User Registration API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
> Additional optional query parameters are allowed

| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| email | string |  ``` Required ```  | Users Email | `email@email.com` | 
| user | string |  ``` Required ```  | Users Username | `UID` | 
| password | string |  ``` Required ```  | Users Password | `Password` | 
| name | string |  ``` Optional ```  | Users Name | `John Doe` | 
| phone | number |  ``` Optional ```  | Users Cellphone Number | `1234567890` | 
| countrycode | number |  ``` Optional ```  | Users Country Code (US = 1) | `1` | 
| address | string |  ``` Optional ```  | Users Address | `3301 South Greenfield Rd, Gilbert, AZ 85297` | 

#### Responses
**200** 


 *Example Body* (**[User Registration Model Response](#user_registration_model_response)**) 

```
{
  "request": "REQUEST TYPE",
  "active": "RETURNS TRUE, IF USER WAS SUCCESSFULLY REGISTERED",
  "id": "TRANSACTION ID",
  "info": {
    "uid": "USERS ID",
    "apiuid": "API SIDE USER ID",
    "realname": "USERS REAL NAME",
    "displayname": "USERS USERNAME",
    "email": "USERS EMAIL",
    "address": "USERS ADDRESS",
    "phone": "USERS CELL PHONE NUMBER"
  }
}
```


### <a name="user_authentication"></a>![Endpoint: ](https://apidocs.io/img/method.png "User Authentication") User Authentication


**`GET`** `/a/u/l`

> User Authentication API


#### Base URL
This endpoint uses server `PATH`.


#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| user | string |  ``` Required ```  | Users Username or Email | `Username` | 
| password | string |  ``` Required ```  | Users Password | `Password` | 

#### Responses
**200** 


 *Example Body* (**[User Authentication Model Response](#user_authentication_model_response)**) 

```
{
  "request": "REQUEST TYPE",
  "uid": "Users UID",
  "valid": "RETURNS TRUE IF USER LOGIN DETAILS ARE VALID",
  "id": "TRANSACTION ID",
  "info": {
    "uid": "USERS ID",
    "apiuid": "API SIDE USER ID",
    "realname": "USERS REAL NAME",
    "displayname": "USERS USERNAME",
    "avatar": "USER AVATAR URL",
    "email": "USERS EMAIL",
    "address": "USERS ADDRESS",
    "phone": "USERS CELL PHONE NUMBER",
    "lastlogin": "USERS LAST LOGIN",
    "ip": "USERS IP",
    "2fa": "RETURNS TRUE IF 2FA IS ENABLED",
    "iplock": "RETURNS TRUE IF IP LOCK IS ENABLED"
  }
}
```


[Back to API Reference](#api_reference)

# <a name="models"></a> Models

### List of Models

* [MMDDYYYYHHMMSS Model](#mmddyyyyhhmmss_model)
* [Logging Logs Model Response](#logging_logs_model_response)
* [Logging Setup Model Response](#logging_setup_model_response)
* [Data Manipulation Model](#data_manipulation_model)
* [Verify Address](#verify_address)
* [User Information Model](#user_information_model)
* [User Update Model](#user_update_model)
* [User Registration Model](#user_registration_model)
* [Info Model](#info_model)
* [Logging Logs Model](#logging_logs_model)
* [Logging Setup Model](#logging_setup_model)
* [WAF Configuration Model](#waf_configuration_model)
* [WAF Creation Model](#waf_creation_model)
* [Encryption Model Response](#encryption_model_response)
* [Encryption Model](#encryption_model)
* [CDN Push Model](#cdn_push_model)
* [CDN Pull Model](#cdn_pull_model)
* [DNS Configuration Model](#dns_configuration_model)
* [Nameservers Model](#nameservers_model)
* [Hosting Model Response](#hosting_model_response)
* [Hosting Model](#hosting_model)
* [Data Manipulation Model Response](#data_manipulation_model_response)
* [Image Manipulation Model Response](#image_manipulation_model_response)
* [Image Manipulation Model](#image_manipulation_model)
* [Two Factor Authentication Token Model](#two_factor_authentication_token_model)
* [Two Factor Authentication Model](#two_factor_authentication_model)
* [Verify User Model](#verify_user_model)
* [Verify Model Response](#verify_model_response)
* [User Deletion Model](#user_deletion_model)
* [User Information Model Response](#user_information_model_response)
* [User Information Secondary Model](#user_information_secondary_model)
* [User Custom Update Model](#user_custom_update_model)
* [User Update Model Response](#user_update_model_response)
* [User Profile Information Model](#user_profile_information_model)
* [User Registration Model Response](#user_registration_model_response)
* [User Authentication Model Response](#user_authentication_model_response)
* [User Authentication Model](#user_authentication_model)
* [Data Model](#data_model)
* [Log Model](#log_model)
* [WAF Configuration Model Response](#waf_configuration_model_response)
* [WAF Creation Model Response](#waf_creation_model_response)
* [Code Protection Model Response](#code_protection_model_response)
* [Code Protection Model](#code_protection_model)
* [CDN Push Model Response](#cdn_push_model_response)
* [CDN Pull Model Response](#cdn_pull_model_response)
* [DNS Configuration Model Response](#dns_configuration_model_response)
* [DNS Creation Model Response](#dns_creation_model_response)
* [DNS Creation Model](#dns_creation_model)
* [Two Factor Authentication Token Model Response](#two_factor_authentication_token_model_response)
* [Two Factor Authentication Model Response](#two_factor_authentication_model_response)
* [Verify Address Response](#verify_address_response)
* [Verify User Model Response](#verify_user_model_response)
* [Verify Model](#verify_model)
* [User Deletion Response Model](#user_deletion_response_model)
## <a name="mmddyyyyhhmmss_model"></a>![Type: ](https://apidocs.io/img/method.png "MMDDYYYYHHMMSS Model") MMDDYYYYHHMMSS Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| data | [Data Model](#data_model) |  ``` Required ```  | - | 



#### Example
```
{
  "data": {
    "result": "result",
    "content": "content",
    "id": "id"
  }
}
```



## <a name="logging_logs_model_response"></a>![Type: ](https://apidocs.io/img/method.png "Logging Logs Model Response") Logging Logs Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| log | [Log Model](#log_model) |  ``` Required ```  | - | 



#### Example
```
{
  "log": {
    "01010101245901": {
      "data": {
        "result": "INFO",
        "content": "LOG: CONTENT AND ACTIONS PERFORMED",
        "id": "FUNCTION ID"
      }
    },
    "01010101245902": {
      "data": {
        "result": "ERROR",
        "content": "LOG: ERROR CONTENT AND ACTIONS PERFORMED",
        "id": "FUNCTION ID"
      }
    }
  }
}
```



## <a name="logging_setup_model_response"></a>![Type: ](https://apidocs.io/img/method.png "Logging Setup Model Response") Logging Setup Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | - | 



#### Example
```
{
  "success": "RETURNS TRUE IF ADVANCED LOGGING IS ACTIVATED"
}
```



## <a name="data_manipulation_model"></a>![Type: ](https://apidocs.io/img/method.png "Data Manipulation Model") Data Manipulation Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| user | string |  ``` Required ```  | - | 
| apiuid | string |  ``` Required ```  | - | 
| url | string |  ``` Required ```  | - | 
| manipulation | string |  ``` Required ```  | - | 
| conversion | string |  ``` Required ```  | - | 
| sorting | string |  ``` Required ```  | - | 
| compression | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "user": "user",
  "apiuid": "apiuid",
  "url": "url",
  "manipulation": "manipulation",
  "conversion": "conversion",
  "sorting": "sorting",
  "compression": "compression"
}
```



## <a name="verify_address"></a>![Type: ](https://apidocs.io/img/method.png "Verify Address") Verify Address








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| user | string |  ``` Required ```  | - | 
| address | string |  ``` Required ```  | - | 
| a | string |  ``` Required ```  | - | 
| sa | string |  ``` Required ```  | - | 
| c | string |  ``` Required ```  | - | 
| s | string |  ``` Required ```  | - | 
| z | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "user": "user",
  "address": "address",
  "a": "a",
  "sa": "sa",
  "c": "c",
  "s": "s",
  "z": "z"
}
```



## <a name="user_information_model"></a>![Type: ](https://apidocs.io/img/method.png "User Information Model") User Information Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| realname | string |  ``` Required ```  | - | 
| displayname | string |  ``` Required ```  | - | 
| avatar | string |  ``` Required ```  | - | 
| email | string |  ``` Required ```  | - | 
| address | string |  ``` Required ```  | - | 
| address1 | string |  ``` Required ```  | - | 
| address2 | string |  ``` Required ```  | - | 
| city | string |  ``` Required ```  | - | 
| state | string |  ``` Required ```  | - | 
| zipcode | string |  ``` Required ```  | - | 
| phone | string |  ``` Required ```  | - | 
| lastlogin | string |  ``` Required ```  | - | 
| ip | string |  ``` Required ```  | - | 
| 2fa | string |  ``` Required ```  | - | 
| iplock | string |  ``` Required ```  | - | 



#### Example
```
{
  "realname": "realname",
  "displayname": "displayname",
  "avatar": "avatar",
  "email": "email",
  "address": "address",
  "address1": "address1",
  "address2": "address2",
  "city": "city",
  "state": "state",
  "zipcode": "zipcode",
  "phone": "phone",
  "lastlogin": "lastlogin",
  "ip": "ip",
  "2fa": "2fa",
  "iplock": "iplock"
}
```



## <a name="user_update_model"></a>![Type: ](https://apidocs.io/img/method.png "User Update Model") User Update Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| user | string |  ``` Required ```  | - | 
| apiuid | string |  ``` Required ```  | - | 
| oldpassword | string |  ``` Required ```  | - | 
| newpassword | string |  ``` Required ```  | - | 
| name | string |  ``` Required ```  | - | 
| email | string |  ``` Required ```  | - | 
| phone | string |  ``` Required ```  | - | 
| avatar | string |  ``` Required ```  | - | 
| countrycode | string |  ``` Required ```  | - | 
| address | string |  ``` Required ```  | - | 
| a | string |  ``` Required ```  | - | 
| sa | string |  ``` Required ```  | - | 
| c | string |  ``` Required ```  | - | 
| s | string |  ``` Required ```  | - | 
| z | string |  ``` Required ```  | - | 
| custom-input | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "user": "user",
  "apiuid": "apiuid",
  "oldpassword": "oldpassword",
  "newpassword": "newpassword",
  "name": "name",
  "email": "email",
  "phone": "phone",
  "avatar": "avatar",
  "countrycode": "countrycode",
  "address": "address",
  "a": "a",
  "sa": "sa",
  "c": "c",
  "s": "s",
  "z": "z",
  "custom-input": "custom-input"
}
```



## <a name="user_registration_model"></a>![Type: ](https://apidocs.io/img/method.png "User Registration Model") User Registration Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| user | string |  ``` Required ```  | - | 
| password | string |  ``` Required ```  | - | 
| name | string |  ``` Required ```  | - | 
| email | string |  ``` Required ```  | - | 
| phone | string |  ``` Required ```  | - | 
| countrycode | string |  ``` Required ```  | - | 
| address | string |  ``` Required ```  | - | 
| a | string |  ``` Required ```  | - | 
| sa | string |  ``` Required ```  | - | 
| c | string |  ``` Required ```  | - | 
| s | string |  ``` Required ```  | - | 
| z | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "user": "user",
  "password": "password",
  "name": "name",
  "email": "email",
  "phone": "phone",
  "countrycode": "countrycode",
  "address": "address",
  "a": "a",
  "sa": "sa",
  "c": "c",
  "s": "s",
  "z": "z"
}
```



## <a name="info_model"></a>![Type: ](https://apidocs.io/img/method.png "Info Model") Info Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| uid | string |  ``` Required ```  | - | 
| apiuid | string |  ``` Required ```  | - | 
| realname | string |  ``` Required ```  | - | 
| displayname | string |  ``` Required ```  | - | 
| avatar | string |  ``` Required ```  | - | 
| email | string |  ``` Required ```  | - | 
| address | string |  ``` Required ```  | - | 
| phone | string |  ``` Required ```  | - | 
| lastlogin | string |  ``` Required ```  | - | 
| ip | string |  ``` Required ```  | - | 
| 2fa | string |  ``` Required ```  | - | 
| iplock | string |  ``` Required ```  | - | 



#### Example
```
{
  "uid": "uid",
  "apiuid": "apiuid",
  "realname": "realname",
  "displayname": "displayname",
  "avatar": "avatar",
  "email": "email",
  "address": "address",
  "phone": "phone",
  "lastlogin": "lastlogin",
  "ip": "ip",
  "2fa": "2fa",
  "iplock": "iplock"
}
```



## <a name="logging_logs_model"></a>![Type: ](https://apidocs.io/img/method.png "Logging Logs Model") Logging Logs Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| name | string |  ``` Required ```  | - | 
| origin | string |  ``` Required ```  | - | 
| time | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "name": "name",
  "origin": "origin",
  "time": "time"
}
```



## <a name="logging_setup_model"></a>![Type: ](https://apidocs.io/img/method.png "Logging Setup Model") Logging Setup Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| name | string |  ``` Required ```  | - | 
| origin | string |  ``` Required ```  | - | 
| activate | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "name": "name",
  "origin": "origin",
  "activate": "activate"
}
```



## <a name="waf_configuration_model"></a>![Type: ](https://apidocs.io/img/method.png "WAF Configuration Model") WAF Configuration Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| name | string |  ``` Required ```  | - | 
| origin | string |  ``` Required ```  | - | 
| cname | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "name": "name",
  "origin": "origin",
  "cname": "cname"
}
```



## <a name="waf_creation_model"></a>![Type: ](https://apidocs.io/img/method.png "WAF Creation Model") WAF Creation Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| origin | string |  ``` Required ```  | - | 
| cname | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "origin": "origin",
  "cname": "cname"
}
```



## <a name="encryption_model_response"></a>![Type: ](https://apidocs.io/img/method.png "Encryption Model Response") Encryption Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| data | string |  ``` Required ```  | - | 
| file | string |  ``` Required ```  | - | 
| success | string |  ``` Required ```  | - | 
| public | string |  ``` Required ```  | - | 
| private | string |  ``` Required ```  | - | 



#### Example
```
{
  "data": "RETURNED ENCRYPTED DATA URL",
  "file": "RETURNED ENCRYPTED FILE URL",
  "success": "SHOWS TRUE IF ENCRYPTION WAS SUCCESSFULL",
  "public": "PUBLIC ENCRYPTION KEY FOR YOUR DATA OR FILES",
  "private": "PRIVATE ENCRYPTION KEY FOR YOUR DATA OR FILES"
}
```



## <a name="encryption_model"></a>![Type: ](https://apidocs.io/img/method.png "Encryption Model") Encryption Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| data | string |  ``` Required ```  | - | 
| file | string |  ``` Required ```  | - | 
| method | string |  ``` Required ```  | - | 
| bit | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "data": "data",
  "file": "file",
  "method": "method",
  "bit": "bit"
}
```



## <a name="cdn_push_model"></a>![Type: ](https://apidocs.io/img/method.png "CDN Push Model") CDN Push Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| cname | string |  ``` Required ```  | - | 
| file | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "cname": "cname",
  "file": "file"
}
```



## <a name="cdn_pull_model"></a>![Type: ](https://apidocs.io/img/method.png "CDN Pull Model") CDN Pull Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| origin | string |  ``` Required ```  | - | 
| cname | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "origin": "origin",
  "cname": "cname"
}
```



## <a name="dns_configuration_model"></a>![Type: ](https://apidocs.io/img/method.png "DNS Configuration Model") DNS Configuration Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| domain | string |  ``` Required ```  | - | 
| records | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "domain": "domain",
  "records": "records"
}
```



## <a name="nameservers_model"></a>![Type: ](https://apidocs.io/img/method.png "Nameservers Model") Nameservers Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| ns1 | string |  ``` Required ```  | - | 
| ns2 | string |  ``` Required ```  | - | 
| ns3 | string |  ``` Required ```  | - | 
| ns4 | string |  ``` Required ```  | - | 



#### Example
```
{
  "ns1": "ns1",
  "ns2": "ns2",
  "ns3": "ns3",
  "ns4": "ns4"
}
```



## <a name="hosting_model_response"></a>![Type: ](https://apidocs.io/img/method.png "Hosting Model Response") Hosting Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | - | 
| url | string |  ``` Required ```  | - | 
| success | string |  ``` Required ```  | - | 
| id | string |  ``` Required ```  | - | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "url": "RETURNED APP HOSTING URL",
  "success": "RETURNS TRUE IF APP WAS SUCCESSFULLY DEPLOYED",
  "id": "TRANSACTION ID"
}
```



## <a name="hosting_model"></a>![Type: ](https://apidocs.io/img/method.png "Hosting Model") Hosting Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| app | string |  ``` Required ```  | - | 
| domain | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "app": "app",
  "domain": "domain"
}
```



## <a name="data_manipulation_model_response"></a>![Type: ](https://apidocs.io/img/method.png "Data Manipulation Model Response") Data Manipulation Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | - | 
| url | string |  ``` Required ```  | - | 
| success | string |  ``` Required ```  | - | 
| id | string |  ``` Required ```  | - | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "url": "RETURNED DATA URL",
  "success": "RETURNS TRUE IF DATA MANIPULATION WAS SUCCESSFULL",
  "id": "TRANSACTION ID"
}
```



## <a name="image_manipulation_model_response"></a>![Type: ](https://apidocs.io/img/method.png "Image Manipulation Model Response") Image Manipulation Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | - | 
| url | string |  ``` Required ```  | - | 
| success | string |  ``` Required ```  | - | 
| moderated | string |  ``` Required ```  | - | 
| id | string |  ``` Required ```  | - | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "url": "RETURNED IMAGE URL AND DATA",
  "success": "RETURNS TRUE IF IMAGE MANIPULATION WAS SUCCESSFULL",
  "moderated": "RETURNS TRUE IF IMAGE CONTAINED GRAPHIC IMAGERY",
  "id": "TRANSACTION ID"
}
```



## <a name="image_manipulation_model"></a>![Type: ](https://apidocs.io/img/method.png "Image Manipulation Model") Image Manipulation Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| image | string |  ``` Required ```  | - | 
| transform | string |  ``` Required ```  | - | 
| moderate | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "image": "image",
  "transform": "transform",
  "moderate": "moderate"
}
```



## <a name="two_factor_authentication_token_model"></a>![Type: ](https://apidocs.io/img/method.png "Two Factor Authentication Token Model") Two Factor Authentication Token Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| user | string |  ``` Required ```  | - | 
| code | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "user": "user",
  "code": "code"
}
```



## <a name="two_factor_authentication_model"></a>![Type: ](https://apidocs.io/img/method.png "Two Factor Authentication Model") Two Factor Authentication Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | - | 
| to | string |  ``` Required ```  | - | 
| verified | string |  ``` Required ```  | - | 
| id | string |  ``` Required ```  | - | 



#### Example
```
{
  "request": "request",
  "to": "to",
  "verified": "verified",
  "id": "id"
}
```



## <a name="verify_user_model"></a>![Type: ](https://apidocs.io/img/method.png "Verify User Model") Verify User Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| user | string |  ``` Required ```  | - | 
| code | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "user": "user",
  "code": "code"
}
```



## <a name="verify_model_response"></a>![Type: ](https://apidocs.io/img/method.png "Verify Model Response") Verify Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | - | 
| to | string |  ``` Required ```  | - | 
| verified | string |  ``` Required ```  | - | 
| id | string |  ``` Required ```  | - | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "to": "USER BEING VERIFIED",
  "verified": "RETURNS TRUE OR FALSE",
  "id": "TRANSACTION ID"
}
```



## <a name="user_deletion_model"></a>![Type: ](https://apidocs.io/img/method.png "User Deletion Model") User Deletion Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| user | string |  ``` Required ```  | - | 
| apiuid | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "user": "user",
  "apiuid": "apiuid"
}
```



## <a name="user_information_model_response"></a>![Type: ](https://apidocs.io/img/method.png "User Information Model Response") User Information Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| user | string |  ``` Required ```  | - | 
| key | string |  ``` Required ```  | Users API Private Key | 
| api | string |  ``` Required ```  | Users API Public Key | 
| info | [User Information Secondary Model](#user_information_secondary_model) |  ``` Required ```  | Users Profile Information | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "uid": "Users UID",
  "apiuid": "API SIDE USER ID",
  "verified": "RETURNS TRUE IF USER IS VERIFIED",
  "id": "TRANSACTION ID",
  "info": {
    "realname": "USERS REAL NAME",
    "displayname": "USERS USERNAME",
    "avatar": "USER AVATAR URL",
    "email": "USERS EMAIL",
    "address": "USERS ADDRESS IN ONE LINE SEPERATED BY COMMAS",
    "address1": "USERS ADDRESS LINE ONE",
    "address2": "USERS ADDRESS LINE TWO",
    "city": "USERS ADDRESS CITY",
    "state": "USERS ADDRESS STATE",
    "zipcode": "USERS ADDRESS ZIPCODE",
    "phone": "USERS CELL PHONE NUMBER",
    "lastlogin": "USERS LAST LOGIN",
    "ip": "USERS IP",
    "2fa": "RETURNS TRUE IF 2FA IS ENABLED",
    "iplock": "RETURNS TRUE IF IP LOCK IS ENABLED"
  }
}
```



## <a name="user_information_secondary_model"></a>![Type: ](https://apidocs.io/img/method.png "User Information Secondary Model") User Information Secondary Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| user | string |  ``` Required ```  | - | 
| apiuid | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "user": "user",
  "apiuid": "apiuid"
}
```



## <a name="user_custom_update_model"></a>![Type: ](https://apidocs.io/img/method.png "User Custom Update Model") User Custom Update Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| uid | string |  ``` Required ```  | - | 
| apiuid | string |  ``` Required ```  | - | 
| avatar | string |  ``` Required ```  | - | 
| custom-input | string |  ``` Required ```  | - | 



#### Example
```
{
  "uid": "uid",
  "apiuid": "apiuid",
  "avatar": "avatar",
  "custom-input": "custom-input"
}
```



## <a name="user_update_model_response"></a>![Type: ](https://apidocs.io/img/method.png "User Update Model Response") User Update Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | - | 
| updated | string |  ``` Required ```  | - | 
| id | string |  ``` Required ```  | - | 
| info | [User Custom Update Model](#user_custom_update_model) |  ``` Required ```  | - | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "updated": "RETURNS TRUE, IF USERS PROFILE WAS SUCCESSFULLY UPDATED",
  "id": "TRANSACTION ID",
  "info": {
    "uid": "USERS ID",
    "apiuid": "API SIDE USER ID",
    "avatar": "INPUTTED AVATAR URL",
    "custom-input": "CUSTOM INPUTTED PROFILE DATA"
  }
}
```



## <a name="user_profile_information_model"></a>![Type: ](https://apidocs.io/img/method.png "User Profile Information Model") User Profile Information Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| uid | string |  ``` Required ```  | - | 
| apiuid | string |  ``` Required ```  | - | 
| realname | string |  ``` Required ```  | - | 
| displayname | string |  ``` Required ```  | - | 
| email | string |  ``` Required ```  | - | 
| address | string |  ``` Required ```  | - | 
| phone | string |  ``` Required ```  | - | 



#### Example
```
{
  "uid": "uid",
  "apiuid": "apiuid",
  "realname": "realname",
  "displayname": "displayname",
  "email": "email",
  "address": "address",
  "phone": "phone"
}
```



## <a name="user_registration_model_response"></a>![Type: ](https://apidocs.io/img/method.png "User Registration Model Response") User Registration Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | - | 
| active | string |  ``` Required ```  | - | 
| id | string |  ``` Required ```  | - | 
| info | [User Profile Information Model](#user_profile_information_model) |  ``` Required ```  | - | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "active": "RETURNS TRUE, IF USER WAS SUCCESSFULLY REGISTERED",
  "id": "TRANSACTION ID",
  "info": {
    "uid": "USERS ID",
    "apiuid": "API SIDE USER ID",
    "realname": "USERS REAL NAME",
    "displayname": "USERS USERNAME",
    "email": "USERS EMAIL",
    "address": "USERS ADDRESS",
    "phone": "USERS CELL PHONE NUMBER"
  }
}
```



## <a name="user_authentication_model_response"></a>![Type: ](https://apidocs.io/img/method.png "User Authentication Model Response") User Authentication Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| valid | string |  ``` Required ```  | - | 
| id | string |  ``` Required ```  | - | 
| info | [Info Model](#info_model) |  ``` Required ```  | - | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "uid": "Users UID",
  "valid": "RETURNS TRUE IF USER LOGIN DETAILS ARE VALID",
  "id": "TRANSACTION ID",
  "info": {
    "uid": "USERS ID",
    "apiuid": "API SIDE USER ID",
    "realname": "USERS REAL NAME",
    "displayname": "USERS USERNAME",
    "avatar": "USER AVATAR URL",
    "email": "USERS EMAIL",
    "address": "USERS ADDRESS",
    "phone": "USERS CELL PHONE NUMBER",
    "lastlogin": "USERS LAST LOGIN",
    "ip": "USERS IP",
    "2fa": "RETURNS TRUE IF 2FA IS ENABLED",
    "iplock": "RETURNS TRUE IF IP LOCK IS ENABLED"
  }
}
```



## <a name="user_authentication_model"></a>![Type: ](https://apidocs.io/img/method.png "User Authentication Model") User Authentication Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| user | string |  ``` Required ```  | - | 
| password | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "user": "user",
  "password": "password"
}
```



## <a name="data_model"></a>![Type: ](https://apidocs.io/img/method.png "Data Model") Data Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| result | string |  ``` Required ```  | - | 
| content | string |  ``` Required ```  | - | 
| id | string |  ``` Required ```  | - | 



#### Example
```
{
  "result": "result",
  "content": "content",
  "id": "id"
}
```



## <a name="log_model"></a>![Type: ](https://apidocs.io/img/method.png "Log Model") Log Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| MMDDYYYYHHMMSSX | [MMDDYYYYHHMMSS Model](#mmddyyyyhhmmss_model) |  ``` Required ```  | - | 
| MMDDYYYYHHMMSSY | [MMDDYYYYHHMMSS Model](#mmddyyyyhhmmss_model) |  ``` Required ```  | - | 



#### Example
```
{
  "MMDDYYYYHHMMSSX": {
    "data": {
      "result": "result",
      "content": "content",
      "id": "id"
    }
  },
  "MMDDYYYYHHMMSSY": {
    "data": {
      "result": "result",
      "content": "content",
      "id": "id"
    }
  }
}
```



## <a name="waf_configuration_model_response"></a>![Type: ](https://apidocs.io/img/method.png "WAF Configuration Model Response") WAF Configuration Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | - | 
| rule | string |  ``` Required ```  | - | 



#### Example
```
{
  "success": "SHOWS TRUE WHEN THE WAF AND ORIGIN SHIELD (DDOS PROTECTION) IS DEPLOYED SUCCESSFULLY",
  "rule": "RULES APPLIED TO WAF"
}
```



## <a name="waf_creation_model_response"></a>![Type: ](https://apidocs.io/img/method.png "WAF Creation Model Response") WAF Creation Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | - | 
| cname | string |  ``` Required ```  | - | 



#### Example
```
{
  "success": "SHOWS TRUE WHEN THE WAF AND ORIGIN SHIELD (DDOS PROTECTION) IS DEPLOYED SUCCESSFULLY",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```



## <a name="code_protection_model_response"></a>![Type: ](https://apidocs.io/img/method.png "Code Protection Model Response") Code Protection Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | - | 
| app | string |  ``` Required ```  | - | 



#### Example
```
{
  "success": "RETURNS TRUE IF APP WAS SUCCESSFULLY OBFUSCTATED AND PROTECTED",
  "app": "OBFUSCATED APP URL"
}
```



## <a name="code_protection_model"></a>![Type: ](https://apidocs.io/img/method.png "Code Protection Model") Code Protection Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| app | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "app": "app"
}
```



## <a name="cdn_push_model_response"></a>![Type: ](https://apidocs.io/img/method.png "CDN Push Model Response") CDN Push Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | - | 
| upload | string |  ``` Required ```  | - | 
| cname | string |  ``` Required ```  | - | 



#### Example
```
{
  "success": "SHOWS TRUE WHEN PUSH ZONE IS DEPLOYED SUCCESSFULLY",
  "upload": "LIST OF FILES UPLOADED TO YOUR PUSH ZONE",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```



## <a name="cdn_pull_model_response"></a>![Type: ](https://apidocs.io/img/method.png "CDN Pull Model Response") CDN Pull Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | - | 
| cname | string |  ``` Required ```  | - | 



#### Example
```
{
  "success": "SHOWS TRUE WHEN PULL ZONE IS DEPLOYED SUCCESSFULLY",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```



## <a name="dns_configuration_model_response"></a>![Type: ](https://apidocs.io/img/method.png "DNS Configuration Model Response") DNS Configuration Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | - | 
| domain | string |  ``` Required ```  | - | 
| records | string |  ``` Required ```  | - | 



#### Example
```
{
  "success": "SHOWS TRUE IF RECORDS WERE SUCCESSFULLY SET",
  "domain": "DOMAIN",
  "records": "RECORDS SET TO DOMAIN"
}
```



## <a name="dns_creation_model_response"></a>![Type: ](https://apidocs.io/img/method.png "DNS Creation Model Response") DNS Creation Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| domain | string |  ``` Required ```  | - | 
| nameservers | [Nameservers Model](#nameservers_model) |  ``` Required ```  | - | 



#### Example
```
{
  "domain": "LIST OF DOMAINS ADDED",
  "nameservers": {
    "ns1": "NAME SERVER ONE TO POINT YOUR DOMAIN AT",
    "ns2": "NAME SERVER TWO TO POINT YOUR DOMAIN AT",
    "ns3": "NAME SERVER THREE TO POINT YOUR DOMAIN AT",
    "ns4": "NAME SERVER FOUR TO POINT YOUR DOMAIN AT"
  }
}
```



## <a name="dns_creation_model"></a>![Type: ](https://apidocs.io/img/method.png "DNS Creation Model") DNS Creation Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| domain | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "domain": "domain"
}
```



## <a name="two_factor_authentication_token_model_response"></a>![Type: ](https://apidocs.io/img/method.png "Two Factor Authentication Token Model Response") Two Factor Authentication Token Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | - | 
| correct | string |  ``` Required ```  | - | 
| id | string |  ``` Required ```  | - | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "correct": "RETURNS IF 2FA TOKEN IS CORRECT",
  "id": "TRANSACTION ID"
}
```



## <a name="two_factor_authentication_model_response"></a>![Type: ](https://apidocs.io/img/method.png "Two Factor Authentication Model Response") Two Factor Authentication Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| to | string |  ``` Required ```  | - | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "to": "USER BEING VERIFIED",
  "verified": "RETURNS TRUE OR FALSE",
  "id": "TRANSACTION ID"
}
```



## <a name="verify_address_response"></a>![Type: ](https://apidocs.io/img/method.png "Verify Address Response") Verify Address Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | - | 
| active | string |  ``` Required ```  | - | 
| id | string |  ``` Required ```  | - | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "active": "RETURNS TRUE, IF ADDRESS IS ACTIVE AND IF USER IS CURRENTLY THERE",
  "id": "TRANSACTION ID"
}
```



## <a name="verify_user_model_response"></a>![Type: ](https://apidocs.io/img/method.png "Verify User Model Response") Verify User Model Response








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | - | 
| correct | string |  ``` Required ```  | - | 
| id | string |  ``` Required ```  | - | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "correct": "RETURNS IF 2FA TOKEN IS CORRECT",
  "id": "TRANSACTION ID"
}
```



## <a name="verify_model"></a>![Type: ](https://apidocs.io/img/method.png "Verify Model") Verify Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | - | 
| uid | string |  ``` Required ```  | - | 
| to | string |  ``` Required ```  | - | 



#### Example
```
{
  "key": "key",
  "uid": "uid",
  "to": "to"
}
```



## <a name="user_deletion_response_model"></a>![Type: ](https://apidocs.io/img/method.png "User Deletion Response Model") User Deletion Response Model








| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | - | 
| deleted | string |  ``` Required ```  | - | 
| id | string |  ``` Required ```  | - | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "deleted": "RETURNS TRUE, IF USERS ACCOUNT WAS SUCCESSFULLY DELETED",
  "id": "TRANSACTION ID"
}
```




