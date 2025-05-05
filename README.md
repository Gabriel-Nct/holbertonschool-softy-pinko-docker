# 🐳 Docker Project for Softy Pinko Application 🐳

## 📋 Overview

This project implements a containerized infrastructure for the Softy Pinko application using Docker. The infrastructure consists of:

- 🔄 A reverse proxy and load balancer
- 🖥️ Multiple API servers (back-end)
- 📄 A static content server (front-end)

## 🛠️ Project Structure

The project is organized into progressive tasks, each building upon the previous:

### Task 0: First Docker Image

- Creating a basic Docker image based on Ubuntu
- Setting up the environment with apt-get update and upgrade

### Task 1: Back-end Setup

- Building a Flask API server
- Exposing a simple endpoint that returns "Hello, World!"

### Task 2: Front-end Setup

- Setting up an Nginx server for static content
- Configuring Nginx to serve the Softy Pinko front-end files

### Task 3: Connecting Front-end and Back-end

- Enabling cross-origin requests with Flask-CORS
- Implementing AJAX calls from the front-end to the back-end

### Task 4: Docker Compose Integration

- Creating a docker-compose.yml file to manage multiple containers
- Defining services, ports, and dependencies

### Task 5: Proxy Server Implementation

- Adding an Nginx proxy server
- Configuring routing to direct traffic to the appropriate services

### Task 6: Horizontal Scaling

- Implementing load balancing with multiple API servers
- Using Docker Compose to scale the back-end service

## 🚀 Key Concepts

### 🔄 Reverse Proxy

The proxy server routes incoming requests to either the front-end static server or the back-end API servers based on the URL path.

### ⚖️ Load Balancing

Requests to the API are distributed across multiple back-end servers using Round Robin load balancing, which evenly distributes traffic to prevent any single server from becoming overwhelmed.

### 🔒 Isolation

Each component runs in its own container, providing isolation and making the application more maintainable and scalable.

## 📝 Notes on Docker

### Docker Images

- Docker images are read-only templates used to create containers
- Built using Dockerfiles that specify the base image and setup instructions

### Docker Containers

- Instances of Docker images that run as isolated processes
- Can communicate with each other through defined networks

### Docker Compose

- Tool for defining and running multi-container Docker applications
- Uses YAML files to configure application services
- Simplifies container management with a single command

## 🏗️ Implementation Details

- The back-end uses Python and Flask to serve API requests
- The front-end uses Nginx to serve static HTML, CSS, and JavaScript
- The proxy server uses Nginx with custom configuration for routing and load balancing
- All components are containerized with Docker for easy deployment and scaling

## 🌐 Benefits of This Architecture

- 🔍 Improved visibility through the proxy server
- 📈 Better scalability with the ability to add more back-end servers
- 🔧 Easier maintenance with isolated components
- 🚀 Consistent environment across development and production

Happy containerizing! 🐳
