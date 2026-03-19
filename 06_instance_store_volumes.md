# Instance store volumes

Some of the instance types comes with instance store volumes
It is a temporary fast storage that is provided. 
The storage of the physical host is provided for the virtual machines

## EC2 instance and EBS 

- If we stop the ec2 and start it.
- The virtual machine can start up in any physical host.
- It will not be started in the same physical host.
- Since EBS volume is a network attached storage. It is a network mounted storage.
- It is not assoicated with the physical host.
- Hence EBS volume will be accessible for the INSTANES
- Since ebs is a network attached storage there will be higher latency 

<img width="625" height="514" alt="Screenshot 2026-03-19 at 4 30 53 PM" src="https://github.com/user-attachments/assets/e26f1c6d-774b-4a3b-a95e-c4e583d016e7" />


<img width="1061" height="690" alt="Screenshot 2026-03-19 at 4 31 37 PM" src="https://github.com/user-attachments/assets/7d3cb0cd-6ed6-4329-8867-a1aea69aee89" />

## Instance store

- It is a temporary storage provided to the ec2 instance from the underlying physical host
- So when the ec2 instance is stopped and started it can start up in a other physical host
- Hence the instance store will not be accessible
- The instance store is non persistent storage
- It provides lower latency Since the storage is physically attached to the host
- If the host is restareted, we will not loose data
- Only temporary data should be stored on instance stores
- It is very fast storage
- The size and number of inbstance store depends on the instance tyope used for ec2 creation

<img width="625" height="549" alt="Screenshot 2026-03-19 at 4 33 39 PM" src="https://github.com/user-attachments/assets/7b6f5bef-c0bd-400d-94b1-89658f73325b" />
