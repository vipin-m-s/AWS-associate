# versioning

## Challenges of storage without versioning

### Overwrite
- If we upload a file called a.txt
- Team member also uploads file called a.txt with different content
- Our file contents are lost

### Deletion 
- If we have file called a.txxt
- If someone deleted the file
- Then file is permanently lost

## To overcome these challenges we have s3 bucket versioning functionality 
- If s3 bucket versioning is enabled
- If we upload a file with same name all its versions is manintained
- If we delete a file, A delete marker is added but the file is not permanently deleted.
- We can click on show versions button to see all version
- version id is maintained for each version
- Older versions can be retrieved


## Points to note
- If versioning is enabled on s3 buckeet, we cannot disable the versioning, bucket versioning will only be suspended
- --- Means new objects version will not be maintained
- --- older objects with version will still exist and it will not be deleted
- If we enable versioning for a s3 bucekt, All objects versioning will be maintained.
- --- We cannot choose some objects for versioning
