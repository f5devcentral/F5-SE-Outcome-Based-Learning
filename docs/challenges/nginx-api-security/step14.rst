Security Headers
================

**Objective**: 

Enable security headers with NGINX

**Why**: 

There are a number of security related headers that can be returned in the HTTP responses to instruct browsers to act in specific ways. However, some of these headers are intended to be used with HTML responses, and as such may provide little or no security benefits on an API that does not return HTML.

The following headers should be included in all API responses:

Header	Rationale
Cache-Control: no-store	Prevent sensitive information from being cached.
Content-Security-Policy: frame-ancestors 'none'	To protect against drag-and-drop style clickjacking attacks.
Content-Type	To specify the content type of the response. This should be application/json for JSON responses.
Strict-Transport-Security	To require connections over HTTPS and to protect against spoofed certificates.
X-Content-Type-Options: nosniff	To prevent browsers from performing MIME sniffing, and inappropriately interpreting responses as HTML.
X-Frame-Options: DENY	To protect against drag-and-drop style clickjacking attacks.
The headers below are only intended to provide additional security when responses are rendered as HTML. As such, if the API will never return HTML in responses, then these headers may not be necessary. However, if there is any uncertainty about the function of the headers, or the types of information that the API returns (or may return in future), then it is recommended to include them as part of a defence-in-depth approach.

Header	Rationale
Content-Security-Policy: default-src 'none'	The majority of CSP functionality only affects pages rendered as HTML.
Feature-Policy: 'none'	Feature policies only affect pages rendered as HTML.
Referrer-Policy: no-referrer	Non-HTML responses should not trigger additional requests.

**How**:

https://content-security-policy.com/examples/nginx/
http://nginx.org/en/docs/http/ngx_http_headers_module.html