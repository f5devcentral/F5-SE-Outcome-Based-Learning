Step 1
============================

**Objective**: Securely expose your website with SSL encryption and a DNS name 
requirements:
- Only allow traffic to your app if it's coming from the XC platform (hint: you will need to configure the specifc cloud tools to achieve this)
- Traffic should be evenly distributed between the two application servers 

**Why**: Encryption is mandatory, time is always a scarce resource. Getting your app exposed with a valid certificate within a few seconds is valuable

**How**:
Follow the XC documentation 
https://docs.cloud.f5.com/docs/how-to/app-networking

Use a domain that is already defined within your tenant. don't create a new domain. 

**Validation**: 
How long did it take to complete the steps here? 
How long does it take to deploy the same load balancer configuration using automation?
Send 100 requests to the application, are the requests evenly distributed? 
Run SSLABS test on your new exposed endpoint, any issues?

