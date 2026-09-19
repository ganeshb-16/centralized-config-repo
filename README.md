# Online Railway Reservation System - Centralized Configuration Repository

This repository serves as the externalized Git configuration source for the **Spring Cloud Config Server** in the Online Railway Reservation System.

## Architecture

```
[Microservices] ───(HTTP)───> [Config Server :8888] ───(Git)───> [Trainreservation Repo]
```

## Configuration Files

| File | Target Service | Default Port | Description |
|------|---------------|--------------|-------------|
| `application.properties` | All Services | Global | Eureka registry, JWT secrets, RabbitMQ broker, Mail & JPA defaults |
| `api-gateway.properties` | `API-GATEWAY` | 8080 | Gateway routes, CORS, and centralized Swagger UI aggregation |
| `auth-service.properties` | `AUTH-SERVICE` | 8081 | Authentication, JWT, and database configs |
| `customer-service.properties` | `CUSTOMER-SERVICE` | 8082 | Customer profile database configs |
| `train-service.properties` | `TRAIN-SERVICE` | 8083 | Train master database configs |
| `station-route-service.properties` | `STATION-ROUTE-SERVICE` | 8084 | Station & route distance configs |
| `schedule-fare-service.properties` | `SCHEDULE-FARE-SERVICE` | 8085 | Timetable, fare rules, and Tatkal configs |
| `inventory-quota-service.properties` | `INVENTORY-QUOTA-SERVICE` | 8086 | Seat inventory and quota isolation configs |
| `search-service.properties` | `SEARCH-SERVICE` | 8087 | Resilience4j circuit breakers and retries |
| `reservation-service.properties` | `RESERVATION-SERVICE` | 8088 | Booking Saga orchestrator & Resilience4j configs |
| `payment-refund-service.properties` | `PAYMENT-REFUND-SERVICE` | 8089 | Payment & refund database configs |
| `notification-service.properties` | `NOTIFICATION-SERVICE` | 8090 | Asynchronous notification & email configs |
