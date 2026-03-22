# IAM policy 

- It is a json document which defines what permiussion iam user, group or role has
- JSON document is jkeyt value pair of strings, in text format , it is both human readable and machine readable
- IAM policy has many fields

Fileds are
- Policy version - defined by aws 2012-06-17
- id - optional
- statement - can contain multiple statements
- Principal - Based on type of polict we should include or not include
- Affect - Allow or deny
- Actions = what are the action we can perform - ec2:STartInstance, ec2:StopInstance etc
- resource - we can specify which resource the policy should apply. We need to add the ARN
- conditions - we can have consitions - Can launch ec2 instance only in us-east-1 region

## TYpes of policies 
### identity based policy 
- This has to be attacvhed to iam user, group, role
- There are 2 types of policies
  - managed policy
    - THis is re-usable policy
      - has 2 types
        - aws managed policy
        - customer managed policy 
  - inline policy
    - specific to each user. Gets deleted when the user is deleted.*/XC
  
### resource based policy 
- THis is attached to an aws resource
- THis deifines which user/group/role can access the aws resource
- For this principal part is required
Example:- AWS IAM user accessing s3 bucket of other aws account./
- There has to be identity based policy in first account for the IAM user to access the s32 buckey
- THere has to be resource based policy on s3 bucket which allows the IAM user to access the s3 bucket.

<img width="588" height="357" alt="Screenshot 2026-03-22 at 8 15 24 AM" src="https://github.com/user-attachments/assets/4bc21dae-4345-40de-ba50-971287fbb463" />

