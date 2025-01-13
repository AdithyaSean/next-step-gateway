# Next Step API Gateway

## Overview
Central API Gateway service for the Next Step platform. Handles routing, security, and request management for all microservices.

## Features
- Centralized routing
- Authentication & authorization
- Rate limiting
- Load balancing
- Circuit breaking
- Request/response transformation
- Service discovery integration
- API documentation aggregation

## Tech Stack
- Spring Cloud Gateway
- Spring Security
- Spring Cloud Netflix
- Spring Boot Actuator

## Setup
1. Configure environment variables:
   ```env
   SERVER_PORT=8080
   EUREKA_CLIENT_SERVICEURL_DEFAULTZONE=http://localhost:8761/eureka/
   SPRING_CLOUD_GATEWAY_ROUTES_PATH=/config/routes
   ```

2. Start the service:
   ```bash
   ./mvnw spring-boot:run
   ```

## API Documentation
See [docs/api.md](docs/api.md) for detailed API documentation.

## Development Guide
- All external requests are routed through this gateway
- Services are discovered automatically via Eureka
- Circuit breakers protect from service failures
- JWT validation for authenticated routes

## Monitoring
- Actuator endpoints for health monitoring
- Prometheus metrics integration
- Circuit breaker metrics
