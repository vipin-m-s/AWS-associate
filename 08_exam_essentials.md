# EBS basices
- provides persistent storage to ec2 instance
- Lifecycle is independent of ec2 instancce. Persists even after ec2 oinstance is terminated
- It is a AZ service. There is data replication within the AZ. hence it can tolerate Host failure but not AZ failure
- Must be in same AZ as ec2 instance
- EBS volume size and IOPS can be changed dynamically. without sstopping ec2 instance

# EBS Types 
