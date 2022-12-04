Sensitive information in HTTP requests
======================================

**Objective**: 

Disable Sensitive information in HTTP requests with NGINX

**Why**: 

RESTful web services should be careful to prevent leaking credentials. Passwords, security tokens, and API keys should not appear in the URL, as this can be captured in web server logs, which makes them intrinsically valuable.

In POST/PUT requests sensitive data should be transferred in the request body or request headers.
In GET requests sensitive data should be transferred in an HTTP Header.

OK::

  https://example.com/resourceCollection/[ID]/action
  https://twitter.com/vanderaj/lists

NOT OK (because API Key is into the URL)::

  https://example.com/controller/123/action?apiKey=a53f435643de32

**How**:

Utilizing a regex match string(s) within a location can stop traffic and respond with a custom HTTP code. NGINX location blocks are read downward, similar to a firewall except it is layer 7 logic. So if a match happens more specifically the traffic is complete. 

Example Documentation:

- https://www.nginx.com/blog/creating-nginx-rewrite-rules/
- https://www.nginx.com/resources/wiki/start/topics/depth/ifisevil/

.. note:: Use NGINX App Protect for enhanced security

NGINX Documentation:

- http://nginx.org/en/docs/http/ngx_http_proxy_module.html#proxy_pass
- http://nginx.org/en/docs/http/ngx_http_proxy_module.html#proxy_pass_header
- https://docs.nginx.com/nginx-app-protect/declarative-policy/policy/#policy/sensitive-parameters
- https://docs.nginx.com/nginx-app-protect/declarative-policy/policy/#policy/data-guard