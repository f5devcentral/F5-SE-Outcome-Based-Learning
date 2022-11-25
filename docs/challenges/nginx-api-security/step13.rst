Audit logs
==========

**Objective**: 

Enable audit logs with NGINX

**Why**: 

- Write audit logs before and after security related events.
- Consider logging token validation errors in order to detect attacks.
- Take care of log injection attacks by sanitizing log data beforehand.

**How**:

https://docs.nginx.com/nginx/admin-guide/monitoring/logging/