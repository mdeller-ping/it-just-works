# It should just work

Quickly stand up individual software assets from Ping Identity, such as PingFederate, using Docker Compose.  Specific image tags are used, to produce predictable outcomes.  Each product directory is self contained.

## Prerequisites

* Docker
* [Ping Identity Devops Key](https://pingidentity-devops.gitbook.io/devops/getstarted/devopsregistration)

## How to use

Clone this repo.  Edit the specific env-vars file.

```
docker-compose up -d
```