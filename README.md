# It should just work

Some Docker Compose examples to quickly get individual and vanilla Ping Identity software assets up and running.  These intentionally do not have any configuration.

## How to use this

Each product is in a self contained directory, with a docker-compose.yaml and env-vars.  Get your Ping Identity [devops keys](https://pingidentity-devops.gitbook.io/devops/getstarted/devopsregistration).  Update the env-vars file with your particulars.

```
docker-compose up -d
```