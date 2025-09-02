# Architecture

## System Context
- Clients → Angular frontend → **API Gateway** → microservices
- Data → PostgreSQL (OLTP), Redis (cache)
- Observability → Prometheus + Grafana

## Request Flow (example)
1. Client calls Angular → Angular calls **API Gateway**
2. Gateway forwards to **Auth** (JWT) or target service
3. Services persist in **PostgreSQL** and use **Redis** for caching
4. Metrics/health exposed for **Prometheus**, visualized in **Grafana**

## Components
- **Gateway:** routing, CORS, rate limiting (future), request logging
- **Auth:** JWT, refresh tokens, users/roles
- **Inventory:** rooms, rates, availability rules
- **Booking:** search & reservation transactions
- **Billing:** invoice generation, tax calculation, payment provider stub
- **Notification:** async email/SMS hooks
- **Analytics:** aggregation jobs → KPIs

## Non-Functional Requirements
- Security (JWT, RBAC)
- Reliability (timeouts, retries, circuit breakers)
- Observability (metrics, logs, tracing in future)
- Scalability (horizontal via K8s)

## Data
- PostgreSQL schemas per service (owning tables)
- Redis for caching (e.g., availability, session, rate plans)
