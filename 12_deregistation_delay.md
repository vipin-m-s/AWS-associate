# connection draining ion CLB / de-registration delay in NLB, ALB

 - Time to complete the inflight requests while the instances is de-registring
 - If the servers are not able to complete the requests within the time, request is forcefully shut off
 - No new requests are sent to that server.
 - Existing requests are given time to complete
 - default value is 300 seconds
 - We can set to 0 to remove the delay
 - If we set too high, the draining of the instances will take time
 - If we set too low, the inflight requests are terminated*/X/XCV
