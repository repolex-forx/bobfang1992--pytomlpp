# Repolex Knowledge Graph of bobfang1992/pytomlpp

RDF knowledge graph data for [bobfang1992/pytomlpp](https://github.com/bobfang1992/pytomlpp), parsed by [repolex](https://repolex.ai).

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
lexq download bobfang1992/pytomlpp
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── blob
│   ├── 0f877ef5602f2ec175eedf429a7e1bd1f11edaca.nq.gz
│   ├── 35780ef9237d7decf68b5c322a8c755d899da103.nq.gz
│   ├── 38bf4afc0752892ce97f9fe5aacd223ccb5db816.nq.gz
│   ├── 79560bfed71719386d2a5379d4c9d9f945047a50.nq.gz
│   ├── 7b85af606f4ef823e03cc324b61a628196d9c6e3.nq.gz
│   ├── 8b68b688a3cc420bd46410906c8bb4a1aaf4e09b.nq.gz
│   ├── 95cc6237a573c57973c9e614e8c2b251cd6f4f11.nq.gz
│   ├── a6b6e5834cea833a6f2c54516e7e412e591022d9.nq.gz
│   ├── aadeb84fddb7668f8479ee1f7ca4ab4e7b0ab405.nq.gz
│   ├── b18bdf7b72fbb386678684caf674431567382576.nq.gz
│   ├── b5b7aadb959617ae58e24139c783f8c52f33ae82.nq.gz
│   ├── b61a282583d68b02a32f6390846ae48c9994d4ce.nq.gz
│   ├── c40a9bbeff7d6fc482af4fd1713e46c16aa9f345.nq.gz
│   ├── d2433028ed3347a4cd9b2245f6b038a43da230eb.nq.gz
│   ├── d69067bb9075b6458c0fb805d21ef359cc9964c4.nq.gz
│   ├── dca82e1b9abc1cd17e44e68f7f7214d1f452f752.nq.gz
│   ├── f495706a5e5caf798560300438846d23414d25d6.nq.gz
│   └── fc3a9afad452d7618786c9ba53b175932ee6797e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c5ea2f5760654731de49bb55bd7ca9f7e2e01b17.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

8 directories, 24 files
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

[bobfang1992/pytomlpp](https://github.com/bobfang1992/pytomlpp)

---
*Parsed on 2026-03-20 by [repolex](https://repolex.ai)*
