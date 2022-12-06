Access NGINX Plus Instance
==========================

**Objective**: 

Gain access to the NGINX instance(s) through SSH to build and store NGINX configuration.

**Why**: 

The configuration of NGINX is stored locally. This means the gateways do not need any outside entity to process traffic, with each gateway independent, scale is practically limitless.

Automation or configuration management tools place NGINX configuration files locally, tools like NGINX Instance Manager can proxy NGINX configuration files into a declarative API for groups of NGINX servers (Plus or OSS).

**How**:

AWS:
  - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstances.html

Azure:
  - https://learn.microsoft.com/en-us/azure/virtual-machines/linux-vm-connect?tabs=Linux

Google Cloud:
  - https://cloud.google.com/compute/docs/instances/connecting-to-instance

**Automation of configuration**:

Ansible:
  - https://www.nginx.com/blog/announcing-nginx-core-collection-ansible

NGINX Instance Manager
  - https://www.nginx.com/products/nginx-management-suite/instance-manager/