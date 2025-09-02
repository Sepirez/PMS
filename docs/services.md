# Services

| Service                | Purpose                              | Tech                        | Status |
|------------------------|--------------------------------------|-----------------------------|--------|
| API Gateway            | Routing, auth hand-off               | Spring Cloud Gateway        | Planned |
| Auth Service           | JWT issuance/validation, users/roles | Spring Boot, JPA, Postgres  | Planned |
| Inventory Service      | Rooms, rates, availability model     | Spring Boot, JPA, Postgres  | Planned |
| Booking Service        | Search availability, create booking  | Spring Boot, JPA, Postgres  | Planned |
| Billing Service        | Invoices, taxes, payments (stub)     | Spring Boot, JPA, Postgres  | Planned |
| Notification Service   | Email/SMS/webpush hooks              | Spring Boot                 | Planned |
| Analytics Service      | KPIs & reports                       | Spring Boot, Postgres       | Planned |
| Frontend (Angular)     | Web app                              | Angular, TypeScript         | Planned |
| Infra                  | K8s manifests, Helm, docker-compose  | K8s, Helm, Docker           | Planned |

> Links to sub-repositories will be added once created.
