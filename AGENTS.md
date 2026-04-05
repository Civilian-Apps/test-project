# Agents

This project uses Claude Code agents for autonomous development.

## Available Agents
- **feature-builder** — TDD implementation (runs in GitHub Actions)
- **feature-reviewer** — PR review against spec (runs in GitHub Actions)
- **hygiene** — periodic cleanup, migration squash, dependency updates

## Workflow
1. Feature specs are created as GitHub Issues
2. Issues labeled `ready-to-build` trigger the feature-builder agent
3. PRs are reviewed by the feature-reviewer agent
4. Human reviews and merges
5. Cloudflare Pages deploys on merge to `main`
