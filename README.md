# homebrew-memo

Homebrew tap for [`mlx-memo`](https://github.com/jagoff/memo) — local MCP memory for AI agents, MLX-native, Apple Silicon.

## Install

```bash
brew tap jagoff/memo
brew install mlx-memo
```

Apple Silicon (M1 / M2 / M3 / M4) only. The formula refuses to install on Intel Macs — MLX, the runtime that loads the embedder + reranker + chat LLM in-process, doesn't build on Intel.

After install, two binaries are on your PATH:

- `memo` — CLI (~28 commands: `save`, `search`, `tui`, `watch`, `mine-history`, …)
- `memo-mcp` — MCP server (stdio) for Claude Code / Claude Desktop / Cursor / etc.

## Upgrading

```bash
brew update && brew upgrade mlx-memo
```

## What's `mlx-memo`?

Persistent semantic memory for AI agents. Markdown is the storage of record (your memorias are plain `.md` files in an Obsidian-readable vault), `sqlite-vec` is the rebuildable vector index, and the embedder / reranker / chat tier all run in-process via [Apple MLX](https://github.com/ml-explore/mlx). Zero Ollama, zero cloud APIs, zero network calls in the hot path.

Full docs: <https://github.com/jagoff/memo>

## Source

- Main repo: <https://github.com/jagoff/memo>
- PyPI: <https://pypi.org/project/mlx-memo/>
- License: MIT
