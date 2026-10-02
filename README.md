# Dockerized HTML Website 🐳

A beginner-friendly Docker project demonstrating how to package and run a simple HTML website inside an Nginx Docker container.

## 📌 Project Overview

This project is my first practical Docker project.

The website is built using HTML and served through an Nginx web server running inside a Docker container.

## 🛠️ Technologies Used

* HTML
* Docker
* Dockerfile
* Nginx
* Linux / Ubuntu

## 📁 Project Structure

```text
Project-01-Dockerized-Website/
├── Dockerfile
├── index.html
└── README.md
```

## 🐳 Dockerfile

The Dockerfile uses the lightweight Nginx Alpine image and copies the HTML file into Nginx's default web directory.

```dockerfile
FROM nginx:alpine

COPY index.html /usr/share/nginx/html/index.html
```

## 🚀 How to Run

### 1. Build the Docker image

```bash
docker build -t my-docker-website .
```

### 2. Run the container

```bash
docker run -d -p 8080:80 --name my-website my-docker-website
```

### 3. Check the running container

```bash
docker ps
```

### 4. Open the website

Open the following address in a browser:

```text
http://localhost:8080
```

## 🛑 Stop the Container

```bash
docker stop my-website
```

## ▶️ Start the Container Again

```bash
docker start my-website
```

## 🔍 View Container Logs

```bash
docker logs my-website
```

## 🧹 Remove the Container

First stop the container:

```bash
docker stop my-website
```

Then remove it:

```bash
docker rm my-website
```

## 🎯 What I Learned

Through this project, I practiced:

* Installing Docker Engine on Ubuntu
* Understanding Docker images and containers
* Creating a Dockerfile
* Building a Docker image
* Running a Docker container
* Port mapping
* Managing containers
* Viewing container logs
* Serving a website using Nginx inside Docker

## 📚 Learning Goal

This project is part of my hands-on journey toward learning Docker and DevOps.

More Docker projects will build on these fundamentals.
