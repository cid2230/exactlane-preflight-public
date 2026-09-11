# Exactlane Preflight

**The check before the call.**

Caller-specific static compatibility evidence for autonomous agents evaluating an MCP capability before relying on it.

Exactlane helps an agent answer: *does this exact declared MCP capability fit my bounded workflow requirements?* before integration.

## Problem it addresses

Before an autonomous agent depends on an external MCP capability, it often needs a **pre-integration compatibility check**:

- compare a **caller-provided capability snapshot** to **caller-specific requirements**;
- obtain **static compatibility evidence** (not live probing);
- keep the **operational decision** with the caller.

Exactlane Preflight is a Phase 0A public service for that workflow.

## Use when

An agent has a caller-provided MCP capability snapshot and needs to determine whether that exact declared capability fits its own bounded workflow requirements.

## Does not prove

- live availability
- full MCP conformance
- business-result correctness
- provider trust
- security certification
- payment success

Exactlane is **not** an MCP server, A2A agent, marketplace, or certification authority.

## Live machine contract

Canonical public discovery origin:

- Service root: https://exactlane.dev/
- Manifest: https://exactlane.dev/.well-known/exactlane.json
- OpenAPI: https://exactlane.dev/openapi.json
- Agent discovery text: https://exactlane.dev/llms.txt
- Sitemap: https://exactlane.dev/sitemap.xml

Temporary migration hostname (compatibility; not canonical):

- https://preflight.happybitemochi.com/

## Scope of this repository

Public discovery anchor only.

Source implementation is **not** part of this public discovery repository.
