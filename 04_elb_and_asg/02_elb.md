# Elastic load balacning 

There are multiple load balancinf services in aws
- Application load abalancer
- network load balancer
- gatyeway load balancer

Some common things between all loadbalancers 
- They can have ec2, ecs containers, ip addresses ( to load balance the on prem servers ) , lambda functions as backend service
- They are regional service and they can load balance across AZs
- They support multiple protocols such as HTTP, HTTPS, TCP, UDP, TLS
- They help in SSL/TLS termination to have secure connection between the client and the ELB
- SUpports Dual stack ( ipv4 and ipv6 traffic )
- It exposes a Single Point of acccess to application (DNS)
- It will send the traffic only to healthy backend servers by performing health checks on the backend servers to detect any failures/unresponsiveness. SO that client requests does not fail

Some Command services with which ELB can connext
- Route 53 -> to provide DNS routing
- ACM -> Amazon certificate management for SSL/TLS termination ( we need to add certtificates in ELB for SSL/TLS termination to ooccur )
- EC2
- ECS
- AWS auto scaling groups
- cloudwatch
<img width="588" height="490" alt="Screenshot 2026-03-26 at 4 31 17 AM" src="https://github.com/user-attachments/assets/75e25f3b-3a24-47e3-9f45-f421c215e610" />
