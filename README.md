# Hi, I'm Derek

I'm a product manager (Red 6 Aerospace, Unlikely Labs) building infrastructure for long-running AI agents.

---

## memory-os — an operating system for an AI agent's long-term memory

**[github.com/derekcedarbaum2/memory-os](https://github.com/derekcedarbaum2/memory-os)**

Most "AI memory" tooling sells you a vector DB and calls it cognition. Mem0, Letta, Zep, Cognee — different logos, same shape. `memory-os` is the opposite: Markdown files, three-tier persistent memory, adversarial review loops, distillation pipelines, and a self-healing automation layer that runs on cron. No vector DB. No SaaS. MIT throughout.

The thesis: **writing-layer over retrieval-layer.** The work has to happen somewhere. Vector DBs pay for it on every retrieval. This system pays for it once, at write time, with version history. Inside the envelope — single knowledge worker, lived-in vault, capable agent — that tradeoff wins on transparency, debuggability, longevity, and cost. Outside it (multi-tenant, vocabulary drift across users, 100k+ docs you don't write yourself), use a vector DB.

Full argument: [`memory-os/docs/thesis.md`](https://github.com/derekcedarbaum2/memory-os/blob/main/docs/thesis.md). The honest envelope: [`memory-os/docs/envelope.md`](https://github.com/derekcedarbaum2/memory-os/blob/main/docs/envelope.md).

### Why one repo, not twelve

Through April–May 2026 I shipped twelve separate repos covering different pieces of this system: `ai-knowledge-system`, `qa-loop`, `learnings-resurface`, `vault-conventions`, and so on. As of May 2026 they are consolidated into `memory-os` and the originals are archived. The unified repo tells the whole story in one place, with a self-healing automation layer as the load-bearing evidence.

The four buckets that used to be separate repos now live as folders inside `memory-os/skills/`:

| Bucket | What it does |
|---|---|
| **memory/** | Three-tier vault memory + frontmatter discipline + weekly hygiene audit. The agent stops starting cold. |
| **quality/** | Multi-agent review loops with competing incentives. Structural anti-sycophancy. |
| **distill/** | Daily and weekly passes that turn raw reading and raw session archives into operational rules. |
| **meta/** | A deterministic CLI that offloads boring work from the LLM, plus a living architecture map that updates itself. |

On top of those, [`memory-os/automation/`](https://github.com/derekcedarbaum2/memory-os/tree/main/automation) is the cron layer that maintains everything weekly — dormancy decay at 90 days, active-venture pinboard refresh, memory dir audit. Read it to see what self-healing actually looks like in ~400 lines of Python and bash.

---

## What I'm building outside of this

I run **Unlikely Labs**, an AI consultancy focused on PM-led AI engineering with a defense-grade track record. I'm a product manager at **Red 6 Aerospace** (AR training platform for fighter pilots). I have a few early-stage ventures (Bastion, Estivon, Tribal Datacenter, AI Build Partners) and write about how I'd build them with current AI tools.

`memory-os` is the daily-use foundation underneath that work — every artifact I ship is reviewed by the `qa-loop` skill, every research call goes through brain-context injection, every session archive feeds back into pattern detection. The system is the leverage.

---

## License

`memory-os` is MIT. Fork it, modify it, ship it. If you build something useful on top, an issue or PR is appreciated but not required.
