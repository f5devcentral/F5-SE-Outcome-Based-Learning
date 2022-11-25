Access Control
==============

**Objective**: 

Enable Access Controls with NGINX

**Why**: 

Non-public REST services must perform access control at each API endpoint. Web services in monolithic applications implement this by means of user authentication, authorization logic and session management. This has several drawbacks for modern architectures which compose multiple microservices following the RESTful style

In order to minimize latency and reduce coupling between services, the access control decision should be taken locally by REST endpoints
user authentication should be centralised in a Identity Provider (IdP), which issues access tokens

**How**:

Example Documentation:

- https://www.nginx.com/blog/authenticating-users-existing-applications-openid-connect-nginx-plus/
- https://github.com/nginxinc/nginx-openid-connect
- https://www.youtube.com/watch?v=ZbOIHc69khc

NGINX Documentation:

- https://docs.nginx.com/search.html#q=oidc&sort=relevancy&f:@f5_product=[NGINX%20Plus]