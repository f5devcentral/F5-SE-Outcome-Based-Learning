CORS
====

**Objective**: 

Enable CORS with NGINX

**Why**: 

Cross-Origin Resource Sharing (CORS) is a W3C standard to flexibly specify what cross-domain requests are permitted. By delivering appropriate CORS Headers your REST API signals to the browser which domains, AKA origins, are allowed to make JavaScript calls to the REST service.

- Disable CORS headers if cross-domain calls are not supported/expected.
- Be as specific as possible and as general as necessary when setting the origins of cross-domain calls.

**How**:

.. note:: Most proxy pass solutions require a Host header to be added since NGINX defaults to passing the original Host header.

Example Documentation:

- https://enable-cors.org/server_nginx.html

.. note:: Use NGINX App Protect for enhanced security

NGINX Documentation:

- https://docs.nginx.com/nginx-app-protect/declarative-policy/policy/