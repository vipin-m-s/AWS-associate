# Instance Meta Data Service v2

- With the help if IMDS v2 we can fetch metdata about the ec2 instance within the ec2 instance
- Users and application can use this to fetch the metadxtaa such as instancer id , private ip , ami id , iam role credentials etc
- When we attach a role to ec2 instance., The AWS SDK uses IMDSv2 to fetch the credentials.
- THe service is running in ip - 169.254.169.254. 
