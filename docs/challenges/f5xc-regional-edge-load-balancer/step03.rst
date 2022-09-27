F5XC Regional Edge Load Balancer
================================

**Objective**:

Create an F5XC TLS Load Balancer advertised on the F5XC backbone

.. note:: You should use the delegated domain of your F5XC tenant, this will allow you to automatically generate a TLS certificate

**Why**:

Utilizing a Regional Edge-only solution allows for additional services above what may be available in a regional location. Disaster recovery regional targeting, or failover/migrations between environments and CSPs. For a consumer of a service that may exist in multiple locations across the internet, F5XC can provide a single target for communication.

**How**:

Create an F5XC Load Balancer:

https://docs.cloud.f5.com/docs/how-to/app-networking/http-load-balancer
https://docs.cloud.f5.com/docs/how-to/advanced-app-nwg/advertise-apps-on-site-service-network

**Validation**: 

What solutions could a Global disaggregation point solve? How would we create a regional failover or advertise in certain locations? Which Regional Edge location did your testing requests originate from?

.. |image01| image:: images/image01.png
   :width: 50%