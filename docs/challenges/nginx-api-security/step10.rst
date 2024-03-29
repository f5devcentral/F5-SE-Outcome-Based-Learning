Validate content types
======================

**Objective**: 

Enable valid content types with NGINX

**Why**: 

A REST request or response body should match the intended content type in the header. Otherwise this could cause misinterpretation at the consumer/producer side and lead to code injection/execution.

- Document all supported content types in your API.
- Validate request content types
- Reject requests containing unexpected or missing content type headers with HTTP response status 406 Unacceptable or 415 Unsupported Media Type.
- For XML content types ensure appropriate XML parser hardening, see the XXE cheat sheet.
Avoid accidentally exposing unintended content types by explicitly defining content types e.g. Jersey (Java) @consumes(application/json); @produces(application/json). This avoids XXE-attack vectors for example.
- Send safe response content types

It is common for REST services to allow multiple response types (e.g. application/xml or application/json, and the client specifies the preferred order of response types by the Accept header in the request.

- Do NOT simply copy the Accept header to the Content-type header of the response.
- Reject the request (ideally with a 406 Not Acceptable response) if the Accept header does not specifically contain one of the allowable types.
- Services including script code (e.g. JavaScript) in their responses must be especially careful to defend against header injection attack.

Ensure sending intended content type headers in your response matching your body content e.g. application/json and not application/javascript. 

**How**:

NGINX utilizing proxy_pass can verify, and manipulate headers. For content types (Media_type or mime-types) NGINX utilizes a created referenced configuration file for allowed objects. This could be a single mime-types file or multiple.

mime-types reference::

  http {
    include /etc/nginx/mime.types;

.. note:: Use NGINX App Protect for enhanced security

Example Documentation:

- https://www.nginx.com/resources/wiki/start/topics/examples/headers_management/
- https://www.nginx.com/blog/avoiding-top-10-nginx-configuration-mistakes/
- https://en.wikipedia.org/wiki/Media_type

NGINX Documentation:

- https://www.nginx.com/resources/wiki/start/topics/examples/full/#mime-types
- https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy/
- https://nginx.org/en/docs/http/ngx_http_proxy_module.html#proxy_pass
- https://docs.nginx.com/nginx-app-protect/declarative-policy/policy/#policy/filetypes
- https://docs.nginx.com/nginx-app-protect/declarative-policy/policy/#policy/headers
