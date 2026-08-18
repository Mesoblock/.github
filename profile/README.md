# <img src="./mesoblock-light-mode.svg#gh-light-mode-only" alt="Mesoblock" height="30" /><img src="./mesoblock-dark-mode.svg#gh-dark-mode-only" alt="Mesoblock" height="30" />

[![License](https://img.shields.io/badge/license-proprietary-blue)](https://github.com/mesoblock/mesoblock/blob/main/LICENSE)

AI-driven workout programming with a human safety net.

Mesoblock generates personalized training plans from a user's starting metrics, goals, and training history — and routes anything flagged as higher-risk (injury history, aggressive targets, low model confidence) to a human reviewer before it reaches the client.

## Status

> [!WARNING]
> Early development. Not yet publicly launched.

## Tech stack

- **Framework:** Next.js
- **Auth:** better-auth
- **Database:** Drizzle ORM + Postgres (Neon)
- **Payments:** Stripe
- **Validation:** Zod + React Hook Form
- **Tooling:** Biome/Ultracite, commitlint, Husky

## Repositories

- [`mesoblock`](https://github.com/mesoblock/mesoblock) — the main application

## Community

- [Code of Conduct](./CODE_OF_CONDUCT.md)
- [Contributing](./CONTRIBUTING.md)
- [Security policy](./SECURITY.md)
- [Support](./SUPPORT.md)