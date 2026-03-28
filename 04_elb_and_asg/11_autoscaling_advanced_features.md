# Termination policy
- When we have lot of instance
- We want to scale in
- To decide which instance to remove
- By defauly removes the oldest instance ( Deploy new version )

# Cooldown period
- After 1 autoscaling event
- The period for which it should wait
- To carry out next autoscaling event
- default 300 seconds

# instance refresh 
- rolling updates to the ec2 instances

# lifecycle hooks
- custom action ( scripts ) can be run on
- ec2 instances before they are being terminated

# warm pools
- ec2 instances can be created in stopped state or hibernating sstate
- When required it can quickly start the ec2 instance and start taking requests
- Or else it might take time to create ec2 instance configure and take requests
