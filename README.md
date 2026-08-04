# Shared engineering workflows

Reusable GitHub Actions workflows for Haniel Azevedo's Laravel, Next.js,
Prisma, and Node.js projects.

The goal is simple: quality gates live here once. Project repositories keep a
small caller workflow and inherit improvements without copying CI plumbing.

## Workflows

- `laravel-ci.yml` — PHP 8.3, Composer, Node 22, SQLite, read-only formatting
  checks, tests, migrations when requested, and a production asset build.
- `next-prisma-ci.yml` — npm, Prisma generation/migrations, typecheck, lint,
  and a production Next.js build.
- `node-quality.yml` — deterministic pnpm install and project quality command.

Callers pin the reusable workflow to a release tag so shared changes are
deliberate and reproducible.
