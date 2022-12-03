Create NGINX Plus Instance(s)
=============================

**Objective**: 

Create a NGINX Plus Instance(s)

**Why**: 

NGINX instance will be used as an API Gateway providing routing, identity, and security

**How**:

NGINX is a software package installed on top of a Linux operating system. With an NGINX certificate + key, or JWT, you can download the NGINX Plus software. The OSS version with limited features is available without the need to access the NGINX premium downloads. In the public cloud, there are marketplace offerings that already have NGINX Plus (and add-ons), these images do not require the installation of the NGINX software as it is included in the offering.

Choosing between manually creating an NGINX installation or a marketplace offering does not affect the features available. The marketplace is exists to reduce time to value in billing constructs and software management.

AWS:
  Manual: 
    - https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-plus-amazon-web-services
  Marketplace: 
    - https://aws.amazon.com/marketplace/pp/prodview-xogyq23b3mfge

Azure:
  Manual:
    - https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-plus-microsoft-azure
  Marketplace: 
    - https://portal.azure.com/#view/Microsoft_Azure_Marketplace/GalleryItemDetailsBladeNopdl/id/nginxinc.nginx_plus_with_nginx_app_protect_developer
  NGINX as a Service:
    - https://portal.azure.com/#create/f5-networks.f5-nginx-for-azure

Google Cloud: 
  Manual:
    - https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-plus-google-cloud-platform
  Marketplace:
    - https://console.cloud.google.com/marketplace/product/nginx-public/nginx-plus-app-protect-ubuntu1804-premium

Docker: 
  Manual:
    - https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-docker
