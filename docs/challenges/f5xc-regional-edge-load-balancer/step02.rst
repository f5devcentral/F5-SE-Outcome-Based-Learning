Update Cloud Construct External Security Group
==============================================

**Objective**:

Update the security group protecting your NGINX application servers for F5XC communication

**Why**:

Security Groups are used to limit access to resources from unknown or known sources. F5XC will communicate directly to the public IP address of the NGINX application servers, for this communication to work the known endpoints of the F5XC regional edge need to be allowed.

**How**:

List of known locations F5XC will communicate from:
https://docs.cloud.f5.com/docs/reference/network-cloud-ref