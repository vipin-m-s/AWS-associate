# ecs anywhere
- We can use onprem servers to host compute backend for ecs service
- The data plane will be on prem and control plane will be in aws cloud ecs service
- THe ecs agent and ssm agent will be in the on prem server
- The task and services will run oin on prem server
<img width="723" height="421" alt="Screenshot 2026-04-05 at 12 23 59 PM" src="https://github.com/user-attachments/assets/5114f40b-2fda-410d-bf00-e93495b47969" />


# eks anywhere
- Both the control plane and data plane is on prem
- On AWS side we have eks tools such as eksctl etc to manage the eks cluster
- EKS runs on prem and uses servers on prem
- It can connect with ecr and cloudwatch in AWS for pulling image and logs
<img width="602" height="368" alt="Screenshot 2026-04-05 at 12 25 58 PM" src="https://github.com/user-attachments/assets/c0143e97-8592-476f-962e-cc1f4267021c" />
