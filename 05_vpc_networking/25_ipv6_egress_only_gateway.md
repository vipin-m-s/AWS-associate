# ipv6 in vpc

- VPC supports dual stack mode. Both ipv4 and ipv6
- IPV6 is optional but ipv4 is mandatory for VPC
- For vpc the ipv6 is /56
- Subnets can be ipv4 only, ipv6 only or dual stack ipv4 and ipv6
- Ec2 instances within the subnet will recieve similarly
- The subnet ipv6 is /64
- Evry ipv6 is globally unique nd publicly acccessible.

Scenario 
- IPV4 to IPV4 is supported by NAT gateway
<img width="762" height="303" alt="Screenshot 2026-03-30 at 3 19 53 PM" src="https://github.com/user-attachments/assets/babebefb-1e87-41eb-a68e-a270b7babcb2" />

- IPV6 to IPV6 is not suppported by NAT gateway
- We need to use Egress only gateway 
<img width="763" height="307" alt="Screenshot 2026-03-30 at 3 22 15 PM" src="https://github.com/user-attachments/assets/919c65ff-c819-43f9-8a9d-56ef1ded2d23" />

- In security group we need to allow/deny ipv4 and ipv6 explicitly
- In route table we need to explicity add route for ipv6
- Useful for avoiding NAT bottleneck
- Useful for IOT
- Useful when large address space is required
