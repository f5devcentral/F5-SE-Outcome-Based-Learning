Kubernetes Load Balancer
========================

**Objective**: Create a cloud provider Load Balancer for the NGINX application

On cloud providers which support external load balancers, setting the type field to LoadBalancer provisions a load balancer for your Service. The actual creation of the load balancer happens asynchronously, and information about the provisioned balancer is published in the Services .status.loadBalancer field. For example:

Traffic from the external load balancer is directed at the backend Pods. The cloud provider decides how it is load balanced.

**Why**: Kubernetes is a closed system by default, F5 provides value in the closed system (Service Mesh) and access to the closed system. There are many ways to expose services from within the kubernetes platform. In 2018 Sandeep Dinesh wrote a medium article which is a favorite of explaining the differences.

|image01|

Source: https://medium.com/google-cloud/kubernetes-nodeport-vs-loadbalancer-vs-ingress-when-should-i-use-what-922f010849e0

**How**:
  - https://kubernetes.io/docs/concepts/services-networking/service/#loadbalancer



.. |image01| image:: images/image01.png
  :width: 25%
  :align: middle
