# Network load balancer 

- This works at layer 4 transport layer
- It supports TCP, UDP and TLS
- It can handle millions of requests per second.
- It can be used when high performance is required
- Each AZ will use one static IP address

target groups 
It can use ewc2 instances 
Private IP aadresses 
Application load balancer
Health check supports the http, https and tcp protocols
<img width="378" height="604" alt="Screenshot 2026-03-21 at 5 55 24 PM" src="https://github.com/user-attachments/assets/5e15a49a-fc9e-45f2-a785-8aaba2369311" />

## advantages of using private IPS as target group is
- We can include EC2 instance
- WE can include instances from our onprem servers as well
- 

## Advantages of using ALB as target group is
We can utilise the HTTP headers
We can take advantage of Static IP of NLB
<img width="210" height="317" alt="Screenshot 2026-03-21 at 5 57 28 PM" src="https://github.com/user-attachments/assets/f9ea83c3-f1c0-49bb-ac15-2b85aca395c5" />
