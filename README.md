# Repolex Knowledge Graph of agronholm/sqlacodegen

RDF knowledge graph data for [agronholm/sqlacodegen](https://github.com/agronholm/sqlacodegen), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/sqlacodegen
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c7eef1f533f2594b2c22537d4a9900a609c07b6a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c7eef1f533f2594b2c22537d4a9900a609c07b6a
│           └── chunk-001.nq.gz
├── blob
│   ├── 07806f8af9dd3253ebdb5710b67e73124aea4941.nq.gz
│   ├── 1c68eca3f2c9dd249b18b1794fefe4892243fc14.nq.gz
│   ├── 1da5f1460cd4ea75053a5447386ff2e0427672bd.nq.gz
│   ├── 29da75839dad012b88a374701e7820da9f43a0c2.nq.gz
│   ├── 307f865c9c9b778c0301a612cd10b1ecea926d94.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 45a2f73673edab66a13ab5de206142341e996f10.nq.gz
│   ├── 4e28416e104515e90fca4b69cc60d0c61fd15d61.nq.gz
│   ├── 56145058a22b998dd0926a356046eb5b308990fe.nq.gz
│   ├── 565288aa55228425a199bc51e47db77ab186417e.nq.gz
│   ├── 59ac9ee9ab545387884b36db4b6ad1ea109c835b.nq.gz
│   ├── 70d4ed85d32dce890a8440dcf2c65a69a23e1c91.nq.gz
│   ├── 77d3f404b9d0fca9874b18062ace332753d20221.nq.gz
│   ├── 8328aed0052ad9a48f44a010603c52da434f8ef8.nq.gz
│   ├── 83bd9182e122cddbcc154048c23653280ae60f6c.nq.gz
│   ├── 8913c07267a9601bd4caa9c344029f17578b858f.nq.gz
│   ├── 8f37373fe3abcbeb07f6dccb8afaa082b9657d71.nq.gz
│   ├── 94ef4d6e08b9effda358b4703646d03b70629728.nq.gz
│   ├── 972dce90c6320bbf1a058f945a1a2d141833c523.nq.gz
│   ├── 9f83bdd7da4710cb250cb170ad2b80fcd43cbc68.nq.gz
│   ├── ae2a085e69b18dee21332b0bac2e8908b6fef64f.nq.gz
│   ├── cf791adfbb55cf57d1df030116fd9f5d455e7f91.nq.gz
│   ├── d4410ff70c4843b855e2db942c27612163388b36.nq.gz
│   ├── d5bd042fba49d8dc955b743e17fa23cd794d29f7.nq.gz
│   ├── e467dc2bc5a74d357d5502d661245e2aeaca5a75.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f62c747a63547090cb0ab734750bf234c076a681.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c7eef1f533f2594b2c22537d4a9900a609c07b6a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 35 files
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

[agronholm/sqlacodegen](https://github.com/agronholm/sqlacodegen)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
