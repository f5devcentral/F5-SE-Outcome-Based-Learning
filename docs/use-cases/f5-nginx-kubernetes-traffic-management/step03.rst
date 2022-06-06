Build a managed Kubernetes Cluster
==================================

Managed Kubernetes is when third-party providers take over responsibility for some or all of the work necessary for the successful set-up and operation of K8s. Depending on the vendor, “managed” can refer to anything from dedicated support, to hosting with pre-configured environments, to full hosting and operation.

Source: https://www.computer.org/publications/tech-news/trends/what-you-need-to-know-about-managed-kubernetes-platforms

**Objective**: Create a managed kubernetes cluster

**Why**: Knowledge about the underpinnings of raw kubernetes are important, but not necessary for day-to-day engineers. Most companies have also adopted this mentality and offload the work of kubernetes management to a service (AKS,EKS,GKE,Rancher, and OpenShift). 

**How**:

Build a managed k8s cluster:
  - Azure: https://docs.microsoft.com/en-us/azure/aks/learn/quick-kubernetes-deploy-portal
  
  - AWS: https://docs.aws.amazon.com/eks/latest/userguide/create-cluster.html
  
  - Google: https://cloud.google.com/kubernetes-engine/docs/deploy-app-cluster