# ADR-001: Separate Frontend and Backend Repositories

## Decision

Frontend and backend will be maintained in separate repositories.

## Reason

- Independent deployment
- Independent versioning
- Cleaner CI/CD pipeline


---


# ADR-002: Use NestJS for Backend

## Decision

NestJS selected as backend framework.

## Reason

- Modular architecture
- TypeScript support
- Dependency injection
- Enterprise-ready structure


---


# ADR-003: Use PostgreSQL with TypeORM

## Decision

PostgreSQL selected as primary database with TypeORM.

## Reason

- Relational data model fits event management
- Strong consistency
- Type-safe entity management


---


# ADR-004: Use Docker for Development Services

## Decision

Database and Redis run through Docker containers.

## Reason

- Consistent development environment
- Easy setup
- Environment isolation