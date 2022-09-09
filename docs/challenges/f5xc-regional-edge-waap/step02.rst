Load balance traffic to your two application servers
====================================================

**Objective**: Load balance traffic to your two application servers

Required Outcome:

- Traffic should be evenly distributed between the application servers
- Application must get the original client ip as an HTTP header 

**Why**: Scaling application traffic, high availability ,progressive application version updates

**How**: 

Follow the F5XC documentation
https://docs.cloud.f5.com/docs/how-to/app-networking

**Validation**: 

- How long did it take to complete the steps here? 
- How long does it take to deploy the same load balancer configuration using automation?
- Run 100 requests (using Hey https://github.com/rakyll/hey or any other tool), was the traffic evenly distributed? 
- What is the avarege latency of each one of your application servers? 
