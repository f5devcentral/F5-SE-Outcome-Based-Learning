Input validation
================

**Objective**: 

Enable input validation with NGINX

**Why**: 

- Do not trust input parameters/objects.
- Validate input: length / range / format and type.
- Achieve an implicit input validation by using strong types like numbers, booleans, dates, times or fixed data ranges in API parameters.
- Constrain string inputs with regexps.
- Reject unexpected/illegal content.
- Make use of validation/sanitation libraries or frameworks in your specific language.
- Define an appropriate request size limit and reject requests exceeding the limit with HTTP response status 413 Request Entity Too Large.
- Consider logging input validation failures. Assume that someone who is performing hundreds of failed input validations per second is up to no good.
- Use a secure parser for parsing the incoming messages. If you are using XML, make sure to use a parser that is not vulnerable to XXE and similar attacks.

**How**:

API requests can send and receive data via the content body (request/response), uris and codes. NGINX can parse bodies, uris and generate custom response codes. After a parse, NGINX can deny the request/response, translate, or give directions to the API client with custom codes. The NJS extension can be used to extend the body parsing with further actions.

.. note:: Use NGINX App Protect for enhanced security

NGINX App Protect also has Data Guard which can replace match strings and XML/JSON validation.

Example Documentation:

- https://www.nginx.com/blog/deploying-nginx-plus-as-an-api-gateway-part-2-protecting-backend-services/#request-bodies
- https://www.nginx.com/resources/wiki/extending/examples/body_filter/

NGINX Documentation:

- https://nginx.org/en/docs/njs/
- https://docs.nginx.com/nginx-app-protect/configuration-guide/configuration/#handling-xml-and-json-content
- https://docs.nginx.com/nginx-app-protect/