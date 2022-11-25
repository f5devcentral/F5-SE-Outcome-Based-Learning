F5 NGINX API Security
=====================

**Introduction**

A foundational element of innovation in todays app-driven world is the API. From banks, retail and transportation to IoT, autonomous vehicles and smart cities, APIs are a critical part of modern mobile, SaaS and web applications and can be found in customer-facing, partner-facing and internal applications. By nature, APIs expose application logic and sensitive data such as Personally Identifiable Information (PII) and because of this have increasingly become a target for attackers. Without secure APIs, rapid innovation would be impossible.

API Security focuses on strategies and solutions to understand and mitigate the unique vulnerabilities and security risks of Application Programming Interfaces (APIs).

Source: https://owasp.org/www-project-api-security/

**Learning Objectives**

As the leading high-performance, lightweight reverse proxy and load balancer, NGINX has the advanced HTTP processing capabilities needed for handling API traffic. This makes NGINX the ideal platform with which to build an API gateway. In this blog post we describe a number of common API gateway use cases and show how to configure NGINX to handle them in a way that is efficient, scalable, and easy to maintain. We describe a complete configuration, which can form the basis of a production deployment.

Many configuration examples of NGINX as an API Gateway (including security), can be found in a three-part series from Liam Crilly:

- https://www.nginx.com/blog/deploying-nginx-plus-as-an-api-gateway-part-1/
- https://www.nginx.com/blog/deploying-nginx-plus-as-an-api-gateway-part-2-protecting-backend-services/
- https://www.nginx.com/blog/deploying-nginx-plus-as-an-api-gateway-part-3-publishing-grpc-services/

.. warning:: This challenge requires the base environment

.. warning:: Estimated completion time 2+ hours

.. toctree::
   :maxdepth: 1
   :glob:

   step*