# Elastic network interface
- EC2 instance get the public ip, private ip and mac address from the ENI elastic network interface
- It is a virtual network card. It is part of the VPc and it is attached to the ec2 instance.
- Each ec2 instance can have 2 ENI ( primary and secondary )
- ENI are independent of ec2 instance. We can manually create it and move it to other ec2 instance ( static IP is required )
- It is useful when we have a software whiich binds to the mac address. So we can move the ENI to another ec2 instance and continue to use the software ( Public IP is mapped to private IP , moving private IP ensure public IP is also moved ) 
- ENI has the following attributes
  - public IP
  - Private IP
  - mac address
  - security group ( security grou pis related to eni and not to ec2 instance )
- ENIs are AZ scoped. Cant move across AZ.

# Use case

## hgih availability 
fail over within an AZ ( move eni from one instance to another for quick failover )

## Static IP retnetion 
Detach eni from failed / temrinated ec2 instance and attach to a new one to retain the same private IP and MAC address. 
Helps avoid DNS update and reconfiguration 

## Multi - network ( multi - homed ) instances
- Attach multiple eni  to same ec2 instance. Each connected to different subnet and security group
- Enables segreggation of traffic. ( app network and database network )
- 1 ENI for external access and another ENI for monitoring/administration
- <img width="678" height="761" alt="Screenshot 2026-03-24 at 8 15 41 AM" src="https://github.com/user-attachments/assets/4300f21b-90c3-4dde-88fa-648ebafde8ac" />
