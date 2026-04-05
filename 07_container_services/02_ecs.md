- [ECS elastic container service](#ecs-elastic-container-service)
- [Architecture of ecs](#architecture-of-ecs)
- [Task](#task)
- [Service](#service)


# ECS elastic container service
- ECS is used to run and manage the containers.
- In ECS, AWS manages the control plane.
- We can use compute options as ec2 instance and serverless for data plane.
- Support spot instance, spot serverless
- It integrates with other AWS services such as aws cloudwatch, aws ELB, aws api endpoint etc.

# Architecture of ecs
<img width="630" height="566" alt="Screenshot 2026-04-05 at 9 23 04 AM" src="https://github.com/user-attachments/assets/a8f48ae8-2a14-4f52-a24e-688e6b095f1c" />


# Task 
- It runs the task defination
- task definaition contains Image, CPU, memory, port etc

# Service
- It runs the tasks continously
- If task failes it will restart it
- It will integrate with NLB, ALB
