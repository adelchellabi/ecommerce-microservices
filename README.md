# E-Commerce Microservice

This project is an e-commerce microservice built using **Java**, **Spring Boot**, and **Maven**. It includes a `product-service` that interacts with a **PostgreSQL** database.

## Features

- **Spring Boot** for building the microservice.
- **PostgreSQL** as the database.
- Dockerized setup using `docker-compose`.
- Hot reload enabled with **Spring DevTools**.
- Environment configuration using `.env` files.

## Prerequisites

- **Java 21** or higher
- **Maven** 3.8+
- **Docker** and **Docker Compose**

## Project Structure

- `product-service/`: Contains the Spring Boot application.
- `docker-compose.yml`: Defines the services and their configurations.
- `.env` and `.env.example`: Environment variable files for configuration.

## Getting Started

### 1. Clone the Repository

```bash
git clone git@github.com:adelchellabi/ecommerce-microservices.git
cd ecommerce-microservices
```
### 2. Set Up Environment Variables
Copy the `.env.example` file to `.env` in the root directory and update the values as needed.
Also, make sure to configure product-service environment variables in the `.env` file. Path is `product-service/.env`

### 3. Build and Run the Application
```bash
docker-compose up --build
```
This command will build the Docker images and start the containers defined in `docker-compose.yml`.
### 4. Access the Application
Once the application is running, you can access it at:
- **Product Service**: `http://localhost:8080/`
- **PostgreSQL**: `localhost:5432` (default port)