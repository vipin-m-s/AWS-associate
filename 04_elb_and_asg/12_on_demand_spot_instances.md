In asg
- Base capacity - we need to mention number of on demand instances for base capacity as there would be no interruptions
- On demand percenyage above base - addition ninstances above base that should be on demand
- spot pools - groupos of instance types  that can be used as spoit instances

ASG will
 - c=reate base on demand instances, so that there is no risk
 - based on requirement creates spot instances from multiple pools to reduce risk
 - Use lifecycle hooks to handle graceful shutdowns
