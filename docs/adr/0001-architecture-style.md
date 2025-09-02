# ADR 0001 — Architecture Style: Microservices with API Gateway

## Status
Proposed

## Context
We need a modular system to support hotel PMS features evolving independently (bookings, billing, CRM), scalable and observable.

## Decision
Adopt a **microservices architecture** with a **Spring Cloud Gateway** fronting the services. Each service owns its data (PostgreSQL) and exposes REST APIs secured with JWT. Use Redis for caching. Deploy with Docker/Kubernetes. 

## Consequences
- ✅ Independent deployability and scaling
- ✅ Clear bounded contexts (Inventory, Booking, Billing…)
- ⚠️ Operational complexity (CI/CD, observability, distributed tracing)
- ⚠️ Data consistency across services requires careful design (sagas/transactions)
