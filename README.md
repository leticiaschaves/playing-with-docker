# Docker Project

This Docker project allows to create, manage, and interact with Docker containers. It includes functionality for running commands on containers, downloading and managing Docker images, and creating Dockerfiles for backend and frontend applications.

This is a project I coded with Trybe support and guidance.

## Prerequisites

- Docker: Make sure you have Docker installed on your system. You can download and install Docker from the official Docker website: [https://www.docker.com/](https://www.docker.com/)

## Usage

Follow the steps below to use the different features of this Docker project.

### Creating a Container

To create a new container, run the following command:

```shell
docker create --name container01 alpine:3.12
```
### Starting a Container
To start a container, use the following command:

```shell
docker start container01
```
### Running a Command on a Container (without attaching)
To run a command on a container without attaching to its console, execute the following command:

```shell
docker exec container01 <command>
```
Replace <command> with the desired command to be executed on the container.

### Removing a Container
To remove a container, use the following command:

```shell
docker rm container01
```

### Downloading and Stopping an Nginx Image on a New Port
To download an Nginx image and run it on a new port, execute the following command:

```shell
docker run -d -p <host-port>:<container-port> nginx
```

### Replace <host-port> with the desired port on your host machine, and <container-port> with the port on which Nginx is running inside the container.

### To stop the Nginx container, use the following command:

```shell
docker stop <container-id>
```
Replace <container-id> with the ID of the running Nginx container.

### Dockerizing Backend and Frontend Applications
This project includes Dockerfiles for backend and frontend applications. You can use them to containerize your applications.

Make sure you have the necessary files in place for your backend and frontend applications, and then build the Docker images using the following commands:

```shell
docker build -t backend-image -f backend.Dockerfile .
docker build -t frontend-image -f frontend.Dockerfile .
```
Replace backend-image and frontend-image with the desired names for your Docker images.

