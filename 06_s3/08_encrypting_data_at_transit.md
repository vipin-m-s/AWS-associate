# encrypting data at transit

- When data is uploaded or downloaded we need to encyrpt the data
- S3 supports both http and https protocols.
- encryption provided using HTTPS ( ssl/tls )
- it allows us to access ipv4, dualstack, ipv4 fips required for us government, dualstack fips
- To allow only the https request and deny all http request we can use below bucket policy
```
{
  "Principal": "*",
  "Affect": "Deny",
  "Resource": "*",
  "Action": "s3:*",
  "condition": {
    "Bool": { "aws:secureTransport": "false" }
  }
}
```
