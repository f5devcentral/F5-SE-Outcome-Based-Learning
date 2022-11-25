Error handling
==============

**Objective**: 

Enable error handling with NGINX

**Why**: 

Respond with generic error messages - avoid revealing details of the failure unnecessarily.
Do not pass technical details (e.g. call stacks or other internal hints) to the client.

**How**:

http://nginx.org/en/docs/http/ngx_http_rewrite_module.html#return