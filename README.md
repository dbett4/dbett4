# Dave Bettner

I help enterprises put agents next to real systems without losing control:
scoped tools, confirm-before-write paths, independent checks, and receipts a
person can rerun.

**Current stack signal:** Python · Hermes Agent · MCP/FastMCP · OAuth/API
integrations · idempotent recovery · GitHub Actions · TypeScript/Electron
(open PR #84621) · Rust (separate open PR work sample) · Docker Compose
(public CI container/restart proof attested)

**Background:** More than ten years in financial-reporting software — SEC
reporting and XBRL at Workiva (2015–2021), Solutions Architect for GRC and
financial-reporting implementations (2022–2024), Workiva platform rollouts at
Citrin Cooperman (2024–2025), and municipal finance / ERP-connected reporting
delivery at LSL, LLP (2025–present). Canonical timeline:
[davebettner.com/experience](https://davebettner.com/experience/).

## Proof-first path

Each public repo leads with a human problem, then a runnable offline check, then
explicit limits. Numbers are evidence, not the story.

### 1. [Hermes Enterprise Deployment Lab](https://github.com/dbett4/hermes-enterprise-deployment-lab)

**Story:** when an agent can touch an internal system, scope the tools, separate
operator approval from the agent, and survive the ugly “API committed then
errored” case without double-writing.

**Proof:** synthetic lab with mock API + MCP server + workflow runner; public CI
attests container restart/replay, native telemetry/trace, and a 240-test
credential-free suite. Not a customer or operated-cloud deployment.

[Proof guide](https://github.com/dbett4/hermes-enterprise-deployment-lab/blob/main/PROOF.md) ·
[Green CI run](https://github.com/dbett4/hermes-enterprise-deployment-lab/actions/runs/31891411678) ·
[Approval decision (ADR 005)](https://github.com/dbett4/hermes-enterprise-deployment-lab/blob/main/docs/adr/005-separated-operator-approval.md)

### 2. [Hermes Agent Desktop/session recovery PR #84621](https://github.com/NousResearch/hermes-agent/pull/84621)

**Story:** recover Desktop sessions hidden behind stale legacy profile shadows.

**Proof:** open, unreviewed upstream PR with focused regression coverage. Work
sample only — not accepted, merged, shipped, or Nous-endorsed.

### 3. [Regulated Reporting MCP](https://github.com/dbett4/regulated-reporting-mcp)

**Story:** a successful API response is not the same as “applied,” and applied is
not the same as “checked.” Keep those outcomes separate.

**Proof:** guarded default tool surface, confirm-before-write, readback, redacted
receipts, credential-free mock demo. Full tool catalog stays behind explicit
unsafe opt-in.

[Proof guide](https://github.com/dbett4/regulated-reporting-mcp/blob/main/docs/PROOF.md) ·
[Security model](https://github.com/dbett4/regulated-reporting-mcp/blob/main/SECURITY.md)

### 4. [Hermes Enterprise Evaluation Kit](https://github.com/dbett4/hermes-enterprise-field-kit)

**Story:** Hermes primitives alone are not enough for a real organization. You
still need job qualification, approved configs, independent checks, and a human
when judgment is required.

**Proof:** version-pinned kit (v0.20.0 / `v2026.8.3`); offline `./scripts/proof.sh`
with no keys or network. One synthetic live one-shot has native attestation and
still ends `needs_review` (no external action, no human disposition, estimated
rather than billed cost, two recorded exceptions).

[Technical notes](https://github.com/dbett4/hermes-enterprise-field-kit/blob/main/PROOF.md)

### 5. [Wingman](https://github.com/dbett4/wingman)

**Story:** find live-workbook defects that disappear in an export; automate only
fixes you can confirm, read back, and reverse.

**Proof:** Chrome extension + local Python service; large credential-free Python
and extension suites in CI. Fictional demo data only.

### 6. [Verify Before Write](https://github.com/dbett4/verify-before-write)

**Story:** plan a change, confirm it, read it back, restore the original file when
reality does not match the prediction; leave judgment items for a person.

**Proof:** runnable inspect → propose → apply → tie-out loop on synthetic
Riverton CSVs.

## Also

- **[Agent Team Ops](https://github.com/dbett4/agent-team-ops)** — Markdown
  templates so multi-agent work lives in the repo (board, owners, handoffs,
  decisions), not in disappearing chat. Template/process artifact, not an
  orchestration product.
- **[block/buzz #5620](https://github.com/block/buzz/pull/5620)** — Rust work
  sample: coordinates REST-bridge 429 retry admission across client clones.
  Open/unmerged with review required; checks green; not accepted upstream.

## Provenance and limits

These public repositories are sanitized extracts published August 2026. GitHub
commit dates are publication history, not the original private development
timeline. Project examples and demo organizations are fictional. No client data
or credentials appear here. Private client history remains confidential; public
claims are limited to inspectable artifacts. Independent work is not a customer
Hermes Enterprise deployment or Nous affiliation.

[davebettner.com](https://davebettner.com) ·
[LinkedIn](https://www.linkedin.com/in/dave-bettner)
