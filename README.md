# Repolex Knowledge Graph of samuelcolvin/logfire_django_demo

RDF knowledge graph data for [samuelcolvin/logfire_django_demo](https://github.com/samuelcolvin/logfire_django_demo), parsed by [repolex](https://repolex.ai).

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
rlex download samuelcolvin/logfire_django_demo
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0e985073ce187749a353454ea631486e02953a5b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0e985073ce187749a353454ea631486e02953a5b
│           └── chunk-001.nq.gz
├── blob
│   ├── 0f2f1842b33e91efcc5f4dce052ca95fee1fdf34.nq.gz
│   ├── 21914d9ab62b0dc193c7d0c282e20baaeb6279f0.nq.gz
│   ├── 26bc605ac9f70f5e2b3d8b2168f8b99d2e062e05.nq.gz
│   ├── 302e48966376a15bf7d8624e2b4547bf9086760a.nq.gz
│   ├── 60dff9bea2528ff4c63b74309617d210c1a31d8e.nq.gz
│   ├── 720ea0922c66c7dbebf5e726e85e6b24d67ed3c1.nq.gz
│   ├── 7ce503c2dd97ba78597f6ff6e4393132753573f6.nq.gz
│   ├── 8c38f3f3dad51e4585f3984282c2a4bec5349c1e.nq.gz
│   ├── a70efb93afde06e1d4904435e8bdd1d7c63e6b3a.nq.gz
│   ├── ce59bae49a973a63e3c6262fc6d23cc954002507.nq.gz
│   ├── e0cc2f941db18dd2c96e47a2bdbd0196799afe15.nq.gz
│   ├── e5bd9924aa1c19740a884e2251d38518d9f5dc20.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e85423d77a92c32f731f1740d39bf1b7bf927aaf.nq.gz
│   ├── ed0a01bb70919ce088c20b7b8c00d44fd0f0253f.nq.gz
│   └── f4677cc3a35b42771a9fda37c5b86f8d0debfec4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0e985073ce187749a353454ea631486e02953a5b.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 22 files
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

[samuelcolvin/logfire_django_demo](https://github.com/samuelcolvin/logfire_django_demo)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
