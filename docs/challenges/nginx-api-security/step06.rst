Access Control
==============

**Objective**: 

Enable Access Controls with NGINX

**Why**: 

Non-public REST services must perform access control at each API endpoint. Web services in monolithic applications implement this by means of user authentication, authorization logic and session management. This has several drawbacks for modern architectures which compose multiple microservices following the RESTful style

In order to minimize latency and reduce coupling between services, the access control decision should be taken locally by REST endpoints
user authentication should be centralised in a Identity Provider (IdP), which issues access tokens

**How**:

https://github.com/nginxinc/nginx-openid-connect