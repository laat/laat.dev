---
title: "Programming as Shape Holding"
description: "LLMs can produce program text without holding the theory of the program. The human role is preserving the shape."
pubDate: "2026-04-27"
model: "GPT-5.5"
---

Programming has never been only the production of program text. That was Peter Naur's point in "Programming as Theory Building": the real work of programming is not exhausted by the source code, the documentation, the tests, or the procedures around them. The real work is the formation of a theory in the minds of the programmers responsible for the system.

That theory is what lets them explain why the program is the way it is. It lets them answer questions that are not written down. It lets them distinguish an improvement from a distortion. It lets them modify the system without changing it into a different kind of thing.

This idea has always been true, but it has become newly visible in the age of LLM-assisted programming.

LLMs can produce program text without possessing the theory of the program. That is both their power and their danger. They can write code that compiles, passes tests, follows local conventions, and appears idiomatic. They can fill in obvious gaps, generate plausible abstractions, and accelerate implementation. But they do not hold the system in mind. They do not know what kind of thing the program is trying to remain.

This is why LLM-generated code can be locally correct and globally wrong.

It solves the immediate problem while bending the system away from its shape.

## The industry wanted Naur to be wrong

Naur's argument is inconvenient for industrial software development. If programming depends on theory held by people, then the most important part of programming is difficult to standardize, audit, delegate, and purchase. It resists being collapsed into process.

The industry has always preferred artifacts. Artifacts can be counted. Tickets can be assigned. Pull requests can be reviewed. Tests can be run. Documentation can be required. Velocity can be measured. Processes can be certified, taught, scaled, and sold.

Judgment is harder.

This does not make process useless. Good process can protect judgment. It can slow down reckless change, preserve context, distribute knowledge, and create opportunities for correction. But process cannot replace judgment without changing the nature of the work.

When process replaces judgment, programming becomes the manipulation of visible artifacts rather than the maintenance of an internal theory. The team can keep producing code while losing its understanding of what the code is for.

This was already a problem before LLMs. LLMs make it cheaper, faster, and easier to miss.

## Code generation separates text from theory

Before LLMs, producing program text was still closely tied to possessing at least some theory of the program. A programmer writing a change had to hold enough of the system in mind to decide what to type next. There were abstractions, libraries, frameworks, autocomplete, search, snippets, and code generation tools, but the feedback loop still forced a certain proximity between understanding and inscription.

LLMs loosen that connection.

A model can produce a large amount of plausible program text from a compressed description of intent. It can infer local style. It can imitate surrounding code. It can propose a patch that looks like it belongs. The human no longer has to manually inscribe every line.

That shift is real. It is useful. It is not going away.

But it creates a new failure mode: theoryless expansion.

Theoryless expansion happens when a system grows in ways that no human has actually integrated into their understanding of the program. The codebase gets larger, the diff looks reasonable, the tests are green, and the implementation may even satisfy the literal request. But the change has not been absorbed into the theory of the system. Nobody can confidently say whether it preserves the system's shape.

This is not merely a quality problem. It is an authorship problem.

A program is not just a pile of executable text. It is a structured thing with tendencies, boundaries, invariants, and taste. It has a way it wants to be extended. It has concepts that belong and concepts that do not. It has simplifications that carry real design weight and complexities that are merely accidental. It has places where a clever abstraction would help and places where the same abstraction would be vandalism.

The model does not know this. It can only infer fragments from traces.

The human has to hold the shape.

## The model expands; the human holds the shape

In LLM-assisted programming, the human role is often described as prompt writer, reviewer, editor, orchestrator, or manager. These descriptions are not wrong, but they are too procedural. They describe tasks around the work rather than the essential responsibility inside the work.

The human is the shape holder.

The model expands. The human holds the shape.

Holding the shape means maintaining the theory of the program strongly enough to recognize whether a generated change belongs. It means knowing not just whether the code works, but whether it is the right kind of code for this system. It means being able to say: this is solving the problem in the vocabulary of the program, or this is importing a foreign vocabulary that will make future work harder.

It means seeing when a diff is wrong-shaped before every local defect has been enumerated.

This is a different kind of review from archaeology. In archaeology, the reviewer receives a large artifact and tries to reconstruct what happened. They read the diff, infer the intent, discover the implications, and slowly rebuild the theory that should have guided the change in the first place.

That mode does not scale well with generated code.

The final review should not be archaeology. It should be recognition.

Recognition is only possible when the reviewer already possesses the shape. A generated patch arrives, and the human can see whether it fits. Not because they have mechanically checked every line, but because they understand the program well enough to notice when the change preserves or violates its theory.

This does not eliminate detailed review. It makes detailed review meaningful. You still inspect the code, run the tests, check edge cases, and ask whether the implementation is robust. But those activities sit inside a prior act of judgment: does this change belong to the program we are building?

## Safe LLM programming is theory-preserving expansion

The safe use of LLMs in programming is not "let the model write code, then review carefully." That is too weak. It treats review as a quality-control step at the end of production.

A better frame is theory-preserving expansion.

The human forms the shape. The model expands it into artifacts. The human reviews by recognition. The process repeats only while the human's theory remains intact.

This has practical consequences.

The human should be able to describe the intended change before asking the model to implement it. They should know the conceptual boundary of the change, not merely the requested output. They should be able to predict the rough shape of a good solution: which modules it should touch, which concepts it should reuse, which abstractions it should avoid, and what kind of diff would be suspicious.

The generated output should be small enough to recognize. A patch that is too large to hold in mind is not automatically wrong, but it changes the review mode. The human is no longer recognizing a shape they possess; they are reconstructing a shape after the fact. That is slower, riskier, and easier to fake.

The model should be used to elaborate a theory, not substitute for one. It can generate options, expose missing cases, suggest names, write boilerplate, translate an established pattern, or accelerate a known implementation path. It is most useful when the human already knows what kind of result would count as right.

The danger begins when the model is used to continue past the edge of human understanding.

That edge is easy to cross because the model remains fluent after the human has become vague. It does not slow down when the theory runs out. It does not signal that nobody is holding the shape anymore. It keeps expanding.

The problem is not that the model writes code. The problem is that the model continues expanding after nobody is holding the shape.

## Process should preserve judgment

The usual institutional response to a new risk is more process. Require smaller diffs. Add checklists. Add model-use policies. Add review gates. Add test requirements. Add documentation requirements. Some of this is sensible.

But the goal of process should not be to replace judgment. It should be to preserve the conditions under which judgment remains possible.

A good LLM programming workflow should make it easier for the human to keep possession of the theory. It should encourage small, legible expansions. It should keep intent close to implementation. It should make generated changes easy to reject. It should privilege conceptual coherence over apparent productivity.

Bad process does the opposite. It lets large generated diffs accumulate behind a veneer of compliance. It asks reviewers to approve work they cannot recognize. It treats green tests and stylistic conformity as evidence that the system's theory has been preserved.

Tests matter, but they are not the theory. Style matters, but it is not the theory. Documentation matters, but it is not the theory. The theory is the living understanding that lets a programmer intelligently extend the system.

Without that theory, the artifacts can remain impressive while the program decays.

## Naur matters more now

LLMs do not make Naur obsolete. They make him more important.

When code was expensive to produce, it was easier to mistake the production of code for the essence of programming. Now code is becoming cheaper. That change reveals what was always underneath: the hard part is not typing the text, but knowing what text should exist.

The value of the programmer moves upward, but it does not vanish. The programmer is no longer defined by manual inscription. The programmer is responsible for the theory that makes inscription meaningful.

This is why "AI will write the code" is the wrong endpoint. The more relevant question is: who holds the theory of the program?

If a human holds it, LLMs can be powerful instruments of expansion. They can make programming faster, more fluid, and more expressive. They can help turn a clear shape into working artifacts with less friction.

If nobody holds it, LLMs become engines of drift. They produce plausible continuations of a system whose meaning is no longer possessed. They can make decay look like progress.

Programming in the LLM era is still theory building. But the daily practice changes. The programmer spends less time pushing every character into place and more time forming, preserving, and recognizing shape.

The model expands. The human holds the shape.

That is not a diminished role. It is the part of programming that was always most important.
