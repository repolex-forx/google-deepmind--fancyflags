# Repolex Knowledge Graph of google-deepmind/fancyflags

RDF knowledge graph data for [google-deepmind/fancyflags](https://github.com/google-deepmind/fancyflags), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download google-deepmind/fancyflags
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 154f0d029010ea25da40ba4e0c2fb477f114395e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 154f0d029010ea25da40ba4e0c2fb477f114395e
│           └── chunk-001.nq.gz
├── blob
│   ├── 09749542e90fe8cc92a2b79d1ff64d074c778f15.nq.gz
│   ├── 0a8e3bda264764a56d59b3c8f6460e2d5b6113b6.nq.gz
│   ├── 17adb12eb21916f2a6eb977af7bb13c86184344b.nq.gz
│   ├── 1d1932f13ef7d0f0949194e8f48fed556017547e.nq.gz
│   ├── 2799739fe046986ec6914fab5a824c67dbbd2679.nq.gz
│   ├── 32850cdb711742d2e3988912cc3ab52b1d5f56cd.nq.gz
│   ├── 6c001e08dba4d6e06f988665e66d1f617333ca63.nq.gz
│   ├── 70f720a21914e8c028a97a4227c71f711b5900b2.nq.gz
│   ├── 815f8cd544432a36e1d31130b075d1cfd7dadd10.nq.gz
│   ├── 939e5341e74dc2371c8b47f0e27b50581bed5f63.nq.gz
│   ├── a158a75249daeed5ef4e33332d3088c09037a5ae.nq.gz
│   ├── a469a0ac8feb028b904e20b1d3ce9332a9101600.nq.gz
│   ├── b7abd8bcd116e49816e6cff241b83ccd0394bdcb.nq.gz
│   ├── b9566e00f7ba90501f1dcaf2c5264fdab9262af9.nq.gz
│   ├── c0c4e1030bc3cd11f732692c241257e8676a5e99.nq.gz
│   ├── d59edf66eca576000ce7023634ae9fb7690ab425.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── e1459b0fbc5015f5fb6a7586fcc11648831714f7.nq.gz
│   ├── e7f1e89ef3aa83ce97475a6ae2ace1a11c0f0ff5.nq.gz
│   ├── f0603a59ee48ad68ca245ca781b1f153ba72da22.nq.gz
│   ├── f548b0cebfe6136c5a36543b9187306570eb599e.nq.gz
│   ├── f56ad7c0a2dcd2d92fb3f6e7ca2b63cc79e2f721.nq.gz
│   ├── f5abe359a124e719224e1892fe8cdfaea1becdc9.nq.gz
│   └── f99bf14467d927ba290e809c4b2e9a9716711ece.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 154f0d029010ea25da40ba4e0c2fb477f114395e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 32 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[google-deepmind/fancyflags](https://github.com/google-deepmind/fancyflags)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
