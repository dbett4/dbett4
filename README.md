# Dave Bettner

I build AI-agent systems that do real work on regulated financial reporting platforms. This is work where a bad write ends up in a government's audited financial statements. Background: 12+ years in enterprise SaaS financial reporting, from Workiva Professional Services and Solutions Architecture to leading a CPA firm's governmental reporting practice. Today that delivery runs through agent tooling I engineer: MCP servers, verify-before-write workflows, and multi-agent operations.

## Agent-assisted verification on regulated data

**[wingman](https://github.com/dbett4/wingman)** — a defect-detection copilot for financial reporting workbooks. The core loop is inspect → propose → apply → verify: every mutation is a journaled changeset with a predicted post-state, adopted by diff or rolled back exactly, and validated against deterministic tie-out oracles rather than model confidence. Architecture decisions are recorded as ADRs in the repo. Demos run on synthetic data for the fictional City of Riverton.

**[verify-before-write](https://github.com/dbett4/verify-before-write)** — the design rationale behind wingman as a standalone reference. It walks through the failure modes that make direct agent writes unacceptable on regulated data (silent partial application, compensating errors that tie out, confident wrong states), explains why adjudicating a diff against a predicted post-state beats trusting model confidence, and closes with a worked example on the synthetic City of Riverton data.

## Multi-agent operations

**[agent-team-ops](https://github.com/dbett4/agent-team-ops)** — the coordination templates I use to run a multi-runtime agent fleet (Claude, Codex, Cursor, Hermes) against live financial reporting delivery: task boards, task packets, handoff templates, decision logs, and worktree leases. Verification is separated from building — an agent never adjudicates its own risky change.

Open source: [block/buzz #3618](https://github.com/block/buzz/pull/3618) (open) — `fix(acp): coordinate HTTP rate-limit retries` across concurrent ACP agents in Block's 26k-star Rust agent framework.

---

All of this exists to get agent output past an audit. That is the bar I build to.

- Site: [davebettner.com](https://davebettner.com)
- LinkedIn: [linkedin.com/in/dave-bettner](https://www.linkedin.com/in/dave-bettner)

