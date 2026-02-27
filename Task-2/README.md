#  Dockerized Portfolio Website Deployment using Nginx

## Project Title
Containerizing a Static Portfolio Website using Docker & Nginx

---

## Project Overview

This project demonstrates how to:

- Create a static portfolio website (HTML, CSS, JS in one file)
- Containerize it using Docker
- Serve it using Nginx
- Run the application inside a Docker container
- Expose the application using port mapping

---

##  Technologies Used

- HTML, CSS, JavaScript
- Docker
- Nginx
- Linux (Ubuntu)

 # Project Steps

### 1️⃣ Check Docker Status

sudo systemctl status docker
docker ps


# if docker not install then install and and user group and refresh 
- sudo apt-get install docker.io
- sudo usermod -aG docker $USER
- newgrp docker    
- docker ps

install docker 

### 2️⃣ Create Project Directory

mkdir portfolio
cd portfolio

### 3️⃣ Create index.html

vim index.html

### 4️⃣ Create Dockerfile

vim Dockerfile

Dockerfile Content:

FROM nginx:alpine
RUN rm -rf /usr/share/nginx/html/*
COPY index.html /usr/share/nginx/html/
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]

### 5️⃣ Build Docker Image

docker build -t portfolio:latest .

### 6️⃣ Run Container

docker run -d -p 8080:80 portfolio:latest

### 7️⃣ Verify Container

docker ps
docker images

### 8 open port 

- go to aws security and edit inbound rules for 8000 | 0.0.0.0/0 
- save this rules


### 9 Access Website

this is my public ip address for the aws 

http://13.235.18.50:8000/    

---

##  Nginx Default Directory

/usr/share/nginx/html

##  Final Result

Successfully deployed a static portfolio website inside a Docker container using Nginx.
