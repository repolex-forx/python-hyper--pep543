# Repolex Knowledge Graph of python-hyper/pep543

RDF knowledge graph data for [python-hyper/pep543](https://github.com/python-hyper/pep543), parsed by [repolex](https://repolex.ai).

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
rlex download python-hyper/pep543
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a7c508911989655bea39f181e5d4ead04e81d47f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a7c508911989655bea39f181e5d4ead04e81d47f
│           └── chunk-001.nq.gz
├── blob
│   ├── 10010317f8794e752c73a73dd2497cf9d25f0e8d.nq.gz
│   ├── 29ec7af0f62bff12881fa8ef8ce34b078feb286e.nq.gz
│   ├── 33f2ddc8934600bdd77b98e2e874c5614419d622.nq.gz
│   ├── 3793ffc1b944af2f8f111fc9d496d607df9a85ea.nq.gz
│   ├── 3b8be7d06e02ab8d93fe1f11d17dc137c88685c8.nq.gz
│   ├── 3ee42538e886a54ab08226cb849294e8a3c8a1ae.nq.gz
│   ├── 4972c3394279d43d84ee5ef206ffcd49f04d57d6.nq.gz
│   ├── 49cfabcb6f5672fe10257a3649f7dbe46252814d.nq.gz
│   ├── 5b4b0a8fed211bc560b263751fc330078374ae76.nq.gz
│   ├── 5e4090017a9bec5de60a745d17007a9e95f31a43.nq.gz
│   ├── 7bfc95272aa9207987fbacc5e4c7c2033d83c1a5.nq.gz
│   ├── 89fa588210feea438ba7b9a62d186a130df8da38.nq.gz
│   ├── 98a24edf8de39bb2f4963bf4eb0a8750f820f392.nq.gz
│   ├── 997fcd11e29a665b357c9c0e7922351bc9db6ed2.nq.gz
│   ├── 9d19e106e3ce4ffa975e054f77e6d2b8a522c942.nq.gz
│   ├── d9a911cc5db238c83a57518b87e624efb8af22fc.nq.gz
│   ├── e2d82beb11ff5a486edb2a5cfc96f53f6f4e1002.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e8e5ac441397e1dacae86f02c98b88e1d21cefdd.nq.gz
│   ├── e9b36cc3ce0a4e20d1839d234626445517d4c63c.nq.gz
│   ├── ecb9bdea4d57731897ce885c840e817cae9c18d0.nq.gz
│   └── f0f6a1ab8019b8bd3c20f04dec37bfcfd2f72d49.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a7c508911989655bea39f181e5d4ead04e81d47f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[python-hyper/pep543](https://github.com/python-hyper/pep543)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
