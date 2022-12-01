Sensitive information in HTTP requests
======================================

**Objective**: 

Disable Sensitive information in HTTP requests with NGINX

**Why**: 

RESTful web services should be careful to prevent leaking credentials. Passwords, security tokens, and API keys should not appear in the URL, as this can be captured in web server logs, which makes them intrinsically valuable.

In POST/PUT requests sensitive data should be transferred in the request body or request headers.
In GET requests sensitive data should be transferred in an HTTP Header.

OK:

- https://example.com/resourceCollection/[ID]/action
- https://twitter.com/vanderaj/lists

NOT OK:

- https://example.com/controller/123/action?apiKey=a53f435643de32 because API Key is into the URL.

**How**:

Utilizing a match on a string(s) with a location will stop traffic and respond with an invalid HTTP code.

Example Documentation:

- https://www.nginx.com/blog/creating-nginx-rewrite-rules/
- https://www.nginx.com/resources/wiki/start/topics/depth/ifisevil/

.. note:: Use NGINX App Protect for enhanced security

NGINX Documentation:

- https://docs.nginx.com/nginx-app-protect/declarative-policy/policy/#policy/sensitive-parameters
- https://docs.nginx.com/nginx-app-protect/declarative-policy/policy/#policy/data-guard