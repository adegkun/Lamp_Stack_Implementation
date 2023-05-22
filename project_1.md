# Project 1 — LAMP STACK IMPLEMENTATION

A technology stack is a set of frameworks and tools used to develop a software product. This set of frameworks and tools are very specifically chosen to work together in creating a well-functioning software. They are acronymns for individual technologies used together for a specific technology product. some examples are…

1. LAMP (Linux, Apache, MySQL, PHP or Python, or Perl)
2. LEMP (Linux, Nginx, MySQL, PHP or Python, or Perl)
3. MERN (MongoDB, ExpressJS, ReactJS, NodeJS)
4. MEAN (MongoDB, ExpressJS, AngularJS, NodeJS)

# Configure the LAMP Stack

LAMP stands for Linux Apache MySQL and PHP. It’s a very common architecture for web applications. If you think about the LAMP stack in broad terms you have an operating system (Linux), a web server (Apache), a database tier (MySQL), and a programming language (PHP). 

# Project Recommendations
It is recommended you have familiarity with the basics of Linux, an understanding of how to configure and download various types of services and formidable researching skills.


Follow below steps to install and run nginx container on Ec2

```
sudo yum update -y
sudo yum install docker 
sudo systemctl start docker
sudo systemctl enable docker
```

Confirm Docker is running 


```
systemctl status docker
```

Pull and Run a nginx container 
```
sudo docker pull nginx
sudo docker run -p 80:80 --name nginx-server -d nginx
```

List Docker images  
```
sudo docker images 
```

List Running Containers
```
sudo docker ps
```

![](imgs/week1/Docker-deployed-on-EC2.PNG)

Stop Running Containers
```
sudo docker stop <Container-ID> --- Insert Container ID
```
# Deployed app on local machine

I installed docker-desktop on windows and deloyed app on local machine

![](imgs/week1/app-deployed-locally.PNG)

# Push Image to DockerHub

Create a repository for the image in DockerHub
```
docker build -t crudbackend-app:1.0 .
docker image tag crudbackend-app:1.0  adegkun/crudbackend-app:1.0
docker push adegkun/crudbackend-app:1.0
```
![](imgs/week1/DockerHub.PNG)

