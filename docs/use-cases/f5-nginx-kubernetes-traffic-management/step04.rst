Kubernetes Nodes and Namespaces
===============================

What:

Node:

  Kubernetes runs your workload by placing containers into Pods to run on Nodes. A node may be a virtual or physical machine, depending on the cluster. Each node is managed by the control plane   and contains the services necessary to run Pods.
  
  Typically you have several nodes in a cluster; in a learning or resource-limited environment, you might have only one node.
  
  The components on a node include the kubelet, a container runtime, and the kube-proxy.

Namespaces:

  In Kubernetes, namespaces provides a mechanism for isolating groups of resources within a single cluster. Names of resources need to be unique within a namespace, but not across namespaces.   Namespace-based scoping is applicable only for namespaced objects (e.g. Deployments, Services, etc) and not for cluster-wide objects (e.g. StorageClass, Nodes, PersistentVolumes, etc).

Why:

How:

Describe Kubernetes Nodes:
  - https://kubernetes.io/docs/concepts/architecture/nodes/

Create Development Namespace:
  - https://kubernetes.io/docs/tasks/administer-cluster/namespaces-walkthrough/