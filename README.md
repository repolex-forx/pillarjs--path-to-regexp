# Repolex Knowledge Graph of pillarjs/path-to-regexp

RDF knowledge graph data for [pillarjs/path-to-regexp](https://github.com/pillarjs/path-to-regexp), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download pillarjs/path-to-regexp
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cbf30259e6d34d6135f9e7dbaa3371e7188f9936
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── cbf30259e6d34d6135f9e7dbaa3371e7188f9936.nq.gz
│   └── repolex
│       └── cbf30259e6d34d6135f9e7dbaa3371e7188f9936
│           └── chunk-001.nq.gz
├── blob
│   ├── 03b0dd0bfa7be84f6a5a145cee89ad1f06bd4335.nq.gz
│   ├── 0814e7725a20cab6a31f1ba7e0d283df69d55325.nq.gz
│   ├── 0bf643ae28b9bd9b13c5ae7b47b9370add03c9c1.nq.gz
│   ├── 1c90cea63cd102f48b586765e9d2654f85384d73.nq.gz
│   ├── 1ecb72ff0d2a497364d277d302ae864fd9da9183.nq.gz
│   ├── 3daf4716906bcb4f2d1719eba15e0ea84986efdc.nq.gz
│   ├── 3db8e883bb62117606b7ac1504cb2acbc69a767d.nq.gz
│   ├── 40a503d8aa491da8f58e0a4b5be1d31dc4448db7.nq.gz
│   ├── 44ca91d4dc1b30e305d605bfa1dd7a5f20cd8f06.nq.gz
│   ├── 66188e6e5ec39cdcf3bb09fca8ac8ca0e9a92b95.nq.gz
│   ├── 80d056986e59fadfe24ef3208dd6c5b0e0b95c40.nq.gz
│   ├── 983fbe8aec3f4e2d4add592bb1083b00d7366f66.nq.gz
│   ├── a1f162ffe35314d36c4a25bc7aff1a8904e175da.nq.gz
│   ├── bf448d92a8cb5504bcf7c48c33ba9fb3d1938d2c.nq.gz
│   ├── c5c2aecc53b245ccded2321e1824efa9d0f67803.nq.gz
│   ├── f33e3924122f641c7319172204b6929e5b01ff79.nq.gz
│   └── fedbb81688a8bf3807672d2ff85d317bc6c53989.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── cbf30259e6d34d6135f9e7dbaa3371e7188f9936.nq.gz
├── filetree
│   └── cbf30259e6d34d6135f9e7dbaa3371e7188f9936.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 27 files
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

## Source repository

[pillarjs/path-to-regexp](https://github.com/pillarjs/path-to-regexp)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
