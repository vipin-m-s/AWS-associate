# nat gatway
- For ec2 instances in private subnet
- inorder to get security updates or reach any outside endpoints
- we can use NAT gateway. The nat gateway is deployed in public subnet and it requires a elastic IP address
- It is a zonal resource, For high availability we need to create nat gateway in each AZ>
- When outbound traffic is sent form private ec2 instance to NAT gateay
- The nat gateway will replace the source IP with its own IP and send to the internet
- Once it receoves the response it will forward to private instance
- No other application will be able to reach private instance from outside.

TO create NAT Gateway 
- Create a public subnet
- Create a NAT gateway and create elastic IP for it
- Add route table in private subnet to route traffic to nat
- The traffic will now flow via NAT

<img width="642" height="571" alt="Screenshot 2026-03-29 at 9 47 41 AM" src="https://github.com/user-attachments/assets/34c2215d-5ea7-45e3-8c60-00207ce77d50" />

High availability NAT gateways
<img width="583" height="613" alt="Screenshot 2026-03-29 at 9 51 59 AM" src="https://github.com/user-attachments/assets/8db8dcb9-8b5e-4cbd-9922-1e2d5c54bda7" />
