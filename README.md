# SDD Fullstack TypeScript Tech Pack

A tech pack for [SDD Core](https://github.com/sdd-engine/sdd-core) that provides full-stack TypeScript development capabilities.

## Stack

- **Backend**: Node.js with CMDO architecture (Controller, Model, DAL, Orchestrator)
- **Frontend**: React with MVVM architecture (View, ViewModel, Model)
- **Database**: PostgreSQL with versioned migrations and seed data
- **Contracts**: OpenAPI 3.x with generated TypeScript types
- **Infrastructure**: Kubernetes via Helm charts
- **CI/CD**: GitHub Actions pipelines
- **Testing**: Vitest (integration) + Playwright (E2E) via Testkube

## Installation

Requires [SDD Core](https://github.com/sdd-engine/sdd-core) installed as a Claude Code plugin.

```
/sdd-run tech-pack install --repo https://github.com/sdd-engine/sdd-fullstack-typescript-techpack
```

## What's Included

### Agents (7)

| Agent | Role |
|-------|------|
| backend-dev | Node.js/TypeScript server development |
| frontend-dev | React/TypeScript webapp development |
| api-designer | OpenAPI contract design |
| db-advisor | PostgreSQL schema and migration design |
| devops | Kubernetes, Helm, and CI/CD |
| tester | Integration and E2E testing |
| reviewer | Code review and verification |

### Component Types (9)

config, contract, database, server, webapp, helm, integration-testing, e2e-testing, cicd

### Commands

Database operations, contract generation, config management, local Kubernetes environment.

## Documentation

- [Agents Reference](docs/agents.md)
- [Component Types](docs/components.md)
- [Configuration Guide](docs/config-guide.md)

## Development

```bash
npm install
npm run build      # Build tech pack system CLI
npm run typecheck   # Type-check without emitting
```

## Lineage

Extracted from [LiorCohen/sdd](https://github.com/LiorCohen/sdd) v7.3.0 (`plugin/fullstack-typescript/`).

## License

MIT
