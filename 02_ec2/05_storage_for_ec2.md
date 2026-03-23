# Storage for ec2

# Elastic bloick storge
- EBS and EC2 are different services
- EBS can exist even after ec2 instance is termintated
- EBS is SAN ( storage area network )
- EBS is independent of ec2 lifecycle
- EBS is elastic - meaning we can increase the size of the volume.
- But we cannot reduce the size as it might contain data. Reducing size is not supporter
- We can create smaller volume, attach to ec2 and migrate from bigger disk to smaller disk
- One ec2 instance can contain multiple EBS volumes
- We can take backup of ebs volumes using ebs snaopshot
- ebs snapshots are stored in s3 buckets
- EC2 and EBS are availability zone speific resources. We can attach ebs volume to ec2 instanc3 in same availability zone
- Each ebs volume can attach to only 1 ec2 instance

# Instance store volume
- Instance store volumes are ephermeral
- If the instance is stopped then the instance store volumes are not accessible
- They are storage from the underlying physical storage
- WHen we stop and start instancce the VM can be started up in any physical host
- EBS volumes are SAN hence it can be instantly connected to any host.
- But underlying host storage is accessible only in that host
- Instance store volumes are free for use
- They have to be used for Temp directory , buffer / cache
- We can choose size for EBS, but instance store volumes are fixed in size
- Only some instance_types come with instance store volumes
