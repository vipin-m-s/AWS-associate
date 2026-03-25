# EC2 Hibernation 

- Stopping of ec2 instance similar to shutting down the laptop. ALl the running processes are stopped.
- But there is also another mode in laptop. Where we can sleep the laptop and then wake up.
- This is called hibernation mode. When we enter the ec2 instance into hibernation mode
- The RAM state is stored in EBS root volume.
- When the EC2 instance is started again the RAM state is loaded from EBS volume
- We will not loose the state. The processes can continue to run once started.

## USe case
Save cost :- When we do not want to pay for compute resource and we can preserve the ram state for long running apps. 
Development environment, analytics workload etc.

<img width="878" height="373" alt="Screenshot 2026-03-24 at 8 23 24 AM" src="https://github.com/user-attachments/assets/db1bdd54-3457-441e-89a0-c360e3e00c2d" />


