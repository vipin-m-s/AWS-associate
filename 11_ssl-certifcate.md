# SSL/TLS certificate

We can enable https and tls protocols to the load balancers using ssl/tls certificate
secure socket layer certificate is obtained from the CA ceritficate authority 
Godaaddy, symantec, letencrypt etc


<img width="662" height="713" alt="Screenshot 2026-03-21 at 7 53 35 PM" src="https://github.com/user-attachments/assets/caa133bb-e8e1-41df-bdea-5a1f304b7ab4" />


We can also include multiple public ssl certificate when hosting multiple domains 
THis is possible with SNI
THe ELB will be able to select the right ssl cetificate based on the domain name
ALB, NLB supports this multiple listeners and multiple certificates

CLB does not support the multiple listeners with multiple certificates, it uses only 1 certtifictate
We need to creatwe multip[le CLB for multiple domains


<img width="701" height="781" alt="Screenshot 2026-03-21 at 7 57 09 PM" src="https://github.com/user-attachments/assets/cb2cb1d5-0b83-4b4c-84a3-ce987e6f8f84" />
