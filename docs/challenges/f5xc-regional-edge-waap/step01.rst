Securely expose your website with SSL encryption and a DNS name
===============================================================

**Objective**: Securely expose your website with SSL encryption and a DNS name 

Required Outcome:

- Only allow traffic to your app if it is coming from the XC platform (hint: you will need to configure the specifc cloud tools to achieve this)
- Get an A score on SSLLABS

**Why**: Encryption is mandatory, time is always a scarce resource. Getting your app exposed with a valid certificate within a few seconds is valuable

**How**:

Follow the F5XC documentation 
https://docs.cloud.f5.com/docs/how-to/app-networking

Use a domain that is already defined within your tenant. Most preconfigured tenants will have a delegated domain located under DNS-Management > Delegated Domain Management.

.. warning:: Most websites will require a HOST header injected into the request. This can be done with Routes, HTTP Load Balancer More Options, and Service Policies.

**Validation**: 

- How long did it take to complete the steps here? 
- How long does it take to deploy the same load balancer configuration using automation?
- Run SSLABS test on your new exposed endpoint, any issues?