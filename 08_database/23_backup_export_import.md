# backup 

There are 2 types of backup options

## point in time restore
- It is automatically backed up continously
- We can restore wih 1 sec granularity for past 35 days
- Recovery creates a new table

## On demand backup 
- This is a manual backup option
- If we want to store the backup for more days we can use this
- We can automate the backup using AWS backup service with daily, weekly or monthly backup
- Recovery creates a new table


# Export and Import
## export
- It uses PITR snapshots to export data from specific point in time
- It doesd not consume read/write capacity 
- We can export the data from the dynamodb table to s3 and then use the data with other services such as Athena for data analyitcs
- Use case :- data analytics

## Import
- We can import the table data stored in dynamodb table
- The data is stored in JSON, csv format
- After importing a new table is created, it will not overwrite the table
- Use case :- bulk loading, migrations

