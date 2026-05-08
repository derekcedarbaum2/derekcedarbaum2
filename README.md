# Hi, I'm Derek

I'm a product manager (Red 6 Aerospace, Unlikely Labs) building infrastructure for long-running AI agents. The repos pinned below are an interconnected ecosystem — each useful on its own, designed to compose.

---

## Long-running AI agents on plain Markdown

Most "AI memory" tooling sells you a vector DB and calls it cognition. Mem0, Letta, Zep, Cognee — different logos, same shape. This is the opposite — Markdown files, three-tier persistent memory, adversarial review loops, distillation pipelines, and a CLI that does the deterministic work so the LLM only does judgment. No vector DB, no SaaS, MIT throughout.

The thesis: **writing-layer over retrieval-layer.** The work has to happen somewhere. Vector DBs pay for it on every retrieval. This system pays for it once, at write time, with version history. Inside the envelope — single knowledge worker, lived-in vault, capable agent — that tradeoff wins on transparency, debuggability, longevity, and cost. Outside it (multi-tenant, vocabulary drift across users, 100k+ docs you don't write yourself), use a vector DB.

The full argument is in [claude-code-setup](https://github.com/derekcedarbaum2/claude-code-setup#the-thesis-writing-layer-over-retrieval-layer).

---

## 🏗 The Claude Code Ecosystem — four products in 12 repos

A 12-repo system for running [Claude Code](https://docs.anthropic.com/claude/code) (or [Codex CLI](https://github.com/openai/codex)) as a daily knowledge-work tool.

### → If you want to install the whole system

**Paste [this prompt](https://github.com/derekcedarbaum2/claude-code-setup/blob/main/INSTALL-PROMPT.md) into your Claude Code or Codex session.** It interviews you, installs in phases (Foundations → Quality → Pipelines → Architecture), rewrites paths for your machine, runs smoke tests, and pauses for confirmation between phases.

### → If you want to read first

- **[ECOSYSTEM map](https://github.com/derekcedarbaum2/claude-code-setup/blob/main/ECOSYSTEM.md)** — 12 repos, what they do, install order, Day 1 / Week 1 / Month 1 / Quarter 1 onboarding.
- **[GLOSSARY](https://github.com/derekcedarbaum2/claude-code-setup/blob/main/GLOSSARY.md)** — every term used across the ecosystem, in plain English.
- **[claude-code-setup](https://github.com/derekcedarbaum2/claude-code-setup)** — umbrella reference: one PM's complete configuration with the *why* behind each decision.

### → If you want one piece

| Bucket | What it does | Repos |
|---|---|---|
| **Persistent memory** | Three-tier vault memory + frontmatter discipline + hygiene audit. The agent stops starting cold. | [ai-knowledge-system](https://github.com/derekcedarbaum2/ai-knowledge-system) · [vault-conventions](https://github.com/derekcedarbaum2/vault-conventions) · [vault-lint](https://github.com/derekcedarbaum2/vault-lint) |
| **Adversarial quality** | Multi-agent review loops with competing incentives — finds real issues without false-positive noise. The structural anti-sycophancy mechanism. | [qa-loop](https://github.com/derekcedarbaum2/qa-loop) · [sense-of-style](https://github.com/derekcedarbaum2/sense-of-style) · [adversarial-agent-pattern](https://github.com/derekcedarbaum2/adversarial-agent-pattern) |
| **Distillation pipelines** | Daily and weekly background passes that turn raw reading and raw session archives into operational rules the agent applies. | [note-highlight-indexer](https://github.com/derekcedarbaum2/note-highlight-indexer) · [learnings-resurface](https://github.com/derekcedarbaum2/learnings-resurface) |
| **Self-documenting architecture** | A CLI that offloads deterministic work from the LLM, plus a living map of the setup that updates itself on every structural change. | [vault-cli](https://github.com/derekcedarbaum2/vault-cli) · [agentic-architecture-map](https://github.com/derekcedarbaum2/agentic-architecture-map) |

Each repo's README leads with the *problem* it solves. Vocabulary in the [glossary](https://github.com/derekcedarbaum2/claude-code-setup/blob/main/GLOSSARY.md).

---

## What I'm building outside of this

I run **Unlikely Labs**, an AI consultancy focused on PM-led AI engineering with a defense-grade track record. I'm a product manager at **Red 6 Aerospace** (AR training platform for fighter pilots). I have a few early-stage ventures (Bastion, Estivon, Tribal Datacenter, AI Build Partners) and write about how I'd build them with current AI tools.

The Claude Code Ecosystem above is the daily-use foundation underneath that work — every artifact I ship is reviewed by `qa-loop`, every research call goes through brain-context injection, every session archive feeds back into pattern detection. The system is the leverage.

---

## License

Everything in this ecosystem is MIT. Fork it, modify it, ship it. If you build something useful on top, an issue or PR is appreciated but not required.
