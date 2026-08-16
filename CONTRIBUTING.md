# Contributing to Mesoblock

Thanks for your interest in Mesoblock. This is an early-stage, mostly solo-maintained project. The process below is intentionally lightweight, but please read it before opening a PR so we're not going back and forth on basics.

---

## Table of Contents

1. [Before You Start](#before-you-start)
2. [Development Setup](#development-setup)
3. [Branch Naming](#branch-naming)

---

## Before you start

For anything beyond a small fix (typo, obvious bug, docs), please [open an issue](https://github.com/mesoblock/mesoblock/issues) first to discuss the change. This project touches health-related data and AI-generated fitness guidance, so larger changes — especially to the plan-generation logic, the review-queue flow, or anything under `src/features/auth/` — need discussion before implementation, not after.

## Development setup

### Prerequisites

Ensure the following are installed before proceeding:

| Requirement | Minimum Version | Notes                                                       |
| ----------- | --------------- | ----------------------------------------------------------- |
| Node.js     | 22.22.1         | Use the version specified in `.nvmrc`                       |
| npm         | 10.9.3          | Required by `package.json` engines                          |
| Git         | 2.40+           | Required for Git hooks                                      |
| VS Code     | Latest          | Recommended editor                                          |

### First-time setup

```bash
git clone https://github.com/mesoblock/mesoblock.git
cd mesoblock
npm install
cp .env.example .env.local   # fill in the required values
npm run dev
```

## Branch naming

```
feat/<short-description>
fix/<short-description>
chore/<short-description>
docs/<short-description>
```

## Commit messages

This repo uses [Conventional Commits](https://www.conventionalcommits.org/), enforced by commitlint via a Husky pre-commit hook. Commits that don't match the format will be rejected locally before they even reach CI.

```
<type>(<scope>): <short summary>

feat(auth): add invite-token validation to signup hook
fix(db): correct precision on client_metrics.weight_kg
chore: bump drizzle-orm to 0.x
docs: update CONTRIBUTING with branch naming convention
```

Common types: `feat`, `fix`, `chore`, `docs`, `refactor`, `test`.

## Code style

Formatting and linting are handled by [Biome](https://biomejs.dev/) via [Ultracite](https://ultracite.ai/), and run automatically on commit via Husky.
You shouldn't need to fight the formatter — if something looks off, run:

```bash
npx ultracite fix
```

Spelling is checked with `cspell`. If it flags a legitimate term (a library name, a domain-specific word), add it to the project dictionary rather than disabling the check.

## Pull requests

- Keep PRs scoped to one logical change — see the commit-grouping approach in the project's own commit history for the general idea.
- Link the issue the PR addresses, if there is one.
- Make sure `npm run lint` and `npm run build` pass locally before requesting review.
- Be patient — this is currently reviewed by a single maintainer.

## Reporting bugs vs. requesting features

Use [GitHub Issues](https://github.com/mesoblock/mesoblock/issues) for both, but please label clearly (`bug` vs. `enhancement`) and include repro steps for bugs.

## A note on health-related contributions

Because Mesoblock generates fitness plans from user-submitted health metrics, any change touching plan-generation logic, body-fat/TDEE calculations, or age/eligibility gating needs to cite the source or formula being used (e.g. "Navy method," "Mifflin-St Jeor") in the PR description. This isn't bureaucracy for its own sake — it's how we keep the reasoning behind health-affecting code auditable.