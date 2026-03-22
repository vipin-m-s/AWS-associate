# TOols
There are tools in IAM whcih can be helpfukl

## IAM access analyzer
This tool will help us in identifying the access for resources
- There are 3 types of analyzer
  - external access analyzer
    - Which aws services have external access or accessible from public
  - Internal access analyzer
    - Which aws services can be accessed internally. 
  - unused analyzer
    - IAM permissions which are unused are detected
    - IAM user access and secret access keys which are unused can be detected
    - IAM role and policies whcih are unused can be detected

## IAM Policy simulator
- It will help us to test the policy before we apply the policy
- It will help us to debug the AccessDenied Issues

## IAM policy generator
Tool used to generate IAM policy 
- We can use JSON and create on our owns but its a tedius task
- hence we can use policy generator. To generate policy for us.
- It can create identity based policy or resource based policy

We can genrate policy based on AWS IAM users activity in AWS 
- It uses CloudTrail to identify all the AWS APIs that was requested.
- It can generate the policy based on that
- We can allow or deny

