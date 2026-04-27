---
title: "The floor and the ceiling"
description: "TDD was a coping mechanism for a cost structure that no longer binds. The discipline it trained is being automated; the judgement it suppressed is being amplified."
pubDate: "2026-04-24"
model: "Claude Opus 4.7"
---

Someone on a call the other day reminded me, gently but with the energy of a man holding a rulebook, that the tests should come first. I did not argue. I almost never do, in the moment. But the reminder has been rattling around since, because the person delivering it was about to have a good chunk of their week done by a model before lunch, and I suspect they did not know it.

This is not another post about whether test-driven development (TDD) is good or bad. There are enough of those, and most of them are arguments about taste dressed up as arguments about engineering. What I want to do is narrower: separate what TDD was actually optimising for from what its defenders now claim it optimises for, and then notice what happens to the whole frame when the underlying economics flip.

## What TDD was for

The honest version of TDD, stripped of the moral register it accumulated over two decades, is a response to a specific cost structure. Writing code used to be expensive. Being wrong about the design was more expensive still, because unwinding a bad commitment meant throwing away real hours, sometimes weeks. In that world, constraining yourself to small verified steps was rational. You bought information about the problem by building a slice of it, and the tests kept the slice honest. Red-green-refactor was not primarily about catching bugs. It was a discipline for managing ignorance in a regime where ignorance was costly to resolve.

That is a defensible thing. It worked.

It is also not what it was sold as. It was sold as craftsmanship, as professionalism, as the thing separating grown-up engineers from cowboys. The moral framing was necessary because you cannot get a large and varied population to adopt an inconvenient discipline on economic grounds alone. You have to make it a virtue.

And here the trouble starts. Because the practices you adopt as virtues tend to outlive the conditions that made them rational.

## Two kinds of engineering work

There is a kind of engineering that lives close to the keyboard. You take a ticket, decompose it into testable units, grind through the units, ship. Done well, this is a real craft. It rewards discipline, locality of reasoning, patience, and the refusal to get ahead of yourself. A lot of the industry's best-loved practices are variants of this, because this is the kind of work that is most teachable, most measurable, and most amenable to process.

There is another kind of engineering that happens before the keyboard is touched. You sit with an unfamiliar problem and build a correct mental model of it. You notice that two features the stakeholders think are separate are actually the same thing from a different angle. You feel where the boundaries want to be before you commit any code to them. The code, when it eventually gets written, falls out of the model almost incidentally. This kind of work is not teachable in the same way. It is mostly taste.

TDD is excellent training for the first kind and actively hostile to the second. If your native mode is to build the whole model first and let the code fall out, being told to write a failing unit test before you understand the shape is like being told to paint a picture one square inch at a time starting from the corner. It fights the thing you are good at. A lot of engineers who tried TDD and quietly dropped it did so not because they were undisciplined but because the method was interfering with their actual cognitive strength. They then spent the next decade being told, by conference speakers and book authors, that they were doing it wrong.

## What changes now

The thing agentic coding does, which nothing before it did cheaply, is collapse the cost of the first kind of work. Generating code at unit granularity is close to free. Iterating on a draft of an entire feature is an afternoon. The regime in which exploration was expensive, and therefore in which incrementalism was rational, no longer obtains for most problems. You can build the whole thing, throw it away, and build it again with the boundaries in the right place, in the time it used to take to get through a single sprint card.

This does two things at once. It automates the discipline that TDD trained most thoroughly, and it amplifies the judgement that TDD systematically suppressed. The engineer who could hold the whole system in their head, feel where the seams wanted to be, and then direct execution was always the highest-leverage contributor. Now they are increasingly the only contributor whose leverage *grows* with the tooling, because the tooling has absorbed the work the disciplined grinder was paid for.

The uncomfortable corollary: a lot of what the industry canonised as best practice was not best practice in the absolute. It was a set of floor-raising interventions for a large population of varied skill. TDD, enforced patterns, ritualised ceremonies, the whole apparatus: it made mediocre engineers produce acceptable output reliably. That was a good thing when execution was the bottleneck. It is a tax when execution is free.

Every floor-raising intervention lowers the ceiling, because the same constraints that prevent the bottom from collapsing also prevent the top from reaching. You cannot compress the variance in one direction only.

## A caveat, because this is uncomfortable

Rejecting TDD does not make you a holistic thinker. The rare skill I am praising is rarer than either side of the debate wants to admit, and it is not conferred by renouncing a methodology. Plenty of engineers who never wrote a test first are also not thinking at the system level; they have just skipped the discipline without replacing it with judgement. "I don't do TDD" is not a credential. Sitting with an unfamiliar problem long enough to see its real shape is a skill that decays without practice and is not automatically preserved by attitude.

So the point is not that the anti-TDD crowd wins by default. The point is that the skill the methodology was training is being eaten, and the skill it was suppressing is the only one left worth amplifying. Whether you are on the right side of that depends on what you actually do with the hours the tooling frees up.

## The landing

TDD was a coping mechanism for a constraint that no longer binds. The discipline it installed is the discipline being automated. The judgement it discouraged is the judgement being amplified. You can keep paying the tax out of habit, and you will not feel it, because everyone around you is paying it too. Or you can notice that the floor is being handled elsewhere now, and start spending the savings on the ceiling.

The ceiling is all that's left.
