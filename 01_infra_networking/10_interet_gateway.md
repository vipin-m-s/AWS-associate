# Internet gateway

It is a component which allows communication between the VPC and the internet

- We have moved to the new house
- Now you want to watch some youtube vides
- But the house does not have internet access
- Similarly newly creaated VPC will not have internet access.

<img width="635" height="602" alt="Screenshot 2026-03-18 at 8 19 06 AM" src="https://github.com/user-attachments/assets/b30aed51-5f8a-4b49-947e-08e8c4f9f4b6" />

- If we want inbound and outbound traffic to VPC.
- We need to create something called a internet gateway
- Internet gateway allows internet access to ec2 instancces within the VPC

<img width="1396" height="671" alt="Screenshot 2026-03-18 at 8 21 38 AM" src="https://github.com/user-attachments/assets/98245b30-9b71-420e-8c27-31636b3cd64f" />

- When we create ec2 instance in default VPC
- The default VPC will be connect to a internet gateway by default
- So We can ssh into ec2 instance created within the default VPC


- After we create a internet gateway
- We need to attach the IGW to the VPC
- Just by attaching IGW to VPC, ec2 instances will not have  internet acceess
- We need to create routes
  
