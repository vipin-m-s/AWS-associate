# TYpes of load balancer
There are 3 types of load balancers
## application load balancer 
- It works at layer 7 ( application layer ) of OSI model
- It supports protocols such as HTTP HTTPS websocket grpc http/2

## netowkr load balancer
- It works at layer 4 ( transport layer ) of OSI model
- It supports protocol such as TCP, UDP and TLS ( secure tcp )
- It gives better performance since it does not have to process HTTP headers

## Gateway load balanccer 
- It works at layer 3 ( network layer )
- It supports GENEVE protocol
- IP protocol
- It is used for monitoring the traffic and not used to serve the requests

# OSD model 
Layer 7 - Application layer - HTTP hTTPS http/2 websocket gRPC 
Layer 6 - Presentation layer 
Layer 5 - 
Layer 4 - Transport Layer
Layer 3 - 
Layer 2 - 
Layer 1 - Physcial layer
