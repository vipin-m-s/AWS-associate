# iam credentils

In IAM there are 2 makjor components
Authentication - Whether the user has the right creedntials, keys
Authorization - whether is user can perform certain actions , whether he has permissions to perform the actions or not( iam policy )


## Authentication via management console happens via username and password
There is a default IAM password policy like the length, chars used etc
WE can create custom IAM password policy 
When we provide users access via management console, WE can set the username andf password

## Authenticatiojn via the cli or sdk requires the access keys
AWS uses 2 keys called access key and secret access key. 
- THese kjeys are used for signingi the http request sent to aws.
- both has to be save securely and we will not be able to access it again.
- We need to delete and recreate if its required again
