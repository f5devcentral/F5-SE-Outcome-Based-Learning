Build a managed Kubernetes Cluster
==================================

Managed Kubernetes is when third-party providers take over responsibility for some or all of the work necessary for the successful set-up and operation of K8s. Depending on the vendor, “managed” can refer to anything from dedicated support, to hosting with pre-configured environments, to full hosting and operation.

Kubernetes already includes an impressive set of features, including scalability, detached credential configuration, self-recovery, workload management and batch execution, and progressive application deployment, but they require significant manual configuration. Managed solutions take care of much of this configuration for you, or at least guide you through the decision-making process. 

Once your set-up is operational, managed solutions provide the tools necessary to automate routine processes such as updates, scaling, load-balancing and monitoring. When managed Kubernetes services include a hosting platform, they will also manage all of the maintenance and configuration needed for your infrastructure.

Source: https://www.computer.org/publications/tech-news/trends/what-you-need-to-know-about-managed-kubernetes-platforms

**Objective**: Create a managed kubernetes cluster

**Why**: Knowledge about the underpinnings of raw kubernetes are important, but not necessary for day-to-day engineers. Most companies have also adopted this mentality and offload the work of kubernetes management to a service (AKS,EKS,GKE,Rancher, and OpenShift). 

**How**:

Build a managed k8s cluster:
  - Azure: https://docs.microsoft.com/en-us/azure/aks/learn/quick-kubernetes-deploy-portal
  
  - AWS: https://docs.aws.amazon.com/eks/latest/userguide/create-cluster.html
  
  - Google: https://cloud.google.com/kubernetes-engine/docs/deploy-app-cluster