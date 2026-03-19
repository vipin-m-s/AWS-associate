# EBS snapshot

- By default the ebs volume in an availability zone can only be attached to ec2 instance within the same availability zone
- If we want to migrate the data to another availability zone
- Then we need to create snapshots.
- Once snapshot is created, with the help of snapshot we can create ebs volumes in other availability zones.
- We can also share the snapshot to different AWS account and create ebs volume from the snapshot.
