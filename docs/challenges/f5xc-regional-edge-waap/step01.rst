Securely expose your website with SSL encryption and a DNS name
===============================================================

**Objective**: Securely expose your website with SSL encryption and a DNS name 
requirements:
- Only allow traffic to your app if it is coming from the XC platform (hint: you will need to configure the specifc cloud tools to achieve this)
- Get an A score on SSLLABS

**Why**: Encryption is mandatory, time is always a scarce resource. Getting your app exposed with a valid certificate within a few seconds is valuable

**How**:

Follow the XC documentation 
https://docs.cloud.f5.com/docs/how-to/app-networking

Use a domain that is already defined within your tenant. do not create a new domain. 

**Validation**: 
- How long did it take to complete the steps here? 

- How long does it take to deploy the same load balancer configuration using automation?

- Run SSLABS test on your new exposed endpoint, any issues?
