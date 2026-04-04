---
title: "The scaffold is not the building"
description: "The first version's job is to be torn down."
pubDate: "2026-04-04"
---

*The first version's job is to be torn down.*

Nobody questions removing scaffolding. It goes up. It lets the work happen. It comes down. The building stands on its own, and nobody mourns the poles and planks that made it possible. The fact that the scaffold took labour — careful, expensive, entirely real labour — does not make it part of the building.

In software, we are sentimental about scaffolding.

The first version absorbs the first burst of effort, so it acquires moral weight. Throwing it away feels like ingratitude. So the wrong abstraction chosen in hour one becomes the wrong abstraction that ships in month six. The data model that made sense when the problem still looked like a screen flow survives after the domain has revealed other intentions. The names coined before the objects were understood become canonical by simple administrative success: too much code now depends on them.

Then the scaffold starts dictating the shape of the building. Not just technically. Psychologically. You stop solving the original problem and start solving the structure you happened to assemble while trying to understand it. Every expedient brace becomes a load-bearing wall by tenure alone.

This is scar tissue. It ships.

---

## Scaffold first

There is a better use for a first version.

Write it quickly. Change it freely. Treat the whole thing as scaffolding: not a building in progress, but a temporary structure erected so you can discover where the real weight falls. Its only serious job is to expose the invariants — the load-bearing truths that remain after your guesses, conveniences, and misunderstandings have been stripped away.

That changes how you treat unfinished parts. If something has not proved load-bearing, do not make it elegant. Do not generalise it. Do not give it a future. A duplicated conditional may remain duplicated. A helper may stay narrow and graceless. A representation may be obviously temporary. Refining a non-structural element is not progress. It is painting the scaffold.

Once the load-bearing elements are visible, the temporary structure has done its work.

So take it down.

Start again from a cleaner description of what the thing is. Not what you first suspected it might be, not what the exploratory code happened to make convenient, but what the probe taught you. The second pass has an unfair advantage: it already knows where the weight goes. It can put supports where supports belong. It can leave empty what should remain empty.

The first version earned its keep by teaching you what to write. It still does not get to ship.

---

## What keeps standing

A clean-slate rewrite is not a return to ignorance. It is the first attempt made by someone who now knows the shape of the thing.

What survives across attempts is structural. A feature that survives three bad implementations is real. An abstraction that keeps reappearing despite your efforts to organise around something else — that is the one the problem wanted. When the scaffold comes down and the same lines remain, those are the lines of the building.

The clean slate is for the artifact, not the author. The author keeps the knowledge. The artifact sheds the accidents.

---

## Demolition

The objection, of course, is waste. From the outside, tearing down a week's work looks indistinguishable from having done none. The commit history is abandoned. The clever stopgaps are discarded. Someone asks what you have been doing, and the honest answer is: learning where the building is.

That is work.

The scaffold was necessary. It let you climb around the problem, find the spans, the awkward corners, the places that only looked structural because you had not yet seen the whole frame. What it produced was not nothing. It produced knowledge.

What it did not produce was the thing itself.

So it comes down.
