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
| Terraform| for infra as code (check with terraform version)|

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

# Challenge 2 - Infrastructure as Code
## Introduction
Symbiosis is a health product manufacturing company and currently on-premises infrastructure. They have recognized the benefits of moving to a cloud infrastructure & would like to evaluate an AWS cloud solution.

Based on their priorities and internal discussions, they have provided you with some high-level requirements which they would like you to implement in the proposed solution. The high-level requirements are as follows:

- A private isolated network which would best suit Symbiosis’s 2 tier architecture needs. In order to meet their internal SLAs they require a highly available solution as well.
- Symbiosis being a B2C company, would typically like their web applications to be accessible over the internet and thus handle HTTP traffic.
- The database tier should have restricted access (not open to HTTP) and allow traffic only through the web tier.
- They would like to reduce the administrative burden of managing their SQL database and require a managed database for their SQL engine in the proposed solution. They need the database to be highly available.
- Currently they experience medium to high traffic on their network. The traffic to the web tier is managed by a load balancer which diverts traffic to healthy instances. They would ideally like a Load Balancer with an ability to perform layer 4 (Transport Protocol) and layer 7 (Application) checks while balancing the load. There is no requirement at this point to balance the load on the database tier.
- In their current setup, the traffic being inconsistent, requires over provisioning resulting in increased costs. In order to overcome this issue, they would like the new system to allow automatic scaling in the event of a traffic spike.

## Deliverables
Write Terraform/Terragrunt code. You can choose any application to host in your implementation. A good example of a webapp that does CRUD operations can also be found here: [NodeJS-MySQL-CRUD](https://github.com/chapagain/nodejs-mysql-crud)


# Challenge 3 - Deployment on AWS
## Task
By writing terraform code, create an AWS ECR repository for pushing the Challenge 1 image into. Lastly, create an AWS ECS cluster and spin up a service using the Challenge 1 docker image.

## Deliverables
APIs should be able to respond to Internet.


# Challenge 4 - Documentation
## Deliverables
- Write documentation for your code 
- An architecture diagram that would suit the needs of the challenge 2 case study
