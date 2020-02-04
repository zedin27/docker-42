# Docker for newbies

## What is `Docker`?

Docker is a tool to make containers, deploy, and run applications in a separate environment. It allows to update needed packages in the container before deploying the full product (libraries, binaries, files, etc). This way, the infrastructure of the software is not messed.

The way Docker works is the ability and run an application in an isolated environment called `container`. Reason behind is they are lightweight and the host of the container is in the kernel by emulating it in the hardware of the machine.

## How does it work?

To operate Docker in the computer, it uses the Docker engine. It is a client-server application that builds and executes containers using Docker components. Many containers can share the same physical resources (like CPU and memory) in a host.

Docker engines uses client-server application made up of the Docker daemon, a REST API that specifies interfaces for interacting with the daemon, and a command line interface (CLI)) client that talks to the daemon (through the REST API wrapper). It accepts `docker` commands from the CLI, such as `docker run <image>`, `docker ps`

[](https://www.notion.so/c790bbb3f9e34bf188c8f2b219da310c#d264db6c369b4e7eb45914067a66ff46)

## Docker-machine

This is where the Docker Engine magic happens. It creates Docker hosts on your operating system, company network, data center, or cloud providers like Azure, AWS, or DigitalOcean. You communicate the docker client and daemon to talk to your host.

The benefits of using docker machine is whenever:

- **Older desktop system and want to run Docker on Mac or Windows**
- **Provision Docker hosts on remote systems**

`docker-machine` uses its own command line client and Docker Engine and instal for one or more virtual system, which they can be local or remote (dockerized hosts on cloud providers).

## How to run a Docker container?

If you get problems about


### References
1) https://github.com/VBrazhnik/docker-1/wiki/How-to-Docker

2) https://docker-curriculum.com/

3) https://omarghader.github.io/docker-tutorial-phpmyadmin-and-mysql-server/
