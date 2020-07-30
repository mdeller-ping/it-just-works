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
git clone https://github.com/mdeller-ping/it-just-works
```

Change into the product directory you wish to run.

```
cd it-just-works/pingfederate
```

Edit the env-vars file adding your EULA acceptance and devops keys.

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

## Default Connection Info

| Product | Listening Ports | Credential | URL |
| --- | --- | --- | --- |
| PingFederate | 9031, 9999 | administrator / 2FederateM0re | https://localhost:9999/pingfederate |
| PingAccess | 9000 | administrator / 2FederateM0re | https://localhost:9000 |
| PingCentral | 9022 | administrator / 2Federate | https://localhost:9022 |
| PingDirectory | 1389, 1443, 1636 | administrator / 2FederateM0re | (See PingDataConsole) |
| PingDataGovernance | 8080, 7389, 7443, 7636 | administrator / 2FederateM0re | (See PingDataConsole) |
| PingDataGovernance PAP | 8443 | administrator / 2FederateM0re | https://localhost:8443 |
| PingDataConsole | 9443 | administrator / 2FederateM0re | https://localhost:9443/console |

## TL;DR PingFederate

```
docker network create pingnet
git clone https://github.com/mdeller-ping/it-just-works
cd it-just-works/pingfederate
vi env-vars
docker-compose up -d
docker-compose logs
```
