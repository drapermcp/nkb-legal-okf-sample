---
type: readme
title: "NKB Legal — Wyoming Criminal Code, an OKF v0.2 reference bundle"
rights_holder: "William Daniel Raper"
copyright_registration: "TXu 2-562-276"
license: "CC-BY-4.0"
---

# NKB Legal — Wyoming Criminal Code (OKF reference bundle)

A public sample of a **Neural Knowledge Base (NKB)** exported as an **Open Knowledge Format v0.2** bundle.

An NKB is an OKF-conformant document bundle **plus** walls OKF does not model. The first wall is a **typed relationship layer** (OKF has no edge files). This sample ships that layer two ways, in plain files:

| layer | where to look |
|---|---|
| Typed inline links (proposed in [knowledge-catalog #322](https://github.com/GoogleCloudPlatform/knowledge-catalog/issues/322)) | each node’s **Related** section: `rel:<type> {strength}` in the link title |
| Local neighbor files | `neighbors/<node-id>.json` — one small file per node; do not grep a domain-wide dump |
| Provenance | Canon Integrity Header + OKF `sources` / `generated` / `status` on each node |
| 6Q (authoring, not the retrieval pitch) | `6q_*` keys in frontmatter — used to *write* thematic edges; not claimed as lookup |

How to ship the graph: [`PATTERN.md`](PATTERN.md). Start at [`index.md`](index.md). Rights in [`NOTICE.md`](NOTICE.md).

## Provenance of the sample

- Source corpus: NKB Legal — United States Criminal Code Compilation, Version 1.0 (34,364 nodes, 45 states). Registered work, U.S. Copyright Office **Reg. No. TXu 2-562-276**, effective 2026-02-23. Statutory text is public domain and is not claimed.
- Format: OKF v0.2 (`GoogleCloudPlatform/open-knowledge-format`, `SPEC.md`). Every concept document here parses as YAML frontmatter with `type`; the reserved `index.md` and `log.md` follow spec sections 8 and 9; unknown keys are the point — consumers must preserve them.
- Method: *Neural Knowledge Bases as OKF Supersets*, DOI [10.5281/zenodo.21861595](https://doi.org/10.5281/zenodo.21861595). Nodes+search vs RAG: DOI [10.5281/zenodo.21613674](https://doi.org/10.5281/zenodo.21613674). Wyoming retrieval pilot: [10.5281/zenodo.22739602](https://doi.org/10.5281/zenodo.22739602). How to ship the graph: [`PATTERN.md`](PATTERN.md).

## License

Original authorship in this sample bundle: **CC-BY-4.0** (see `NOTICE.md` for the attribution line). The full compilation is not covered by this license.

William Daniel Raper — https://intentgate.ai
