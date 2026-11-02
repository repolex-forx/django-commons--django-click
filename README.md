# Repolex Knowledge Graph of django-commons/django-click

RDF knowledge graph data for [django-commons/django-click](https://github.com/django-commons/django-click), parsed by [repolex](https://repolex.ai).

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
rlex download django-commons/django-click
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 283b15f5323b1465e2a4e994cbf41d735995df14
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 283b15f5323b1465e2a4e994cbf41d735995df14
│           └── chunk-001.nq.gz
├── blob
│   ├── 0a022aa4322fab6fbe8573dd16b00dabf78db6ea.nq.gz
│   ├── 1261ca1e57d8c0677dd5f1a1da7842ac769993ec.nq.gz
│   ├── 2553e6939591edd996ea0e60c7b6ddd7e2751a81.nq.gz
│   ├── 2e647279f5ce00d3d37ed8d4ed94c4774bb756ba.nq.gz
│   ├── 32b6d3f206966b3fba645b6edff0241827876bea.nq.gz
│   ├── 34e6ef65879027edcd94ad95b20357c83feabe9c.nq.gz
│   ├── 3a760908bdeaadcda660071bda0474e0a92650ff.nq.gz
│   ├── 41ef1053ab5bf648c82669ad24f665f0072f02a7.nq.gz
│   ├── 44cadb2e84b36dabb9256e9718587fcf66c7ef78.nq.gz
│   ├── 49ec2e8ad2fc7525e788acdb6664e7cbf3091338.nq.gz
│   ├── 4ac7be159b19fb487c019cf33a3a2f4c4558eb3c.nq.gz
│   ├── 4b90b2a0590ef0e6f1a31e411d8f97f5f06729a0.nq.gz
│   ├── 51d211fda5d3db1e59b85bf5ac713743a4a9a968.nq.gz
│   ├── 5a611dcafc47e679a5d4135ab0c52353467e88f6.nq.gz
│   ├── 66dfeb33f61d0225b7bae083f039ad1ddd13aebe.nq.gz
│   ├── 6d66705cf7c828ea8963c7e6efca2655be709551.nq.gz
│   ├── 80e535c66d32640ee886cb3847122cce26593a19.nq.gz
│   ├── 8c695fe35ceb096fa361e17644d2a9ed56a477d5.nq.gz
│   ├── 9ccea5d9e4c970e34e1e6559453c3b865c0c90ad.nq.gz
│   ├── a10ca9144e1a7a5f7cb141c9cb9bef6e6f627a7d.nq.gz
│   ├── a3a1d0f9ce31e2aef2d830103f963c43b4fffacc.nq.gz
│   ├── a73bda1cc5a4ce32d0fcee3487cb94d9bb8797c7.nq.gz
│   ├── a750919a9c9784bf992711c7bad49e0c2ff1902c.nq.gz
│   ├── ada12a03a21491585690cf26d61800101a644d76.nq.gz
│   ├── afa98c7df4c5d069c47be535a013351ab09a0520.nq.gz
│   ├── b3181c44fbac58346f0f62922af9913685959c37.nq.gz
│   ├── b493d96c3c7ececd77a948120f9d9a0b3091b061.nq.gz
│   ├── baf6a43f1d56cf0a772fa0e1fff6c64924eb841d.nq.gz
│   ├── bbbc829205a758750cdb6b0746471d7d8c1a9c35.nq.gz
│   ├── c2955b3d359313a10b4b40a3828a9e9c97b6ef37.nq.gz
│   ├── c4eef05e3d6042514efc4d3195b5976722c11c84.nq.gz
│   ├── d13bb124f1adeb9c650ece1ca12bb2d303512740.nq.gz
│   ├── d3a8b3b2e630285268836fcd79e42807c9de9d88.nq.gz
│   ├── d672f580d1ad2a4dc7971ddacacac436af2c5be1.nq.gz
│   ├── d70be255eaed5a4a5f2000a0d1aba4e0cc57ffd3.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e79cdb457b97b98c5a384a9568a121e0ebbb1126.nq.gz
│   ├── f0920de2ec5a64d9657c1ad6d7f1ac85059dcaec.nq.gz
│   └── f60dae81c8e9fca8ce0da43cad6c8a8708a80a63.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 283b15f5323b1465e2a4e994cbf41d735995df14.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
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

[django-commons/django-click](https://github.com/django-commons/django-click)

---
*Parsed on 2026-11-02 by [repolex](https://repolex.ai)*
