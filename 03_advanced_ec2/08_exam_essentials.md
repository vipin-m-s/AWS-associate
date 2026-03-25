# EBS basices
- provides persistent storage to ec2 instance
- Lifecycle is independent of ec2 instancce. Persists even after ec2 oinstance is terminated
- It is a AZ service. There is data replication within the AZ. hence it can tolerate Host failure but not AZ failure
- Must be in same AZ as ec2 instance
- EBS volume size and IOPS can be changed dynamically. without sstopping ec2 instance

# EBS volume Types 
- gp3 / gp2 - general purpose SSD - default choice - configure throughput/iops
- io1/io2 block express - provisioned IOPS SSD - low latenecy , critical apps database ( supports multi attach )
- st1 ( throught optimized HDD )  - big data, log processing sequential IO
- sc1 ( cold hdd ) - low cost, infrfequent acess, archieval
- AWS recommends migration from gp2 -> gp3 can be done without interruption

# EBS snapshot
- point in time backup of ebs volume
- it is regional service. 
- it can be copied to differnt region / account
- intance can be created in different region / accocunt
- Amazon DLM data lifecycle manager is used to manage the creation and deletion

# EBS advacned featire
- multi attach - io1 and io2 ( attach ebs volume to multiple instances ) 
- ebs optimized storage - dedicated bandwidth for consistent performance.

# ebs encyrption 
- in transit, rest
- keys can be used from amazon kms
- CMK defauly is aws/ebs
- We can use CMK for compliance
- If disabled -> temporary lock
- If deltefd -> permanent data loss


