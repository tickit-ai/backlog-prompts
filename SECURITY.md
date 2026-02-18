# Security Policy

## Reporting a vulnerability

If you discover a security vulnerability in this repository, please report it responsibly using [GitHub Security Advisories](https://github.com/tickit-ai/backlog-prompts/security/advisories/new) for private disclosure.

**Do not** open a public issue for security vulnerabilities.

## Scope

This repository contains markdown prompt files only — no executable code, no dependencies, no build artifacts. The primary security concerns are:

- **Secrets in prompt files** — API keys, tokens, or credentials accidentally committed
- **Prompt injection** — malicious content designed to manipulate AI tools consuming these prompts
- **Social engineering** — PRs that appear benign but contain hidden malicious instructions

## Protections in place

- All PRs require maintainer review before merge
- CI scans prompt files for potential secrets on every PR
- Secret scanning and push protection are enabled on the repository
- Only squash merges are allowed (clean, auditable history)
- CODEOWNERS requires approval from project maintainers

## Supported versions

Only the latest version on `main` is supported.
