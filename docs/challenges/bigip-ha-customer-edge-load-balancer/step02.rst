Pass Traffic to Application
===========================

**Objective**:

Pass traffic to the juice shop backend application through BIG-IP HA Cluster

**Why**:

After the Cluster is created, we need some visible success.

Create a virtual server, health monitor, and pool and expose the juice shop publicly. 

Remember to lock down access to the VIP to your IP Address only. Security first :-)

**How**:

Depending on your cloud environment - make the juice shop reachable through a public IP via the BIG-IP Cluster.
