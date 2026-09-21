---
name: Unsupported schema keyword
about: Your snapshot came back UNSUPPORTED for a keyword the profile does not interpret
title: "[unsupported] "
labels: unsupported-keyword
---

The fixed profile interprets a small set of JSON Schema keywords and reports anything
else as `UNSUPPORTED` rather than ignoring it. `UNSUPPORTED` means Exactlane did not
decide — not that your capability is incompatible. These reports are how the supported
set gets extended, so the keyword and the shape matter more than the snapshot.

`POST https://exactlane.dev/v0/snapshot-lint` names the same keywords without spending
a check, and needs no credential.

## Keyword

Which keyword, and the pointer the lint or report gave (for example
`$.properties.mode.enum`):

## The shape it appears in

The smallest fragment that reproduces it. **Redact anything sensitive** — a field name
is usually enough:

```json
```

## What your workflow needs from it

Whether you need Exactlane to interpret the keyword, or only to stop treating its
presence as undecidable:

## Profile

The `requirements.schema_version` you sent (`exactlane.consumer-requirements/0.3`,
`/0.2` or `/0.1`):
