# delete on termination

Ec2 instance and EBS is separate entities
EBS volumes can exist wwihtout ec2 instance
When we are creating ec2 instance we have option to not delete the ebs volume after the ec2 instance is terminated
Delete on Termination -> YES -> EBS volume is deleted
Delete on Termination -> No -> EBS volume stays even after the ec2 instance is terminated
