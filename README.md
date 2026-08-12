# Dave Bettner

I build and integrate agent workflows for consequential enterprise environments—with
inspectable, reversible writes, readback checks, and receipts a human operator can rerun.

**Current stack signal:** Python · Hermes Agent · MCP/FastMCP · OAuth/API integrations ·
idempotent recovery · GitHub Actions · Rust (open PR work sample) · Docker Compose
(public CI parse-only; container run not attested)

**Background:** More than ten years in financial-reporting software—SEC reporting and
XBRL at Workiva (2015–2021), Solutions Architect for GRC and financial-reporting
implementations (2022–2024), Workiva platform rollouts at Citrin Cooperman
(2024–2025), and municipal finance / ERP-connected reporting delivery at LSL, LLP
(2025–present). Canonical timeline:
[davebettner.com/experience](https://davebettner.com/experience/).

## Proof-first path

Runnable checks first. Each repo has a credential-free proof path and explicit limits.

### 1. [Hermes Enterprise Deployment Lab](https://github.com/dbett4/hermes-enterprise-deployment-lab)

Synthetic deployment lab: FastMCP server, mock enterprise API, workflow runner, and
a Compose configuration parsed in public CI; container startup is not attested in
the public tree. Exercises post-commit failure and idempotent resume through a
credential-free proof suite. Built organically July–August 2026; not a customer
deployment claim.

[Proof guide](https://github.com/dbett4/hermes-enterprise-deployment-lab/blob/main/PROOF.md) ·
[Approval decision (ADR 005)](https://github.com/dbett4/hermes-enterprise-deployment-lab/blob/main/docs/adr/005-separated-operator-approval.md)

### 2. [Regulated Reporting MCP](https://github.com/dbett4/regulated-reporting-mcp)

MCP server for a Workiva-shaped reporting API: OAuth client credentials, token refresh,
429 backoff, pagination, async operations, and controlled mutations. Default server
exposes **3** guarded tools; the full **117-tool** registry requires an explicit unsafe
opt-in. **126** credential-free tests; offline end-to-end demo.

[Proof guide](https://github.com/dbett4/regulated-reporting-mcp/blob/main/docs/PROOF.md) ·
[Security model](https://github.com/dbett4/regulated-reporting-mcp/blob/main/SECURITY.md)

### 3. [Hermes Enterprise Evaluation Kit](https://github.com/dbett4/hermes-enterprise-field-kit)

Version-pinned Hermes evaluation kit (v0.20.0 / tag `v2026.8.3`): **318-row**
capability map, **8** negative tests, **214** preflight tests (`PASS_WITH_LIMITS`),
one-command check `./scripts/proof.sh`.

**Limit:** One synthetic S1 live one-shot now has native Hermes CLI attestation and a
deterministic-oracle pass. It remains `needs_review`: no external action or human
disposition occurred, the recorded $0.406986 is an estimate rather than an actual
billed amount, and two execution-time exceptions are preserved in the public receipt.

[Technical notes](https://github.com/dbett4/hermes-enterprise-field-kit/blob/main/PROOF.md)

### 4. [Wingman](https://github.com/dbett4/wingman)

Chrome extension and local Python service for financial-reporting workbook defects.
Applies only changes it can check and reverse. **462** Python tests pass, **13**
integration-dependent tests skip, and **243** extension tests pass.

### 5. [Verify Before Write](https://github.com/dbett4/verify-before-write)

Runnable example: plan a write, check the source has not changed, read the result
back, restore the original file on mismatch. **13** credential-free tests on the
committed Riverton loop.

## Also

- **[Agent Team Ops](https://github.com/dbett4/agent-team-ops)** — Markdown templates
  and a worked example for multi-agent coordination. A template/process artifact, not an
  orchestration product.
- **[block/buzz #5620](https://github.com/block/buzz/pull/5620)** — Rust work sample:
  coordinates REST-bridge 429 retry admission across client clones. **+297 / −9**.
  GitHub currently lists it **open and unmerged, with no review decision**; it is not
  presented as accepted upstream or shipped work.

## Provenance and limits

These public repositories are sanitized extracts published August 2026. GitHub commit
dates are publication history, not the original private development timeline. Project
examples and demo organizations are fictional. No client data or credentials appear
here. Private client history remains confidential; public claims are limited to
inspectable artifacts.

[davebettner.com](https://davebettner.com) ·
[LinkedIn](https://www.linkedin.com/in/dave-bettner)
