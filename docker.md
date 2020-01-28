# DOCKER

- Docker is useful to create **isolated enviroments** _(containers)_

  - Enviroments that isn't gonna interfer with other pieces of software on our system and our application

- A system **appart** of your OS, great for development services, like databases for instance

## HOW DOES IT WORK

- We create a isolated container and it will expose a specific port for the communication _(we can change and configure the hole communication)_

## CONCEPTS

- **IMAGE**: a docker service (postgres, mongodb, redis...)
- **CONTAINER**: a instance of an image
- **DOCKER REGISTRY / HUB**: a place where you can find all the published images of docker
- **DOCKER FILE**: **recipe** (step by step) for creating a docker image

```docker
  # the entry point is an exising image
  FROM node:10

  # definition of the folder and copy the files
  WORKDIR /usr/app
  COPY . ./

  # installing dependencies
  RUN yarn

  # what port to expose (setting communication)
  EXPOSE 3333

  # run the application
  CMD yarn start
```
