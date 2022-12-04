HTTPS
=====

**Objective**: 

Enable HTTPS with NGINX

**Why**: 

Secure REST services must only provide HTTPS endpoints. This protects authentication credentials in transit, for example passwords, API keys or JSON Web Tokens. It also allows clients to authenticate the service and guarantees integrity of the transmitted data

Consider the use of mutually authenticated client-side certificates to provide additional protection for highly privileged web services

**How**:

NGINX utilizes TLS certificates that are available based on a local path. NGINX TLS is dependent on the version of SSL (typically OpenSSL) installed in the operating system. TLS certificates are referenced in NGINX configuration with a local path, preference of storing certificates together or at a more application-specific design pattern are both valid.

.. note:: Most proxy pass solutions require a Host header to be added since NGINX defaults to passing the original Host header.

Example Documentation:

- https://www.nginx.com/blog/nginx-ssl/
- https://www.nginx.com/blog/using-free-ssltls-certificates-from-lets-encrypt-with-nginx/
- https://www.nginx.com/nginxconf/2019/session/mtls-nginx/
- https://www.nginx.com/blog/improving-nginx-performance-with-kernel-tls/

NGINX Documentation:

- http://nginx.org/en/docs/http/configuring_https_servers.html
- https://docs.nginx.com/nginx/admin-guide/security-controls/terminating-ssl-http/