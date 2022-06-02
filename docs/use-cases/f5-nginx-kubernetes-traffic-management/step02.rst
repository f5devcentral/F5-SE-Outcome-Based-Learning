Create a cloud construct for Managed Kubernetes
===============================================

Objective: Create an environment where a managed kubernetes can be deployed

Why: Access to a cloud doesnt mean created resources. After access is provided consumers need to create or subscribe to services. Clouds call these different things, usally a VPC or Resource Group.

Differences between the two: https://docs.microsoft.com/en-us/azure/architecture/aws-professional/resources

How:

Azure:
  - https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/manage-resource-groups-portal
  - https://docs.microsoft.com/en-us/azure/virtual-network/quick-create-portal

AWS: 
  - https://docs.aws.amazon.com/eks/latest/userguide/creating-a-vpc.html

Google:
  - https://cloud.google.com/vpc/docs/create-modify-vpc-networks