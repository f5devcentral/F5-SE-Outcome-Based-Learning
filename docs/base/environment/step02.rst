Cloud Construct
===============

**Objective**: Create an 'infrastructure as a service' environment where resources can be deployed 

Requirements: 

Tags: 
- All resources in the environemnt must be tagged with the following key:value 
  - Owner: <f5 email address> 
  - Application: <SE-OBT-yourname>

Networking: 
- Subnet that supports public internet connectivity (Public subnet)
- Private subnet (no internet connectivity)
- Management subnet with internet connectivity 

Documentation:
- Document all resources so they can be deleted when you are done 



Microsoft Azure:
  A resource group is a container that holds related resources for an Azure solution. The resource group can include all the resources for the solution, or only those resources that you   want to manage as a group. You decide how you want to allocate resources to resource groups based on what makes the most sense for your organization. Generally, add resources that share   the same lifecycle to the same resource group so you can easily deploy, update, and delete them as a group.
  
  The resource group stores metadata about the resources. Therefore, when you specify a location for the resource group, you are specifying where that metadata is stored. For compliance   reasons, you may need to ensure that your data is stored in a particular region.

  Source: https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/manage-resource-groups-portal

Amazon Web Services: 
  Amazon Virtual Private Cloud (Amazon VPC) gives you full control over your virtual networking environment, including resource placement, connectivity, and security. Get started by setting up your VPC in the AWS service console. Next, add resources to it such as Amazon Elastic Compute Cloud (EC2) and Amazon Relational Database Service (RDS) instances. Finally, define how your VPCs communicate with each other across accounts, Availability Zones, or AWS Regions. In the example below, network traffic is being shared between two VPCs within each Region.

  Source: https://aws.amazon.com/vpc/

Google Cloud Platform:
  Virtual Private Cloud (VPC) provides networking functionality to Compute Engine virtual machine (VM) instances, Google Kubernetes Engine (GKE) clusters, and the App Engine flexible environment. VPC provides networking for your cloud-based resources and services that is global, scalable, and flexible.

  Source: https://cloud.google.com/vpc/docs/overview

**Why**: Access to a cloud doesnt mean created resources. After access is provided consumers need to create or subscribe to services. Clouds call these different things, usally a VPC or Resource Group.

Differences between the two: https://docs.microsoft.com/en-us/azure/architecture/aws-professional/resources

**How**:

Azure:
  - https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/manage-resource-groups-portal
  - https://docs.microsoft.com/en-us/azure/virtual-network/quick-create-portal

AWS: 
  - https://docs.aws.amazon.com/eks/latest/userguide/creating-a-vpc.html

Google:
  - https://cloud.google.com/vpc/docs/create-modify-vpc-networks