# docker-star
Ref: 
* https://docs.docker.com/machine/reference/
* https://docs.docker.com/get-started/
* [10 docker cli commands you should know](https://medium.com/the-code-review/top-10-docker-commands-you-cant-live-without-54fb6377f481)

## 10 docker cli commands
```
docker ps //lists running containers
docker pull  //pull a docker image from Docker Hub
docker build  //build a Docker Image from Dockerfile and context
docker run //Run a docker container based on a docker image
docker logs  //display the logs of a container
docker volume ls
docker rm  //removes one or more docker containers
docker rmi //remove one or more images
docker stop //stop one or more containers
docker kill $(docker ps -q)  //kill all running containers
docker rm $(docker ps -a -q)  //delete all stopped containers
docker rmi $(docker images -q)  //delete all images
```

## Test Docker version
* Run docker --version and ensure that you have a supported version of Docker

```
docker --verion
Docker version 18.06.1-ce, build e68fc7a
```

* Run docker info to view more details

```
docker info 

Containers: 2
 Running: 0
 Paused: 0
 Stopped: 2
Images: 1
Server Version: 18.06.1-ce
Storage Driver: overlay2
 Backing Filesystem: extfs
Kernel Version: 4.4.0-36-generic
Operating System: Ubuntu 16.04 LTS
OSType: linux
Architecture: x86_64
CPUs: 4
Total Memory: 15.56GiB
...

```

## Test Docker installation
* List all image that was downloaded to your machince
```
docker image ls
```

* Execute Docker image 

```
docker run [docker-image]
docker run hello-world

Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
1b930d010525: Pull complete 
Digest: sha256:92695bc579f31df7a63da6922075d0666e565ceccad16b59c3374d2cf4e8e50e
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.
```


* List Docker containers (running, all, all in quiet mode)
```
docker container ls
docker container ls --all
docker container ls -aq
```
* Folder contains docker images on host machine

The contents of the ```/var/lib/docker``` directory vary depending on the driver Docker is using for storage.
Ref: [link](https://stackoverflow.com/questions/19234831/where-are-docker-images-stored-on-the-host-machine)

## Containers
* Define a container with ```Dockerfile```

Create an empty directory on your local machine. Change directories (cd) into the new directory, create a file called Dockerfile, copy-and-paste the following content into that file, and save it. Take note of the comments that explain each statement in your new Dockerfile.

```
# Use an official Python runtime as a parent image
FROM python:2.7-slim

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable
ENV NAME World

# Run app.py when the container launches
CMD ["python", "app.py"]

```
* Create app: Create 2 files, ```requirements.txt``` and ```app.py```, and put them in the same folder with ```Dockerfile```.
requirements.txt
```
Flask
Redis
```
app.py
```
rom flask import Flask
from redis import Redis, RedisError
import os
import socket

# Connect to Redis
redis = Redis(host="redis", db=0, socket_connect_timeout=2, socket_timeout=2)

app = Flask(__name__)

@app.route("/")
def hello():
    try:
        visits = redis.incr("counter")
    except RedisError:
        visits = "<i>cannot connect to Redis, counter disabled</i>"

    html = "<h3>Hello {name}!</h3>" \
           "<b>Hostname:</b> {hostname}<br/>" \
           "<b>Visits:</b> {visits}"
    return html.format(name=os.getenv("NAME", "world"), hostname=socket.gethostname(), visits=visits)

if __name__ == "__main__":
    app.run(host='0.0.0.0', port=80)
```

* Build app
```
$ ls
Dockerfile		app.py			requirements.txt
```
Now run the build command. This creates a Docker image, which we’re going to name using the --tag option. Use -t if you want to use the shorter option.
```
docker build --tag=friendlyhello .
```
Where is your built image? It’s in your machine’s local Docker image registry:
```
$ docker image ls

REPOSITORY            TAG                 IMAGE ID
friendlyhello         latest              326387cea398
```

* Run the app
```
docker run -p 4000:80 friendlyhello
```
You should see a message that Python is serving your app at http://0.0.0.0:80. But that message is coming from inside the container, which doesn’t know you mapped port 80 of that container to 4000, making the correct URL http://localhost:4000

