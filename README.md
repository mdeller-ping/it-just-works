# It should just work

Quickly stand up vanilla software assets from Ping Identity, such as PingFederate, using Docker Compose.  Specific image tags are used, to produce predictable outcomes.  Each product directory is self contained.

## Prerequisites

* Docker
* [Ping Identity Devops Key](https://pingidentity-devops.gitbook.io/devops/getstarted/devopsregistration)

## Create a network

Create an external bridged network for communication between containers.

```
docker network create pingnet
```

## How to use

Clone this repo.  Edit the specific env-vars file with your devops keys and acceptance of the EULA.

```
docker-compose up -d
```

## TL;DR PingFederate

```
docker network create pingnet
git clone https://github.com/mdeller-ping/it-just-works
cd pingfederate
vi env-vars
docker-compose up -d
```
