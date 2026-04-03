# s3 pre signed url 
- If we want to provide temporary access to s3 objects which are in private bucket
- We can do it via presigned url. The credentials to access the url will be in url. These are temporary credentials
- We do not need to share any crecentials with the anonymouse user.
- The pre signed url is created using The creators credentials. It can be created only if the cretor has the correct permisssions
- Any one with the url can access the object
- We can specify the expiration time 
- If the permission of the creator is deleted , then the link will not be accessible for anyone.
- can be generated via console, cli
- Supports uploading and downloading the objects via presigned url 
