# CS3219: Docker and Kubernetes Lab

## Docker
Docker Docs defines Docker as follows: 
> _Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production._

The documentation can be found [here](https://docs.docker.com/).

### Introduction
Docker allows developers to package their applications and dependencies into a lightweight container by providing a layer of abstraction of OS-level virtualisation on Linux.

Docker containers are relatively well isolated from eachother and the host machine. So, developers can run their applications on any machine that has Docker installed, regardless of the underlying OS.

Unlike virtual machines, containers do not have high overhead and therefore able to efficiently use the system resources.

Apart from portability, Docker has many benefits, including:
1. **Streamlining [SDLC](## "Software Development Lifecycle")**: Allows developers to work in standardised environments with local containers. As such, containers are very useful in [CI/CD](## "continuous integration and continuous delivery/continuous deployment" ) workflows.  
2. **Scaling**: Docker's portability and lightweight nature allows for easy scaling of applications. It makes it easy to dynamically manage workloads, scale up/tear down applications and services as required, in almost real-time.
3. **Allowing multiple workloads on same hardware**: Docker provides a cost-effective alternative to virtual machines.  

### Installation and Setup
Please install Docker for your respective OS [here](https://docs.docker.com/get-docker/).

Please follow the instructions/install updates (if any). If successful, you will have installed Docker Desktop on your device. 

Docker Desktop provides a GUI to help manage containers, applications, images, etc. It can be used as is or as a complementary tool to the Docker CLI.

You can find what is included in Docker Desktop [here](https://docs.docker.com/desktop/).

Test your installation by running the following command in your terminal:
```bash
docker run hello-world
```
If successful, you should see something similar to the following output:
```bash
Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
 ```

 > ⚠️ _**Warning**_ ⚠️
    > You will face errors if you don't start the Docker daemon before running the command. If you are using Docker Desktop, you can start the daemon by clicking on the Docker icon in your taskbar/open the Docker Desktop app. If you are using Docker CLI, you can start the daemon by running `dockerd` in your terminal (This option better applies to Linux users).

> 📝 **Note:** Running your terminal and Docker at different privilege levels may cause issues. For example, running your terminal as an administrator and docker as a normal user may cause issues. If you face any issues, try running both at the same privilege level.

### Concepts and Terminologies
Before we get our hands dirty, lets familiarise ourselves with some of the common concepts and terminologies associated with Docker.