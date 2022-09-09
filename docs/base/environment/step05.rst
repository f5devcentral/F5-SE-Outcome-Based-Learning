Expose the application
======================

**Objective**: Expose the Juice Shop application 
  
**Why**: Challenges will proxy the Juice Shop application differently. For SaaS-only solutions, the Juice Shop application must be exposed directly from the public cloud it is hosted in. For Hybrid Edge, and Customer Edge challenges, Juice Shop can be left as a private resource.

**How**: 

.. warning:: Resouces hosted in CSPs exposed are security risks, Security Groups should be utilized to allow access only from trusted sources (personal internet/VPN)

Choose and exposure option
  - Public addresses directly on the virtual machines
  - CSP platform native load balancer

Public Address:

Microsoft Azure Public IP Address:
  - https://docs.microsoft.com/en-us/azure/virtual-network/ip-services/create-public-ip-portal

Amazon Web Service Elastic IP Address:
  - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html

Google Cloud Platform External IP Address:
  - https://cloud.google.com/compute/docs/ip-addresses/reserve-static-external-ip-address#reserve_new_static

Public Load Balancer:

Microsoft Azure Public Load Balancer:
  - https://docs.microsoft.com/en-us/azure/load-balancer/quickstart-load-balancer-standard-public-portal

Amazon Web Service Application Load Balancer:
  - https://docs.aws.amazon.com/elasticloadbalancing/latest/application/create-application-load-balancer.html

Google Cloud Platform External Load Balancer:
  - https://cloud.google.com/compute/docs/ip-addresses/reserve-static-external-ip-address#reserve_new_static