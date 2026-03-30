# Flow logs vs traffic mirroring

- flow logs collect only metadata of the packets such as source ip, source port, dest ip , dest port etc , whereas the traffic mirroring captures actual packet payload data
- flow logs is used for troubleshooting connectivity issues where as traffic mirroring is used for Deep packet insection, intrusion prevention
- flow logs are lightweight whereas the traffic mirroring is heavy
- Flow logs are cheap whereas traffic mirroring is costly
- Flow logs can be shared with s3, kinesis etc,. Whereas the traffic mirroring is used to share with 3rd party network appliances
