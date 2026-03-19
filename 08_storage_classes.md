# storage classes

There are multiple storage classes provided for storage service for all types of customer use cases
Some of the storage classes are 
1) S3 standard storage
- When we have frequently access data we can use standard
- When we want fast retrieval times we can use standard
- It is a premium storage service
- It provided 11 9s durability
- we will loose 1 file in 10 million years
- Cost is high - 23 dollars for 1 TB storage

2) S3 standard infrequent access
- We can use this for infrequently accessed data
- But we want to retrieve this data fast when we need it
- It is cheaper than standard
- If lesser data is accessed. The cost will be reduced
- It also provied 11 9s durability 

3) S3 glacier
- glacier is used for storing archieve data or logs for long term
- It is for storing infrequently accessed data
- It is used for data which is not required fast access
- It can take hours to get back the data
- Now, if we pay more money we can get data within minutes. 
