Error handling
==============

**Objective**: 

Enable error handling with NGINX

**Why**: 

- Respond with generic error messages - avoid revealing details of the failure unnecessarily.
- Do not pass technical details (e.g. call stacks or other internal hints) to the client.

**How**:

.. note:: Most proxy pass solutions require a Host header to be added since NGINX defaults to passing the original Host header.

Example Documentation:

- https://www.nginx.com/blog/creating-nginx-rewrite-rules/
- https://www.nginx.com/resources/wiki/modules/substitutions/

NGINX Documentation:

- http://nginx.org/en/docs/http/ngx_http_rewrite_module.html#return
- http://nginx.org/en/docs/http/ngx_http_sub_module.html