---
title: "If you can't grep it, it's not yours"
description: "Markdown files on my disk. CLI, MCP server, mine."
pubDate: "2026-04-04"
---

Stuff gets buried. Notes in some SaaS. Snippets in Slack. Context trapped in products I don't control.

This is not a storage problem. It is an ownership problem.

The notes exist. The SaaS will assure you they're backed up, searchable, shareable. But they live on someone else's server, in someone else's schema, behind someone else's authentication. You have access. You do not have a lease. When Slack changes its search, your search changes. When the startup pivots or the free tier ends, the notes are gone — or held behind an export button you'll never click in time.

There is a simple test: can you `grep` it at 2am without a network connection? If not, you don't own it.

---

## The burial

The snippet you needed this morning — the RxJS operator with the edge-case behavior, the Fastify middleware you wrote for chaos testing, the architecture note from the meeting six months ago — is in a Slack thread. Or a dead gist. Or a Notion page in a workspace that has been reorganized twice since.

You know it exists. You cannot find it. The SaaS has eaten it.

The situation is worse with AI. When you want an assistant to use your context mid-conversation, the context needs to be *callable* — not "findable in five minutes of clicking," but retrievable on demand. Anything short of that might as well not exist.

---

## Repatriation

[mor](https://github.com/laat/mor) is markdown files on your disk. `cat`, `grep`, `git`. Same spirit as Obsidian and org-mode, but I wrote it — so when I want to change it, I change it. FTS5 full-text search, regex grep, optional vector search. Add from files, URLs, stdin, `$EDITOR`, or chat.

It is also an MCP server. Claude and other tools call `memory_search` and `memory_read` directly. Mid-conversation, need a snippet? It's there.

The notes stay yours because the substrate is yours. `.md` files are not a format — they are a position on permanence. Proprietary formats rot. SaaS companies pivot. A directory of markdown files survives all of that by being boring.

So do the notes inside it.

---

[GitHub](https://github.com/laat/mor). For laughs, check out [mor's homepage](https://mor.laat.dev). Made soaking with irony.
