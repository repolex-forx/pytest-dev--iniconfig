# Repolex Knowledge Graph of pytest-dev/iniconfig

RDF knowledge graph data for [pytest-dev/iniconfig](https://github.com/pytest-dev/iniconfig), parsed by [repolex](https://repolex.ai).

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
lexq download pytest-dev/iniconfig
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7faed13ae50bad7c5da3f5782f254a8a7736bb84
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 7faed13ae50bad7c5da3f5782f254a8a7736bb84.nq.gz
│   └── repolex
│       └── 7faed13ae50bad7c5da3f5782f254a8a7736bb84
│           └── chunk-001.nq.gz
├── blob
│   ├── 18ebf4f5d4ba149f176be50d87716f448c6100f0.nq.gz
│   ├── 1e54504055a115014ec627a8c8b301e6dee13b02.nq.gz
│   ├── 46f4b2846fd708ecb81b2d665434ce6379aa1101.nq.gz
│   ├── 50db162a7a7cdca77366d316198f96941357f74a.nq.gz
│   ├── 57b9b44e4cccca635651b8d4380aed1e2ab020a8.nq.gz
│   ├── 65481d2074ae33c12980ea72ca7eec7e07487be1.nq.gz
│   ├── 792c126a68af86b28ba019a430460a31c00fba93.nq.gz
│   ├── 8368741fbffb2415a891c659cf49759ded6cbf14.nq.gz
│   ├── 85193c52698a6080c42b8c670ec90e61ca69956d.nq.gz
│   ├── 948e8832c47147639dfe642dca4c52d3dc1624df.nq.gz
│   ├── b84809f8e9dc0db6fba3505fcc29ca26c3383cce.nq.gz
│   ├── badaa0c349fe741b055297b41f8bb0a73235893d.nq.gz
│   ├── d078bc659504cf79d3cedefe66dd828af9a9d9e0.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f122ddde29a26a092d4cc3104d2d7137cdcb6789.nq.gz
│   └── f1a42cb12dc353bd8cd33fe0fa3d897bd88b4dc4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7faed13ae50bad7c5da3f5782f254a8a7736bb84.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 25 files
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

[pytest-dev/iniconfig](https://github.com/pytest-dev/iniconfig)

---
*Parsed on 2026-09-17 by [repolex](https://repolex.ai)*
