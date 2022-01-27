# GoBusiness - Bring home assessment

## Instruction
This repository contains a simple Spring Boot program written in Kotlin. The service responds with "pong" when POSTMAN triggers a GET request to `/api/ping`. The service listens on port `8080`.

## Pre-requisites
You will need the following installed:
| Package | Detail |
| ------ | ------ |
| Docker | for image building/publishing (check with docker version) |
| Docker-compose | for environment provisioning (check with docker-compose version) |
| Git| for source control (check with git -v)|

## Get Started

- Clone this repository
- Create your own repository on GitHub
- Set your local repository's remote to point to your GitHub repository
- Make your changes locally according to your tasks below
- Push to your GitHub repository

# Challenge 1 - Containerisation
## Task
Create a `Dockerfile` in the root directory according to any best practices you may know about.

## Deliverables
Running `docker build -t devops/webapp:latest .` should result in a successful image named `devops/webapp:latest` which is reflected in the output of `docker image ls`.

Running `docker run -p 8080:8080 devop/webapp:latest` should result in the same behaviour as running `RUN ./gradlew clean bootRun`

# Challenge 2 - Deployment on AWS

- Create ECR repository
- Push image to ECR repository
- Create EC2 container

# Challenge 3 - Infrastructure as Code

The objective of this part is to run your created Docker image on an AWS Fargate cluster and call the ping successfully.
- Write Terraform/Terragrunt code

# Challenge 4 - Documentation

- Write documentation for your code
- Draw the architecture diagram for the AWS infrastructure
