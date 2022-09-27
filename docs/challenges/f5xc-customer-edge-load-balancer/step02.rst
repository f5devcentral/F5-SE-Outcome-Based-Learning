F5XC Customer Edge Origin Pool
==============================

**Objective**:

Create an Origin Pool(s) with the private ip addresses of the dual NGINX Application Servers

**Why**:

Creating origin pools of servers allows for the grouping of like applications. An F5XC load balancer can contain one, or many origin pools. The flexibility of origin pool objects allows for simple to advanced deployments, from Round-Robin to Canary, and Blue-Green.

.. note:: For even more advanced choices of origins, a **Route** can be utilized on the load balancer.

**How**:

Create an Origin Pool:

https://docs.cloud.f5.com/docs/how-to/app-networking/origin-pools

**Validation**: 

Did you create a single pool, or multiple pools, use FQDN or IP?