# Online Railway Reservation System - Centralized Configuration Repository

This repository serves as the externalized Git configuration source for the **Spring Cloud Config Server** in the Online Railway Reservation System.

## Architecture

```
[Microservices] ───(HTTP)───> [Config Server :8888] ───(Git)───> [Trainreservation Repo]
```

## Configuration Files

| File | Target Service | Default Port | Description |
|------|---------------|--------------|-------------|
| `application.yml` | All Services | Global | Eureka registry & RabbitMQ message broker credentials |
| `api-gateway.yml` | `API-GATEWAY` | 8080 | Gateway routes and filter configs |
| `auth-service.yml` | `AUTH-SERVICE` | 8081 | Authentication, JWT, and database configs |
| `customer-service.yml` | `CUSTOMER-SERVICE` | 8082 | Customer profile database configs |
| `train-service.yml` | `TRAIN-SERVICE` | 8083 | Train master database configs |
| `station-route-service.yml` | `STATION-ROUTE-SERVICE` | 8084 | Station & route distance configs |
| `schedule-fare-service.yml` | `SCHEDULE-FARE-SERVICE` | 8085 | Timetable, fare rules, and Tatkal configs |
| `inventory-quota-service.yml` | `INVENTORY-QUOTA-SERVICE` | 8086 | Seat inventory and quota isolation configs |
| `search-service.yml` | `SEARCH-SERVICE` | 8087 | Aggregator service configs |
| `reservation-service.yml` | `RESERVATION-SERVICE` | 8088 | Booking Saga orchestrator configs |
| `payment-refund-service.yml` | `PAYMENT-REFUND-SERVICE` | 8089 | Payment & IRCTC refund matrix configs |
| `notification-service.yml` | `NOTIFICATION-SERVICE` | 8090 | Asynchronous notification configs |
