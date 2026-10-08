# Personal Finance Manager

REST API for managing personal finances, built for the Object-Oriented Programming 2 course at FIT, Mediterranean University.

## Features

- Users with profiles and multiple accounts (with account details)
- Transactions with categories and tags, filterable by category, type and account
- Budgets per category
- File attachments for transactions (multipart upload)
- Currency conversion through an external exchange rate API
- IP-based location and timezone lookup through external APIs
- Scheduled job that checks every 60 seconds for accounts with a negative balance
- Authentication and role-based access with Keycloak (OpenID Connect)

## Tech stack

Java 25, Quarkus, Hibernate ORM, PostgreSQL, Quarkus REST (JAX-RS), MicroProfile REST Client, Quarkus Scheduler, Keycloak

## Running locally

Requirements:
- Java 25
- PostgreSQL with database `pfm_db` (user `pfm_user`) on port 5432
- Keycloak on port 8180 with realm `personal-finance-manager` and client `pfm-client`

Start in dev mode:

```
./mvnw quarkus:dev
```

Credentials in `application.properties` are for local development only.