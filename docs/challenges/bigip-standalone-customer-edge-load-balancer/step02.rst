Pass Traffic to Application
===========================

**Objective**:

Pass traffic to the juice shop backend application through BIG-IP

**Why**:

After the BIG-IP is created, we need some visible success.

Create a virtual server, health monitor, and pool and expose the juice shop publicly. 

Remember to lock down access to the VIP to your IP Address only. Security first :-)

**How**:

Make the juice shop reachable through a public IP via the BIG-IP Cluster.
