# Repolex Knowledge Graph of asimov-platform/asimov-universe.rb

RDF knowledge graph data for [asimov-platform/asimov-universe.rb](https://github.com/asimov-platform/asimov-universe.rb), parsed by [repolex](https://repolex.ai).

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
lexq download asimov-platform/asimov-universe.rb
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f11fb581d4fc2cdcf9ed248129ca60dbe2ad875e
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── f11fb581d4fc2cdcf9ed248129ca60dbe2ad875e.nq.gz
│   └── repolex
│       └── f11fb581d4fc2cdcf9ed248129ca60dbe2ad875e
│           └── chunk-001.nq.gz
├── blob
│   ├── 0074ac243e97f58407fc5578ba1618c45bf1d23e.nq.gz
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 44b41ab48433ad5cc4388b2d66be380c0f6ad512.nq.gz
│   ├── 53683c76d06540eafca0436baf95f3981081e9f4.nq.gz
│   ├── 5fce5dcb9a147bfdd7584bbf66e02199b1b4dfc2.nq.gz
│   ├── 6f83656972dcf4cdabab996bd49dde3986bc10be.nq.gz
│   ├── b4e2a20bb6069d33479542fc863e7e36810e0f01.nq.gz
│   ├── b7f3a74ca7603fb0a6e32c31de0a52de3ac5befd.nq.gz
│   ├── bb67c988519445888ae76a7c7c4041de9dee75cf.nq.gz
│   ├── bec646ebc92f27af7bd284c6c8895f0ba82544c2.nq.gz
│   ├── cc6f535b40f4ebf04221043237ff3deaf67f9549.nq.gz
│   ├── cd138f62a7d2e53edef94443810d0162e2c9f095.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── f11fb581d4fc2cdcf9ed248129ca60dbe2ad875e.nq.gz
├── filetree
│   └── f11fb581d4fc2cdcf9ed248129ca60dbe2ad875e.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 23 files
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

[asimov-platform/asimov-universe.rb](https://github.com/asimov-platform/asimov-universe.rb)

---
*Parsed on 2026-04-15 by [repolex](https://repolex.ai)*
