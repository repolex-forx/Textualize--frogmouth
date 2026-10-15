# Repolex Knowledge Graph of Textualize/frogmouth

RDF knowledge graph data for [Textualize/frogmouth](https://github.com/Textualize/frogmouth), parsed by [repolex](https://repolex.ai).

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
rlex download Textualize/frogmouth
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 15c3e85a6e84b2e4a6845723acf12beb54c81eb2
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 15c3e85a6e84b2e4a6845723acf12beb54c81eb2
│           └── chunk-001.nq.gz
├── blob
│   ├── 0f5e04bbba8543883b7b691fc720d4b662d75e10.nq.gz
│   ├── 19f71ccee0c20089f6ee7b4ebc3ca4a69807f805.nq.gz
│   ├── 1a1838ca94043a645f343ec7c87584d73030507d.nq.gz
│   ├── 2715b1835a090e05d2670872e0d0431d5b07e328.nq.gz
│   ├── 3ca4b1e1fd5ba452028eb258393219ecd11f6819.nq.gz
│   ├── 3d4a6737da3461335dc910fbce7b9d56205da47b.nq.gz
│   ├── 408aaf1e8873c1c45bd4beab1a0e4a908026d395.nq.gz
│   ├── 42cfc471d4fd764339391187e35888303e1348f5.nq.gz
│   ├── 4b0bf61b489a0acb393d61821c3687f4c7aa8c7f.nq.gz
│   ├── 56d46a428fcee9d65e9943ff131abd3c2a08b38b.nq.gz
│   ├── 58010f8c8eb77f151c5812f803fafadc98a5eb1a.nq.gz
│   ├── 64b9d7bc82c58eb016ad6e1313c9893193c0e443.nq.gz
│   ├── 7615b8695ea3c2c8f107e43e9edb82815c51c565.nq.gz
│   ├── 7753b456ac5e8edb924d8fb2aa818a0f13209f2b.nq.gz
│   ├── 7bcae66ce3ec18c4c0ca3486c2200fbfe5e1a324.nq.gz
│   ├── 7be510828575ec13662b50b372ce099ccf420b75.nq.gz
│   ├── 8462cc2ca0e3141dbedf650961f345b150907c50.nq.gz
│   ├── 8a11d80157be7c71d10ef70b250064edfdd25ba4.nq.gz
│   ├── 8e041417ad4b1c3e4203079740a6452cb707a48c.nq.gz
│   ├── 90b59c7179647b2871c640f54fd4bcfa6fc94455.nq.gz
│   ├── 9283f7854741aa6a787f38827746026488d6f2ab.nq.gz
│   ├── 9384fc189a56afd4833afeedc6b742880e5746d8.nq.gz
│   ├── 976efd32beaff68c3b187091b290e724821187b0.nq.gz
│   ├── 98c18e95c1e70c7895a0999b8be2ab7bcc8b4aaf.nq.gz
│   ├── 98ed42891999fe3f928dc36139e7b5e3f4faa736.nq.gz
│   ├── 990d399c0e4618fad084f4df4b6a3ce712ce55a1.nq.gz
│   ├── a99ae9d8b67be684884434f0c53370b895feb7a0.nq.gz
│   ├── b08db0c9ce92eb62b5ada025d20dae13f6bfa780.nq.gz
│   ├── b528ba27c3dd255ffca6bd2e4df6c29f8d03832d.nq.gz
│   ├── b56bb261fb878c01271192dda7b52b7191e07131.nq.gz
│   ├── bda3ff7d66794fa129486d9e333130065dd83d21.nq.gz
│   ├── c83b936ff647f2756b01fe468032d5017fbae088.nq.gz
│   ├── c8a18b8bb5c28ae53b0950d0369044ff32f16fd6.nq.gz
│   ├── d3c62dee52da1a582276af8003c5286997a962c7.nq.gz
│   ├── db65eb4dc5515e59c4dd0493bb08d9ccab066113.nq.gz
│   ├── dea3ab947ee2e19057ef9e3120cfa01e17e11478.nq.gz
│   ├── e59b77a20fdff013805d1178d8ac2422091c7050.nq.gz
│   ├── e738234f986e5f42fe51b0b3c2a1249b1551c624.nq.gz
│   ├── e9b37f479daea5bedd9f1ffa82126974164bd2d6.nq.gz
│   ├── f44cf404a3d5e66234ef604c5783ca033dfc8a45.nq.gz
│   └── f6f1a431a1644bf64b6480cf1c843c1c9de29dd2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 15c3e85a6e84b2e4a6845723acf12beb54c81eb2.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 49 files
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

[Textualize/frogmouth](https://github.com/Textualize/frogmouth)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
