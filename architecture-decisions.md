# Architecture Decision Records (ADR)

This document records significant architectural decisions made during the development of the Choloo Jaai platform.

---

## ADR-001: Repository Strategy

**Status:** Accepted

### Decision

Maintain three separate Git repositories:

- `choloo-jaai-frontend`
- `choloo-jaai-backend`
- `choloo-jaai-docs`

### Rationale

- Independent version control
- Independent deployment pipelines
- Clear separation of responsibilities
- Easier collaboration and maintenance

---

## ADR-002: Backend Framework

**Status:** Accepted

### Decision

Use **NestJS** as the backend framework.

### Rationale

- Modular architecture
- Built-in dependency injection
- TypeScript-first development
- Scalable project structure
- Strong community support

---

## ADR-003: Database

**Status:** Accepted

### Decision

Use **PostgreSQL** with **TypeORM**.

### Rationale

- Strong relational data modeling
- ACID compliance for financial and booking operations
- Excellent TypeScript support
- Mature migration system

---

## ADR-004: Caching Layer

**Status:** Accepted

### Decision

Use **Redis**.

### Rationale

Redis will be used for:

- Application caching
- Session storage
- Rate limiting
- Queue support (future)

---

## ADR-005: Development Environment

**Status:** Accepted

### Decision

Use Docker for local development.

### Rationale

- Consistent environments
- Simple onboarding
- Easy database setup
- Platform-independent development