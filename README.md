# simple-docker-image-building
Process to create a docker image using python base image.

# Docker Python Application

This is a simple Python application that demonstrates the use of Docker to containerize a Python script. The script prints a message and the current working directory when the container is run.

## Files

- **Dockerfile**: Defines the container image and the steps to set up the environment.
- **app.py**: A basic Python script that prints "This is the first image!!!" and the current working directory.

## Requirements

- [Docker](https://www.docker.com/get-started) installed on your system.
- Python (in the container, so no need to install it locally).

## Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/your-repository-name.git
   cd your-repository-name

2. Build the Docker image:

docker build -t python-docker-app .

3. Run the Docker container:

docker run python-docker-app

You should see the following output:
This is the first image!!!
Current Dir is:  /app


How it works:
The Dockerfile specifies that the container should use the official Python image as the base image.
The WORKDIR instruction sets the working directory inside the container to /app.
The COPY instruction copies the contents of the current directory (where the Dockerfile and app.py are located) into the /app directory inside the container.
The CMD instruction tells Docker to run python3 app.py when the container starts.

