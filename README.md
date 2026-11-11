# Docker Workshop
> CSUS Academic Team

## Docker? I Just Met Her!

Docker is a program that creates virtual environments so that services can run in isolation from each other. It also streamlines the build process for creating these containers.

## Getting started

### Windows

Install the Docker Desktop application

### MacOS

???

### Linux

Install docker using your preferred package manager

## Relevant Parts

For the purposes of this workshop, we are interested in Docker Compose. This allows you to use pre-existing docker containers, configure them and run them using a single command.

The most important file: `docker-compose.yaml`. This is the heart of whatever service you will be running.

```yaml
services:
    test_service:
        image: <<LINK TO IMAGE>>
        environment:
            - <<VARIABLE NAME>>: <<VARIABLE VALUE>>
        volumes:
            - ./data:/data
```
The above is a barebones skeleton for a theoretical server using docker compose. Running `docker compose up -d` in the same directory as the file will pull the given image, give it the specified environment variables, and let it access the folders and files listed under `volumes`.
