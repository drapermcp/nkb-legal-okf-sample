---
type: pattern
title: "Shipping a typed relationship layer inside an OKF bundle"
rights_holder: "William Daniel Raper"
copyright_registration: "TXu 2-562-276"
license: "CC-BY-4.0"
---

# How a producer ships a graph inside OKF

OKF v0.2 has no relationship files. A markdown link is an untyped directed edge whose meaning lives in the surrounding prose. There is no reverse index and no way to say “nothing connects here.”

This bundle shows two producer patterns for an **explicit** layer. Both are original authorship named on TXu 2-562-276 (relationship mapping). Statutory text is public domain.

## 1. Typed inline links (proposed in knowledge-catalog #322)

Each node’s **Related** section:

```markdown
- [§ 6-1-104](/nodes/wyoming-criminal-section-6-1-104.md "rel:sequential-section {strength: 0.85}")
```

A generic markdown tool round-trips the title. A consumer who does not understand `rel:` still sees a link.

## 2. Local neighbor files (the shape that made lookup and neighbourhood both work)

One small file per node, not one domain-wide dump:

```
neighbors/wyoming-criminal-section-6-2-101.json
```

```json
[{"type":"sequential-section","peer":"wyoming-criminal-section-6-2-102","strength":0.85}]
```

**Do not** put a multi-hundred-edge JSON on the same recursive search path as the documents. A retrieval pilot (Wyoming Title 6, 264 nodes, 2026-09-13) found: grepping a domain-wide edge file exhausted the tool budget and lookup scored 0. The same protocol with these per-node files recovered lookup and recorded-neighbourhood. That reproduces an earlier result on edge locality (DOI 10.5281/zenodo.21613674, addendum v2.1a).

MAP: read `neighbors/<id>.json` for that node only. Absence of a file, or an empty list, is reportable negative space.

## What this is not

- Not a claim that six-dimension (6Q) frontmatter finds statutes. Citation lookup saturated without it.
- Not a claim that keyword search of a statute finds the governing natural-law article. That bridge is a curated crosswalk, not a retrieval trick.

## Rights

See `NOTICE.md`. The map travels with the notice.
