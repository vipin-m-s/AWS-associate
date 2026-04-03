# s3 performance

- multi part upload and byte range access
- Prefix paritioning
- AWS s3 transfer acceleration
- AWS cloud front

# prefix partitioning
- S3 scales the requests as per prefix
- PUT POST DELETE COPY 3300 requests/sec per prefix
- GET/HEAAD 5500 requests/sec per prefix
- Instead of stopring /logs/2016_05_01.log store in /logs/2016/05/01/file.log this will increade the throughput
- Store image1/hash1/img image2/hash2/img etc
- The throughput increases when we create multiple paritions
- We can perform parallel access on prefixes
- Prefixes are also used in lifecycle , bucket replication

# Multi part upload
- It is used to increase the performance of object upload process
- The object > 100 MB is divided into parts and parts are uploaded to s3 and the parts are rejoined in s3
- It is recommended for objects > 100 MB
- It is must for objects > 5GB
- If we are uploading 5 GB file and if network is flaky and uplkoad fails , we might have to reupload the entire file again
- With the multi part upload only the failed parts are re-uploaded
- with aws s3 cp commmands it uses multi part upload by default
- With non multi part upload we might not fully use bandwidth since there is limit for each hhtttp requesy
- With multo part upload + multiple threads we can fully utilize bandwidth

# byte range fetch 
- this feature is used for improving performance of download
- We can download the object in byte ranges for parallel downloads
- THis increases the throughput of download
- use cases
  - downloading large file
  - media file
  - We want to do partial read operation
  - resumable download
- done using aws s3api cli command `--range bytes=0-500`

# S3 transfer acceleration 
- When we are inh in india and bucket is in US, our traffic will flow through non-aws network and hence latency might be high
- If we use transfer acceleration our data will flow to the nearest edge location and it is connected to region via AWS backbone network 
- There are edge locations created across the world by amazon and they manage it
- The latency will be very low when using s3 transfer acceleration
- They are a  charged service
- They can be enabled/disabled at bucket level
- They use optimized network protocols
- They have different endpoint accelerate.amazonaws.com

# s3 with cloudfront 
- Cloudfront is a CDN service by AWS
- It will serve the content via edge locations
- It will cache the static contents such as images, vedios etc in edge locations
- It has reduced data transfer out charges compared to s3
- It supports multiple source data points
<img width="794" height="478" alt="Screenshot 2026-04-03 at 5 47 59 PM" src="https://github.com/user-attachments/assets/9520b599-e602-4439-a832-4231d3713cdd" />

