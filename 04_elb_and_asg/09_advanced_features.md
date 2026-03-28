# ADvanced features

## External vs internal load balaner

- When three tier application is used
- THere will be web tier, app tier and database tier
- There will 2 load balancer required
- 1 for public facing in public subnet
- another for internal for app tier in private subnet
  <img width="388" height="539" alt="Screenshot 2026-03-28 at 5 57 04 PM" src="https://github.com/user-attachments/assets/55c030b1-1fea-4012-aefa-fb05ff678dae" />

### External loadbalancer 
- load balances the incoming traffic from the outside world and distributes to web trer.
- It is placed in public subnet
- Has public DNS

### internal load balancer
- Will recieve the traffic from within the VPC from private subnet
- It is plaaced in private subnmet
- it is not exposed to outside world
- It does not have public DNS


## Cross zone load balacing
- WHen there are uneven number of instances between 2 AZs
- The instances might get over whelmed from the traffic and there is uneven distribution of data
- 2 instances will recieve 25% of data and others will recieve 12% of data
<img width="403" height="324" alt="Screenshot 2026-03-28 at 6 01 10 PM" src="https://github.com/user-attachments/assets/448a1fa5-c97c-41ff-9e21-05277c4bfc72" />

### If cross zone load abalncing is enabled
- The load balancers will equally distribute the traffic to all instances
- Ensures even distribution of data to backend servers
- No server get overwhelmed

### ALB
- The cross zone load balancing is enabled by default, we cannot disable it
- There is not addition al charge for data movement

### NLB and GWLB
- The cross zone load abalcing is disabled by default and we can enable it
- There is additional cost charged when there is data movement from one AZ to another



## SNI server name indication
<img width="608" height="630" alt="Screenshot 2026-03-28 at 6 05 51 PM" src="https://github.com/user-attachments/assets/15727414-0536-4529-8dd1-5b76acd2c518" />

- ALB and NLB supports SNI server name indication. Does not work for GWLB
- THE LB can store multiple SSL certificates
- Based on clients request to any domain 
- The appropriate SSL certificate will be shared
- We can have a single LB for multiple domains
- This will help in reducing the cost


## Client IP preservation 
### ALB 
- in alb the client ip is hidden from backend servers by default
- We can enable it. A header will be included with name X-forwarded-for which will have source IP

### NLB.
- by default it is transparent load balancer.
- the servers will see source ip address
- But if ssl termination is done at NLB.
- Then the source Ip is not shared to the backend servers
- We can use proxy protocol v2
- This will share source ip, source port, dest ip, dest port and protocol to backend servers
- It is an IP protocol

## Differences betwween the 3 load balancers


