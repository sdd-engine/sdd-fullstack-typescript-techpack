# CLAUDE.md

## Repository Structure

```
sdd-fullstack-typescript-techpack/
├── .github/
│   └── workflows/
│       └── release.yml           # Version-triggered release
├── techpack/
│   ├── techpack.yaml             # Tech pack manifest (version, components, commands)
│   ├── agents/                    # 7 specialized AI agents
│   ├── skills/                    # Tech-pack-specific skills
│   ├── system/                    # TypeScript CLI for tech-pack operations
│   │   ├── src/
│   │   ├── package.json           # @sdd/fs-ts-system workspace
│   │   ├── tsconfig.json
│   │   └── system-run.sh          # CLI entry point
│   └── templates/                 # Code generation templates
├── docs/                          # User-facing documentation
├── package.json                   # Root workspace config
├── CHANGELOG.md
├── README.md
└── LICENSE
```

## Build Rules

- `npm run build` — build tech pack system CLI (`tsc + tsc-alias`)
- `npm run typecheck` — type-check without emitting
- **NEVER run `npx tsc` directly** — requires `tsc-alias` for `@/` path aliases

## Tech Pack Manifest

The `techpack/techpack.yaml` is the source of truth for:
- Namespace (`fs-ts`)
- Version
- Component types and their scaffolding skills
- Available commands
- Agent assignments

## No Plugin Manifests

This repo has NO `plugin.json` or `marketplace.json`. It is installed into SDD Core via `tech-pack install --repo`.
