- [Container  basics](#container--basics)
- [containers](#containers)
    + [key benefits of containers](#key-benefits-of-containers)
- [Docker](#docker)
- [Container orchestration](#container-orchestration)

<small><i><a href='http://github.com/3kh0/readme-toc/'>Table of contents generated with readme-toc</a></i></small>


<img width="651" height="281" alt="Screenshot 2026-04-05 at 7 32 13 AM" src="https://github.com/user-attachments/assets/132d978f-3cb6-47e5-999e-7bb602a5e461" />There are 3 container services provided by AWS
- AWS ECS 
- AWS EKS
- AWS Fargate ( serverless data plane )

# Container  basics
- Containers solve the problem of It runs on my machine.
- When developers develop application with code, libs etc.
- The server might have different version of the apps/libs.

<img width="722" height="332" alt="Screenshot 2026-04-05 at 7 28 23 AM" src="https://github.com/user-attachments/assets/1c2a11dc-05a3-46c0-b759-c06d0f36e833" />

<img width="645" height="277" alt="Screenshot 2026-04-05 at 7 32 21 AM" src="https://github.com/user-attachments/assets/befd34d2-dbc6-475a-b7d3-db0e645fd7e7" />


# containers
- Containers are lightweight , they do not contain the operating system
- We can boot container images within seconds
<img width="299" height="596" alt="Screenshot 2026-04-05 at 7 30 17 AM" src="https://github.com/user-attachments/assets/3ec0dbf3-60a6-459b-b369-0450d1175081" />

### key benefits of containers
1) Isolated environment - each container runs in its own isolated environment
2) Lightweight - since containers utilize underlying os, they are lightweight, minimal kernel
3) Consistency - we can run the same container in many environments all will have same configuration
4) Portable - we can run the container in dev laptop, physical server and vm in cloud 

# Docker 
- Docker is an open platform for developing, shipping and running application as containers.
1. Launch ec2 instance
2. Install docker - sudo dnf install docker -y
3. Create a index.html
4. Create a docker file
FROM httpd
COPY index.html /usr/share/apache2/htdocs/
6. Create a docker image
docker build -t myserver .
7. Create a docker container
docker run --name web-server-1 --port 80:80 -d myserver

# Container orchestration 
- Earlier monolitchic architecture was user where there was UI service -> Large Backend service -> Database
- It is difficvult to modify only one service, any issues will bring entire backend down, difficult to update one service
- Hence microservices was started.
- There will be many services which communicatwe with each other and reach service runs inside a container.
- There can be 1000s of containers. To manage it is difficult like restart container, placement of container.
- Hence we need orchestration of containers.
![Uploading Screenshot 2026-04-05 at 8.15.32 AM.png…]()

