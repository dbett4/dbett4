# Dave Bettner

> **Provenance.** These public repositories are sanitized extracts published August
> 2026. GitHub commit dates are publication history, not the original private
> development timeline. Project examples and demo organizations are fictional. No client data or
> credentials appear here. Private client history remains confidential; public claims
> are limited to inspectable artifacts.

I connect agents to consequential enterprise systems—with inspectable, reversible writes,
readback checks, and receipts a human operator can rerun.

**Background:** More than ten years in financial-reporting software—SEC reporting and
XBRL at Workiva (2015–2021), Solutions Architect for GRC and financial-reporting
implementations (2022–2024), Workiva platform rollouts at Citrin Cooperman
(2024–2025), and municipal finance / ERP-connected reporting delivery at LSL, LLP
(2025–present). Canonical timeline:
[davebettner.com/experience](https://davebettner.com/experience/).

## Proof-first path

Runnable checks first. Each repo has a credential-free proof path and explicit limits.

### 1. [Hermes Enterprise Field Kit](https://github.com/dbett4/hermes-enterprise-field-kit)

Version-pinned Hermes evaluation kit (v0.20.0 / tag `v2026.8.3`): **318-row**
capability map, **8** negative tests, **214** preflight tests (`PASS_WITH_LIMITS`),
one-command check `./scripts/proof.sh`.

**Limit:** No live-attested Hermes mission. The committed S1 record passes local
deterministic checks but lacks native runtime attestation—I do not present it as proof
of a live model run.

[Technical notes](https://github.com/dbett4/hermes-enterprise-field-kit/blob/main/PROOF.md)

### 2. [Regulated Reporting MCP](https://github.com/dbett4/regulated-reporting-mcp)

MCP server for a Workiva-shaped reporting API: OAuth client credentials, token refresh,
429 backoff, pagination, async operations, and controlled mutations. Default server
exposes **3** guarded tools; the full **117-tool** registry requires an explicit unsafe
opt-in. **126** credential-free tests; offline end-to-end demo.

[Proof guide](https://github.com/dbett4/regulated-reporting-mcp/blob/main/docs/PROOF.md) ·
[Security model](https://github.com/dbett4/regulated-reporting-mcp/blob/main/SECURITY.md)

### 3. [Hermes Enterprise Deployment Lab](https://github.com/dbett4/hermes-enterprise-deployment-lab)

Synthetic deployment lab: FastMCP server, mock enterprise API, workflow runner, and a
Compose configuration parsed in CI; container startup is optional and not attested in the public tree. Exercises post-commit failure and idempotent
resume. **73** credential-free tests. Built organically July–August 2026; not a customer
deployment claim.

[Proof guide](https://github.com/dbett4/hermes-enterprise-deployment-lab/blob/main/PROOF.md) ·
[Approval decision (ADR 005)](https://github.com/dbett4/hermes-enterprise-deployment-lab/blob/main/docs/adr/005-separated-operator-approval.md)

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
- **[block/buzz #3618](https://github.com/block/buzz/pull/3618)** — Open contribution
  for shared rate-limit handling in a large Rust agent project. Unreviewed, unmerged,
  and **not accepted upstream**; I do not present it as shipped work.

[davebettner.com](https://davebettner.com) ·
[LinkedIn](https://www.linkedin.com/in/dave-bettner)
