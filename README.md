# Gurujix Platform Portal

Backstage-based Internal Developer Platform portal for Gurujix.

| Environment | URL |
| --- | --- |
| Local | `http://localhost:3000` |
| Future public | `https://platform.gurujix.com` |
| Hub site | `https://gurujix.com/` |

## Prerequisites

- Node.js 22 or 24 (`nvm use` reads `.nvmrc`)
- Yarn 4 via Corepack (`corepack enable`)
- Git

## Start locally

```sh
yarn install
yarn start
```

Open `http://localhost:3000`. Local auth uses the guest provider.

## Software Catalog (Phase 1)

| File | What it defines |
| --- | --- |
| `catalog-info.yaml` | This portal as a Component |
| `catalog/org.yaml` | Group `platform-team` (owner) |
| `catalog/platform.yaml` | Domain `gurujix`, System `developer-platform` |

Those files are loaded from `app-config.yaml` → `catalog.locations`.  
Server-oriented path overrides live in `app-config.production.yaml` (same entities, different paths / env-based DB).

Catalog shape:

```text
Domain: gurujix
  └── System: developer-platform
        └── Component: platform-portal
              owner: platform-team
```

## Secrets and git hygiene

- Never commit `.env`, tokens, keys, or credentials.
- Optional pre-commit secret scan:

```sh
brew install pre-commit
pre-commit install
pre-commit run --all-files
```

## Note

This repo is the platform front door. Application microservices are separate repos (later phases).
