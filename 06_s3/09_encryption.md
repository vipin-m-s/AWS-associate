There are 2 types of encryption in s3
# server side encryption 
- The encytion occurs s3 bucket
- There are 3 types of server side encurption

## SSE-s3
- the encrption keys are generated and managed by s3 service itself
- THis is on by default, we can disable this option.
- For s3 data is being stored so it will encyrpt any data
- For SSE-s3 the http header will include the encryption algorithm
- "x-amz-server-side-encryption" : "AES256"

## SSE-KMS
- Encryption key is managed by amazon key management service
- It can be used for audiiting the necyrptioin keys, audition the objects etc using cloudTrail
- "x-amz-server-size-encryption" : "aws:kms"

## SSE-C
- customer manager encryption keys
- customer will generate the encruption keys and share the encyrption keys to s3
- It can only work with HTTPS.
- "x-amz-server-side-encryption-algorithm" : "AES256"
- "x-amz-server-side-encryption-key" : 256 bit, base64 encoded keys

# client side encryption 
Inclient side encyrption client will encrypt the data and send to the s3
- aws provides aws encruption client
- which can be used to create keys, and encyrpt / decrypt the data
- we can doiuble encyrypt the data with server side encyrptyion as well



