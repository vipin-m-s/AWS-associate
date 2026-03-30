# Interface endpoint
- If we want to communicate to other aws services such as amazon sqs, kinesis, s3, dynamodb we can use interface endpoint
- Interface endpoint uses the aws private link 
- The interface endpoint after attaching to vpc will create an ENI within the same private subnet
- There will also be a private DNS for interface endpoint provided which will resolve to the eni
- ENI comes with security group hence port 443 inbound traffic should be allowed

<img width="985" height="614" alt="Screenshot 2026-03-30 at 5 35 13 AM" src="https://github.com/user-attachments/assets/a9158590-9717-42d3-bc55-ebeba1a14d1c" />

Our own services
- we not pnly can connect to aws services
- we can also connect to out own services which are exposed via NLB
- We need to specifyg custom option


<img width="1241" height="623" alt="Screenshot 2026-03-30 at 5 37 25 AM" src="https://github.com/user-attachments/assets/fa650793-df07-479d-b901-338884c329a2" />

VPC peering and VPN/DX
- Interface endpoint can be acccess not only within the VPC
- It can also be accessed from the Peered VPC and also the on prem to which we have connection via VPN/DX


<img width="1287" height="565" alt="Screenshot 2026-03-30 at 5 39 11 AM" src="https://github.com/user-attachments/assets/87e68552-2ce7-4653-99cb-11e35ae2a153" />


Interface endpoint demo 
- Same as previous
- Create sqs queue
- modify IAM role to add sqs full access
- Login to private ec2 instance
- check for access using aws sqs --queue-url <> --message "Hi from aws"
- We will not be able to access
- Create interface endpoint and copy the private DNS
- Check for access using aws sqs --queue-url <> --message "hi from aws" --endpoint-url <private DNS>
- we should be able to send the message
- Go to vpc and enable DNS HOSTNAMES and DNS RESOLUTION
- GO to interface endpoint and enable private dns settings
- We should now be able to access without endpoint url aws sqs --queue-url <> --message "hi"

- 
