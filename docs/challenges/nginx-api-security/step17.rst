HTTP Return Code
================

**Objective**: 

Set HTTP Return Codes with NGINX

**Why**: 

HTTP defines status code. When designing REST API, dont just use 200 for success or 404 for error. Always use the semantically appropriate status code for the response.

Here is a non-exhaustive selection of security related REST API status codes. Use it to ensure you return the correct code.

+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Code | Message                | Description                                                                                                                                                                                                       |
+======+========================+===================================================================================================================================================================================================================+
| 200  | OK                     | Response to a successful REST API action. The HTTP method can be GET, POST, PUT, PATCH or DELETE.                                                                                                                 |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 201  | Created                | The request has been fulfilled and resource created. A URI for the created resource is returned in the Location header.                                                                                           |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 202  | Accepted               | The request has been accepted for processing, but processing is not yet complete.                                                                                                                                 |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 301  | Moved Permanently      | Permanent                                                                                                                                                                                                         |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 304  | Not Modified           | Caching related response that returned when the client has the same copy of the resource as the server.                                                                                                           |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 307  | Temporary Redirect     | Temporary redirection of resource.                                                                                                                                                                                |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 400  | Bad Request            | The request is malformed, such as message body format error.                                                                                                                                                      |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 401  | Unauthorized           | Wrong or no authentication ID/password provided.                                                                                                                                                                  |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 403  | Forbidden              | Its used when the authentication succeeded but authenticated user doesnt have permission to the request resource.                                                                                                 |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 404  | Not Found              | When a non-existent resource is requested.                                                                                                                                                                        |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 405  | Method Not Acceptable  | The error for an unexpected HTTP method. For example, the REST API is expecting HTTP GET, but HTTP PUT is used.                                                                                                   |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 406  | Unacceptable           | The client presented a content type in the Accept header which is not supported by the server API.                                                                                                                |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 413  | Payload too large      | Use it to signal that the request size exceeded the given limit e.g. regarding file uploads.                                                                                                                      |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 415  | Unsupported Media Type | The requested content type is not supported by the REST service.                                                                                                                                                  |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 429  | Too Many Requests      | The error is used when there may be DOS attack detected or the request is rejected due to rate limiting.                                                                                                          |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 500  | Internal Server Error  | An unexpected condition prevented the server from fulfilling the request. Be aware that the response should not reveal internal information that helps an attacker, e.g. detailed error messages or stack traces. |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 501  | Not Implemented        | The REST service does not implement the requested operation yet.                                                                                                                                                  |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 503  | Service Unavailable    | The REST service is temporarily unable to process the request. Used to inform the client it should retry at a later time.                                                                                         |
+------+------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

**How**:

NGINX API Gateway configuration is the definition of routes accessible, in each of those routes can specifically set a response code and custom body. In NGINX App Protect there is also the ability to import an OpenAPI/Swagger file, which can contain response codes and bodies.

.. note:: Most proxy pass solutions require a Host header to be added since NGINX defaults to passing the original Host header.

.. note:: Use NGINX App Protect for enhanced security

Example Documentation:

- https://www.nginx.com/blog/creating-nginx-rewrite-rules/

NGINX Documentation:

- https://docs.nginx.com/nginx-app-protect/declarative-policy/policy/#policy/response-pages
- http://nginx.org/en/docs/http/ngx_http_rewrite_module.html#return
- https://docs.nginx.com/nginx-app-protect/declarative-policy/policy/#policy/open-api-files