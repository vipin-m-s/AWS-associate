# table class
- similar to the s3 storage cloass, we have the dynamo db table class
- There are 2 options provided

## Standard 
- It is the default option
- Used for frequently accessed data
- Higher storage cost, lower read/write cost
- Hot data should be stored

## Infrequent Access
- Used for infrequently accessed dataa
- Lower storage cost, higher read/write cost
- cold data such as historic tables, old session data.

We can switch between the 2 table classes
