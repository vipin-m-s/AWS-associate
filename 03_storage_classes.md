# Storage classes
- There are multiple storage classes provided by AWS based on freuqency of the access, retrieval time and cost.

## frequently accessed data
### s3 standard 
- general purpose storage for frequently accessed dataa
- Use cases are media content, gaming application
- Data storage cost is high
- The data can be accessed in milliseconds
- Per GB cost per month is 0.023
- Data retrieval cost is not applicable here
- It is stored in Minimum 3 AZ
- Provides 11 9's of durability

## Infrequent access data
### Standard IA 
- Used for storing infrequently accessed data
- Data stored commitment is 30 days. Even if we store for 1 day we will be charged for 30 days
- Infrequently accessed data which is accessed such as hot backups, older media contents
- Data storage cost is better than standard
- Data retrieval cost is applicable
- Provide 11 9s of durability
- Per gb per month cost is 0.012
- Data stored in minimum 3 AZ

### One zone IA 
- Data is stored only in 1 AZ
- The data that can be recreated or does not required HA can be stored here
- Secondary Copies of on prem
- Data storage cost is 0.01
- Data retrieval cost is applicable
- Commitment of 30 days is required
- Data retrival time is milliseconds

## Intelligent acces
### Intelligent tier
- When we do not manually want to move data from standard to IA to glacier
- We can storage unknown , changing or unpredictable data access patterns.
- We can use intelligent tiering
- It will help in reducing the cost
- There is monitoring charges applicable + data storage cost as per underlying storage class
- Data retirval cost is as per underlying storage class

## Archieval data storage 
### S3 glacier instant retrival 
- It is used to store archieval data/ long term storage for complianxce
- There is commitment of 90 days
- Data retrival time is within milliseconds
- Data retrival cost is applicable
- Data storage cost is 0.004

### s3 galcier flexible retrival 
- It provides flexibility of data retrival times
- It is used for long term arhival of data / long term complicance
  - There are 3 options
    - expidited - 1 minutes - 5 minutes
    - standard - 5 minutes to 5 hours
    - bulk - 5 hours to 12 hours
- Data retrival cost is applicable
- Data storage cost is 0.003 gb / month

### s3 glacier deep archieval 
- There are 2 options
  - standard - within 12 hours
  - bulk - within 48 hours
- data retrival cost is 0.00099 gb / month 
