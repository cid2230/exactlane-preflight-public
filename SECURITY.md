# Security

## Reporting

Report a suspected vulnerability by opening a **private** GitHub security advisory on
this repository (Security → Report a vulnerability). Please do not open a public issue
for a suspected vulnerability.

Email support is not yet an active contact channel, so a security advisory is the
reliable path. Expect acknowledgement to be best-effort: Exactlane is a Phase 0A
service without a staffed on-call rotation, and that is stated here rather than implied
otherwise.

## Please do not include

Exactlane never needs these, and they should not appear in an advisory, an issue or a
capability snapshot:

- bearer tokens, API keys or `Authorization` header values
- Public Agent Preview credentials (they expire in 30 minutes; let them expire)
- internal hostnames, IP addresses or infrastructure identifiers
- personal data in a snapshot or in caller requirements

A capability snapshot is the provider's own `tools/list` entries. If yours carries
anything above, redact it before sharing.

## Scope

In scope: the hosted service at `https://exactlane.dev`, its REST contract, the remote
MCP adapter at `/mcp`, and the discovery artifacts in this repository.

Out of scope, because they are documented behaviour rather than defects:

- absence of live probing — Exactlane never calls a caller-supplied endpoint, by design
- `initialize` returning `METHOD_NOT_FOUND` — MCP 2026-07-28 removed the handshake, and
  no session or compatibility shim is implemented
- `PUBLIC_ACCESS_DISABLED` while Public Agent Preview is off on a deployment
- Public Agent Preview quotas, rate limits and the 30-minute lifetime
- a report verdict you disagree with — a verdict is evidence, not a decision, and
  `UNSUPPORTED` records an evaluator boundary rather than a compatibility claim

Reports of these are welcome as ordinary issues.
