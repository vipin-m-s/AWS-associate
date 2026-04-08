# AWS glue
- It is a serverless data integration and ETL service
- It supports 70+ data source such as rds, aurora, on prem db, third party data base, it just needs connection to the database
- Automatic schema discovery:-
  - Glue crawlers crawl the database and create a glue data catalog consiting of schema
- We need to add transform script ( python, apache, ray )
- Then we can trigger the job for ETL
- Then it can load the result to s3, redshift or other data warehousing.


# data catalog
- It is a centralized repository for storing the metadata information about the schema like headers, type of headers etc
- It can be utilized by other AWS services such as Athena for quering

# glue crawleres
- Data catlaog is automatically creeated and updated by crawlers
- The AWS glue performs scehma discovery with the help of crawlers
- We can trigger manually or scheduled
- If data source is AWS service, It requires the IAM role with IAM policy for accessing it example. s3 bucket.


# Glue jobs
- If we want to extract transform load, we need to create glue job
- We specify the source and target data
- Then we can trigger on-demand or based on event

# Job bookmarks
- If we trigger the job agin, then same data is read, transformed and loaded.
- It can be enabled and disabled any time

# without job bookmarks
- It will create duplicate date in targte
- It will be expensive and time consuming

# with  job bookmarks
- Only changed or new data is Extracted, transformed and loaded
- It will be cheaper since only new data/updated data is processed
- Less time consuming and less storage is required

# Glue studio 
- It is used for graphical user interface based Glue job creation  1
