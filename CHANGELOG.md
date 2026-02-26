# Changelog

All notable changes to the SDD Fullstack TypeScript Tech Pack.

---

## [0.2.0] - 2026-02-26

### Added

- **v2 manifest format**: Self-describing `techpack.yaml` with 7 top-level sections — techpack, skills, agents, components, phases, help, commands
- **Skills registry** (31 entries): Flat name→path mapping replacing LLM-interpreted router
- **Agents registry** (7 entries): Flat name→path mapping for all agents
- **Phases section**: Lifecycle phase contributions (spec, planning, implementation, verification) with orchestrator skills and agents
- **Commands section**: Nested namespace/action structure with handler type (system/skill), destructive flags, and arg schemas
- **check-prerequisites command**: Manifest declaration for prerequisite verification during init
- **speccing-standards skill**: Component type selection guidance for the spec phase

### Removed

- **skills-router skill**: LLM-based routing replaced by deterministic `route-skills` CLI command
- **command-router skill**: LLM-based routing replaced by deterministic `route-command` CLI command

### Changed

- **Components**: Now use name references (skill names, agent names) instead of relative paths — all resolved through registries
- **Help section**: Replaces `documentation` — references skills by name (capabilities, help-content)

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
