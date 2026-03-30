# interface endpoint dns
- by default, the interface endpoint recieives the private DNS. whihc is very length and very inconvinient
- We need use --endpoint-url <private-dns> in aws sqs --queue-url <> --message <message> --endpoint-url <private-dns>
- So if we want to make use of only the queue url which is short we need to
  - enable DNS routing in VPC
  - enable DNS hostname in VPC
  - enable private dns in interface endpoint
- Now we do not need to use --endpoint-url.

# How resolution works
- when ec2 sends request to the public sqs endpoint
- It is resolved to private sqs endpoint
- it is then resolved to private IP of ENI
- And then traffic flows to interface endpoint
