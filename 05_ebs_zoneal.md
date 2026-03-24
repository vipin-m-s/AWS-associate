# EBS

- EBS are availability zone scoped.
- They can attach to ec2 instances within the same AZ.
- We cannot attach ec2 instance to ec2 in different AZ
- We can detach the NON root ebs volume and attach to other instancce within the same AZ
- WE cannot ATTACH root ebs volumes to other ec2 instance as it contains OS

# Detach and attach
<img width="532" height="586" alt="Screenshot 2026-03-24 at 5 42 59 AM" src="https://github.com/user-attachments/assets/6f269ff1-f637-4a45-a4d3-385f72f492c1" />


<img width="606" height="598" alt="Screenshot 2026-03-24 at 5 43 19 AM" src="https://github.com/user-attachments/assets/b3cbaabe-2fcc-466f-8a54-44b3086e5c9c" />
<img width="583" height="598" alt="Screenshot 2026-03-24 at 5 43 32 AM" src="https://github.com/user-attachments/assets/33470f44-0964-42d7-b98e-1be5a1534ed9" />

# Moving ebs volume to other AZ

<img width="722" height="683" alt="Screenshot 2026-03-24 at 5 44 18 AM" src="https://github.com/user-attachments/assets/a4286c96-2560-4361-a5a5-94d8ceca6737" />

## create snapshot

<img width="633" height="675" alt="Screenshot 2026-03-24 at 5 44 55 AM" src="https://github.com/user-attachments/assets/5ca0895e-e4d9-49eb-8848-07ed43474d2d" />
## Create new volume
<img width="623" height="748" alt="Screenshot 2026-03-24 at 5 45 20 AM" src="https://github.com/user-attachments/assets/e0670b5b-0d4a-49bb-84e4-612999ace282" />

## attach to ec2
<img width="684" height="710" alt="Screenshot 2026-03-24 at 5 45 56 AM" src="https://github.com/user-attachments/assets/9d24e597-5eb5-4177-9162-fb63ad91edb9" />
