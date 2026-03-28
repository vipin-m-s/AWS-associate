# autoscaling groups
- It automatically scales ec2 instance scale inout
- We need to spicify the min, desired and max capacity
- The ec2 instance will not go below min and go above max
- Min is set so that it does not terminate all instance when scaling in
- Max is set so that it does not increase above  certain limit when scaling out
- It ensures desrired number of ec2 instance is always running.
- It requires launch template
- It can integrate with ALB/NLB and automatically register or dereigster instances
- performs helth checks based on ec2 status ( also can prform elb health checks )
- Scaling policies
- Uses cloudwatch alarm to trigger scaling actions

# Autoscaling policies
Manual scaling 
- we set the number of ec2 instances

Dynamic scalong
-simple and step scaling
  - when cpu > 50% add 1 instance
  - When cpu > 75% add 2 instance
  - when cpu < 40% remove 1 instance
  - When sqs queue has high number of msgs
- target tracking
  - maintain avg cpu 40% 

Scheduled scaling
- sat 1-6PM

predictive scaling
- based on historic utilization uses machine learning
