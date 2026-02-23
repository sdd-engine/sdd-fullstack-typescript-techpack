# Contributing to SDD Fullstack TypeScript Tech Pack

## Development Setup

```bash
git clone https://github.com/sdd-engine/sdd-fullstack-typescript-techpack.git
cd sdd-fullstack-typescript-techpack
npm install
npm run build
```

## Making Changes

1. Create a feature branch: `git checkout -b feature/my-change`
2. Make changes in `techpack/` (agents, skills, system, templates)
3. Build and verify: `npm run build && npm run typecheck`
4. Update `techpack/techpack.yaml` version if needed
5. Open a pull request

## Versioning

Version is tracked in `techpack/techpack.yaml` under `techpack.version`.

## Code Standards

- TypeScript strict mode with all strict checks
- Path aliases use `@/` prefix (resolved by `tsc-alias`)
- Agent prompts follow the agents-standards skill format
- Skill markdown follows the skills-standards format

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
