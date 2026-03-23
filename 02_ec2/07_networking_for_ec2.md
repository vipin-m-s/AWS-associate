# Networking

- In a corporate office. There will be a private network
- We go to office and connect to their internal network
- We will be able to access the resources.
- There will be router to access internet

- Similarly in AWS we can create private networks using VPC
- VPC is regional service
- We cannot use VPC created in mumbair region in Hyderabad region
- For each Availability zone we create subnet
- WE cannot create ec2 instance in region
- we create ec2 instance withing an availabiluty zone using subnet
- subnet is part of VPC which is tied to the availability zone

# Private IP 
- ec2 instances launched within an vpc and subnet
- Will automaticaly get private IP from the subnet CIDR range
- This is used for communication within the VPC
- Every ec2 instance should include a private IP
- It is free service
  
# Public IP 
- This is optional
- we can choose not to have public IP
- If we want ec2 instance to be accessible from internet we need to attach a public IP
- We do not need to add public IP to App serves , since they recieve traffic only from web server
- Public IP is provided from pool of Public IPs from amazon.
- When we stop instance, the public IP is released.
- When we start instance, new public IP is recieved fro ec2 instance
- It is charged service

# Elastic IP 
- This is static IP address
- If we do not want the public IP of ec2 instance to change when stopped.
- WE can attach static public IP address to the instance
- Customers can use the static IP address to access the instance
- We can also detach the Elastic IP from one ec2 instance and attach to othwer ec2 instance in fail over scenarios.
- SO that app is accessible over other the same IP address
- IT is a charged service
