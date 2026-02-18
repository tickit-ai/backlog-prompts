# Backlog Prompts

Open-source prompt library for AI-assisted software engineering. These are system prompts designed to be pasted into AI coding tools (Claude Code, Cursor, ChatGPT, Gemini) to improve the quality of AI-generated code.

## What's inside

Each prompt is a markdown file with YAML frontmatter (metadata) and a system prompt body. Prompts are organized into categories:

| Category | Description |
|----------|-------------|
| `before-you-code` | Architecture review, risk assessment, and planning prompts to run before writing code |
| `after-code-generation` | Security review, test coverage, and quality audit prompts to run after AI generates code |
| `product-decisions` | PRD critique, prioritization, and stakeholder alignment prompts for product decisions |

## Usage

1. Browse the `prompts/` directory and find a prompt that matches your task
2. Copy the prompt body (everything below the frontmatter `---` delimiter)
3. Paste it into your AI tool as a system prompt or conversation starter
4. Provide the context described in the `contextFields` section of the frontmatter

## Prompt format

Each prompt file includes:

```yaml
---
title: "Prompt Name"
slug: "prompt-slug"
category: "before-you-code"
tags: ["tag1", "tag2"]
version: "1.0"
description: "What this prompt does"
difficulty: "beginner | intermediate | advanced"
targetModels: ["claude", "gpt-4", "gemini"]
whenToUse: "When to reach for this prompt"
expectedOutput: "What the AI will produce"
contextFields:
  - id: "field_name"
    label: "Field Label"
    placeholder: "What to provide..."
    required: true
    type: "short | long"
---

[System prompt body here]
```

## Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for how to submit new prompts or improve existing ones.

## Security

See [SECURITY.md](SECURITY.md) for our security policy and how to report vulnerabilities.

## License

MIT
