# Contributing to Backlog Prompts

Thanks for your interest in contributing! We welcome new prompts, improvements to existing ones, and bug reports.

## Submitting a new prompt

1. **Fork** this repository
2. **Create a branch** from `main` (e.g., `add-prompt/my-new-prompt`)
3. **Add your prompt** as a markdown file under the appropriate category directory in `prompts/`
4. **Open a pull request** targeting `main`

### Prompt file requirements

Every prompt file must include valid YAML frontmatter with these required fields:

| Field | Type | Description |
|-------|------|-------------|
| `title` | string | Human-readable name (max 120 chars) |
| `slug` | string | URL-safe identifier (`[a-z0-9-]+`) |
| `category` | string | One of: `before-you-code`, `after-code-generation`, `product-decisions` |
| `version` | string | Semantic version (`1.0`, `1.1`, etc.) |
| `description` | string | One-sentence summary (max 300 chars) |
| `whenToUse` | string | When this prompt is most useful |
| `tags` | string[] | Relevant tags for discovery |
| `targetModels` | string[] | AI models this works with (e.g., `["claude", "gpt-4", "gemini"]`) |
| `contextFields` | array | Inputs the user needs to provide (see existing prompts for format) |

### Guidelines

- **One prompt per PR** — makes review easier
- **Test your prompt** — run it through at least one AI tool before submitting
- **No secrets** — never include API keys, tokens, passwords, or credentials
- **Be specific** — prompts with clear structure and concrete instructions outperform vague ones
- **Include context fields** — define what inputs the user needs to provide

## Improving an existing prompt

1. Open an issue describing the improvement
2. Fork, branch, make changes, and open a PR
3. Bump the `version` field in frontmatter

## Reporting issues

Use the "Bug Report" issue template to report problems with existing prompts.

## Review process

All PRs are reviewed by maintainers (@afaraj, @ismaildesouki). We aim to review within a few business days. Every PR must:

- Pass CI validation (frontmatter check + secret scan)
- Receive approval from at least one maintainer
- Be merged via squash merge (we maintain a clean commit history)

## Code of Conduct

Be respectful, constructive, and helpful. We reserve the right to remove content or block contributors who violate this principle.
