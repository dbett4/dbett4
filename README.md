# Dave Bettner

I build agent systems for regulated enterprise work: API integrations, bounded tool use, failure recovery, deterministic verification, and evidence an operator can inspect. My background is 12+ years delivering financial-reporting software—from Workiva Professional Services and Solutions Architecture to leading a CPA firm's governmental reporting practice.

## Start with the proof

### [Enterprise Agent Deployment Field Kit for Hermes](https://github.com/dbett4/hermes-enterprise-playbook)

A Hermes-first method for policy-resolved configuration, bounded authority, typed disposition, and reconstructable evidence.

- Pinned to Hermes Agent v0.20.0 / `v2026.8.3` and its peeled release commit.
- Materialized 318-row capability map with seven explicit unsupported gaps.
- Eight negative cases exercise fail-closed behavior through the evaluator or reference pipeline.
- Includes one committed operator-recorded mission output. It passes its deterministic oracle and remains `needs_review`, but no native runtime attestation was captured, so the repository does not claim that the declared Hermes release produced it.
- One-command credential-free proof: `./scripts/proof.sh`.
- Inspect: [proof map](https://github.com/dbett4/hermes-enterprise-playbook/blob/main/PROOF.md) · [committed recorded artifact](https://github.com/dbett4/hermes-enterprise-playbook/tree/main/reference-suite/runs/s1-decide-20260811-025135)

### [Regulated Reporting MCP](https://github.com/dbett4/regulated-reporting-mcp)

A guarded MCP integration for Workiva-shaped regulated reporting: OAuth2 client credentials, 401 recovery, 429 backoff, pagination, asynchronous-operation handling, explicit mutation contracts, and synthetic mock mode.

- `workiva-mcp` defaults to a three-tool guarded dispatcher; the raw 117-tool registry requires a named unsafe opt-in.
- Contracts distinguish a local execution receipt from deterministic readback.
- Formula writes and missing proof return `indeterminate`, never verified success.
- Payload-redacted, create-once local receipts are emitted for normal mutation outcomes and post-dispatch exceptions.
- One-command proof runs lint, exact contract coverage, 126 credential-free tests, and the offline end-to-end demo.
- Inspect: [proof map](https://github.com/dbett4/regulated-reporting-mcp/blob/main/docs/PROOF.md) · [security boundary](https://github.com/dbett4/regulated-reporting-mcp/blob/main/SECURITY.md)

### [Hermes Enterprise Deployment Lab](https://github.com/dbett4/hermes-enterprise-deployment-lab)

A containerized, customer-shaped lab with a FastMCP server, mock enterprise API, workflow runner, health/readiness checks, scoped credentials, correlation IDs, separated operator approval, and idempotent recovery after an injected post-commit failure.

- Docker/Compose topology plus a no-container local demo.
- Mutations require a separate operator approval record; capabilities expire and become terminal after a confirmed apply or replay.
- Resume reuses the original idempotency key so an ambiguous retry does not duplicate the side effect.
- Seventy-three credential-free tests cover approval lifecycle, forged and expired capabilities, auth scope, audit, and recovery behavior.
- CI reproduces tests, protocol inspection, the failure/recovery demo, and a fresh-clone run.
- Synthetic lab only—not a customer deployment, identity provider, Kubernetes environment, or production scale claim.
- Inspect: [proof map](https://github.com/dbett4/hermes-enterprise-deployment-lab/blob/main/PROOF.md) · [approval ADR](https://github.com/dbett4/hermes-enterprise-deployment-lab/blob/main/docs/adr/005-separated-operator-approval.md)

## Additional work

**[Wingman](https://github.com/dbett4/wingman)** — a Chrome extension and Python service for inspecting financial-reporting workbooks, proposing bounded changes, applying them behind account and authorization gates, reading back results, and reverting mismatches. Public demos use the fictional City of Riverton.

**[Verify Before Write](https://github.com/dbett4/verify-before-write)** — a dependency-light reference workflow for prestate hashing, predicted poststate, staleness refusal, deterministic tie-out, journaling, and exact rollback on synthetic city data.

**[Agent Team Ops](https://github.com/dbett4/agent-team-ops)** — documentation and worked examples for task contracts, handoffs, decision records, blockers, and builder/verifier separation. It is process evidence, not an executable orchestration engine.

Open source: [block/buzz #3618](https://github.com/block/buzz/pull/3618) is an open, unmerged contribution covering shared rate-limit coordination and related secure-delivery work in a large Rust agent framework. The PR is public evidence of the work, not a claim of upstream acceptance.

## Boundaries

- Public examples use synthetic data and contain no client credentials or client-owned source.
- The committed field-kit output is operator-recorded and runtime-unattested; it is evaluation-shape evidence, not proof that the named Hermes release executed.
- Production-domain experience and public repository age are separate facts: these repositories were published in August 2026 as sanitized, Dave-authored portfolio artifacts.

- Site: [davebettner.com](https://davebettner.com)
- LinkedIn: [linkedin.com/in/dave-bettner](https://www.linkedin.com/in/dave-bettner)
