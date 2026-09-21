---
name: Integration blocked
about: You tried to use Exactlane and could not reach a finished report
title: "[blocked] "
labels: blocked
---

**Do not paste bearer tokens, Preview credentials or `Authorization` headers.**
Preview credentials expire in 30 minutes; let one expire rather than sharing it.

## Which path

- [ ] Remote MCP (`POST https://exactlane.dev/mcp`)
- [ ] REST (`/v0/public-access/grants` → `/v0/capabilities` → `/v0/checks`)
- [ ] Something else

## What you sent

JSON-RPC method or REST route, and the `MCP-Protocol-Version` you sent if using MCP:

```
```

## What came back

HTTP status and the error body. For MCP, the JSON-RPC `error.code` and `error.data`
matter more than the HTTP status:

```
```

## Client

Client or SDK and version, or `curl`. If your client sends `initialize` first, say so:
MCP 2026-07-28 removed the handshake and Exactlane implements no session, so that call
returns `-32601` `METHOD_NOT_FOUND` with HTTP 200 and an `error.data` naming the next
call.

## Anything else

Whether a retry, a different client or the REST path worked.
