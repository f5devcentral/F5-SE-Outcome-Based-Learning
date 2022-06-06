Kubernetes Nodes and Namespaces
===============================

**Objective**: Utilize kubectl to create a namespace and describe a node.

Node:

  Kubernetes runs your workload by placing containers into Pods to run on Nodes. A node may be a virtual or physical machine, depending on the cluster. Each node is managed by the control plane   and contains the services necessary to run Pods.
  
  Typically you have several nodes in a cluster; in a learning or resource-limited environment, you might have only one node.
  
  The components on a node include the kubelet, a container runtime, and the kube-proxy.

  Source: https://kubernetes.io/docs/concepts/architecture/nodes/

Namespaces:

  In Kubernetes, namespaces provides a mechanism for isolating groups of resources within a single cluster. Names of resources need to be unique within a namespace, but not across namespaces.   Namespace-based scoping is applicable only for namespaced objects (e.g. Deployments, Services, etc) and not for cluster-wide objects (e.g. StorageClass, Nodes, PersistentVolumes, etc).

  Source: https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/

**Why**: F5 solutions will require the knowledge of namespaces, for discovery of resources, and to isolate resources. Customers will use namespaces in a variety of ways, form environments to applications. Node understanding comes for licenseing, F5 NGINX can be licensed on the number of pods in a deployment or the number of nodes in a cluster. AspenMesh is licensed by the number of clusters, BIG-IP and F5XC do not currently care about cluster sizing or nodes for licenses.


**How**:

Describe Kubernetes Nodes:
  - https://kubernetes.io/docs/concepts/architecture/nodes/

Create Development Namespace:
  - https://kubernetes.io/docs/tasks/administer-cluster/namespaces-walkthrough/