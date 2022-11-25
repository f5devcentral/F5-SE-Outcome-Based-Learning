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

Example Documentation:

- https://hub.docker.com/r/nginxinc/nginx-unprivileged

NGINX Documentation:

- https://docs.nginx.com/nginx/admin-guide/monitoring/live-activity-monitoring/#configuring-the-api