# It should just work

Quickly stand up vanilla software assets from Ping Identity, such as PingFederate, using Docker Compose.  Specific image tags are used, to produce predictable outcomes.  Each product directory is self contained.  Your data will persist in the volume sub directory.

## Prerequisites

* Docker
* [Ping Identity Devops Key](https://pingidentity-devops.gitbook.io/devops/getstarted/devopsregistration)

## How to use

Create an external bridged network for communication between containers.

```
docker network create pingnet
```

Clone this repo.

```
docker-compose up -d
```

Change into the product directory you wish to run.

```
cd it-just-works/pingfederate
```

Edit the env-vars file with your devops keys and acceptance of the EULA.

```
vi env-vars
```

Use docker-compose to start the container

```
docker-compose up -d
```

View the log files

```
docker-compose logs -f
```

Stop the container

```
docker-compose down
```

## TL;DR PingFederate

```
docker network create pingnet
git clone https://github.com/mdeller-ping/it-just-works
cd it-just-works/pingfederate
vi env-vars
docker-compose up -d
docker-compose logs
```
