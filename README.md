# TrainingPage gateway-service

## Description 

A fitness application built with multiple microservices to help you with planning, logging and improving your home training.
The system is a microservice application built with Spring Boot, React, and PostgreSQL and containerized using Docker for easy setup and deployment.


The Gateway Service acts as the API Gateway for the TrainingPage microservice ecosystem. It is the single entry point for the frontend and is responsible for:

Request Routing: Forwarding requests to the correct microservice (User, Training, or Statistic).

Security: Validating JWT tokens for all protected routes.

Service Discovery: Registering with Eureka and dynamically locating service instances.

## Technology stack

* Spring Cloud Gateway
* Spring Security (JWT Validation)
* Eureka Client


## Routing Logic

The gateway routes requests based on the following path patterns:
/user/** → User Service (Protected)
/training/** → Training Service (Protected)
/exercise/** → Training Service (Protected)
/statistic/** → Statistic Service (Protected)

## Setup

This service is designed to be run as part of the Docker Compose cluster.
For instructions on how to start the project go to the readme file at [trainingpage](https://github.com/TheSteinkamp/trainingpage.git)
