NGINX API Gateway Security
==========================

**Objective**: 

Implement security for API/Web traffic

**Why**: 

API Security focuses on strategies and solutions to understand and mitigate the unique vulnerabilities and security risks of Application Programming Interfaces (APIs)

Source: https://owasp.org/www-project-api-security

**How**:

Implement security practices recommend in the OWASP REST Security Cheat Sheet:

Source: https://cheatsheetseries.owasp.org/cheatsheets/REST_Security_Cheat_Sheet.html

NGINX Plus and OSS have many inherent security best practice tools. However, there are additional tools beyond Plus or OSS. For more all-inclusive security NGINX App Protect WAF and DDoS are available.

- https://docs.nginx.com/nginx-app-protect/
- https://docs.nginx.com/nginx-app-protect-dos/

+------------------------+
|                        |
|    NAP Feature         |
+========================+
| applicationLanguage    |
+------------------------+
| blocking-settings      |
+------------------------+
| bot-defense            |
+------------------------+
| browser-definitions    |
+------------------------+
| caseInsensitive        |
+------------------------+
| character-sets         |
+------------------------+
| cookie-settings        |
+------------------------+
| csrf-protection        |
+------------------------+
| csrf-urls              |
+------------------------+
| data-guard             |
+------------------------+
| enforcer-settings      |
+------------------------+
| general                |
+------------------------+
| grpc-profiles          |
+------------------------+
| header-settings        |
+------------------------+
| headers                |
+------------------------+
| host-names             |
+------------------------+
| idl-files              |
+------------------------+
| json-profiles          |
+------------------------+
| json-validation-files  |
+------------------------+
| methods                |
+------------------------+
| open-api-files         |
+------------------------+
| parameters             |
+------------------------+
| response-pages         |
+------------------------+
| sensitive-parameters   |
+------------------------+
| server-technologies    |
+------------------------+
| signature-requirements |
+------------------------+
| signature-sets         |
+------------------------+
| signature-settings     |
+------------------------+
| signatures             |
+------------------------+
| template               |
+------------------------+
| threat-campaigns       |
+------------------------+
| urls                   |
+------------------------+
| whitelist-ips          |
+------------------------+
| xml-profiles           |
+------------------------+

Recommended Starting Challenges

.. toctree::
   :maxdepth: 1
   :glob:

   step08
   step07
   step16

Additional Challenges

.. toctree::
   :maxdepth: 1
   :glob:

   step05
   step06
   step09
   step10
   step11
   step12
   step13
   step15
   step17

Example Documentation:

- https://www.nginx.com/blog/secure-your-api-gateway-with-nginx-app-protect-waf/