# Application load balancer 

- Application load balancer works at Layer 7, APplication layer
- Hence it can read the http headers, http information from the request
- It can then redirect the request to set of servers based on path, based on header, based of request, based on source IP etc.

Routing tables for different target groups 
- routing based on path in URL ( example.com/users and example.com/posts )
- routing based on hostnames ( one.exampple.com and other.example.com )
- routing based on query string, headers ( example.com/users?id=1&order=false )

 ALB are great fit for microservices and container based application 
 Has a port mapping feature
If we use CLB we might need to create multiple CLB. With ALB with one can support many applications

Target groups:- 
- can be ec2 instances ( auto scaling group )
- can be lambda functions
- Can be ECS
- Can be private IP addresses

## Path based routing 
<img width="709" height="413" alt="Screenshot 2026-03-21 at 8 20 42 AM" src="https://github.com/user-attachments/assets/9592391d-c20e-4b35-b07c-9dbc759d0818" />

## Query string parameters routing 
<img width="686" height="484" alt="Screenshot 2026-03-21 at 8 22 07 AM" src="https://github.com/user-attachments/assets/debd9c33-dca0-4740-8046-6ca3ad233e2c" />

## Good to know
- It comes with a Fixed hostname ( xxx.region.alb.amazonaws.com )
- Application servers do not see the client IP directly
  - IP can be found in http header - X-Forwarded-For
  - Port can be found in http header - X-Forwarded-Port


<img width="709" height="605" alt="Screenshot 2026-03-21 at 8 25 29 AM" src="https://github.com/user-attachments/assets/e41fa8a3-1ccf-4943-92cb-d148780a6719" />
