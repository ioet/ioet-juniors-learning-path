---
layout: "../../../../layouts/BlogPost.astro"
title: "Docker"
---

In this guide, you will learn about tools to help you improve your experience in your development process using docker.

## Authors

- Jefferson Oña @jeffqev

## Topics

- [Authors](#authors)
- [Topics](#topics)
- [What is Docker?](#what-is-docker)
- [What are Containers?](#what-are-containers)
  - [Differences between virtual machines and containers?](#differences-between-virtual-machines-and-containers)
- [How docker helps your environment?](#how-docker-helps-your-environment)
- [How to start with docker](#how-to-start-with-docker)
  - [Linux](#linux)
  - [Mac](#mac)
  - [Windows](#windows)
    - [Docker Desktop](#docker-desktop)
    - [Docker Toolbox](#docker-toolbox)
- [Create a MySQL server using docker](#create-a-mysql-server-using-docker)
- [Docker Compose](#docker-compose)
- [References](#references)

## What is Docker?

> Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime.

## What are Containers?

Containerization is an approach to software development in which an application or service, its dependencies, and its configuration are packaged together as a container standard image. The containerized application can be tested as a unit and deployed as a container image instance to the host operating system, containers also isolate applications from each other on a shared OS this way enables developers and IT professionals to deploy them across environments with little or no modification.

### Differences between virtual machines and containers?

Virtual Machine:
It runs on top of an emulating software called the hypervisor which sits between the hardware and the virtual machine. The hypervisor is the key to enabling virtualization. It manages the sharing of physical resources into virtual machines. Each virtual machine runs its own guest operating system. They are less agile and have low portability than containers.

Container:
It sits on the top of a physical server and its host operating system. They share a common operating system that requires care and feeding for bug fixes and patches. They are more agile and have high portability than virtual machines.

![VM vs Containers](https://s7280.pcdn.co/wp-content/uploads/2018/08/containers-vs-virtual-machines-1024x522.png)

[Read more differences](https://sourcelevel.io/blog/what-is-a-linter-and-why-your-team-should-use-it)

## How docker helps your environment?

Docker helps to solve the famous phrase 'it works on my machine' because it packages all the dependencies making a standardized image.

## How to start with docker

Docker is available on different operating systems

### Linux

Depending on your Linux distro you can follow the instructions in [installing Docker Engine](https://docs.docker.com/engine/install/)

### Mac

You can just download the [docker desktop](https://docs.docker.com/desktop/install/mac-install/) for macOS

### Windows

#### Docker Desktop

You can just download the [docker desktop](https://docs.docker.com/desktop/install/windows-install/) for windows

#### Docker Toolbox

Docker toolbox allows you to deploy development containers in legacy Windows systems that do not meet the requirements of the new Docker for Windows
you can do the following instructions to install Docker [Toolbox](https://docs.bitnami.com/containers/how-to/install-docker-in-windows/#:~:text=Docker%20Toolbox%20allows%20you%20to,new%20Docker%20for%20Windows%20application.)

## Create a MySQL server using docker

With the following command, we are going to create a Mysql 8 container on background named ioetdb and the connection port in 8090

Also, the MySQL data will persist in `/home/<$USER>/data/mysql` and we pass it an environment variable that allows us to assign a password

``` shell

docker run -d --name ioetdb -p 8090:3306 \
  -v /home/user/data/mysql:/var/lib/mysql \
  -e MYSQL_ROOT_PASSWORD=S3cret \
  mysql:8

```

Now we can see the new container using the command

``` shell
docker ps

output 
CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS         PORTS                                                  NAMES
f38a2448637d   mysql:8   "docker-entrypoint.s…"   4 minutes ago   Up 4 minutes   33060/tcp, 0.0.0.0:8090->3306/tcp, :::8090->3306/tcp   ioetdb
```

We can access the container and execute a command to login into Mysql using the password defined previously

``` shell
docker exec -it ioetdb mysql -p
```

Now we can execute any SQL query

``` shell

mysql> create database demo;
Query OK, 1 row affected (0.26 sec)

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| demo               |
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
5 rows in set (0.00 sec)
```

Learn more about docker run options in [Docker run references](https://docs.docker.com/engine/reference/run/)

You also can learn more in this youtube [tutorial](https://www.youtube.com/playlist?list=PL4cUxeGkcC9hxjeEtdHFNYMtCpjNBm3h7)

## Docker Compose

Docker Compose is a tool that was developed to help define and share multi-container applications. With Compose, we can create a YAML file to define the services and with a single command, can spin everything up or tear it all down

Using docker compose the command to create a MySQL server that we used in the previous step can be summarized in the following file

``` YAML
version: '3.9'

services:
  mysql:
    image: mysql:8
    ports:
      - 8090:3306
    volumes:
      - /home/user/data/mysql:/var/lib/mysql
    environment:
      - MYSQL_ROOT_PASSWORD=S3cret
```

In case we need another database the YAML file would look like this

``` YAML
version: '3.9'

services:
  mysql:
    image: mysql:8
    ports:
      - 8090:3306
    volumes:
      - /home/user/data/mysql:/var/lib/mysql
    environment:
      - MYSQL_ROOT_PASSWORD=S3cret

  pg:
    image: postgres:14
    ports:
      - 8091:5432
    volumes:
      - /home/user/data/pg:/var/lib/postgresql/data
    environment:
      - POSTGRES_USER=postgres
      - POSTGRES_PASSWORD=postgres
```

We can stack several containers in this way

## References

- [What is Docker?](https://aws.amazon.com/docker/)
- [Introduction to Containers and Docker](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/container-docker-introduction/)
- [Difference between Virtual Machines and Containers](https://www.geeksforgeeks.org/difference-between-virtual-machines-and-containers/)
