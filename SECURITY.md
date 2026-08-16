# Security Policy

## Reporting a Vulnerability

Mesoblock handles health-related personal data and payment information (via Stripe), so please report suspected vulnerabilities privately rather than opening a public issue.

**Please email: [security@mesoblock.com](mailto:security@mesoblock.com)**

Alternatively, use GitHub's [private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing/privately-reporting-a-security-vulnerability) feature on the main repository, if enabled.

Please include:

- A description of the vulnerability and its potential impact
- Steps to reproduce, or a proof of concept
- Any relevant logs, screenshots, or affected endpoints

## What's in scope

- Authentication and session handling (`better-auth` configuration and integration)
- Access control around role-gated routes (`user` / `reviewer` / `admin`)
- Handling of health metrics, consent records, and other PII
- Stripe webhook handling and subscription/plan gating

## What's out of scope

- Findings that require physical access to a user's device
- Social engineering against maintainers or users
- Denial-of-service via brute-force volume rather than a logic flaw

## Response expectations

This is currently a small, mostly solo-maintained project — please allow up to **5 business days** for an initial response. We'll credit reporters (with permission) once a fix ships, unless you'd prefer to
remain anonymous.

## Supported versions

Mesoblock is pre-1.0 and under active development. Only the latest commit on `main` is supported; there is no LTS branch at this stage.