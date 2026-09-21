---
name: Bug report
about: Something behaved differently from the documented contract
title: ""
labels: bug
---

**Do not paste bearer tokens, Preview credentials or `Authorization` headers.**

## What the contract says

The line in `llms.txt`, `openapi.json`, `/.well-known/exactlane.json` or a page on
exactlane.dev that you relied on:

## What happened instead

Route or JSON-RPC method, HTTP status, error code, and the relevant part of the body.
Redact snapshot contents you cannot share:

```
```

## Reproduction

The smallest request that shows it:

```
```

## Notes

Reports are evidence-shaped: a finished report carries digests of the snapshot,
requirements, profile and runner it compared. Quoting `profile`, `coverage` and the one
failing `check_id` is usually enough, without the whole report.
