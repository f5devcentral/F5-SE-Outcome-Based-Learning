Error handling
==============

**Objective**: 

Enable error handling with NGINX

**Why**: 

- Respond with generic error messages - avoid revealing details of the failure unnecessarily.
- Do not pass technical details (e.g. call stacks or other internal hints) to the client.

**How**:

As an API Gateway NGINX sees traffic from both perspectives of the client and upstreams (servers). The upstream might send a generic response code and or generic errors. When NGINX notices this we can replace that code with something more API friendly and also modify or remove the content. If the client is trying to access a route that is not allowed NGINX can simply return a code and body notifying the client.

Example Documentation:

- https://www.nginx.com/blog/creating-nginx-rewrite-rules/
- https://www.nginx.com/resources/wiki/modules/substitutions/

NGINX Documentation:

- http://nginx.org/en/docs/http/ngx_http_rewrite_module.html#return
- http://nginx.org/en/docs/http/ngx_http_sub_module.html