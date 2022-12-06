Access Control
==============

**Objective**: 

Enable Access Controls with NGINX

**Why**: 

Non-public REST services must perform access control at each API endpoint. Web services in monolithic applications implement this by means of user authentication, authorization logic and session management. This has several drawbacks for modern architectures which compose multiple microservices following the RESTful style

In order to minimize latency and reduce coupling between services, the access control decision should be taken locally by REST endpoints
user authentication should be centralized in a Identity Provider (IdP), which issues access tokens

**How**:

NGINX Plus API Access Controls:

.. toctree::
   :maxdepth: 1
   :glob:

   step05
   step07
   step08

NGINX OSS API Access Controls:

.. toctree::
   :maxdepth: 1
   :glob:

   step05
   step08

Example Documentation:

- https://www.nginx.com/blog/validating-oauth-2-0-access-tokens-nginx/
- https://www.nginx.com/blog/authenticating-api-clients-jwt-nginx-plus/
- https://www.nginx.com/blog/nginx-plus-authenticate-users/

NGINX Documentation:

- https://docs.nginx.com/nginx/deployment-guides/single-sign-on/
- https://docs.nginx.com/nginx/admin-guide/security-controls/configuring-subrequest-authentication/