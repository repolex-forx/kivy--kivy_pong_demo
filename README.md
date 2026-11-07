# Repolex Knowledge Graph of kivy/kivy_pong_demo

RDF knowledge graph data for [kivy/kivy_pong_demo](https://github.com/kivy/kivy_pong_demo), parsed by [repolex](https://repolex.ai).

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
rlex download kivy/kivy_pong_demo
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── be21a8d0e25ce92db528bc18c21550f78cc5d139
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── be21a8d0e25ce92db528bc18c21550f78cc5d139
│           └── chunk-001.nq.gz
├── blob
│   ├── 06ca7b0c75af8c2cb3d061e8f79245f2caa86f64.nq.gz
│   ├── 086bfb6e7b43c3fd1affd0ed47bce232b12b22ba.nq.gz
│   ├── 1376aa3d307af8492fabb06856d55edc08e283cc.nq.gz
│   ├── 3a2d30e277738126e2354c3858f4562677b7a24b.nq.gz
│   ├── 3b2dfcc9e57ae3ac54011257bb5d2864ece0f14c.nq.gz
│   ├── 3eb0258ea3f448030dba3df8b9db62ca2a952bbd.nq.gz
│   ├── 48fffb49c19a9820382d65c860c108b134a9a73e.nq.gz
│   ├── 59feab641ef103d8b639b352ab6dfc1c21cc5535.nq.gz
│   ├── 5f4a13a225db317dbb3f4cb3ca1e5dc5b10eec2a.nq.gz
│   ├── 63790c27e7a6e5fbd6b1192bf7c6a0e8d6afef5b.nq.gz
│   ├── 6cca4a38a45d044db3c3e68c29ca07ebca2dec10.nq.gz
│   ├── 6ff47f82effe93b171123d9aa2bc1573c763811c.nq.gz
│   ├── 70b6b4696bf00fd654a7e9140612d18e307c6dff.nq.gz
│   ├── 7f9cd2ff48807c69dc2afbc9fb39d3340687277c.nq.gz
│   ├── 9534b018135ed7d5caed6298980c55e8b1d2ec82.nq.gz
│   ├── 990bd1a6bdba162c370cf452b6486ffcdd9aadf0.nq.gz
│   ├── ab250a21e9db108f9eb10a30bf1ee722792ddad8.nq.gz
│   ├── b5b53d636773686564b2ca9e6feb158089592d17.nq.gz
│   ├── b6e47617de110dea7ca47e087ff1347cc2646eda.nq.gz
│   ├── ca3c71a63812a7724d6ef1e7bb372ec2401f9d5c.nq.gz
│   ├── ced5f8aea6dbbe9d6c2a5f3d0b3c80306952f749.nq.gz
│   ├── d0c3cbf1020d5c292abdedf27627c6abe25e2293.nq.gz
│   ├── d714fbcc20ab7fe3b393999c2927dd7b7694d488.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f007ef1a6f44baed5542d1f0d8dcf16957e02068.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── be21a8d0e25ce92db528bc18c21550f78cc5d139.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[kivy/kivy_pong_demo](https://github.com/kivy/kivy_pong_demo)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
