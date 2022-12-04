Audit logs
==========

**Objective**: 

Enable audit logs with NGINX

**Why**: 

- Write audit logs before and after security related events.
- Consider logging token validation errors in order to detect attacks.
- Take care of log injection attacks by sanitizing log data beforehand.

**How**:

NGINX has three main forms of logs, access, error, and security; access and error logs can be stored at a local location like (/var/log), or be streamed to a syslog endpoint. NGINX Security logs from NGINX App Protect should be streamed syslog to an endpoint.

.. note:: Use NGINX App Protect for enhanced security logging and sensitive parameters

Example Documentation:

- https://www.nginx.com/resources/webinars/analyzing-nginx-logs-datadog
- https://www.nginx.com/blog/operational-intelligence-nginx-plus-splunk-enterprise
- https://nginx.org/en/docs/syslog.html

NGINX Documentation:

- https://docs.nginx.com/nginx/admin-guide/monitoring/logging
- https://docs.nginx.com/nginx/admin-guide/monitoring/live-activity-monitoring
- http://nginx.org/en/docs/http/ngx_http_log_module.html
- https://nginx.org/en/docs/http/ngx_http_session_log_module.html
- https://nginx.org/en/docs/stream/ngx_stream_log_module.html
- https://docs.nginx.com/nginx-app-protect/logging-overview/security-log/
- https://docs.nginx.com/nginx-app-protect/declarative-policy/policy/#policy/sensitive-parameters