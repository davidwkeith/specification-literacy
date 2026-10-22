# Specification Literacy

**A K–12+ framework for teaching specification literacy: the discipline of describing problems precisely enough that any interpreter, human or machine, will produce the same result.**

As AI systems become general-purpose interpreters of human intent — generating code, drafting documents, making decisions — everyone who works with them is, knowingly or not, writing specifications. The gap between what a person *means* and what they *specify* is where failures occur, and it is invisible from the inside: the author of an underspecified description does not believe they have been ambiguous. This project argues that **specification literacy** — the ability to find and close that gap — belongs alongside reading, writing, and numeracy as a foundational literacy, and shows how it can be developed across every grade band and into adult professional life.

## The core idea

The same failure pattern recurs across law, science, and engineering: an author produces a description they believe is complete, it contains an ambiguity they never noticed, an interpreter resolves it differently than intended, and the divergence only surfaces once consequences land — a lawsuit, an irreproducible result, a destroyed spacecraft. Mature disciplines have each built systematic practices for catching this before it ships. The framework names the underlying skill, traces how it develops from kindergarten upward, and proposes teaching it explicitly.

Two ideas anchor the framework:

- **The Verification Principle** — the output is the beginning, not the end. Whether the interpreter is an AI, a classmate, or a contractor, your job is to check whether the result matches what you meant and figure out why it didn't. In its formal form: *specify, generate, trace, compare, explain, find the limits.*
- **Develop bottom-up, deploy top-down** — the disposition matures in a person from early childhood up, but the curriculum is built and validated in the opposite order, starting with consenting adult learners where the feedback loop is shortest, then pushing proven materials down one band at a time.

## What's in this repository

| File | What it is |
|------|------------|
| [`index.md`](index.md) | The main framework document — the philosophical case, the underspecification problem, the four K–12 developmental bands plus an adult band, cross-curricular integration, a practical guide for any teacher, and the top-down deployment strategy. |
| [`docs/de-anza-course-outline.md`](docs/de-anza-course-outline.md) | *Problem Architecture for Working Professionals* — the adult anchor course outline for a De Anza College contract-education cohort. |
| [`docs/pilot-plan.md`](docs/pilot-plan.md) | Pilot and evaluation plan for the De Anza Phase 0 cohort. |
| [`docs/specs/`](docs/specs/) | Design documents for major additions to the framework. |
| [`docs/plans/`](docs/plans/) | Implementation plans corresponding to those designs. |

## The developmental progression

The through-line, from kindergarten through working life, is: **how precisely can you describe what you mean, and how do you know whether what happened matches what you meant?**

| Band | Capacity | Verification question |
|------|----------|------------------------|
| K–2 | Notice the gap between intention and result | "Did it come out the way you wanted?" |
| 3–5 | Write multi-step instructions and test them | "Did someone else get the same result from your steps?" |
| 6–8 | Systematically audit assumptions and categorize failure modes | "What kinds of gaps should you look for?" |
| 9–12 | Apply formal specification methods within each discipline | "What does this domain's notation leave unspecified?" |
| Adult / Continuing Ed | Specify, delegate, and verify under real stakes | "When I hand this off and it acts for me, how do I know — before the consequences land — that it did what I needed?" |

The 6–8 band is formalized in an anchor course, *Introduction to Problem Architecture: Specification Literacy Through Algorithms and AI*, in which AI generates all code and students specify, trace, verify, and explain it.

## Status

This is a draft framework document (v3, April 2026). The first real-world instance is a Phase 0 adult cohort at De Anza College; see the pilot plan for the evaluation design.

## License

[CC0 1.0 Universal](LICENSE) — dedicated to the public domain. Copy, adapt, translate, and teach from it, for any purpose, without asking or crediting.
