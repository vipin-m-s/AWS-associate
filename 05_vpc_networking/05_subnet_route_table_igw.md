# Subnet
- Dividing the large network into smaller networks for further isolation is called subnet work or subnet
- We need to include the ip CIDR for subnet as well
- We can create public subnet and private subnet aswell

# internet gateway 
- If we want the resources witihin our vpc to talk to the internwt
- We need to create Internet gatewayt and attacjh it to the vpc
- It will help our ec2 instance to be reachable via internet
- It will help ec2 instance to communicate to the internet

# route table
- By default when VPC is created there will be a main route table created
- It will just have 1 entry
- For ec2 instances to communicate within the VPC there is a local router.
- There is entry for loacl router.
- If we want our ec2 instance to communicate with internet we need to
- Add a route to IGW.
- the route table with IGW entry is called public subnet and without it is called private subnet
- Its recommended to create a route table for each subnet.
![Uploading Screenshot 2026-03-29 at 8.53.29 AM.png…]()

<img width="676" height="630" alt="Screenshot 2026-03-29 at 8 58 06 AM" src="https://github.com/user-attachments/assets/77ca7105-2511-4273-8a7e-390d7e65fe1b" />

- We will not be able to access the internet from private ec2 instance in private subnet
- Inorder to access internet or be accessed from intertnet.
  - ec2 instance should be in public subnet
  - ec2 instance should have public IP address
<img width="623" height="624" alt="Screenshot 2026-03-29 at 9 01 53 AM" src="https://github.com/user-attachments/assets/3af05f60-7b5d-4313-b009-acffed2b4477" />
