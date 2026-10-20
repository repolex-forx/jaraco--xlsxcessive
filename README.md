# Repolex Knowledge Graph of jaraco/xlsxcessive

RDF knowledge graph data for [jaraco/xlsxcessive](https://github.com/jaraco/xlsxcessive), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/xlsxcessive
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a4c270b6be70278a4a9e89e8e2c836b28cb703a9
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a4c270b6be70278a4a9e89e8e2c836b28cb703a9
│           └── chunk-001.nq.gz
├── blob
│   ├── 10d412f406891b9683f832fcbc134c9bdf4f916e.nq.gz
│   ├── 1afe5cbec4d22521f923a48a25c3b0ed00212a73.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 23d0053d3c158d08107646860acd43bfb19e77e0.nq.gz
│   ├── 240329c3604d8ead4c10aa8c88352caa8e4ce7b2.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 3ae9682b053b098b29e71b65cb7fce24c1f24134.nq.gz
│   ├── 505164ec04a637808a77a43121224a612b5c24e2.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 59f87f5600519bc09070e4da9c173bed3fee041f.nq.gz
│   ├── 5a2d48bd890646faaee4426a25f53d44dee5309b.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 66d2ad54cc9329bd10f5ce19e0b932c224a1ed21.nq.gz
│   ├── 69241fa038f92fd2dec34075fe0697aef97ee501.nq.gz
│   ├── 6e2e7dfb17283fe51c293e4b4c81d31ed9330dde.nq.gz
│   ├── 6fe1796ca5886471980474a3a084bd7e8f32a273.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 8091f32bbdc5bb65856d4731cd4c13b4597ae26d.nq.gz
│   ├── 888725ad4fb4dd2685ffc56d6a32c754db148199.nq.gz
│   ├── 8bb8797957cee23ddbd1eeac30b66a57f08df3af.nq.gz
│   ├── 9806ba627a28e2fee44ca70d97a1124b7240fbc9.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── 9b60e106fd2fe669c14b910d4a20702db58482c8.nq.gz
│   ├── af3a0abc0abdfd6f5955470b90403394bd6b317b.nq.gz
│   ├── b6006b4ab487898858d927166b23a1ffdacbcffc.nq.gz
│   ├── b72de8a454b732f60b13836fe29101e2fd36d74d.nq.gz
│   ├── bacb14e9743d1622be338473360052925fbd43cd.nq.gz
│   ├── bd65d68ba290f16d5f4de7a9a6872ed29beff9da.nq.gz
│   ├── cc60a3dfd4b580c69efda46962b2a1bfaa8edd61.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── efcb8cbc2043faa7caf4f92fc7488bd6914c934c.nq.gz
│   ├── f0bcf024c25c00fba4843f1bf38a3b944abca41c.nq.gz
│   ├── f7559270c03acc40964c873938f667282309bc66.nq.gz
│   └── fabc0495d303aeba91ab5ec592344e02fbd6996d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a4c270b6be70278a4a9e89e8e2c836b28cb703a9.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
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

[jaraco/xlsxcessive](https://github.com/jaraco/xlsxcessive)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
