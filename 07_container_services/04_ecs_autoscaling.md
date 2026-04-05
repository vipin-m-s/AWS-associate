- [ECS autoscaling](#ecs-autoscaling)
- [Scaling policy](#scaling-policy)



# ECS autoscaling
- In order to scale the ecs task, we cannot use ec2 autoscaling group as it works only with ec2 instance.
- We need to horizaontally scale the ecs task, we can use ec2 service autoscaling
- It uses application auto scaling in the background.
- Based on the scaling policy the new task will be added or task will be removed.
- For fargate we do not have to do this, it is fully managed by aws
- For ec2 instance compute type. The service autoscaling does not manage scaling of ec2 instace
- for that we need to use ec2 compute provider. Then it will manage both service autoscaling and ec2 autoscaling.


# Scaling policy
- Target tracking :-
  - If we want to maintain a certain level of average CPU etc. We can make use of target tracking
  - Example :- thermostat, it will increase decrease temperature to meet that value
- Step scaling :-
  - It will utilize the cloudwatch alarms and we can specify to add 1 instacne when cpu >50% and add 2 instance when Cpu > 75%
- Scheduled scaling :-
  - If we know before hand there will be increase in load at certian time
  - Example:- nightly build.
- predictive scaling :-
  - Uses machine learning to preduct the load

