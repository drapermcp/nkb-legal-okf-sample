---
type: readme
title: "NKB Legal — Wyoming Criminal Code, an OKF v0.2 reference bundle"
rights_holder: "William Daniel Raper"
copyright_registration: "TXu 2-562-276"
license: "CC-BY-4.0"
---

# NKB Legal — Wyoming Criminal Code (OKF reference bundle)

A public sample of a **Neural Knowledge Base (NKB)** exported as an **Open Knowledge Format v0.2** bundle.

An NKB is an OKF-conformant document bundle **plus** layers OKF does not model. This repo shows three of them in plain files any OKF consumer can read:

| layer | where to look |
|---|---|
| Provenance (pre-OKF Canon Integrity Header + OKF `sources` / `generated` / `status`) | frontmatter of any node in `nodes/` |
| Six-dimension analytical enrichment (**6Q**: what / who / when / where / how / why) | `6q_*` keys in frontmatter |
| Typed relationship graph (696 edges over 264 nodes) | the **Related** section of each node: markdown links whose title carries `rel:<type> {strength}` (the typed-link convention proposed in [knowledge-catalog #322](https://github.com/GoogleCloudPlatform/knowledge-catalog/issues/322)) |

Start at [`index.md`](index.md). History in [`log.md`](log.md). Rights in [`NOTICE.md`](NOTICE.md).

## Provenance of the sample

- Source corpus: NKB Legal — United States Criminal Code Compilation, Version 1.0 (34,364 nodes, 45 states). Registered work, U.S. Copyright Office **Reg. No. TXu 2-562-276**, effective 2026-02-23. Statutory text is public domain and is not claimed.
- Format: OKF v0.2 (`GoogleCloudPlatform/knowledge-catalog`, `okf/SPEC.md`). Every document here parses as YAML frontmatter with `type`; unknown keys are the point — consumers must preserve them.
- Method and measurement: *Neural Knowledge Bases as OKF Supersets* (CC-BY technical note), DOI [10.5281/zenodo.21861595](https://doi.org/10.5281/zenodo.21861595). Retrieval measurement (nodes + agency vs RAG): DOI [10.5281/zenodo.21613674](https://doi.org/10.5281/zenodo.21613674).

## License

Original authorship in this sample bundle: **CC-BY-4.0** (see `NOTICE.md` for the attribution line). The full compilation is not covered by this license.

William Daniel Raper — https://intentgate.ai
