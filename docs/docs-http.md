# 

**`API Version:`** `1.02`

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



## Base URL

The base URL for this API is `https://api.rest.sh/api`



## Authentication
This API uses `custom query` parameter(s) for authentication.



### Authentication Parameters

The parameters required for authentication are listed below:

| Parameter | Description | Example | 
|-----------|-------------| ------- |
| key | Your API Key | `"API"` |
| uid | Your User ID | `"UID"` |



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
* [WAF & DDOS Protection](#waf_&_ddos_protection)
* [Encryption](#encryption)
* [CDN](#cdn)
* [DNS](#dns)
* [Code Obfuscation](#code_obfuscation)
* [Hosting](#hosting)
* [Data Manipulation, Conversion, Sorting, and Compression API](#data_manipulation,_conversion,_sorting,_and_compression_api)
* [Image Manipulation and Moderation API](#image_manipulation_and_moderation_api)
* [Verification](#verification)
* [Two Factor Authentication API](#two_factor_authentication_api)
* [User Management](#user_management)
* [Login and Registration](#login_and_registration)

## <a name="advanced_logging"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Advanced Logging") Advanced Logging


### <a name="https://api.rest.sh/api/security/logging/info"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/logging/info") https://api.rest.sh/api/security/logging/info


**`GET`** `/security/logging/info`

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| name | string |  ``` Required ```  | TODO: Add a parameter description | `origin-name` | 
| origin | string |  ``` Required ```  | TODO: Add a parameter description | `origin.yourdomain.tld` | 
| time | string |  ``` Required ```  | TODO: Add a parameter description | `01/01/0101;24:59:01` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/security/logging/infoResponse](#https://api.rest.sh/api/security/logging/info_response)**) 

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


### <a name="https://api.rest.sh/api/security/logging"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/logging") https://api.rest.sh/api/security/logging


**`GET`** `/security/logging`

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| name | string |  ``` Required ```  | TODO: Add a parameter description | `origin-name` | 
| origin | string |  ``` Required ```  | TODO: Add a parameter description | `origin.yourdomain.tld` | 
| activate | boolean |  ``` Required ```  | TODO: Add a parameter description | `true` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/security/loggingResponse](#https://api.rest.sh/api/security/logging_response)**) 

```
{
  "success": "RETURNS TRUE IF ADVANCED LOGGING IS ACTIVATED"
}
```


### <a name="https://api.rest.sh/api/security/logging/info"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/logging/info") https://api.rest.sh/api/security/logging/info


**`POST`** `/security/logging/info`

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Info




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/security/logging/infoRequest](#https://api.rest.sh/api/security/logging/info_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "name": "YOUR WAF'S NAME",
  "origin": "ORIGIN URL",
  "time": "LOOKUP SPECIFIC TIMES IN LOG (MM/DD/YYYY;HH:MM:SS) SEPERATED BY A COMMA OR ('*' / ALL)"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/security/logging/infoResponse](#https://api.rest.sh/api/security/logging/info_response)**) 

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


### <a name="https://api.rest.sh/api/security/logging"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/logging") https://api.rest.sh/api/security/logging


**`POST`** `/security/logging`

> *Tags:*  ``` Skips Authentication ``` 

> WAF Log Setup




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/security/loggingRequest](#https://api.rest.sh/api/security/logging_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "name": "YOUR WAF'S NAME",
  "origin": "ORIGIN URL",
  "activate": "TRUE OR FALSE IF YOU WANT ADVANCED LOGGING ACTIVATED"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/security/loggingResponse](#https://api.rest.sh/api/security/logging_response)**) 

```
{
  "success": "RETURNS TRUE IF ADVANCED LOGGING IS ACTIVATED"
}
```


[Back to API Reference](#api_reference)

## <a name="waf_&_ddos_protection"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "WAF & DDOS Protection") WAF & DDOS Protection


### <a name="https://api.rest.sh/api/security/waf/configure"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/waf/configure") https://api.rest.sh/api/security/waf/configure


**`GET`** `/security/waf/configure`

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| name | string |  ``` Required ```  | TODO: Add a parameter description | `origin-name` | 
| origin | string |  ``` Required ```  | TODO: Add a parameter description | `origin.yourdomain.tld` | 
| rule | string |  ``` Required ```  | TODO: Add a parameter description | `header:Access-Control-Allow-Origin;yourdomain.tld;seconddomain.tld,match:ip;127.0.0.1;does` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/security/waf/configureResponse](#https://api.rest.sh/api/security/waf/configure_response)**) 

```
{
  "success": "SHOWS TRUE WHEN THE WAF AND ORIGIN SHIELD (DDOS PROTECTION) IS DEPLOYED SUCCESSFULLY",
  "rule": "RULES APPLIED TO WAF"
}
```


### <a name="https://api.rest.sh/api/security/waf"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/waf") https://api.rest.sh/api/security/waf


**`GET`** `/security/waf`

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| origin | string |  ``` Required ```  | TODO: Add a parameter description | `origin.yourdomain.tld` | 
| cname | string |  ``` Required ```  | TODO: Add a parameter description | `yourdomain.tld,www.yourdomain.tld` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/security/wafResponse](#https://api.rest.sh/api/security/waf_response)**) 

```
{
  "success": "SHOWS TRUE WHEN THE WAF AND ORIGIN SHIELD (DDOS PROTECTION) IS DEPLOYED SUCCESSFULLY",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```


### <a name="https://api.rest.sh/api/security/waf/configure"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/waf/configure") https://api.rest.sh/api/security/waf/configure


**`POST`** `/security/waf/configure`

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/security/waf/configureRequest](#https://api.rest.sh/api/security/waf/configure_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "name": "WHAT YOU WISH TO NAME YOUR WAF",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/security/waf/configureResponse](#https://api.rest.sh/api/security/waf/configure_response)**) 

```
{
  "success": "SHOWS TRUE WHEN THE WAF AND ORIGIN SHIELD (DDOS PROTECTION) IS DEPLOYED SUCCESSFULLY",
  "rule": "RULES APPLIED TO WAF"
}
```


### <a name="https://api.rest.sh/api/security/waf"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/waf") https://api.rest.sh/api/security/waf


**`POST`** `/security/waf`

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/security/wafRequest](#https://api.rest.sh/api/security/waf_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/security/wafResponse](#https://api.rest.sh/api/security/waf_response)**) 

```
{
  "success": "SHOWS TRUE WHEN THE WAF AND ORIGIN SHIELD (DDOS PROTECTION) IS DEPLOYED SUCCESSFULLY",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```


[Back to API Reference](#api_reference)

## <a name="encryption"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Encryption") Encryption


### <a name="https://api.rest.sh/api/security/encryption"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/encryption") https://api.rest.sh/api/security/encryption


**`GET`** `/security/encryption`

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| data | string |  ``` Required ```  | TODO: Add a parameter description | `DATA` | 
| method | string |  ``` Required ```  | TODO: Add a parameter description | `DES,RSA` | 
| bit | number |  ``` Required ```  | TODO: Add a parameter description | `4096` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/security/encryptionResponse](#https://api.rest.sh/api/security/encryption_response)**) 

```
{
  "data": "RETURNED ENCRYPTED DATA URL",
  "file": "RETURNED ENCRYPTED FILE URL",
  "success": "SHOWS TRUE IF ENCRYPTION WAS SUCCESSFULL",
  "public": "PUBLIC ENCRYPTION KEY FOR YOUR DATA OR FILES",
  "private": "PRIVATE ENCRYPTION KEY FOR YOUR DATA OR FILES"
}
```


### <a name="https://api.rest.sh/api/security/encryption"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/encryption") https://api.rest.sh/api/security/encryption


**`POST`** `/security/encryption`

> *Tags:*  ``` Skips Authentication ``` 

> Data and File Encryption API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/security/encryptionRequest](#https://api.rest.sh/api/security/encryption_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "data": "DATA YOU WISH TO ENCRYPT",
  "file": "FILE YOU WISH TO ENCRYPT",
  "method": "SINGLE OR MULTIPLE ENCRYPTION TYPES TO APPLY TO DATA OR FILES SEPERATED BY A COMMA (DES, RSA, BLOWFISH, TWOFISH, AES, IDEA, PGP)",
  "bit": "SIZE OF ENCRYPTION KEY"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/security/encryptionResponse](#https://api.rest.sh/api/security/encryption_response)**) 

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


### <a name="https://api.rest.sh/api/service/cdn/push"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/cdn/push") https://api.rest.sh/api/service/cdn/push


**`GET`** `/service/cdn/push`

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| cname | string |  ``` Required ```  | TODO: Add a parameter description | `cdn.yourdomain.tld,cdn1.yourdomain.tld,cdn2.yourdomain.tld` | 
| file | string |  ``` Required ```  | TODO: Add a parameter description | `static.yourdomain.tld/file.type` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/service/cdn/pushResponse](#https://api.rest.sh/api/service/cdn/push_response)**) 

```
{
  "success": "SHOWS TRUE WHEN PUSH ZONE IS DEPLOYED SUCCESSFULLY",
  "upload": "LIST OF FILES UPLOADED TO YOUR PUSH ZONE",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```


### <a name="https://api.rest.sh/api/service/cdn/pull"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/cdn/pull") https://api.rest.sh/api/service/cdn/pull


**`GET`** `/service/cdn/pull`

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| origin | string |  ``` Required ```  | TODO: Add a parameter description | `origin.yourdomain.tld` | 
| cname | string |  ``` Required ```  | TODO: Add a parameter description | `cdn.yourdomain.tld,cdn1.yourdomain.tld,cdn2.yourdomain.tld` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/service/cdn/pullResponse](#https://api.rest.sh/api/service/cdn/pull_response)**) 

```
{
  "success": "SHOWS TRUE WHEN PULL ZONE IS DEPLOYED SUCCESSFULLY",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```


### <a name="https://api.rest.sh/api/service/cdn/push"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/cdn/push") https://api.rest.sh/api/service/cdn/push


**`POST`** `/service/cdn/push`

> *Tags:*  ``` Skips Authentication ``` 

> CDN Push Zone API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/service/cdn/pushRequest](#https://api.rest.sh/api/service/cdn/push_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "cname": "DOMAIN OR DOMAINS YOU WISH TO ALLOW CNAME ACCESS SEPERATED BY A COMMA",
  "file": "FILE OR FILES YOU WISH TO UPLOAD SEPERATED BY A COMMA"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/service/cdn/pushResponse](#https://api.rest.sh/api/service/cdn/push_response)**) 

```
{
  "success": "SHOWS TRUE WHEN PUSH ZONE IS DEPLOYED SUCCESSFULLY",
  "upload": "LIST OF FILES UPLOADED TO YOUR PUSH ZONE",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```


### <a name="https://api.rest.sh/api/service/cdn/pull"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/cdn/pull") https://api.rest.sh/api/service/cdn/pull


**`POST`** `/service/cdn/pull`

> *Tags:*  ``` Skips Authentication ``` 

> CDN Pull Zone API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/service/cdn/pullRequest](#https://api.rest.sh/api/service/cdn/pull_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "origin": "ORIGIN DOMAIN TO PULL ASSETS FROM",
  "cname": "DOMAIN OR DOMAINS YOU WISH TO ALLOW CNAME ACCESS SEPERATED BY A COMMA"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/service/cdn/pullResponse](#https://api.rest.sh/api/service/cdn/pull_response)**) 

```
{
  "success": "SHOWS TRUE WHEN PULL ZONE IS DEPLOYED SUCCESSFULLY",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```


[Back to API Reference](#api_reference)

## <a name="dns"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "DNS") DNS


### <a name="https://api.rest.sh/api/service/dns/configure"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/dns/configure") https://api.rest.sh/api/service/dns/configure


**`GET`** `/service/dns/configure`

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| domain | string |  ``` Required ```  | TODO: Add a parameter description | `yourdomain.tld` | 
| records | string |  ``` Required ```  | TODO: Add a parameter description | `set:root:a:127.0.0.1,set:www:a:127.0.0.1,set:cdn:cname:cname.domain.com` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/service/dns/configureResponse](#https://api.rest.sh/api/service/dns/configure_response)**) 

```
{
  "success": "SHOWS TRUE IF RECORDS WERE SUCCESSFULLY SET",
  "domain": "DOMAIN",
  "records": "RECORDS SET TO DOMAIN"
}
```


### <a name="https://api.rest.sh/api/service/dns/configure"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/dns/configure") https://api.rest.sh/api/service/dns/configure


**`POST`** `/service/dns/configure`

> *Tags:*  ``` Skips Authentication ``` 

> DNS Configuration API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/service/dns/configureRequest](#https://api.rest.sh/api/service/dns/configure_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "domain": "DOMAINS TO SET DNS RECORDS",
  "records": "RECORDS TO SET TO DOMAIN"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/service/dns/configureResponse](#https://api.rest.sh/api/service/dns/configure_response)**) 

```
{
  "success": "SHOWS TRUE IF RECORDS WERE SUCCESSFULLY SET",
  "domain": "DOMAIN",
  "records": "RECORDS SET TO DOMAIN"
}
```


### <a name="https://api.rest.sh/api/service/dns/add"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/dns/add") https://api.rest.sh/api/service/dns/add


**`GET`** `/service/dns/add`

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| domain | string |  ``` Required ```  | TODO: Add a parameter description | `yourdomain.tld,seconddomain.tld` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/service/dns/addResponse](#https://api.rest.sh/api/service/dns/add_response)**) 

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


### <a name="https://api.rest.sh/api/service/dns/add"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/dns/add") https://api.rest.sh/api/service/dns/add


**`POST`** `/service/dns/add`

> *Tags:*  ``` Skips Authentication ``` 

> DNS Creation API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/service/dns/addRequest](#https://api.rest.sh/api/service/dns/add_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "domain": "DOMAINS SEPERATED BY A COMMA TO ADD TO DNS"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/service/dns/addResponse](#https://api.rest.sh/api/service/dns/add_response)**) 

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


### <a name="https://api.rest.sh/api/service/obfuscation"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/obfuscation") https://api.rest.sh/api/service/obfuscation


**`GET`** `/service/obfuscation`

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| app | string |  ``` Required ```  | TODO: Add a parameter description | `git://app.git` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/service/obfuscationResponse](#https://api.rest.sh/api/service/obfuscation_response)**) 

```
{
  "success": "RETURNS TRUE IF APP WAS SUCCESSFULLY OBFUSCTATED AND PROTECTED",
  "app": "OBFUSCATED APP URL"
}
```


### <a name="https://api.rest.sh/api/service/obfuscation"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/obfuscation") https://api.rest.sh/api/service/obfuscation


**`POST`** `/service/obfuscation`

> *Tags:*  ``` Skips Authentication ``` 

> Code/Application Obfuscation and Anti-Tampering API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/service/obfuscationRequest](#https://api.rest.sh/api/service/obfuscation_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "app": "APP GIT URL or URL CONTAINING YOUR APP IN A ZIP FILE"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/service/obfuscationResponse](#https://api.rest.sh/api/service/obfuscation_response)**) 

```
{
  "success": "RETURNS TRUE IF APP WAS SUCCESSFULLY OBFUSCTATED AND PROTECTED",
  "app": "OBFUSCATED APP URL"
}
```


[Back to API Reference](#api_reference)

## <a name="hosting"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Hosting") Hosting


### <a name="https://api.rest.sh/api/service/hosting"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/hosting") https://api.rest.sh/api/service/hosting


**`GET`** `/service/hosting`

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| app | string |  ``` Required ```  | TODO: Add a parameter description | `git://app.git` | 
| domain | string |  ``` Required ```  | TODO: Add a parameter description | `yourdomain.tld,seconddomain.tld` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/service/hostingResponse](#https://api.rest.sh/api/service/hosting_response)**) 

```
{
  "request": "REQUEST TYPE",
  "url": "RETURNED APP HOSTING URL",
  "success": "RETURNS TRUE IF APP WAS SUCCESSFULLY DEPLOYED",
  "id": "TRANSACTION ID"
}
```


### <a name="https://api.rest.sh/api/service/hosting"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/hosting") https://api.rest.sh/api/service/hosting


**`POST`** `/service/hosting`

> *Tags:*  ``` Skips Authentication ``` 

> Node.JS Web APP Hosting




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/service/hostingRequest](#https://api.rest.sh/api/service/hosting_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "app": "APP GIT URL OR URL CONTAINING YOUR APP IN A ZIP FILE",
  "domain": "ALLOWED DOMAIN NAMES SEPERATED BY A COMMA TO CNAME WITH ACCESS TO HOSTED APP"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/service/hostingResponse](#https://api.rest.sh/api/service/hosting_response)**) 

```
{
  "request": "REQUEST TYPE",
  "url": "RETURNED APP HOSTING URL",
  "success": "RETURNS TRUE IF APP WAS SUCCESSFULLY DEPLOYED",
  "id": "TRANSACTION ID"
}
```


[Back to API Reference](#api_reference)

## <a name="data_manipulation,_conversion,_sorting,_and_compression_api"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Data Manipulation, Conversion, Sorting, and Compression API") Data Manipulation, Conversion, Sorting, and Compression API


### <a name="https://api.rest.sh/api/data"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/data") https://api.rest.sh/api/data


**`GET`** `/data`

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| user | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| apiuid | string |  ``` Required ```  | TODO: Add a parameter description | `apiUID` | 
| data | string |  ``` Required ```  | TODO: Add a parameter description | `https://static.yourcdn.com/data.file` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/dataResponse](#https://api.rest.sh/api/data_response)**) 

```
{
  "request": "REQUEST TYPE",
  "url": "RETURNED DATA URL",
  "success": "RETURNS TRUE IF DATA MANIPULATION WAS SUCCESSFULL",
  "id": "TRANSACTION ID"
}
```


### <a name="https://api.rest.sh/api/data"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/data") https://api.rest.sh/api/data


**`POST`** `/data`

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add Description




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/dataRequest](#https://api.rest.sh/api/data_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "apiuid": "USERS API SIDE USER ID",
  "url": "DATA URL OR DIRECT FILE UPLOAD FROM CLIENT",
  "manipulation": "DATA MANIPULATION DIRECTIVES",
  "conversion": "CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)",
  "sorting": "SORT BY (NAME, DATE, TYPE, SIZE)",
  "compression": "COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/dataResponse](#https://api.rest.sh/api/data_response)**) 

```
{
  "request": "REQUEST TYPE",
  "url": "RETURNED DATA URL",
  "success": "RETURNS TRUE IF DATA MANIPULATION WAS SUCCESSFULL",
  "id": "TRANSACTION ID"
}
```


[Back to API Reference](#api_reference)

## <a name="image_manipulation_and_moderation_api"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Image Manipulation and Moderation API") Image Manipulation and Moderation API


### <a name="https://api.rest.sh/api/image"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/image") https://api.rest.sh/api/image


**`GET`** `/image`

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| image | string |  ``` Required ```  | TODO: Add a parameter description | `https://img.yourdomain.tld/image.type` | 
| transform | string |  ``` Required ```  | TODO: Add a parameter description | `x:flip,y:flip,grayscale:true,compress:true;80,convert:png` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/imageResponse](#https://api.rest.sh/api/image_response)**) 

```
{
  "request": "REQUEST TYPE",
  "url": "RETURNED IMAGE URL AND DATA",
  "success": "RETURNS TRUE IF IMAGE MANIPULATION WAS SUCCESSFULL",
  "moderated": "RETURNS TRUE IF IMAGE CONTAINED GRAPHIC IMAGERY",
  "id": "TRANSACTION ID"
}
```


### <a name="https://api.rest.sh/api/image"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/image") https://api.rest.sh/api/image


**`POST`** `/image`

> *Tags:*  ``` Skips Authentication ``` 

> Image Manipulation API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/imageRequest](#https://api.rest.sh/api/image_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "image": "DIRECT IMAGE URL OR CLIENT UPLOAD",
  "transform": "IMAGE MANIPULATION DIRECTIVES",
  "moderate": "SET TO TRUE IF YOU WISH TO AUTOMATICALLT CENSOR GRAPHIC IMAGES"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/imageResponse](#https://api.rest.sh/api/image_response)**) 

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


### <a name="https://api.rest.sh/api/verify/address"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/verify/address") https://api.rest.sh/api/verify/address


**`GET`** `/verify/address`

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| user | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| a | string |  ``` Required ```  | TODO: Add a parameter description | `3301 South Greenfield Rd` | 
| sa | string |  ``` Required ```  | TODO: Add a parameter description | `Address Line Two` | 
| c | string |  ``` Required ```  | TODO: Add a parameter description | `Gilbert` | 
| s | string |  ``` Required ```  | TODO: Add a parameter description | `AZ` | 
| z | number |  ``` Required ```  | TODO: Add a parameter description | `85297` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/verify/addressResponse](#https://api.rest.sh/api/verify/address_response)**) 

```
{
  "request": "REQUEST TYPE",
  "active": "RETURNS TRUE, IF ADDRESS IS ACTIVE AND IF USER IS CURRENTLY THERE",
  "id": "TRANSACTION ID"
}
```


### <a name="https://api.rest.sh/api/verify/address"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/verify/address") https://api.rest.sh/api/verify/address


**`POST`** `/verify/address`

> *Tags:*  ``` Skips Authentication ``` 

> User Address Verification API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/verify/addressRequest](#https://api.rest.sh/api/verify/address_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS UID",
  "address": "ADDRESS IN ONE LINE SEPERATED BY COMMAS",
  "a": "ADDRESS LINE ONE",
  "sa": "ADDRESS LINE TWO",
  "c": "CITY OR PROVINCE",
  "s": "STATE OR REGION",
  "z": "ZIPCODE"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/verify/addressResponse](#https://api.rest.sh/api/verify/address_response)**) 

```
{
  "request": "REQUEST TYPE",
  "active": "RETURNS TRUE, IF ADDRESS IS ACTIVE AND IF USER IS CURRENTLY THERE",
  "id": "TRANSACTION ID"
}
```


### <a name="https://api.rest.sh/api/verify/user"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/verify/user") https://api.rest.sh/api/verify/user


**`GET`** `/verify/2fa`

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| user | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| code | string |  ``` Required ```  | TODO: Add a parameter description | `CODE` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/verify/userResponse](#https://api.rest.sh/api/verify/user_response)**) 

```
{
  "request": "REQUEST TYPE",
  "correct": "RETURNS IF 2FA TOKEN IS CORRECT",
  "id": "TRANSACTION ID"
}
```


### <a name="https://api.rest.sh/api/verify/user"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/verify/user") https://api.rest.sh/api/verify/user


**`POST`** `/verify/user`

> *Tags:*  ``` Skips Authentication ``` 

> User Verification API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/verify/userRequest](#https://api.rest.sh/api/verify/user_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS UID",
  "code": "USER INPUTTED TOKEN"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/verify/userResponse](#https://api.rest.sh/api/verify/user_response)**) 

```
{
  "request": "REQUEST TYPE",
  "correct": "RETURNS IF 2FA TOKEN IS CORRECT",
  "id": "TRANSACTION ID"
}
```


### <a name="https://api.rest.sh/api/verify"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/verify") https://api.rest.sh/api/verify


**`GET`** `/verify`

> *Tags:*  ``` Skips Authentication ``` 

> Verification API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| to | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/verifyResponse](#https://api.rest.sh/api/verify_response)**) 

```
{
  "request": "REQUEST TYPE",
  "to": "USER BEING VERIFIED",
  "verified": "RETURNS TRUE OR FALSE",
  "id": "TRANSACTION ID"
}
```


### <a name="https://api.rest.sh/api/verify"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/verify") https://api.rest.sh/api/verify


**`POST`** `/2fa`

> *Tags:*  ``` Skips Authentication ``` 

> Verification API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/verifyRequest](#https://api.rest.sh/api/verify_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "to": "USERS UID"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/verifyResponse](#https://api.rest.sh/api/verify_response)**) 

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


### <a name="https://api.rest.sh/api/2fa/token"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/2fa/token") https://api.rest.sh/api/2fa/token


**`GET`** `/verify/2fa`

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| user | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| code | string |  ``` Required ```  | TODO: Add a parameter description | `CODE` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/2fa/tokenResponse](#https://api.rest.sh/api/2fa/token_response)**) 

```
{
  "request": "REQUEST TYPE",
  "correct": "RETURNS IF 2FA TOKEN IS CORRECT",
  "id": "TRANSACTION ID"
}
```


### <a name="https://api.rest.sh/api/2fa/token"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/2fa/token") https://api.rest.sh/api/2fa/token


**`POST`** `/verify/2fa`

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication Token Reply




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/2fa/tokenRequest](#https://api.rest.sh/api/2fa/token_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS UID",
  "code": "USER INPUTTED TOKEN"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/2fa/tokenResponse](#https://api.rest.sh/api/2fa/token_response)**) 

```
{
  "request": "REQUEST TYPE",
  "correct": "RETURNS IF 2FA TOKEN IS CORRECT",
  "id": "TRANSACTION ID"
}
```


### <a name="https://api.rest.sh/api/2fa"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/2fa") https://api.rest.sh/api/2fa


**`GET`** `/verify`

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| to | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/2faResponse](#https://api.rest.sh/api/2fa_response)**) 

```
{
  "request": "REQUEST TYPE",
  "to": "USER BEING VERIFIED",
  "verified": "RETURNS TRUE OR FALSE",
  "id": "TRANSACTION ID"
}
```


### <a name="https://api.rest.sh/api/2fa"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/2fa") https://api.rest.sh/api/2fa


**`POST`** `/verify`

> *Tags:*  ``` Skips Authentication ``` 

> Two Factor Authentication API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/2faRequest](#https://api.rest.sh/api/2fa_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "to": "USERS UID"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/2faResponse](#https://api.rest.sh/api/2fa_response)**) 

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


### <a name="https://api.rest.sh/api/user/info"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/user/info") https://api.rest.sh/api/user/info


**`GET`** `/user/info`

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| user | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| apiuid | string |  ``` Required ```  | TODO: Add a parameter description | `apiUID` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/user/infoResponse](#https://api.rest.sh/api/user/info_response)**) 

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


### <a name="https://api.rest.sh/api/user/info"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/user/info") https://api.rest.sh/api/user/info


**`POST`** `/user/info`

> *Tags:*  ``` Skips Authentication ``` 

> Get User Info API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/user/infoRequest](#https://api.rest.sh/api/user/info_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "apiuid": "USERS API SIDE USER ID"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/user/infoResponse](#https://api.rest.sh/api/user/info_response)**) 

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


### <a name="https://api.rest.sh/api/user/update"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/user/update") https://api.rest.sh/api/user/update


**`GET`** `/user/update`

> *Tags:*  ``` Skips Authentication ``` 

> Update User API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| user | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| apiuid | string |  ``` Required ```  | TODO: Add a parameter description | `apiUID` | 
| avatar | string |  ``` Required ```  | TODO: Add a parameter description | `https://img.cdnurl.com/UID/image` | 
| custom input | string |  ``` Required ```  | TODO: Add a parameter description | `custom input` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/user/updateResponse](#https://api.rest.sh/api/user/update_response)**) 

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


### <a name="https://api.rest.sh/api/user/update"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/user/update") https://api.rest.sh/api/user/update


**`POST`** `/user/update`

> *Tags:*  ``` Skips Authentication ``` 

> Update User API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/user/updateRequest](#https://api.rest.sh/api/user/update_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "apiuid": "USERS API SIDE USER ID",
  "oldpassword": "SEND A ENCRYPTED VERSION OF YOUR USERS CURRENT PASSWORD USING THE PRIVATE KEY ON YOUR DASHBOARD",
  "newpassword": "SEND A ENCRYPTED VERSION OF YOUR USERS NEW PASSWORD USING THE PRIVATE KEY ON YOUR DASHBOARD",
  "name": "USERS REAL NAME",
  "email": "USERS EMAIL",
  "phone": "USERS CELL PHONE NUMBER",
  "avatar": "UPDATE USER AVATAR",
  "countrycode": "USERS CELL PHONE COUNTRY CODE",
  "address": "ADDRESS IN ONE LINE SEPERATED BY COMMAS",
  "a": "ADDRESS LINE ONE",
  "sa": "ADDRESS LINE TWO",
  "c": "CITY OR PROVINCE",
  "s": "STATE OR REGION",
  "z": "ZIPCODE",
  "custom-input": "ADD CUSTOM DATA/INPUTS TO YOUR USERS PROFILE"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/user/updateResponse](#https://api.rest.sh/api/user/update_response)**) 

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


### <a name="https://api.rest.sh/api/user/delete"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/user/delete") https://api.rest.sh/api/user/delete


**`GET`** `/user/delete`

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| api | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| user | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| apiuid | string |  ``` Required ```  | TODO: Add a parameter description | `apiUID` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/user/deleteResponse](#https://api.rest.sh/api/user/delete_response)**) 

```
{
  "request": "REQUEST TYPE",
  "deleted": "RETURNS TRUE, IF USERS ACCOUNT WAS SUCCESSFULLY DELETED",
  "id": "TRANSACTION ID"
}
```


### <a name="https://api.rest.sh/api/user/delete"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/user/delete") https://api.rest.sh/api/user/delete


**`POST`** `/user/delete`

> *Tags:*  ``` Skips Authentication ``` 

> Delete User API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/user/deleteRequest](#https://api.rest.sh/api/user/delete_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "apiuid": "USERS API SIDE USER ID"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/user/deleteResponse](#https://api.rest.sh/api/user/delete_response)**) 

```
{
  "request": "REQUEST TYPE",
  "deleted": "RETURNS TRUE, IF USERS ACCOUNT WAS SUCCESSFULLY DELETED",
  "id": "TRANSACTION ID"
}
```


[Back to API Reference](#api_reference)

## <a name="login_and_registration"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Login and Registration") Login and Registration


### <a name="https://api.rest.sh/api/auth/user/register"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/auth/user/register") https://api.rest.sh/api/auth/user/register


**`GET`** `/auth/user/register`

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| user | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| password | string |  ``` Required ```  | TODO: Add a parameter description | `Password` | 
| name | string |  ``` Required ```  | TODO: Add a parameter description | `John Doe` | 
| email | string |  ``` Required ```  | TODO: Add a parameter description | `email@email.com` | 
| phone | number |  ``` Required ```  | TODO: Add a parameter description | `1234567890` | 
| countrycode | number |  ``` Required ```  | TODO: Add a parameter description | `1` | 
| address | string |  ``` Required ```  | TODO: Add a parameter description | `3301 South Greenfield Rd, Gilbert, AZ 85297` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/auth/user/registerResponse](#https://api.rest.sh/api/auth/user/register_response)**) 

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


### <a name="https://api.rest.sh/api/auth/user/register"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/auth/user/register") https://api.rest.sh/api/auth/user/register


**`POST`** `/auth/user/register`

> *Tags:*  ``` Skips Authentication ``` 

> User Registration API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/auth/user/registerRequest](#https://api.rest.sh/api/auth/user/register_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "password": "SEND A ENCRYPTED VERSION OF YOUR USERS PASSWORD USING THE PRIVATE KEY ON YOUR DASHBOARD",
  "name": "USERS REAL NAME",
  "email": "USERS EMAIL",
  "phone": "USERS CELL PHONE NUMBER",
  "countrycode": "USERS CELL PHONE COUNTRY CODE",
  "address": "ADDRESS IN ONE LINE SEPERATED BY COMMAS",
  "a": "ADDRESS LINE ONE",
  "sa": "ADDRESS LINE TWO",
  "c": "CITY OR PROVINCE",
  "s": "STATE OR REGION",
  "z": "ZIPCODE"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/auth/user/registerResponse](#https://api.rest.sh/api/auth/user/register_response)**) 

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


### <a name="https://api.rest.sh/api/auth/user/login"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/auth/user/login") https://api.rest.sh/api/auth/user/login


**`GET`** `/auth/user/login`

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| key | string |  ``` Required ```  | TODO: Add a parameter description | `API` | 
| uid | string |  ``` Required ```  | TODO: Add a parameter description | `UID` | 
| user | string |  ``` Required ```  | TODO: Add a parameter description | `Username` | 
| password | string |  ``` Required ```  | TODO: Add a parameter description | `Password` | 

#### Request Headers
>Content-Type=application/json;

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/auth/user/loginResponse](#https://api.rest.sh/api/auth/user/login_response)**) 

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


### <a name="https://api.rest.sh/api/auth/user/login"></a>![Endpoint: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/auth/user/login") https://api.rest.sh/api/auth/user/login


**`POST`** `/auth/user/login`

> *Tags:*  ``` Skips Authentication ``` 

> User Authentication API




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [https://api.rest.sh/api/auth/user/loginRequest](#https://api.rest.sh/api/auth/user/login_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "password": "SEND A ENCRYPTED VERSION OF YOUR USERS PASSWORD USING THE PRIVATE KEY ON YOUR DASHBOARD"
}
``` 

#### Responses
**200** 


 *Example Body* (**[https://api.rest.sh/api/auth/user/loginResponse](#https://api.rest.sh/api/auth/user/login_response)**) 

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

* [https://api.rest.sh/api/security/logging/infoRequest](#https://api.rest.sh/api/security/logging/info_request)
* [https://api.rest.sh/api/security/loggingRequest](#https://api.rest.sh/api/security/logging_request)
* [https://api.rest.sh/api/dataRequest](#https://api.rest.sh/api/data_request)
* [https://api.rest.sh/api/verify/addressRequest](#https://api.rest.sh/api/verify/address_request)
* [https://api.rest.sh/api/security/waf/configureRequest](#https://api.rest.sh/api/security/waf/configure_request)
* [https://api.rest.sh/api/security/wafRequest](#https://api.rest.sh/api/security/waf_request)
* [Info17](#info17)
* [https://api.rest.sh/api/security/encryptionResponse](#https://api.rest.sh/api/security/encryption_response)
* [https://api.rest.sh/api/security/encryptionRequest](#https://api.rest.sh/api/security/encryption_request)
* [https://api.rest.sh/api/service/cdn/pushRequest](#https://api.rest.sh/api/service/cdn/push_request)
* [https://api.rest.sh/api/service/cdn/pullRequest](#https://api.rest.sh/api/service/cdn/pull_request)
* [https://api.rest.sh/api/user/updateRequest](#https://api.rest.sh/api/user/update_request)
* [https://api.rest.sh/api/service/dns/configureRequest](#https://api.rest.sh/api/service/dns/configure_request)
* [Data](#data)
* [Log](#log)
* [Nameservers](#nameservers)
* [https://api.rest.sh/api/service/hostingResponse](#https://api.rest.sh/api/service/hosting_response)
* [https://api.rest.sh/api/security/waf/configureResponse](#https://api.rest.sh/api/security/waf/configure_response)
* [https://api.rest.sh/api/auth/user/registerRequest](#https://api.rest.sh/api/auth/user/register_request)
* [https://api.rest.sh/api/security/wafResponse](#https://api.rest.sh/api/security/waf_response)
* [https://api.rest.sh/api/service/obfuscationResponse](#https://api.rest.sh/api/service/obfuscation_response)
* [https://api.rest.sh/api/service/hostingRequest](#https://api.rest.sh/api/service/hosting_request)
* [https://api.rest.sh/api/dataResponse](#https://api.rest.sh/api/data_response)
* [https://api.rest.sh/api/service/obfuscationRequest](#https://api.rest.sh/api/service/obfuscation_request)
* [https://api.rest.sh/api/imageResponse](#https://api.rest.sh/api/image_response)
* [https://api.rest.sh/api/imageRequest](#https://api.rest.sh/api/image_request)
* [Info](#info)
* [https://api.rest.sh/api/2fa/tokenRequest](#https://api.rest.sh/api/2fa/token_request)
* [https://api.rest.sh/api/2faResponse](#https://api.rest.sh/api/2fa_response)
* [https://api.rest.sh/api/verify/userRequest](#https://api.rest.sh/api/verify/user_request)
* [https://api.rest.sh/api/service/cdn/pushResponse](#https://api.rest.sh/api/service/cdn/push_response)
* [https://api.rest.sh/api/service/cdn/pullResponse](#https://api.rest.sh/api/service/cdn/pull_response)
* [https://api.rest.sh/api/verifyResponse](#https://api.rest.sh/api/verify_response)
* [https://api.rest.sh/api/user/deleteRequest](#https://api.rest.sh/api/user/delete_request)
* [https://api.rest.sh/api/service/dns/configureResponse](#https://api.rest.sh/api/service/dns/configure_response)
* [https://api.rest.sh/api/user/infoResponse](#https://api.rest.sh/api/user/info_response)
* [https://api.rest.sh/api/service/dns/addResponse](#https://api.rest.sh/api/service/dns/add_response)
* [https://api.rest.sh/api/user/infoRequest](#https://api.rest.sh/api/user/info_request)
* [https://api.rest.sh/api/service/dns/addRequest](#https://api.rest.sh/api/service/dns/add_request)
* [Info12](#info12)
* [https://api.rest.sh/api/user/updateResponse](#https://api.rest.sh/api/user/update_response)
* [https://api.rest.sh/api/2fa/tokenResponse](#https://api.rest.sh/api/2fa/token_response)
* [https://api.rest.sh/api/2faRequest](#https://api.rest.sh/api/2fa_request)
* [Info7](#info7)
* [https://api.rest.sh/api/verify/addressResponse](#https://api.rest.sh/api/verify/address_response)
* [https://api.rest.sh/api/auth/user/registerResponse](#https://api.rest.sh/api/auth/user/register_response)
* [https://api.rest.sh/api/verify/userResponse](#https://api.rest.sh/api/verify/user_response)
* [https://api.rest.sh/api/auth/user/loginResponse](#https://api.rest.sh/api/auth/user/login_response)
* [MMDDYYYYHHMMSS](#mmddyyyyhhmmss)
* [https://api.rest.sh/api/auth/user/loginRequest](#https://api.rest.sh/api/auth/user/login_request)
* [https://api.rest.sh/api/security/logging/infoResponse](#https://api.rest.sh/api/security/logging/info_response)
* [https://api.rest.sh/api/verifyRequest](#https://api.rest.sh/api/verify_request)
* [https://api.rest.sh/api/security/loggingResponse](#https://api.rest.sh/api/security/logging_response)
* [https://api.rest.sh/api/user/deleteResponse](#https://api.rest.sh/api/user/delete_response)
## <a name="https://api.rest.sh/api/security/logging/info_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/logging/infoRequest") https://api.rest.sh/api/security/logging/infoRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| origin | string |  ``` Required ```  | TODO: Add a property description | 
| time | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "name": "YOUR WAF'S NAME",
  "origin": "ORIGIN URL",
  "time": "LOOKUP SPECIFIC TIMES IN LOG (MM/DD/YYYY;HH:MM:SS) SEPERATED BY A COMMA OR ('*' / ALL)"
}
```



## <a name="https://api.rest.sh/api/security/logging_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/loggingRequest") https://api.rest.sh/api/security/loggingRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| origin | string |  ``` Required ```  | TODO: Add a property description | 
| activate | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "name": "YOUR WAF'S NAME",
  "origin": "ORIGIN URL",
  "activate": "TRUE OR FALSE IF YOU WANT ADVANCED LOGGING ACTIVATED"
}
```



## <a name="https://api.rest.sh/api/data_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/dataRequest") https://api.rest.sh/api/dataRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| user | string |  ``` Required ```  | TODO: Add a property description | 
| apiuid | string |  ``` Required ```  | TODO: Add a property description | 
| url | string |  ``` Required ```  | TODO: Add a property description | 
| manipulation | string |  ``` Required ```  | TODO: Add a property description | 
| conversion | string |  ``` Required ```  | TODO: Add a property description | 
| sorting | string |  ``` Required ```  | TODO: Add a property description | 
| compression | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "apiuid": "USERS API SIDE USER ID",
  "url": "DATA URL OR DIRECT FILE UPLOAD FROM CLIENT",
  "manipulation": "DATA MANIPULATION DIRECTIVES",
  "conversion": "CONVERT DATA TYPE TO (JSON, XML, HTML, RAW, BINARY, TEXT)",
  "sorting": "SORT BY (NAME, DATE, TYPE, SIZE)",
  "compression": "COMPRESS DATA IF SET TO TRUE (TYPES = GZIP, ZIP, 7Z, MINIFICATION, REWRITE)"
}
```



## <a name="https://api.rest.sh/api/verify/address_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/verify/addressRequest") https://api.rest.sh/api/verify/addressRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| user | string |  ``` Required ```  | TODO: Add a property description | 
| address | string |  ``` Required ```  | TODO: Add a property description | 
| a | string |  ``` Required ```  | TODO: Add a property description | 
| sa | string |  ``` Required ```  | TODO: Add a property description | 
| c | string |  ``` Required ```  | TODO: Add a property description | 
| s | string |  ``` Required ```  | TODO: Add a property description | 
| z | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS UID",
  "address": "ADDRESS IN ONE LINE SEPERATED BY COMMAS",
  "a": "ADDRESS LINE ONE",
  "sa": "ADDRESS LINE TWO",
  "c": "CITY OR PROVINCE",
  "s": "STATE OR REGION",
  "z": "ZIPCODE"
}
```



## <a name="https://api.rest.sh/api/security/waf/configure_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/waf/configureRequest") https://api.rest.sh/api/security/waf/configureRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| origin | string |  ``` Required ```  | TODO: Add a property description | 
| cname | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "name": "WHAT YOU WISH TO NAME YOUR WAF",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
}
```



## <a name="https://api.rest.sh/api/security/waf_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/wafRequest") https://api.rest.sh/api/security/wafRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| origin | string |  ``` Required ```  | TODO: Add a property description | 
| cname | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "origin": "ORIGIN YOU WISH TO PROTECT",
  "cname": "CNAMES YOU WISH TO USE WITH YOUR WAF"
}
```



## <a name="info17"></a>![Type: ](https://apidocs.io/img/method.png "Info17") Info17



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| realname | string |  ``` Required ```  | TODO: Add a property description | 
| displayname | string |  ``` Required ```  | TODO: Add a property description | 
| avatar | string |  ``` Required ```  | TODO: Add a property description | 
| email | string |  ``` Required ```  | TODO: Add a property description | 
| address | string |  ``` Required ```  | TODO: Add a property description | 
| address1 | string |  ``` Required ```  | TODO: Add a property description | 
| address2 | string |  ``` Required ```  | TODO: Add a property description | 
| city | string |  ``` Required ```  | TODO: Add a property description | 
| state | string |  ``` Required ```  | TODO: Add a property description | 
| zipcode | string |  ``` Required ```  | TODO: Add a property description | 
| phone | string |  ``` Required ```  | TODO: Add a property description | 
| lastlogin | string |  ``` Required ```  | TODO: Add a property description | 
| ip | string |  ``` Required ```  | TODO: Add a property description | 
| 2fa | string |  ``` Required ```  | TODO: Add a property description | 
| iplock | string |  ``` Required ```  | TODO: Add a property description | 



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



## <a name="https://api.rest.sh/api/security/encryption_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/encryptionResponse") https://api.rest.sh/api/security/encryptionResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| data | string |  ``` Required ```  | TODO: Add a property description | 
| file | string |  ``` Required ```  | TODO: Add a property description | 
| success | string |  ``` Required ```  | TODO: Add a property description | 
| public | string |  ``` Required ```  | TODO: Add a property description | 
| private | string |  ``` Required ```  | TODO: Add a property description | 



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



## <a name="https://api.rest.sh/api/security/encryption_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/encryptionRequest") https://api.rest.sh/api/security/encryptionRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| data | string |  ``` Required ```  | TODO: Add a property description | 
| file | string |  ``` Required ```  | TODO: Add a property description | 
| method | string |  ``` Required ```  | TODO: Add a property description | 
| bit | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "data": "DATA YOU WISH TO ENCRYPT",
  "file": "FILE YOU WISH TO ENCRYPT",
  "method": "SINGLE OR MULTIPLE ENCRYPTION TYPES TO APPLY TO DATA OR FILES SEPERATED BY A COMMA (DES, RSA, BLOWFISH, TWOFISH, AES, IDEA, PGP)",
  "bit": "SIZE OF ENCRYPTION KEY"
}
```



## <a name="https://api.rest.sh/api/service/cdn/push_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/cdn/pushRequest") https://api.rest.sh/api/service/cdn/pushRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| cname | string |  ``` Required ```  | TODO: Add a property description | 
| file | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "cname": "DOMAIN OR DOMAINS YOU WISH TO ALLOW CNAME ACCESS SEPERATED BY A COMMA",
  "file": "FILE OR FILES YOU WISH TO UPLOAD SEPERATED BY A COMMA"
}
```



## <a name="https://api.rest.sh/api/service/cdn/pull_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/cdn/pullRequest") https://api.rest.sh/api/service/cdn/pullRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| origin | string |  ``` Required ```  | TODO: Add a property description | 
| cname | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "origin": "ORIGIN DOMAIN TO PULL ASSETS FROM",
  "cname": "DOMAIN OR DOMAINS YOU WISH TO ALLOW CNAME ACCESS SEPERATED BY A COMMA"
}
```



## <a name="https://api.rest.sh/api/user/update_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/user/updateRequest") https://api.rest.sh/api/user/updateRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| user | string |  ``` Required ```  | TODO: Add a property description | 
| apiuid | string |  ``` Required ```  | TODO: Add a property description | 
| oldpassword | string |  ``` Required ```  | TODO: Add a property description | 
| newpassword | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| email | string |  ``` Required ```  | TODO: Add a property description | 
| phone | string |  ``` Required ```  | TODO: Add a property description | 
| avatar | string |  ``` Required ```  | TODO: Add a property description | 
| countrycode | string |  ``` Required ```  | TODO: Add a property description | 
| address | string |  ``` Required ```  | TODO: Add a property description | 
| a | string |  ``` Required ```  | TODO: Add a property description | 
| sa | string |  ``` Required ```  | TODO: Add a property description | 
| c | string |  ``` Required ```  | TODO: Add a property description | 
| s | string |  ``` Required ```  | TODO: Add a property description | 
| z | string |  ``` Required ```  | TODO: Add a property description | 
| custom-input | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "apiuid": "USERS API SIDE USER ID",
  "oldpassword": "SEND A ENCRYPTED VERSION OF YOUR USERS CURRENT PASSWORD USING THE PRIVATE KEY ON YOUR DASHBOARD",
  "newpassword": "SEND A ENCRYPTED VERSION OF YOUR USERS NEW PASSWORD USING THE PRIVATE KEY ON YOUR DASHBOARD",
  "name": "USERS REAL NAME",
  "email": "USERS EMAIL",
  "phone": "USERS CELL PHONE NUMBER",
  "avatar": "UPDATE USER AVATAR",
  "countrycode": "USERS CELL PHONE COUNTRY CODE",
  "address": "ADDRESS IN ONE LINE SEPERATED BY COMMAS",
  "a": "ADDRESS LINE ONE",
  "sa": "ADDRESS LINE TWO",
  "c": "CITY OR PROVINCE",
  "s": "STATE OR REGION",
  "z": "ZIPCODE",
  "custom-input": "ADD CUSTOM DATA/INPUTS TO YOUR USERS PROFILE"
}
```



## <a name="https://api.rest.sh/api/service/dns/configure_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/dns/configureRequest") https://api.rest.sh/api/service/dns/configureRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| domain | string |  ``` Required ```  | TODO: Add a property description | 
| records | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "domain": "DOMAINS TO SET DNS RECORDS",
  "records": "RECORDS TO SET TO DOMAIN"
}
```



## <a name="data"></a>![Type: ](https://apidocs.io/img/method.png "Data") Data



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| result | string |  ``` Required ```  | TODO: Add a property description | 
| content | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "result": "result",
  "content": "content",
  "id": "id"
}
```



## <a name="log"></a>![Type: ](https://apidocs.io/img/method.png "Log") Log



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| MMDDYYYYHHMMSSX | [MMDDYYYYHHMMSS](#mmddyyyyhhmmss) |  ``` Required ```  | TODO: Add a property description | 
| MMDDYYYYHHMMSSY | [MMDDYYYYHHMMSS](#mmddyyyyhhmmss) |  ``` Required ```  | TODO: Add a property description | 



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



## <a name="nameservers"></a>![Type: ](https://apidocs.io/img/method.png "Nameservers") Nameservers



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| ns1 | string |  ``` Required ```  | TODO: Add a property description | 
| ns2 | string |  ``` Required ```  | TODO: Add a property description | 
| ns3 | string |  ``` Required ```  | TODO: Add a property description | 
| ns4 | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "ns1": "ns1",
  "ns2": "ns2",
  "ns3": "ns3",
  "ns4": "ns4"
}
```



## <a name="https://api.rest.sh/api/service/hosting_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/hostingResponse") https://api.rest.sh/api/service/hostingResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | TODO: Add a property description | 
| url | string |  ``` Required ```  | TODO: Add a property description | 
| success | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "url": "RETURNED APP HOSTING URL",
  "success": "RETURNS TRUE IF APP WAS SUCCESSFULLY DEPLOYED",
  "id": "TRANSACTION ID"
}
```



## <a name="https://api.rest.sh/api/security/waf/configure_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/waf/configureResponse") https://api.rest.sh/api/security/waf/configureResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | TODO: Add a property description | 
| rule | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "success": "SHOWS TRUE WHEN THE WAF AND ORIGIN SHIELD (DDOS PROTECTION) IS DEPLOYED SUCCESSFULLY",
  "rule": "RULES APPLIED TO WAF"
}
```



## <a name="https://api.rest.sh/api/auth/user/register_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/auth/user/registerRequest") https://api.rest.sh/api/auth/user/registerRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| user | string |  ``` Required ```  | TODO: Add a property description | 
| password | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| email | string |  ``` Required ```  | TODO: Add a property description | 
| phone | string |  ``` Required ```  | TODO: Add a property description | 
| countrycode | string |  ``` Required ```  | TODO: Add a property description | 
| address | string |  ``` Required ```  | TODO: Add a property description | 
| a | string |  ``` Required ```  | TODO: Add a property description | 
| sa | string |  ``` Required ```  | TODO: Add a property description | 
| c | string |  ``` Required ```  | TODO: Add a property description | 
| s | string |  ``` Required ```  | TODO: Add a property description | 
| z | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "password": "SEND A ENCRYPTED VERSION OF YOUR USERS PASSWORD USING THE PRIVATE KEY ON YOUR DASHBOARD",
  "name": "USERS REAL NAME",
  "email": "USERS EMAIL",
  "phone": "USERS CELL PHONE NUMBER",
  "countrycode": "USERS CELL PHONE COUNTRY CODE",
  "address": "ADDRESS IN ONE LINE SEPERATED BY COMMAS",
  "a": "ADDRESS LINE ONE",
  "sa": "ADDRESS LINE TWO",
  "c": "CITY OR PROVINCE",
  "s": "STATE OR REGION",
  "z": "ZIPCODE"
}
```



## <a name="https://api.rest.sh/api/security/waf_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/wafResponse") https://api.rest.sh/api/security/wafResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | TODO: Add a property description | 
| cname | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "success": "SHOWS TRUE WHEN THE WAF AND ORIGIN SHIELD (DDOS PROTECTION) IS DEPLOYED SUCCESSFULLY",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```



## <a name="https://api.rest.sh/api/service/obfuscation_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/obfuscationResponse") https://api.rest.sh/api/service/obfuscationResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | TODO: Add a property description | 
| app | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "success": "RETURNS TRUE IF APP WAS SUCCESSFULLY OBFUSCTATED AND PROTECTED",
  "app": "OBFUSCATED APP URL"
}
```



## <a name="https://api.rest.sh/api/service/hosting_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/hostingRequest") https://api.rest.sh/api/service/hostingRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| app | string |  ``` Required ```  | TODO: Add a property description | 
| domain | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "app": "APP GIT URL OR URL CONTAINING YOUR APP IN A ZIP FILE",
  "domain": "ALLOWED DOMAIN NAMES SEPERATED BY A COMMA TO CNAME WITH ACCESS TO HOSTED APP"
}
```



## <a name="https://api.rest.sh/api/data_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/dataResponse") https://api.rest.sh/api/dataResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | TODO: Add a property description | 
| url | string |  ``` Required ```  | TODO: Add a property description | 
| success | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "url": "RETURNED DATA URL",
  "success": "RETURNS TRUE IF DATA MANIPULATION WAS SUCCESSFULL",
  "id": "TRANSACTION ID"
}
```



## <a name="https://api.rest.sh/api/service/obfuscation_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/obfuscationRequest") https://api.rest.sh/api/service/obfuscationRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| app | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "app": "APP GIT URL or URL CONTAINING YOUR APP IN A ZIP FILE"
}
```



## <a name="https://api.rest.sh/api/image_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/imageResponse") https://api.rest.sh/api/imageResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | TODO: Add a property description | 
| url | string |  ``` Required ```  | TODO: Add a property description | 
| success | string |  ``` Required ```  | TODO: Add a property description | 
| moderated | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 



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



## <a name="https://api.rest.sh/api/image_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/imageRequest") https://api.rest.sh/api/imageRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| image | string |  ``` Required ```  | TODO: Add a property description | 
| transform | string |  ``` Required ```  | TODO: Add a property description | 
| moderate | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "image": "DIRECT IMAGE URL OR CLIENT UPLOAD",
  "transform": "IMAGE MANIPULATION DIRECTIVES",
  "moderate": "SET TO TRUE IF YOU WISH TO AUTOMATICALLT CENSOR GRAPHIC IMAGES"
}
```



## <a name="info"></a>![Type: ](https://apidocs.io/img/method.png "Info") Info



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| apiuid | string |  ``` Required ```  | TODO: Add a property description | 
| realname | string |  ``` Required ```  | TODO: Add a property description | 
| displayname | string |  ``` Required ```  | TODO: Add a property description | 
| avatar | string |  ``` Required ```  | TODO: Add a property description | 
| email | string |  ``` Required ```  | TODO: Add a property description | 
| address | string |  ``` Required ```  | TODO: Add a property description | 
| phone | string |  ``` Required ```  | TODO: Add a property description | 
| lastlogin | string |  ``` Required ```  | TODO: Add a property description | 
| ip | string |  ``` Required ```  | TODO: Add a property description | 
| 2fa | string |  ``` Required ```  | TODO: Add a property description | 
| iplock | string |  ``` Required ```  | TODO: Add a property description | 



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



## <a name="https://api.rest.sh/api/2fa/token_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/2fa/tokenRequest") https://api.rest.sh/api/2fa/tokenRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| user | string |  ``` Required ```  | TODO: Add a property description | 
| code | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS UID",
  "code": "USER INPUTTED TOKEN"
}
```



## <a name="https://api.rest.sh/api/2fa_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/2faResponse") https://api.rest.sh/api/2faResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | TODO: Add a property description | 
| to | string |  ``` Required ```  | TODO: Add a property description | 
| verified | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "to": "USER BEING VERIFIED",
  "verified": "RETURNS TRUE OR FALSE",
  "id": "TRANSACTION ID"
}
```



## <a name="https://api.rest.sh/api/verify/user_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/verify/userRequest") https://api.rest.sh/api/verify/userRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| user | string |  ``` Required ```  | TODO: Add a property description | 
| code | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS UID",
  "code": "USER INPUTTED TOKEN"
}
```



## <a name="https://api.rest.sh/api/service/cdn/push_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/cdn/pushResponse") https://api.rest.sh/api/service/cdn/pushResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | TODO: Add a property description | 
| upload | string |  ``` Required ```  | TODO: Add a property description | 
| cname | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "success": "SHOWS TRUE WHEN PUSH ZONE IS DEPLOYED SUCCESSFULLY",
  "upload": "LIST OF FILES UPLOADED TO YOUR PUSH ZONE",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```



## <a name="https://api.rest.sh/api/service/cdn/pull_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/cdn/pullResponse") https://api.rest.sh/api/service/cdn/pullResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | TODO: Add a property description | 
| cname | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "success": "SHOWS TRUE WHEN PULL ZONE IS DEPLOYED SUCCESSFULLY",
  "cname": "RECORD TO APPEND YOUR URLS TO VIA A CNAME"
}
```



## <a name="https://api.rest.sh/api/verify_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/verifyResponse") https://api.rest.sh/api/verifyResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | TODO: Add a property description | 
| to | string |  ``` Required ```  | TODO: Add a property description | 
| verified | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "to": "USER BEING VERIFIED",
  "verified": "RETURNS TRUE OR FALSE",
  "id": "TRANSACTION ID"
}
```



## <a name="https://api.rest.sh/api/user/delete_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/user/deleteRequest") https://api.rest.sh/api/user/deleteRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| user | string |  ``` Required ```  | TODO: Add a property description | 
| apiuid | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "apiuid": "USERS API SIDE USER ID"
}
```



## <a name="https://api.rest.sh/api/service/dns/configure_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/dns/configureResponse") https://api.rest.sh/api/service/dns/configureResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | TODO: Add a property description | 
| domain | string |  ``` Required ```  | TODO: Add a property description | 
| records | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "success": "SHOWS TRUE IF RECORDS WERE SUCCESSFULLY SET",
  "domain": "DOMAIN",
  "records": "RECORDS SET TO DOMAIN"
}
```



## <a name="https://api.rest.sh/api/user/info_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/user/infoResponse") https://api.rest.sh/api/user/infoResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| apiuid | string |  ``` Required ```  | TODO: Add a property description | 
| verified | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 
| info | [Info17](#info17) |  ``` Required ```  | TODO: Add a property description | 



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



## <a name="https://api.rest.sh/api/service/dns/add_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/dns/addResponse") https://api.rest.sh/api/service/dns/addResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| domain | string |  ``` Required ```  | TODO: Add a property description | 
| nameservers | [Nameservers](#nameservers) |  ``` Required ```  | TODO: Add a property description | 



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



## <a name="https://api.rest.sh/api/user/info_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/user/infoRequest") https://api.rest.sh/api/user/infoRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| user | string |  ``` Required ```  | TODO: Add a property description | 
| apiuid | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "apiuid": "USERS API SIDE USER ID"
}
```



## <a name="https://api.rest.sh/api/service/dns/add_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/service/dns/addRequest") https://api.rest.sh/api/service/dns/addRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| domain | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "domain": "DOMAINS SEPERATED BY A COMMA TO ADD TO DNS"
}
```



## <a name="info12"></a>![Type: ](https://apidocs.io/img/method.png "Info12") Info12



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| apiuid | string |  ``` Required ```  | TODO: Add a property description | 
| avatar | string |  ``` Required ```  | TODO: Add a property description | 
| custom-input | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "uid": "uid",
  "apiuid": "apiuid",
  "avatar": "avatar",
  "custom-input": "custom-input"
}
```



## <a name="https://api.rest.sh/api/user/update_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/user/updateResponse") https://api.rest.sh/api/user/updateResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | TODO: Add a property description | 
| updated | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 
| info | [Info12](#info12) |  ``` Required ```  | TODO: Add a property description | 



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



## <a name="https://api.rest.sh/api/2fa/token_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/2fa/tokenResponse") https://api.rest.sh/api/2fa/tokenResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | TODO: Add a property description | 
| correct | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "correct": "RETURNS IF 2FA TOKEN IS CORRECT",
  "id": "TRANSACTION ID"
}
```



## <a name="https://api.rest.sh/api/2fa_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/2faRequest") https://api.rest.sh/api/2faRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| to | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "to": "USERS UID"
}
```



## <a name="info7"></a>![Type: ](https://apidocs.io/img/method.png "Info7") Info7



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| apiuid | string |  ``` Required ```  | TODO: Add a property description | 
| realname | string |  ``` Required ```  | TODO: Add a property description | 
| displayname | string |  ``` Required ```  | TODO: Add a property description | 
| email | string |  ``` Required ```  | TODO: Add a property description | 
| address | string |  ``` Required ```  | TODO: Add a property description | 
| phone | string |  ``` Required ```  | TODO: Add a property description | 



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



## <a name="https://api.rest.sh/api/verify/address_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/verify/addressResponse") https://api.rest.sh/api/verify/addressResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | TODO: Add a property description | 
| active | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "active": "RETURNS TRUE, IF ADDRESS IS ACTIVE AND IF USER IS CURRENTLY THERE",
  "id": "TRANSACTION ID"
}
```



## <a name="https://api.rest.sh/api/auth/user/register_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/auth/user/registerResponse") https://api.rest.sh/api/auth/user/registerResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | TODO: Add a property description | 
| active | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 
| info | [Info7](#info7) |  ``` Required ```  | TODO: Add a property description | 



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



## <a name="https://api.rest.sh/api/verify/user_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/verify/userResponse") https://api.rest.sh/api/verify/userResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | TODO: Add a property description | 
| correct | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "correct": "RETURNS IF 2FA TOKEN IS CORRECT",
  "id": "TRANSACTION ID"
}
```



## <a name="https://api.rest.sh/api/auth/user/login_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/auth/user/loginResponse") https://api.rest.sh/api/auth/user/loginResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| valid | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 
| info | [Info](#info) |  ``` Required ```  | TODO: Add a property description | 



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



## <a name="mmddyyyyhhmmss"></a>![Type: ](https://apidocs.io/img/method.png "MMDDYYYYHHMMSS") MMDDYYYYHHMMSS



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| data | [Data](#data) |  ``` Required ```  | TODO: Add a property description | 



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



## <a name="https://api.rest.sh/api/auth/user/login_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/auth/user/loginRequest") https://api.rest.sh/api/auth/user/loginRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| user | string |  ``` Required ```  | TODO: Add a property description | 
| password | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "user": "USERS EMAIL OR USERNAME",
  "password": "SEND A ENCRYPTED VERSION OF YOUR USERS PASSWORD USING THE PRIVATE KEY ON YOUR DASHBOARD"
}
```



## <a name="https://api.rest.sh/api/security/logging/info_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/logging/infoResponse") https://api.rest.sh/api/security/logging/infoResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| log | [Log](#log) |  ``` Required ```  | TODO: Add a property description | 



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



## <a name="https://api.rest.sh/api/verify_request"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/verifyRequest") https://api.rest.sh/api/verifyRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| key | string |  ``` Required ```  | TODO: Add a property description | 
| uid | string |  ``` Required ```  | TODO: Add a property description | 
| to | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "key": "YOUR API KEY",
  "uid": "YOUR USER ID",
  "to": "USERS UID"
}
```



## <a name="https://api.rest.sh/api/security/logging_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/security/loggingResponse") https://api.rest.sh/api/security/loggingResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| success | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "success": "RETURNS TRUE IF ADVANCED LOGGING IS ACTIVATED"
}
```



## <a name="https://api.rest.sh/api/user/delete_response"></a>![Type: ](https://apidocs.io/img/method.png "https://api.rest.sh/api/user/deleteResponse") https://api.rest.sh/api/user/deleteResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| request | string |  ``` Required ```  | TODO: Add a property description | 
| deleted | string |  ``` Required ```  | TODO: Add a property description | 
| id | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "request": "REQUEST TYPE",
  "deleted": "RETURNS TRUE, IF USERS ACCOUNT WAS SUCCESSFULLY DELETED",
  "id": "TRANSACTION ID"
}
```




