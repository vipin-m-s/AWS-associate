# Pre signed url 

Imagine a music company who is responsible for creating musoic files and uploading to s3 bucket
Suppose they want the customers to download music only for whcih they have signed for
By default only the owner of the objects will be able to access the objects
With help of pre signed URL the owner can allow others to access the file and download for a time- limit in minutes/hours.  
The pre signed URL will expire after the exipry duration and the content will be not accessible 
