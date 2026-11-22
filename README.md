# Repolex Knowledge Graph of mitsuhiko/similar-asserts

RDF knowledge graph data for [mitsuhiko/similar-asserts](https://github.com/mitsuhiko/similar-asserts), parsed by [repolex](https://repolex.ai).

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
rlex download mitsuhiko/similar-asserts
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4eff50b597acc7f7ca65606d015da2fc5061273c
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 4eff50b597acc7f7ca65606d015da2fc5061273c.nq.gz
│   └── repolex
│       └── 4eff50b597acc7f7ca65606d015da2fc5061273c
│           └── chunk-001.nq.gz
├── blob
│   ├── 0cb5507a0baab24d5f8db52c632f328f6777176a.nq.gz
│   ├── 1560fac8a288a23c1e1e24c9a12aed4da427de9c.nq.gz
│   ├── 16fe87b06e802f094b3fbb0894b137bca2b16ef1.nq.gz
│   ├── 1859c8251b2b79633093bd585d51fc2789d61319.nq.gz
│   ├── 18b16becec4a7e299eaed17e7971c106ec6e8875.nq.gz
│   ├── 1e95303f698729288f07cb0a3122248517d4547a.nq.gz
│   ├── 1f8c5156cf5f40f5958b0d836d766778b47871c0.nq.gz
│   ├── 231c155700ddd20976fc527e8c571aba59b8ccbb.nq.gz
│   ├── 2c96eb1b6517f2617f9ddeae9f07f5fd7bd7ddef.nq.gz
│   ├── 31bd516ec26b41425a08f0be867197c6bf2ed22b.nq.gz
│   ├── 3606b44f4ec2f6065e8afbf26cb3208a11a967c0.nq.gz
│   ├── 3d7e6b714b2aa0926646ddb7fdf80b626a4fde43.nq.gz
│   ├── 43e8fa8a26e28c12c794c84eba12f4d445ff1005.nq.gz
│   ├── 449aea61fdf18f95aaedfb6ca5684020f6449ecf.nq.gz
│   ├── 4b5052cb5f67b39277c9a32c48f599ac131a6567.nq.gz
│   ├── 73926b3f21e2568071e904c5447dfc726ecad69d.nq.gz
│   ├── 7a8b1135c963e3db38903d8beda187ea373c32f6.nq.gz
│   ├── 909f05cfa0ccb41316af89f5ef530cc568bed663.nq.gz
│   ├── b1f0fbcf1df57816283877a0286227219881411e.nq.gz
│   ├── c2f8580eb932eade75c835fd8b00d55e185b2cfd.nq.gz
│   ├── cd44b103ddd43c07c7495e63ed76cbff079baed4.nq.gz
│   ├── cfe41fb6f823e0aca87072ad6aad3cfba67edce3.nq.gz
│   ├── d088abe8c8e2478f78519f3fbb0b6ebf391e6b65.nq.gz
│   ├── e9654858213dc0717d25baed1a89038a7032ae3f.nq.gz
│   └── ee57f1df49f10e6d30c97484f4001cbf2088d385.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 4eff50b597acc7f7ca65606d015da2fc5061273c.nq.gz
├── filetree
│   └── 4eff50b597acc7f7ca65606d015da2fc5061273c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 35 files
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

[mitsuhiko/similar-asserts](https://github.com/mitsuhiko/similar-asserts)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
