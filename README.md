# Project Title

Docker Exercise - An absolute freestyle project

## Getting Started

These instructions will enable you to run the tests intended for the files created here.

## Prerequisites

What things you need to install the software and how to install them

```
Docker CE
```
## Procedure

### Step one

First step is to build the docker files

```
$ docker build -f ./flask-app-test2/Dockerfile -t flask-app:1.0.0 .
```

And 

```
$ docker build -f ./nginxreverseproxy/Dockerfile -t nginx-proxy:1.0.0 .
```

It can be tagged as latest
### Step two

Create network

```
$ docker network create --driver bridge test-network
```

### Step three

Run the containers

```
docker run --name flask-test-app --network test-network -d flask-app
```

```
docker run --name nginx-test-proxy --network test-network -d -p 9939:80 nginx-proxy
```

## Tests

Visit localhost:9939

## Built With

* [Flask](https://flask.palletsprojects.com/en/1.1.x/) - The web framework used
* [Nginx](https://www.nginx.com/) - Reverse proxy
* [Docker](https://www.docker.com/) - Container 

## Authors

* **Ejiro Agarin** 

See also a resource [document](https://medium.com/@codingwithmanny/create-an-nginx-reverse-proxy-with-docker-a1c0aa9078f1) by Manny whose article was handy in this project.


## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
