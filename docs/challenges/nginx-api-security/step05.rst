HTTPS
=====

**Objective**: 

Enable HTTPS with NGINX

**Why**: 

Secure REST services must only provide HTTPS endpoints. This protects authentication credentials in transit, for example passwords, API keys or JSON Web Tokens. It also allows clients to authenticate the service and guarantees integrity of the transmitted data.

See the Transport Layer Protection Cheat Sheet for additional information.

Consider the use of mutually authenticated client-side certificates to provide additional protection for highly privileged web services.

**How**:

https://docs.nginx.com/nginx/admin-guide/security-controls/terminating-ssl-http/

mTLS: https://www.youtube.com/watch?v=BuDK5g49UDg