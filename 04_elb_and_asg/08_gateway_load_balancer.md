# Gateway loadbalancer
- It is a bit different than ALB and NLB. It is not used for load balancing backend servers
- It is used to manage, scale the network appliances such as firewalls, intrusion detection, intrusion prevention, deep packet inspection tool.
- Before the source packets reaches the destination packets we will perform the inspection.
- This uses the protocol of GENEVE
- generic network virtualization encryption
- This operates at Layer 3 ( network layer )
- It uses a port of 6081 for communication
- There will be a GWLB endpoint created in each VPC and in the appliance VPC we create the GWLB.
- It does not modify the source IP address. Transparent IP 

we can also centralize the network security by creating applicance VPC, and other application VPC
- <img width="708" height="570" alt="Screenshot 2026-03-28 at 5 07 54 PM" src="https://github.com/user-attachments/assets/da8f5e39-859a-4307-a7ee-a1331c95d956" />


