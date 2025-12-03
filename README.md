# BranchRunner – Multi-branch Sports Retail & Inventory Platform

[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.3-6DB33F?logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Java](https://img.shields.io/badge/Java-21-ED8B00?logo=openjdk&logoColor=white)](https://openjdk.java.net/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-336791?logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

**BranchRunner** is a full-featured backend for multi-branch sports retail stores (built for my real sport shop business and designed as a portfolio project).  
It manages products, per-branch inventory, orders, deliveries, employees, and basic reports — everything a growing sports retail chain needs.

The project is intentionally built as a **modular monolith with layered/clean architecture** and is prepared for painless evolution into microservices when the time comes.

## Key Features (so far / planned)

- Multi-branch management
- Product catalog with categories
- Stock control per branch (with automatic reservation on order)
- Order processing and history
- Delivery tracking (pending → shipped → delivered)
- Employee registration & role-based access (admin / branch manager / employee)
- JWT authentication with Spring Security
- Event-driven design with RabbitMQ (async stock updates, notifications)
- Production-ready monitoring with Spring Boot Actuator
- API documentation with Springdoc OpenAPI (Swagger UI)
- Database migrations with Flyway
- Docker + docker-compose setup

Future steps: extract services (Inventory, Order, etc.) into real microservices with Spring Cloud Gateway, Eureka, and Resilience4j.

## Architecture

Modular Monolith (Layered / Clean Architecture)
├─ web            → Controllers & DTOs
├─ application    → Services / Use Cases
├─ domain         → Entities & business rules (no Spring dependencies)
└─ infrastructure → Repositories, external clients, JPA config

## Tech Stack

- **Java 21**  
- **Spring Boot 3.3**  
- **Spring Data JPA** + **PostgreSQL**  
- **Spring Security** + **JWT**  
- **RabbitMQ** (event-driven)  
- **Flyway** (migrations)  
- **Lombok**  
- **Spring Boot Actuator** (health, metrics)  
- **Springdoc OpenAPI** (Swagger)  
- **Docker** & **docker-compose**
