API Keys
========

**Objective**: 

Enable API Keys with NGINX

**Why**: 

Public REST services without access control run the risk of being farmed leading to excessive bills for bandwidth or compute cycles. API keys can be used to mitigate this risk. They are also often used by organisation to monetize APIs; instead of blocking high-frequency calls, clients are given access in accordance to a purchased access plan

API keys can reduce the impact of denial-of-service attacks. However, when they are issued to third-party clients, they are relatively easy to compromise

- Require API keys for every request to the protected endpoint
- Return 429 Too Many Requests HTTP response code if requests are coming in too quickly
- Revoke the API key if the client violates the usage agreement
- Do not rely exclusively on API keys to protect sensitive, critical or high-value resources

**How**:

Example Documentation:

- https://www.nginx.com/blog/authenticating-api-clients-jwt-nginx-plus/
- https://github.com/nginx/njs-examples

NGINX Documentation:

- http://nginx.org/en/docs/http/ngx_http_map_module.html