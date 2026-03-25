# High availability and scalability 

## high availabilituy 
- The application has to be availabile even when there is a host failure or a datacenter failure.
- It means distributing in multiple AZs in AWS

## Scalability 
We should be aable to scale on demand
- horizontal scaling :- Adding more servers
- veritcal scaling :- increasing the ccpu and ram of the servers

### Both hogh availability and scalability go hand in hand
- We can achieve this architecture usiong ELB and auto scaling groups.
- ELB :- distribute the traffic to EC2 instances across the AZs
- Auto scaling group :- We can dynamiocally add or remove the ec2 instances based on conditions and rules
<img width="554" height="354" alt="Screenshot 2026-03-26 at 4 13 51 AM" src="https://github.com/user-attachments/assets/7ce9d00c-3dd6-48d6-adef-f2bb79687863" />

## Options for scaling

### Scale up/down 
Moving from m5.large -> m5.xlarge increase in vcpu and ram

### scale out/in
Add more ec2 instances 
