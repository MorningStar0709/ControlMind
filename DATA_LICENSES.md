# Data Licenses and Release Boundary

ControlMind is dual-licensed by asset type:

- **Code** — the `controlsci/` package, CLI entry points, scripts, pipeline
  code, and frontend sources: **Apache-2.0**, see [`LICENSE-CODE`](LICENSE-CODE).
- **Data and content** — benchmark datasets, corpus chunks, reports, schemas,
  documentation, and other project-authored materials: **CC-BY-4.0**, see
  [`LICENSE`](LICENSE).

ControlMind combines these original assets with derived artifacts from
public third-party literature. Third-party source documents, parsed text,
extracted chunks, images, metadata, and evidence traces that originate from
PMC, arXiv, or other external publishers retain their original licenses,
attribution requirements, and reuse restrictions. Some source articles may
use non-commercial or no-derivatives terms. This repository does not
relicense those third-party materials under the project licenses.

## Included Public Data

- `corpus/chunks/`: derived scientific-document chunks used to reproduce the
  benchmark evidence.
- `data/sources_medical/`: public medical-literature working artifacts used by
  the local-first Medical RAG track.
- `data/sources_flywheel/`: public literature artifacts used by the agent
  flywheel demonstrations.
- `docs/submissions/data_trace_bundle/`: curated evidence summaries, scalar
  outputs, representative images, and trace manifests cited by the reports.

These artifacts are included for auditability and reproduction. Before reusing,
redistributing, or publishing a derivative dataset, inspect the original source
license for each document and preserve required attribution.

## Excluded or Untracked Data

The public Git history should not track rebuildable binary indexes, embedding
matrices, local checkpoint caches, credentials, `.env` files, private documents,
patient-level records, dependency folders, build outputs, or local scratch
workspaces. Rebuildable indexes and matrices are generated from the public
pipeline and should be distributed outside normal Git history when needed.

## Privacy Statement

The public release is built from public or sanitized materials. It is not a
patient dataset and should not contain patient-level private records, live API
keys, or local machine credentials. Medical RAG code is designed for local-first
deployment so institutions can substitute their own private corpora without
publishing those materials.
