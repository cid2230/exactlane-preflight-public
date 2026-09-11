# Exactlane Preflight

**The check before the call.**

Caller-specific static compatibility evidence for autonomous agents evaluating an MCP capability before relying on it.

Exactlane stores a caller-provided MCP capability snapshot and evaluates it against a fixed consumer-fit profile for a bounded workflow. It produces compatibility evidence. The caller owns the operational decision.

## Use when

An agent has a caller-provided MCP capability snapshot and needs to determine whether that exact declared capability fits its own bounded workflow requirements.

## Does not prove

- live availability
- full MCP conformance
- business-result correctness
- provider trust
- security certification
- payment success

## Live machine contract

- Service root: https://preflight.happybitemochi.com/
- Manifest: https://preflight.happybitemochi.com/.well-known/exactlane.json
- OpenAPI: https://preflight.happybitemochi.com/openapi.json
- Agent discovery text: https://preflight.happybitemochi.com/llms.txt

## Scope of this repository

This is a **public discovery anchor** only.

Source implementation is **not** part of this public discovery repository.
Do not treat this repository as an MCP server, A2A agent, or registry listing.

Phase: Public Agent Preview (temporary hostname).
