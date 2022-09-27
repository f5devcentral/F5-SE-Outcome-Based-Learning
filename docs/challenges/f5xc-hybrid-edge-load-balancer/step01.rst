F5XC Cloud Site
===============

**Objective**:

Create an F5XC CSP site (Azure, AWS, GCP) with two interfaces

Site is made up of a cluster of one or more Nodes and the cluster can be scaled up or down based on load by addition or deletion of Nodes. Each Node is a linux-based software appliance (appliance is delivered as ISO or deployment spec on k8s) that is deployed in a virtual machine, in a k8s cluster, commodity hardware, or our edge hardware. Kubernetes is used as clustering technology and all our software services run as k8s workloads on these clusters. In addition, customer workloads also run on this k8s if App Stack services are enabled on these Nodes. This managed k8s on Node is referred to as “physical k8s” from now on.

A physical location may be deployed with multiple clusters of Nodes, each individual cluster is considered as its own individual Site to ease manageability. As a result, an individual Site is a combination of location and cluster. If a physical Site has two clusters then there are two Sites in that location. Henceforward, a Site may be referred to as Site or Location in the rest of the documentation. If the Location is expected to have multiple Sites, it will be made explicit in the documentation when we differ in this assumption.

Source: https://docs.cloud.f5.com/docs/ves-concepts/site

**Why**:

A local site is created for the target of the hybrid-edge load balancer. Since these services are private, a communication and discovery endpoint needs to be available (Customer Edge)

**How**:

It is recommended that you create your F5XC site in a separate cloud construct (Resource Group, VPC) than your other CSP resources. This is to allow the segregation of duties, and easy delete when done with the resources.

https://docs.cloud.f5.com/docs/how-to/site-management

**Validation**: 

Where in the F5XC console can you see the site connectivity and health? How else could a connection from F5XC regional edge to a customer environment be established?