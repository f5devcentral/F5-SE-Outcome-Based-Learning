F5XC Regional Edge Origin Pool
==============================

**Objective**:

Create an Origin Pool(s) that target either:

- The public ip addresses of the application servers hosting Juice Shop
- The public facing website such as nginx.org

**Why**:

An F5XC load balancer can contain one, or many origin pools. With a regional edge load balancer, we will target externally available services. 

.. note:: For even more advanced choices of origins, a **Route** can be utilized on the load balancer.

**How**:

Create an Origin Pool:

https://docs.cloud.f5.com/docs/how-to/app-networking/origin-pools

**Validation**: 

Did you create a single pool, or multiple pools, use FQDN or IP? 