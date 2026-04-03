---
title: "mor: personal memory I own"
description: "Markdown files on my disk. CLI, MCP server, mine."
pubDate: "2026-04-04"
---

Stuff gets buried. Notes in some SaaS. Snippets in Slack. Context trapped in products I don't control.

[mor](https://github.com/laat/mor) — markdown files on *my* disk. `cat`, `grep`, `git`, done. Same spirit as Obsidian and org-mode, but it's TypeScript. I write TypeScript. When I want to change how it works, I change it.

It's also an MCP server, so claude.ai and chatgpt.com can access the notes too. Feels nice... for now.

## What's in there

Stuff I refuse to write twice. A [Fastify chaos plugin](https://github.com/laat/mor) that randomly 500s requests. An [RxJS BehaviorSubject](https://github.com/laat/mor) backed by localStorage with cross-tab sync. Architecture plans for [readme-assert v7](https://github.com/laat/readme-assert). The kind of thing that ends up in a dead gist or a Slack message from six months ago.

Mid-conversation, need a snippet? AI calls `memory_search`, pulls it up. No digging.

## Usage

```bash
echo "Always use snake_case for Python" | mor add -t "Python naming"

mor find python naming
mor grep -E "async\s+function"
```

FTS5 full-text search, regex grep, optional vector search (OpenAI/Azure/Ollama). Add from files, URLs, stdin, `$EDITOR`, and chat.

MCP server exposes `memory_search`, `memory_read`, `memory_create`. Hook it up to Claude Code, Claude Desktop, Cursor — whatever.

## Remote

`mor serve` on a box, connect from anywhere. OAuth or bearer token. `mor sync` for git-backed sync across machines.

---

Personal project. My workflow, my opinions. [GitHub](https://github.com/laat/mor). For laughs, check out [mor's homepage](https://mor.laat.dev). Made soaking with irony.
