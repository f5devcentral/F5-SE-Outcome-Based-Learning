JWT
===

**Objective**: 

Enable JWT with NGINX 

**Why**: 

There seems to be a convergence towards using JSON Web Tokens (JWT) as the format for security tokens. JWTs are JSON data structures containing a set of claims that can be used for access control decisions. A cryptographic signature or message authentication code (MAC) can be used to protect the integrity of the JWT.

Ensure JWTs are integrity protected by either a signature or a MAC. Do not allow the unsecured JWTs: {"alg":"none"}.
See here
In general, signatures should be preferred over MACs for integrity protection of JWTs.
If MACs are used for integrity protection, every service that is able to validate JWTs can also create new JWTs using the same key. This means that all services using the same key have to mutually trust each other. Another consequence of this is that a compromise of any service also compromises all other services sharing the same key. See here for additional information.

The relying party or token consumer validates a JWT by verifying its integrity and claims contained.

A relying party must verify the integrity of the JWT based on its own configuration or hard-coded logic. It must not rely on the information of the JWT header to select the verification algorithm. See here and here
Some claims have been standardized and should be present in JWT used for access controls. At least the following of the standard claims should be verified:

iss or issuer - is this a trusted issuer? Is it the expected owner of the signing key?
aud or audience - is the relying party in the target audience for this JWT?
exp or expiration time - is the current time before the end of the validity period of this token?
nbf or not before time - is the current time after the start of the validity period of this token?
As JWTs contain details of the authenticated entity (user etc.) a disconnect can occur between the JWT and the current state of the users session, for example, if the session is terminated earlier than the expiration time due to an explicit logout or an idle timeout. When an explicit session termination event occurs, a digest or hash of any associated JWTs should be submitted to a block list on the API which will invalidate that JWT for any requests until the expiration of the token. See the JSON_Web_Token_for_Java_Cheat_Sheet for further details.

**How**:

JWT validation works against the proxy_pass directive. For a quick example of injecting security in front of a service proxy_pass against www.nginx.org.

.. note:: Most proxy pass solutions require a Host header to be added since NGINX defaults to passing the original Host header.

Example Documentation:

- https://www.nginx.com/blog/authenticating-api-clients-jwt-nginx-plus/
- https://github.com/nginx/njs-examples

NGINX Documentation:

- https://docs.nginx.com/nginx/admin-guide/security-controls/configuring-jwt-authentication/
- http://nginx.org/en/docs/http/ngx_http_proxy_module.html#proxy_pass
- http://nginx.org/en/docs/http/ngx_http_proxy_module.html#proxy_pass_header