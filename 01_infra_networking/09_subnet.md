# sub networking

- Subnetworking is creating sub divisions of the network
- VPC spans across all the availability zones
- We can create an EC2 instance in a availability zone
  
<img width="1105" height="720" alt="Screenshot 2026-03-18 at 6 57 03 AM" src="https://github.com/user-attachments/assets/94d9d118-5048-4047-9168-403527a927a1" />

- Since the VPC spans across all availabiliuty zone
- We cannot create ec2 instance in VPC
- Each subnet lives within an availability zone
- We create ec2 instance within a subnet and behind the scenes we are creating within that availability zone


<img width="1130" height="658" alt="Screenshot 2026-03-18 at 6 59 06 AM" src="https://github.com/user-attachments/assets/6263ec97-2a72-46e7-ab1b-24d792eed9f6" />

- In each region we have default VPC
- Default VPC will have default subnet
- number of default subnet = number of availability zone in the region
- By default 4090 IPs per default subnet


- If we have crweate a ec2 instance in public subnet of the same VPC aalso
- We will not be able to connect to private ec2 instance in private subnet using public IP
- If we use public IP the traffic is sent to the internet
- And the instances in private subnet will not be accessible via internet
- We can use only private IP from the bastion host
<img width="746" height="662" alt="Screenshot 2026-03-18 at 7 17 20 PM" src="https://github.com/user-attachments/assets/9db1bf60-88ca-46ac-b4b6-8136d3bf930d" />
