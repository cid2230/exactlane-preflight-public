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

Exactlane Preflight is primarily a REST evidence service with a thin remote MCP adapter at `/mcp`. It is **not** an A2A agent, marketplace, or certification authority.

## Live machine contract

Canonical public discovery origin:

- Service root: https://exactlane.dev/
- Manifest: https://exactlane.dev/.well-known/exactlane.json
- OpenAPI: https://exactlane.dev/openapi.json
- Agent discovery text: https://exactlane.dev/llms.txt
- Sitemap: https://exactlane.dev/sitemap.xml
- Remote MCP: https://exactlane.dev/mcp

Temporary migration hostname (compatibility; not canonical):

- https://preflight.happybitemochi.com/

## Scope of this repository

Public discovery anchor only.

Source implementation is **not** part of this public discovery repository.

## Official MCP Registry

- **Server name:** `dev.exactlane/preflight`
- **Version:** `0.1.0`
- **Remote:** Streamable HTTP `https://exactlane.dev/mcp`
- **Registry search:** https://registry.modelcontextprotocol.io/v0.1/servers?search=exactlane

Primary tool: `check_mcp_capability` (adapter over Exactlane Phase 0A; no live probing; caller owns CONTINUE/UPDATE/HOLD).
