# ELB

- Suppose we arwe hosting aa website
- We might start with 1 server
- But the one server is SPOF single point of failure
- If the server goes down , Then the website will become offline
- And not reachable to the end user

- We mgiht consider increasing the nnumber of servers 2, 3 etc
- But there is problem with this approach
-- when we want to add more servers, it requires manual configuration to DNS etc
-- One server might get overloaded and all request might hit same server
-- There is no 1 single end point for the website

## Load balancer 
Load baalncer is a component in the system design 
Which is responsible for distributing the treaffic evenly across the back end servers
It sends the traffic to healthy servers only

With the load balancer, If 1 server goes down. 
The loadbalancder will redirect the traffic to other server

## LOad balancer goes down
If load balancer goes down then even if backend sweerrvers are healthy
Then the website will not be reachable
Hence manageing the load balancer is critical. 
If we have just one load balancer, It will be a bottleneck in the design 

Limitations
- High availability
  - If load balancer goes down , then website will not be accessible
- security
  - We need to keep updating the security patches for the software/hardware load balancer example ngingx, ha proxy 
- performance
  - We might require high performance for the load balancer, Which is difficult to achieve

## ELB
elastic load balancer is a load balancing solution provided by AWS
IT is fully managed server. Whcih is respobsible for redirecting the traffic to healthy backend servers

It is scalbale. hgihly available and high performance load balancer.

Handled by AWS
- Highly available
- Secure
- performance

## Types of load balancer 
- Application load balancer
  - For application working in Layer 7 ( http/https )
  - Application layer

- Netowrk load balancer
  - For application working in layer 4 ( tcp/udp/tls )
  - Transport layer
  - Can handle millions of requests per seoncd
  - For high performance

- Gateway load balancer
  - Can be used when we have virtual appliances such as firewall, ID, IPS systems

- Classic load balancer
  - Old generation of load balancer
  - Supports Layer 4/7
  - http/https/tcp/ssl
