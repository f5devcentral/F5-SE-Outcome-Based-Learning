F5XC Hybrid Edge Load Balancer
==============================

**Objective**:

Create an F5XC TLS Load Balancer advertised on the F5XC backbone

In this deployment scenario, the Mesh nodes need two interfaces attached. The first interface is the outside interface through which services running on the node can connect to the Internet.

As shown in the below figure, the outside interface is on the outside subnet which is associated with the outside subnet route table, whose default route is pointing to the Internet gateway. This interface can send and receive traffic from the Internet. In case of inside subnets, these are associated with the inside subnet route table which is also the main route table for this VNet, meaning that any newly created subnet in this VNet is automatically associated with the inside subnet route table. This private subnet route table has a default route pointing to the inside IP address of the Mesh node (192.168.0.186).

|image01|

.. note:: You should use the delegated domain of your F5XC tenant, this will allow you to automatically generate a TLS certificate

**Why**:

A Hybrid Edge Load Balancer will advertise on one or many F5XC Regional Edge, but utilize the RE to CE link for the data path. This solution allows for CE reachable services to be Globally advertised on the F5XC backbone. F5XC Regional Edges have the benefit of AnyCast advertisement, allowing consumers of applications to connect to the closest RE.

**How**:

https://docs.cloud.f5.com/docs/how-to/app-networking/http-load-balancer
https://docs.cloud.f5.com/docs/how-to/advanced-app-nwg/advertise-apps-on-site-service-network

**Validation**: 

What solutions could a Global disaggregation point solve? How would we create a regional failover or advertise in certain locations? Which Regional Edge location did your testing requests originate from?

.. |image01| image:: docs/index/images/image01.png
   :width: 50%