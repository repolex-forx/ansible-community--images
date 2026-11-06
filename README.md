# Repolex Knowledge Graph of ansible-community/images

RDF knowledge graph data for [ansible-community/images](https://github.com/ansible-community/images), parsed by [repolex](https://repolex.ai).

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
rlex download ansible-community/images
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4202d8e9e34680204004e57c837efd33f5bd633f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4202d8e9e34680204004e57c837efd33f5bd633f
│           └── chunk-001.nq.gz
├── blob
│   ├── 01487b0e2c459b0b53c0fdd67d684cb35c747744.nq.gz
│   ├── 04685a1fd9cb36aabc21ce8de06cb7281534ae95.nq.gz
│   ├── 11064722791e7712cc669e81091c986bf4d2c840.nq.gz
│   ├── 1531100ac7bf6a51d678eecaf585e47f40a05a46.nq.gz
│   ├── 17b6fd534a9afeec012c31509d6ecbc11129f09f.nq.gz
│   ├── 1d50dde5a83a643f05b4d072e018b0160e3e8ef3.nq.gz
│   ├── 20bc843425c28873249db1ad2a8201977253185b.nq.gz
│   ├── 288ad8b10b6817e66f56ce4c58f18480883e35d4.nq.gz
│   ├── 2f4ff900d88f292b8d102272e2d3a5b466706423.nq.gz
│   ├── 30ed66dcb9782d64f89048aa3360dff925c18c52.nq.gz
│   ├── 3de39c09dc780b7f71ddc0c149d9db58af66baa6.nq.gz
│   ├── 3eb4b3c572d87d12bf3340f1ec687370c6eaa1a9.nq.gz
│   ├── 4220a85f530faa2069830200bb98ab06f0bb0ad0.nq.gz
│   ├── 63faf050f31cb0becce6cdfb3aed88d8fae4ba4c.nq.gz
│   ├── 69b77a8288c001e986880add560bf67a23d1cfd8.nq.gz
│   ├── 6ee5298aaa09dedb829771e932515e10927b5af0.nq.gz
│   ├── 713d98b79d0055f5afb0456f7914568f6cf076c2.nq.gz
│   ├── 76dfbe666284a9d41fcdc4795e5e0d15cf1f4d8e.nq.gz
│   ├── 8e991ca9fde95f8f365c5e4a49b06d0a9169911e.nq.gz
│   ├── 9cecc1d4669ee8af2ca727a5d8cde10cd8b2d7cc.nq.gz
│   ├── ae0f257303be3707d4b8ad47f93eb5e93555c26e.nq.gz
│   ├── b117346283781c45dcecf6911030d481e4eab3b3.nq.gz
│   ├── b4d90790223b95552556ea895ac541a489a7379d.nq.gz
│   ├── b78c4f042547dd1b7f42553305aa66010320fa95.nq.gz
│   ├── c449d1b0f1582b942e2b91abdce60dc9ea261f1d.nq.gz
│   ├── cb7d68e01048487d17029e49a23c4d0de8f18830.nq.gz
│   ├── d56fc9897e73270cee2592ea2e6216130933e543.nq.gz
│   ├── d7873f9c21010f7c65f85ddc4d42c92a54650304.nq.gz
│   ├── e0233adff29f3ed930e9c8769b42e6a91fabdfbb.nq.gz
│   ├── e052b6426917d4892b622a4705577a11a9257e2f.nq.gz
│   ├── e29d27433f3009163a4a258180abcbfa3d908984.nq.gz
│   ├── e6baa2935642b52bf71459c63993b2acf97166d2.nq.gz
│   ├── e759bc4b745d7099bd4b172be775a529f8c4b5a8.nq.gz
│   ├── fe230c62c4fd37e0fc38f015927a3a12d1bab996.nq.gz
│   └── fe51426f76a4442089c11bce8bc8b57ad557a149.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4202d8e9e34680204004e57c837efd33f5bd633f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 43 files
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

[ansible-community/images](https://github.com/ansible-community/images)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
