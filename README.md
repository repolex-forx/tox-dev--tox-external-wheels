# Repolex Knowledge Graph of tox-dev/tox-external-wheels

RDF knowledge graph data for [tox-dev/tox-external-wheels](https://github.com/tox-dev/tox-external-wheels), parsed by [repolex](https://repolex.ai).

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
rlex download tox-dev/tox-external-wheels
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ad1867878fd601af91be4dffb5d9180764bad789
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ad1867878fd601af91be4dffb5d9180764bad789
│           └── chunk-001.nq.gz
├── blob
│   ├── 0fd806c7a513250d8561c42d19325375f5654dda.nq.gz
│   ├── 126a5e154f389b4e646af65be975801f37c25151.nq.gz
│   ├── 20f8cdba0f463d3f646c2ce72223307254ac7314.nq.gz
│   ├── 28d47b7c2f1ab94d678a097f736d425eec7c2e8a.nq.gz
│   ├── 28f2999419ab9d0bb1302519f3c932f2f37ce744.nq.gz
│   ├── 37ac4ee57ac7a1d6c68ad9bb21a01c4caa766cca.nq.gz
│   ├── 37d4c5b6606787ae59325bfc2167fc55b2189042.nq.gz
│   ├── 3d5a91b5988bc473942268eba56aabb9f90e19f1.nq.gz
│   ├── 3f8a1718a054d83dfdf5d8ab49275ab016b4c3b2.nq.gz
│   ├── 40108653cd89aba44b89fe106c8230c99e347aae.nq.gz
│   ├── 496df6add62dcdc0ecc5e572c439ef7e6840ecf5.nq.gz
│   ├── 4b0c907829cc6fcde7cc67caa064cee4a50f4992.nq.gz
│   ├── 68d70c387326f9399a6e6082ee258541a808e4ab.nq.gz
│   ├── 6a3b0faccf97c9b940f835059fcea1848172b4f0.nq.gz
│   ├── 764f4ca499736affc2bd9830121fb5ca19570376.nq.gz
│   ├── 81b69de2a5b140dbf0c26ef06fdd00e28f97e8cb.nq.gz
│   ├── 912add4eca6c6faa9575722b60638e7886277e61.nq.gz
│   ├── 93d36eb10a01c802cb8fe93c108b7d4919e687c5.nq.gz
│   ├── 97f03190012a904bf7d78151c0364d351e808cfc.nq.gz
│   ├── 9b933fdabeb04bddc98cf67a78a7ce6f20366c81.nq.gz
│   ├── b533102bd24e5c00392ccd5e306c3e29d7afdd51.nq.gz
│   ├── c4ebaf22d59a007250bc1b5a972e223e2d4b136c.nq.gz
│   ├── d038a8b45571af8cffda232155d3b722d1ce9fee.nq.gz
│   ├── f24c49255917b29a3ff41e3d4322ae17299984e3.nq.gz
│   ├── f3e9a2e222363ebc06f026fb145b7a94dee7bb0b.nq.gz
│   ├── f7f8a6108da6469c54e7d28053864cc19c8a6077.nq.gz
│   └── fcafe597b07d06de5b1e90febe66d6a6bb482059.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ad1867878fd601af91be4dffb5d9180764bad789.nq.gz
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

[tox-dev/tox-external-wheels](https://github.com/tox-dev/tox-external-wheels)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
