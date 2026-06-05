# Hi, I'm Derek

I'm a product manager with 13 years in deep-tech startups, building first-of-its-kind products where hardware meets software. As the #2 hire at Red 6, I co-owned the roadmap for the world's first in-cockpit augmented reality system for fighter pilots and ran the 0-to-1 prototype that led to $120M+ raised, scaling the team from 5 to 150+.

Now I run **Unlikely Labs**, an AI consultancy focused on PM-led AI engineering, and I build tooling for people who do real work with AI agents every day. Two pieces of it are below — both MIT, both filesystem-native, both pulled straight out of daily use rather than a product roadmap.

---

## memory-os — an operating system for an AI agent's long-term memory

**[github.com/derekcedarbaum2/memory-os](https://github.com/derekcedarbaum2/memory-os)**

Most "AI memory" tooling sells you a vector DB and calls it cognition. Mem0, Letta, Zep, and Cognee all make the same bet: embed your notes, retrieve by vector similarity. `memory-os` goes the other way: Markdown files, three-tier persistent memory, adversarial review loops, distillation pipelines, and a self-healing automation layer that runs on cron. No vector DB. No SaaS.

The thesis: **writing-layer over retrieval-layer.** The work of organizing memory has to happen somewhere. Vector DBs pay for it on every retrieval; this system pays once, at write time, with version history. For a single knowledge worker with a lived-in vault and a capable agent, that trade wins on transparency, debuggability, longevity, and cost. Outside that envelope — multi-tenant, vocabulary drift across users, 100k+ docs you didn't write — use a vector DB.

The load-bearing evidence is [`automation/`](https://github.com/derekcedarbaum2/memory-os/tree/main/automation): the cron layer that decays dormant notes at 90 days, refreshes the active-venture pinboard, and audits the memory directory every week, in ~400 lines of Python and bash you can read. Full argument in [`docs/thesis.md`](https://github.com/derekcedarbaum2/memory-os/blob/main/docs/thesis.md); the honest envelope in [`docs/envelope.md`](https://github.com/derekcedarbaum2/memory-os/blob/main/docs/envelope.md).

---

## brand-system-kit — a brand system you can run, not just read

**[github.com/derekcedarbaum2/brand-system-kit](https://github.com/derekcedarbaum2/brand-system-kit)**

Most brand guidelines are a PDF nobody opens and nothing enforces, so colors drift and the wrong blue ships. This kit makes the rules executable. Define a brand once in a single `tokens.json`, and the tooling keeps every output on-brand or fails the build: a linter blocks off-palette colors and banned words, a WCAG gate checks contrast by computation instead of by eye, and a render step turns any artifact into an image so you (or an agent) can judge what a rule can't catch — whether it actually looks right.

Zero dependencies, plain Node. It ships with two demo brands, Northwind and Graphite, built on one idea: **match the visual register to the buyer's trust model.** A technical operator distrusts polish; a non-technical exec distrusts hand-waving. Same discipline, two registers, so the pipeline runs the moment you clone it. Any agent (Codex, Cursor, Claude Code) can scaffold a new brand by running the built-in interview.

---

## What else I'm building

A few early-stage ventures on the side — Estivon, AI Build Partners, and others — which I treat as build-with-current-AI experiments and write about as I go.

Both repos above are the foundation under that work. Every artifact I ship gets reviewed by the `qa-loop` skill and gated by the brand kit before it leaves the building. The tooling is the point.

---

## License

Both repos are MIT. Fork them, modify them, ship them. If you build something useful on top, an issue or PR is appreciated but not required.
