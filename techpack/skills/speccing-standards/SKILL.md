---
name: speccing-standards
description: Techpack-specific guidance for decomposing requirements into fullstack TypeScript component types during the spec phase.
user-invocable: false
---

# Speccing Standards — Fullstack TypeScript

Guide the spec phase by helping decompose user requirements into the component types this techpack provides.

## Component Type Selection

When analyzing requirements, map them to these component types:

| Requirement Pattern | Component Type | Example |
|---|---|---|
| API endpoint, business logic, background job | `server` | "User authentication service" |
| Browser UI, user interaction, dashboard | `webapp` | "Admin dashboard" |
| Data storage, migrations, queries | `database` | "User accounts database" |
| API contract between frontend and backend | `contract` | "Auth API specification" |
| Deployment, infrastructure | `helm` | "Production Helm chart" |
| Shared settings, environment config | `config` | "Environment configuration" |
| CI/CD pipeline | `cicd` | "GitHub Actions workflow" |
| Cross-service testing | `integration-testing` | "Auth flow integration tests" |
| End-to-end user journey testing | `e2e-testing` | "Login flow E2E tests" |

## Dependency Rules

Components must respect the dependency graph defined in the manifest:

- `config` has no dependencies (always first)
- `contract` depends on `config`
- `database` depends on `config`
- `server` depends on `contract`, `config`, `database`
- `webapp` depends on `contract`
- `helm` depends on `server`, `webapp`
- `integration-testing` depends on `contract`, `server`, `database`, `helm`
- `e2e-testing` depends on `server`, `webapp`, `database`, `helm`
- `cicd` depends on `helm`

## Singleton vs Multi-Instance

- `config` is a **singleton** — one per project
- All other component types support **multiple named instances** (e.g., `users-db`, `orders-db`)

## Spec Completeness Checklist

For each component in the spec:
- [ ] Component type identified
- [ ] Instance name chosen (for multi-instance types)
- [ ] Dependencies on other components listed
- [ ] Key behaviors or endpoints described
- [ ] Standards skill applicable (from manifest skills registry)
