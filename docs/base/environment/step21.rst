Optional - Container Registry
=============================

**Objective**: Create a container registry 

A container registry is a *repository or collection of repositories used* to store and access container images. Container registries can support container-based application development, often as part of DevOps processes. Container registries can connect directly to container orchestration platforms like Docker and Kubernetes. 

Container registries save developers valuable time in the creation and delivery of cloud-native applications, acting as the intermediary for sharing container images between systems.

Source: https://www.redhat.com/en/topics/cloud-native-apps/what-is-a-container-registry

**Why**: NGINX Ingress can be pulled from the NGINX registry only with a production license. For demo licenses a container registry is required to store the image after creation.

**How**:

Microsoft Azure:
  Create container registry
    - https://docs.microsoft.com/en-us/azure/container-registry/container-registry-get-started-portal
  Link AKS and ACR
    - https://docs.microsoft.com/en-us/azure/aks/cluster-container-registry-integration?tabs=azure-cli#configure-acr-integration-for-existing-aks-clusters

Amazon Web Services: 
  Create container registry
    - https://docs.aws.amazon.com/AmazonECR/latest/userguide/getting-started-console.html
  Link EKS and ECR
    - https://docs.aws.amazon.com/AmazonECR/latest/userguide/ECR_on_EKS.html

Google Cloud Platform:
  Create artifact registry
    - https://cloud.google.com/artifact-registry/docs/docker/store-docker-container-images
  Link GKE and Google artifact registry
    - https://cloud.google.com/artifact-registry/docs/integrate-gke