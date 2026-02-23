# Changelog

All notable changes to the SDD Fullstack TypeScript Tech Pack.

---

## [0.1.0] - 2026-02-23

### Added

- **Initial release** extracted from [LiorCohen/sdd](https://github.com/LiorCohen/sdd) v7.3.0
- **7 agents**: backend-dev, frontend-dev, api-designer, db-advisor, devops, tester, reviewer
- **9 component types**: config, contract, database, server, webapp, helm, integration-testing, e2e-testing, cicd
- **Tech pack commands**: Database operations (setup, migrate, seed, reset, teardown, psql, port-forward), contract generation, config management, local Kubernetes environment
- **System CLI**: Tech-pack-specific operations (check-prerequisites, database, contract, config, local-env)
- **Templates**: Scaffolding templates for all component types

### Lineage

This repo continues the fullstack TypeScript tech pack originally developed as part of the monolithic [LiorCohen/sdd](https://github.com/LiorCohen/sdd) repository (v7.2.0 introduced the core/techpack split). The extraction enables independent versioning and git-based installation.
