# Dave Bettner

I build AI tools that can work with real business systems without hiding what they
did. My recent projects focus on API integrations, controlled writes, recovery after
partial failures, and checks that a human operator can rerun.

I have spent more than 12 years building financial-reporting software, including
Workiva Professional Services and Solutions Architecture and leading a CPA firm's
government reporting practice.

## Selected projects

### [Hermes Enterprise Field Kit](https://github.com/dbett4/hermes-enterprise-field-kit)

A version-pinned example of how I would configure and evaluate Hermes for enterprise
work. It includes a 318-row capability map, explicit unsupported cases, eight negative
tests, and a one-command local check: `./scripts/proof.sh`.

One sample run is committed for inspection. It was recorded by the operator and passes
the repository's checks, but it does not contain a native Hermes runtime attestation. I
leave that distinction visible instead of presenting the sample as a verified live run.

[Read the technical notes](https://github.com/dbett4/hermes-enterprise-field-kit/blob/main/PROOF.md)

### [Regulated Reporting MCP](https://github.com/dbett4/regulated-reporting-mcp)

An MCP server for a Workiva-shaped reporting API. It handles OAuth client credentials,
token refresh after a 401, rate-limit backoff, pagination, asynchronous operations, and
controlled mutations. The default server exposes three guarded tools; the full
117-tool registry requires an explicit unsafe opt-in.

The repository has 126 credential-free tests and an offline end-to-end demo. A local
write receipt is not treated as remote verification, and uncertain formula results are
reported as `indeterminate`.

[Read the proof guide](https://github.com/dbett4/regulated-reporting-mcp/blob/main/docs/PROOF.md) ·
[Review the security model](https://github.com/dbett4/regulated-reporting-mcp/blob/main/SECURITY.md)

### [Hermes Enterprise Deployment Lab](https://github.com/dbett4/hermes-enterprise-deployment-lab)

A small deployment lab with a FastMCP server, a mock enterprise API, a workflow runner,
and Docker Compose. The useful part is the failure path: a write can succeed remotely
and then appear to fail locally, and the retry reuses the same idempotency key so the
side effect happens once.

Operator approval is stored separately from the workflow, capabilities expire, and 73
credential-free tests cover approval, authorization, audit records, and recovery. This
is a synthetic lab, not a claim that I deployed it in a customer environment.

[Read the proof guide](https://github.com/dbett4/hermes-enterprise-deployment-lab/blob/main/PROOF.md) ·
[Read the approval decision](https://github.com/dbett4/hermes-enterprise-deployment-lab/blob/main/docs/adr/005-separated-operator-approval.md)

## More work

- **[Wingman](https://github.com/dbett4/wingman)** is a Chrome extension and local
  Python service that finds defects in financial-reporting workbooks. It applies only
  the changes it can check and reverse; everything else stays in review.
- **[Verify Before Write](https://github.com/dbett4/verify-before-write)** is a small,
  runnable example of planning a write, checking that the source has not changed,
  reading the result back, and restoring the original file on a mismatch.
- **[Agent Team Ops](https://github.com/dbett4/agent-team-ops)** contains the Markdown
  templates I use to coordinate agent work across sessions. It is a process example,
  not an orchestration product.
- **[block/buzz #3618](https://github.com/block/buzz/pull/3618)** is my open contribution
  for shared rate-limit handling in a large Rust agent project. It has not been merged,
  so I do not present it as accepted upstream work.

These examples use fictional data and contain no client credentials or source. I
published the public versions in August 2026 after removing the private details, so
their GitHub dates are newer than the work behind them.

[davebettner.com](https://davebettner.com) ·
[LinkedIn](https://www.linkedin.com/in/dave-bettner)
