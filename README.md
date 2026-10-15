# Repolex Knowledge Graph of simonw/s3-credentials

RDF knowledge graph data for [simonw/s3-credentials](https://github.com/simonw/s3-credentials), parsed by [repolex](https://repolex.ai).

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
rlex download simonw/s3-credentials
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4611f333407d2428b2e21771469e34fd52a5165d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4611f333407d2428b2e21771469e34fd52a5165d
│           └── chunk-001.nq.gz
├── blob
│   ├── 070a74ca59310ec0a4312957ef37077821808cb1.nq.gz
│   ├── 0f65763addf8a9623007bbd8a75e8d98e38f2496.nq.gz
│   ├── 19767f08ee427b2ca99669cd7df90eb491056343.nq.gz
│   ├── 1aad3e9b50c1d82853147a8e4e454fdd0a8f3441.nq.gz
│   ├── 1da90d56ed0fc498179f9318267e07b4739aa527.nq.gz
│   ├── 1df9bb06316ae8a2906be3b5afb5e364dbc95fe8.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 265fcc9655cb4bb60128e90a937eeecaf6e5c82e.nq.gz
│   ├── 3637256a5e943a18051ed6f801654e9732a05e48.nq.gz
│   ├── 4e88bd7e2406cb78484013df96c21a80d38f3a73.nq.gz
│   ├── 53605b7a5ec51bc95dca4fb43fdb350bf9362435.nq.gz
│   ├── 6f11f5951f4654cb098806eac3408a2ad1e343d1.nq.gz
│   ├── 7c461830ba934923f012152d5331c06d472d09ed.nq.gz
│   ├── 8041842bf8029443af9d3fe558159a5f5aec3337.nq.gz
│   ├── a0420f7269cd1775306d43c6ae659de9f2dc70e3.nq.gz
│   ├── a279768f126b210e024ba7e983a9ee2ccfd15118.nq.gz
│   ├── a7f3b7fdb00e20a6336b912a4f320f528e1f7699.nq.gz
│   ├── af8ae73e7fc55cf101ff1bb2e67fb210918107e8.nq.gz
│   ├── b1c22b4a9a3495e7024220a6f3c53a4147a5f2dc.nq.gz
│   ├── b38df29f46e14033477513e27b6b7a689b75ed51.nq.gz
│   ├── b419f80b3e82e37b9eb11aabab43383783df49f9.nq.gz
│   ├── b6031dbc4016c8721a9b31dd129f9db0de08977f.nq.gz
│   ├── b72bb06850500a36900cfd361890b1dcb6853b3b.nq.gz
│   ├── bc83ff4d4621262990c2370ae1a4fe07902ce893.nq.gz
│   ├── e35d8850c9688b1ce82711694692cc574a799396.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e7099c9c004ead18a8221cf6c4fa2628e26842d8.nq.gz
│   ├── ea10a189a24416b792c2160a14a25713a568b391.nq.gz
│   └── edd893abcf1949dec478e5f517ffc7339979d04e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4611f333407d2428b2e21771469e34fd52a5165d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
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

[simonw/s3-credentials](https://github.com/simonw/s3-credentials)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
