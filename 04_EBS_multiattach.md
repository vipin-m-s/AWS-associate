# EBS multi attach 

- We can attach single ebs volume to multiple ec2 instance.
- This can be done only for io1 and io2 block express volumes ( provisioned iops )
- We can attach ebs volume to upto 16 ec2 instances
- Each ec2 instance will have full read/write access to the ec2 instance.
- Use case
  - highly available applications. Where if one node goes down another node can come up and access data
  - Zero down time apps
  - parallel processing of data

<img width="552" height="576" alt="Screenshot 2026-03-24 at 5 36 23 AM" src="https://github.com/user-attachments/assets/d529c6a9-ccb3-401e-8bf8-c6150a0c8572" />

## disadvantages
- boot volumes are not allowed
- Application must handle the consistency and parallel operations. It is not AWS responsibility
