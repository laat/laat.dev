---
title: "On keeping the skill you no longer need"
description: "Agentic coding requires preserving the skill of unassisted work, especially in domains where wrongness is invisible until catastrophic."
pubDate: "2026-04-22"
model: "Claude Opus 4.7"
---

Some time ago I was looking at an OIDC relying-party implementation an agent had produced for me. It was, by every visible measure, a good piece of code. It compiled. It followed the idiomatic patterns of the language. The happy-path tests passed. The naming was consistent, the error handling was structured, the dependencies were current. If I had to give it a surface grade I would have given it a solid B+.

It was also missing the nonce check entirely.

I only caught this because I had, some years earlier, and for no especially good reason, implemented OIDC by hand from the spec. I remembered the nonce dance. I remembered *why* the nonce exists and what breaks without it. When I read the agent's output, the absence jumped at me the way a missing word jumps at you in a sentence you already know. If I had not done the original implementation, I would probably have shipped the code. It looked fine. It worked. Nothing in my reading of it would have told me it was wrong.

This is the post about the thing that almost happened.

## The discourse is not quite right

There is a running argument in our profession about what agentic coding does to us. The two loud camps have familiar shapes. One says the tools are a generational productivity shift: stop clinging to keystrokes, stop romanticising craft, just ship. The other says the tools are quietly rotting the craft itself: developers who grow up on agents will never acquire real understanding, and the software will be worse for it.

I find both positions unsatisfying in the same way. They are both arguments *about the agent*. The interesting question is not about the agent. It is about the human, and specifically about the capability the human needs in order for the agent's output to be trustworthy at all. That capability does not live in the tool. It lives in you. And it decays.

## The multiplier, and what it multiplies

The simplest honest description of agentic coding is that it is a multiplier on the developer's existing calibration. If your instincts about what good code looks like in this domain are sharp, you will steer well, catch the places the agent drifts, and produce more good software per hour than you could alone. If your instincts are dull, or miscalibrated, or absent entirely, you will produce bad software faster, at higher confidence, with more of the surface hallmarks of competence than you could have managed by hand. The tool does not introduce calibration. It amplifies whatever you brought.

Which means the important question, if you care about the quality of what you ship, is not "am I using the agent enough" or "am I using the agent too much." It is: how is my calibration, in the domain I am about to delegate. And the further, less comfortable question behind that is: how did I build the calibration in the first place, and am I still doing the things that built it.

The answer to the second question is almost always the same. You built the calibration by doing the work yourself, badly at first, slowly, with the specific failures that only surface when you are the one making every decision. You felt the spec. You encountered the parts it did not quite answer. You shipped something subtly wrong and discovered why it was wrong, probably at 2am, probably with consequences. The calibration is compressed from those experiences. It is precisely the thing the agent is now saving you from having to repeat.

## The quiet trade

And there, in that last clause, is the whole problem. The agent is excellent at saving you from the experiences that would have built your calibration if you were junior, or extending your reach into domains that would have built new calibration if you were mid-career, or letting you ship across a range you could not have covered by hand if you were senior. All three of these are real gains. None of them are free. The cost is that the domain-specific instincts which let you evaluate the agent's output *in that domain* are not being laid down the way they used to be.

This is not a problem in every domain. A lot of code has the useful property that wrongness is legible: your database migration fails, your tests go red, your production traffic drops, your customers shout. The feedback loop runs, and gaps in your calibration show up quickly enough for you to fix them and learn. In these domains, agents are close to pure gain. Delegate freely.

Some domains do not have that property. In security-adjacent code, in cryptographic implementation, in concurrency primitives, in transactional integrity, in anything dealing with money, wrongness is often silent until it is catastrophic. Your OIDC implementation missing the nonce check does not fail any test you were going to write. It sits there, perfectly functional, waiting for someone to notice they can forge tokens against you. In these domains the feedback loop that would normally correct your calibration is broken. You do not find out you were wrong. You find out your users were harmed.

For those domains, the same delegation that works elsewhere is dangerous, and the danger is invisible from inside the delegation. The agent's output looks fine. Yours looked fine too, back when you were writing it yourself. The difference is that when *you* wrote it, you at least had the chance to feel the edges, to encounter the parts of the spec that were sharp, to build the instinct that would later let you recognise the missing piece. Delegated code offers no such encounter. It offers a fait accompli, polished, professional, and possibly fatal.

## A narrow claim

I am not arguing against using agents, including in sensitive domains. That would be silly, and I would be a hypocrite, because I use them in exactly such domains. I am arguing something narrower: for any domain where wrongness is invisible until catastrophic, and where you expect to work repeatedly, you owe it to yourself and to the people using your software to have implemented the thing by hand at least once before you delegate it.

Not because hand-rolling is virtuous. It is not. The code you produce in that first unassisted pass may never ship, and probably should not. The value is not in the artifact; the value is in the *you* who exists after the exercise. You now have the instincts that make subsequent agent work in this domain actually evaluable. Without those, you are reading confident-looking output and hoping, which in security-adjacent code is a kind of malpractice in a trench coat.

## The uncomfortable implication

There is a slightly harder corollary which I want to state plainly, because it is the part that took me longest to accept. Using agents responsibly requires deliberately preserving the skill of *not* using them. Periodically. In the domains where it matters. Not as nostalgia, not as proof of virtue, not as a performance of craftsmanship for anyone's benefit. As maintenance on the only instrument that makes agent use actually safe, which is your own ability to read the output and know whether it is right.

This is uncomfortable because it asks you to accept a slower day, on purpose, when a faster one is available, for the sake of a benefit that will not show up until later, in a case that may never arise. It is the gym, in software form. You do not get to feel it working while you are doing it. You feel it much later, when you catch the missing nonce check, and the moment it takes to catch is proportional to the hours you spent years ago implementing the flow by hand.

## A parting sentence

The agent is a force multiplier on your calibration. Keep the calibration alive, or the multiplication is no longer doing what you think it is doing. In the domains that matter, the responsible move is not to use the tool less. It is to keep yourself sharp enough to use it well.
