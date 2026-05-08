# Hi, I'm Derek

I'm a product manager (Red 6 Aerospace, Unlikely Labs) building tools that make AI agents do more of the work I used to do by hand. The repos pinned below are an interconnected ecosystem — each useful on its own, designed to compose into a coherent system.

---

## 🏗 The Claude Code Ecosystem

A 12-repo system for running [Claude Code](https://docs.anthropic.com/claude/code) (or [Codex CLI](https://github.com/openai/codex)) as a serious daily tool — persistent memory, structured workflows, distillation pipelines, deterministic CLI primitives, self-documenting infrastructure.

### → If you want to install the whole system

**Paste [this prompt](https://github.com/derekcedarbaum2/claude-code-setup/blob/main/INSTALL-PROMPT.md) into your Claude Code or Codex session.** It interviews you, installs the ecosystem in phases (Foundations → Quality skills → Pipelines → Architecture), rewrites paths for your machine, runs smoke tests, and pauses for confirmation between phases.

### → If you want to read first

- **[ECOSYSTEM map](https://github.com/derekcedarbaum2/claude-code-setup/blob/main/ECOSYSTEM.md)** — the 12 repos, what they do, install order, numbered Day 1 / Week 1 / Month 1 / Quarter 1 onboarding sequence.
- **[GLOSSARY](https://github.com/derekcedarbaum2/claude-code-setup/blob/main/GLOSSARY.md)** — every term used across the ecosystem, defined in plain English.
- **[claude-code-setup](https://github.com/derekcedarbaum2/claude-code-setup)** — the umbrella reference: a worked example of one PM's complete configuration with reasoning behind each decision.

### → If you want one piece

| Layer | Repos |
|---|---|
| **Memory + vault foundations** | [ai-knowledge-system](https://github.com/derekcedarbaum2/ai-knowledge-system) · [vault-conventions](https://github.com/derekcedarbaum2/vault-conventions) |
| **Quality skills** | [qa-loop](https://github.com/derekcedarbaum2/qa-loop) · [sense-of-style](https://github.com/derekcedarbaum2/sense-of-style) |
| **Distillation pipelines** | [note-highlight-indexer](https://github.com/derekcedarbaum2/note-highlight-indexer) · [learnings-resurface](https://github.com/derekcedarbaum2/learnings-resurface) |
| **Architecture & meta** | [vault-cli](https://github.com/derekcedarbaum2/vault-cli) · [adversarial-agent-pattern](https://github.com/derekcedarbaum2/adversarial-agent-pattern) · [agentic-architecture-map](https://github.com/derekcedarbaum2/agentic-architecture-map) · [vault-lint](https://github.com/derekcedarbaum2/vault-lint) |

Each repo's README leads with the *problem* it solves in plain English. Vocabulary is in the [glossary](https://github.com/derekcedarbaum2/claude-code-setup/blob/main/GLOSSARY.md).

---

## What I'm building outside of this

I run **Unlikely Labs**, an AI consultancy focused on PM-led AI engineering with a defense-grade track record. I'm a product manager at **Red 6 Aerospace** (AR training platform for fighter pilots). I have a few early-stage ventures (Bastion, Estivon, Tribal Datacenter, AI Build Partners) and write about how I'd build them with current AI tools.

The Claude Code Ecosystem above is the daily-use foundation underneath that work — every artifact I ship is reviewed by `qa-loop`, every research call goes through brain-context injection, every session archive feeds back into pattern detection. The system is the leverage.

---

## License

Everything in this ecosystem is MIT. Fork it, modify it, ship it. If you build something useful on top, an issue or PR is appreciated but not required.
