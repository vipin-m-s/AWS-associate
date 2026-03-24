# EC2 image builder
- When we are creating custom AMI the current process we follow is

##  Create ec2 instance from base image ( base image contains the snapshot )
##  ec2 instance is launched with ebs volume created from snapshot
##  Install packages 
## Create new AMI from ec2 instance 

<img width="695" height="464" alt="Screenshot 2026-03-24 at 7 44 20 AM" src="https://github.com/user-attachments/assets/4d6c846a-a234-477f-9d77-0bdba0fc6fd7" />

# It is a manual process. ANd we want to regularly update the AMI based on the requirement. 

- we can use ec2 image builder to automate the entire process of creation and management of AMIs
- works across different account and regions as well
- We provide recipie to install the packages
- It can also be run on scheduel  baseis ( weekly )
- free servive
- Configures the required pipelines to automate updates and system patching

