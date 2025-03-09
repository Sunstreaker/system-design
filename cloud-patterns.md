# Tips

## Customer Facing
* load balancer

## backend
* message brokers


# Loadbalancer

Enable a loadbalancing API before the application servers, will be help scaling the backend for dynamic consumer demand. If the consumer demand is high, servers can be increased without any impact to the clients

Implementation patterns
1. cloud loadbalancing
2. Load balancing with auto-scaling

## Load balancing with auto-scaling

The cloud services will track the number of services running behind a load balancer. In case of the less traffic, the load balancer will redirect the traffic to minimum nuber of servers to reduce the cost.
And in case the traffic increases, it can also spin up more pods to catchup with the new demand


## Algorithms
1. Round robin
   1.1 It will pick the server in round robin way.
   1.2 This algorithm can be implemented only in case of stateless servers
2. Sticky session or session affinity
   2.1 Using this algorithm the loadbalancer can send the request from a client to the same server
   2.2 This can be done only for a shorter session
   2.3 One way to achieve this is a cookie will be placed in the client, this will send to the loadbalancer for every request
   2.4 Another way is to send the IP address from the client, using this IP address the server can forward the same client request to a particular server
   2.5 If a same client is having a greater number of connections, this can cause problem to the server. The server may be overloaded and performance can degrade.
3. Least connection
   3.1 This overcomes the drawback of the "Sticky Sessions". The loadbalancer will try to see if a single server is overloaded it can see the least connection server and can redirect the request. This can be used for "SQL, "LDAP" or other activities


# Message Brokers

Simillar to the loadbalancer for the customer facing, message broker can be implemented at the backend layer for scaling reasons. This will not act like a loadbalancer, but it enables a way to scale the consumers in case the volume is high.

