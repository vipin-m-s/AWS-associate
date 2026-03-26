## HTTP 
- When we communicate with our bank website using http
- The username and password is sent as plain text over the internet.
- a attacker is able to steal the credentials and get access to the website
<img width="1010" height="664" alt="Screenshot 2026-03-26 at 5 09 58 AM" src="https://github.com/user-attachments/assets/23c1725d-9115-4bcd-a3de-7237469d6541" />

## HTTPS
- When we use https ( application  layer - http ) , it uses ssl/tls which are layer 5 and layer 6 protocols
- We encrypt the data which is sent from client to the server
- Hence the hacker will not be able to read the data

## Simple analogy
- Suppose Mr x gives you lot of money and asks you to give it to mr y
- You will carry the money in your hand
- Now there can be a thief who can interupt you in middle and steal all your money
- He does it because youre carrying money in hand and eveyrone can see it
- THis is called privacy ( No1 should be able to see what is being sent between client and server ) 
<img width="1168" height="345" alt="Screenshot 2026-03-26 at 5 13 16 AM" src="https://github.com/user-attachments/assets/0934ee28-22fc-4a55-a65e-ecdb42e864d3" />
- We can pack the money in a suitcase with lock and then send it
- And mr y only knows the combination to unlock the suitecase
- Now attacker cannot see whats inside the suitecase
- If he steals also he will not be able to open it
<img width="1221" height="710" alt="Screenshot 2026-03-26 at 5 15 06 AM" src="https://github.com/user-attachments/assets/25bf247d-a4e5-4032-9c69-0760114a69b9" />


Lets now conside a scenario
- When you are going to send money
- If there is dummY who is impersonating Mr. Y
- you have never seen mr.y
- This is called authenticity ( we are delivering the message to right party )
- WE can request the person to show hiss ID, Since dummY dioesnt have we wil ask mr.Y he has ID sp we can give him the cxase
<img width="1208" height="460" alt="Screenshot 2026-03-26 at 5 17 29 AM" src="https://github.com/user-attachments/assets/eba67c2d-7a4c-4359-aad2-94123dea3e02" />

lets consider a scenario now
- You become greedy
- When you are putting the moneuy in suitecase
- you steal some money and deliver it to the mr.y
- But mr.y will call mr.x and ask about the money
- Then we will know if money was stolen.
- This is called Integrity ( what was senmt is what is recived )


## Principles of secure communication
- Authenticity
- privacy
- integrity

### Authenticity
- How can client know if the server is the right server and not fake server?
- The server needs certificate which can prove its authenticity
- It creates a certificate and sends a CSR ( ceritficate signing request ) to CA ( ceritifcate authority )
- The CAs are well established organizations
- The add there digital signature to the certificate


<img width="1169" height="605" alt="Screenshot 2026-03-26 at 5 24 07 AM" src="https://github.com/user-attachments/assets/b80e8630-2910-46a8-81a8-0f0d02a2b65f" />
- Now the certificate is digitally signed by the CA
- The client will send a hello message to the sserver.
- The server will send the certificate to prove his authenticity
- How will client trust the server ? How does it know whether the certificate is geniune.
- SInce CA has signed the ceritificate.
- The Client has a trust store. This trust store has list of all the digital signatures of the Certificate Authorities.
- It will compare the digital signature from the ceritifcate and the trust store with which he will know it is genuine


<img width="1148" height="494" alt="Screenshot 2026-03-26 at 5 27 15 AM" src="https://github.com/user-attachments/assets/ea5bf4b5-cbda-4cbc-b578-d9910b77b714" />

- Authenticity is now solved

## Privacy 
- The data needs to be encrypted between the client and the server
- The server generates a public key and private key ( asymmetirc keys :- data encrytped used public key can be decrpyted using private key )
- The server along with the ceritificate send the public key.
- The client upon reciving the public key
- Will encyrpt data using public key and send send encypted data to the server
- Some algorithms for this are RSA ( Rivet - Shamir - adleman )
- It is very computationally heavy to encyrpt
- Hence cannot be used for evry traffic request andf not suitabler for traffic data encyrption

<img width="1231" height="601" alt="Screenshot 2026-03-26 at 5 30 32 AM" src="https://github.com/user-attachments/assets/f5ebf009-34a2-49f5-868c-d9cc5ac2f0eb" />

- The problem is that, there can be only 1 way communication
- The private key cannot encrypt the data.
- Which is undesireable

- The client generates a session key ( symmetric key - we can encrypt and decrpyt data using same keys )
- Some algorithms are AES ( advaned encryption standard ) , 3DES ( triple data encryption standard ) 
- They are not computationally heavy. They are suitable for network encyrption.
- But the challenge is how can we transfer the symmetric key to server
- If we directly send it They hacker can get access to session keys and he will be able to read the data being sent
- So we need to encrypt the session key using public key and send it toserver
- The server using private key will decrypt the session key
- The session key is then used to encyrpt the network traffic betwween the client and server


<img width="1126" height="756" alt="Screenshot 2026-03-26 at 5 40 17 AM" src="https://github.com/user-attachments/assets/3e748576-8887-4999-a34c-074254d79e0b" />

- Data privacy is now solved
- No1 is able to view what is being sent from client to server and server to client

## Integrity 
- How can client/data ensure that the data was not tampered on its way
- It uses hashing function
- Hash is generated for the data and it is unique to the data. The hash cannot generate data.
- The client will send data along with hash to the server
- The server once it recieves the data + hash
- Generates the has from the same data.
- The generated hash and recieved hash is compared to check for integrity
- If it matches there is no tampering.

<img width="1019" height="733" alt="Screenshot 2026-03-26 at 5 45 12 AM" src="https://github.com/user-attachments/assets/dc6de09e-9371-4530-8449-5af63f054bf7" />

- Popular algorithms for hash algorithms are
- MD5 - message digest
- SHA - secure hashing algorithm

# How will the client and server know which algorithm to use for asymmetric key, symmetric key and hash ? 
- Cipher suite
- When client sends the hello message to server
- The server responds with certificate + public key + cipher suite ( Collection of all algorithms the server has - AES - RSA - SHA )
- The client then decides upon the algorithm it has. If there is common algorithm they agree
- If there is no common algorithm then there can be failures

