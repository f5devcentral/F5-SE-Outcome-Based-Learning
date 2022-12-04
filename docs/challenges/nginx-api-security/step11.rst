Management endpoints
====================

**Objective**: 

Disable management endpoints on NGINX

**Why**: 

- Avoid exposing management endpoints via Internet.
- If management endpoints must be accessible via the Internet, make sure that users must use a strong authentication mechanism, e.g. multi-factor.
- Expose management endpoints via different HTTP ports or hosts preferably on a different NIC and restricted subnet.
- Restrict access to these endpoints by firewall rules or use of access control lists.

**How**:

NGINX OSS does not have a management endpoint, since the configuration is loaded from local configuration files. NGINX Plus does have an API that can be utilized with a Dashboard or API. The API should be locked down to known good addresses or local to the instance for NGINX Agents to harvest statistics.

.. note:: Both the NGINX Plus dashboard, and the API endpoint that it uses are disabled by default.

NGINX Plus Dashboard:

|image02|

NGINX Plus API and Dashboard configuration::

  server {
      listen 8080;

      location /api {
          api write=on;
          # directives limiting access to the API
      }

      location = /dashboard.html {
          root   /usr/share/nginx/html;
      }

      # Redirect requests made to the pre-NGINX Plus API dashboard
      location = /status.html {
          return 301 /dashboard.html;
      }
  }

Example Documentation:

- http://nginx.org/en/docs/http/ngx_http_access_module.html
- https://hub.docker.com/r/nginxinc/nginx-unprivileged

NGINX Documentation:

- https://docs.nginx.com/nginx/admin-guide/monitoring/live-activity-monitoring/#configuring-the-api

.. |image02| image:: images/image01.png
   :width: 50%