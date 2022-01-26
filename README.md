# GoBusiness - Bring home assessment

## Instruction
This repository contains a simple srping boot program written in Kotlin. The service responds with "pong" when POSTMAN triggers it.

## Pre-requisites
You will need to following installed:
| Package | Detail |
| ------ | ------ |
| Docker | for image building/publishing (check with docker version) |
| Docker-compose | for environment provisioning (check with docker-compose version) |
| Git| for source control (check with git -v)|

## Get Started

- Clone this repository
- Create your own repository on Github
- Set your local repository's remote to pount to your Github repository
- Make your changes locally accordding to your tasks below
- Push to your Github repository

# Challenge 1

# Containerisation
## Task
Create a `Dockerfile` in the root directory according to any best practices you may know about.

##Deliverable
Running `docker build -t devops/webapp:latest .` should result in a successful image named `devops/webapp:latest` which is reflected in the output of `docker imgae ls`.

Running `docker -ir -p 8080:8080 devop/webapp:latest` should result in the same behaviour as running `RUN ./gradlew clean bootJar`
