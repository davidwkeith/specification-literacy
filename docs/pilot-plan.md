# Pilot and Evaluation Plan: The De Anza Phase 0 Cohort

This document is the **pilot and evaluation plan** for the first cohort of the Specification Literacy framework. It is the operational companion to two other documents: the framework itself, [`../index.md`](../index.md), and the course outline it evaluates, [`./de-anza-course-outline.md`](./de-anza-course-outline.md). Where the framework sets out the philosophy and the course outline sets out what is taught, this plan sets out how the first run is staffed, consented, measured, debriefed, revised, and handed downward.

---

## 1. Purpose

This is **Phase 0** of the deployment strategy in [`../index.md`](../index.md) §13. The framework argues — at length, in §13.1 and §13.4 — that although specification literacy *develops* bottom-up, from kindergarten through grade 12, the framework that teaches it should be *built and validated* top-down, beginning with adult learners and pushing proven materials down one band at a time. Phase 0 is the first link in that chain: validate the pedagogy with an autonomous adult cohort before any version of it reaches a K-12 classroom.

The **vehicle** is the De Anza College contract / Community-Education course described in [`./de-anza-course-outline.md`](./de-anza-course-outline.md) — eight weekly evening sessions of three hours each (24 contact hours), roughly 70% real workplace specification artifacts at increasing stakes and roughly 30% a running read-and-trace code thread, assessed pass/fail on a verification journal, taught by the framework's author as a volunteer. This plan does not restate that course; it evaluates it.

The **gate this pilot exists to test** is the one stated for Phase 0 in [`../index.md`](../index.md) §13.3: *do adults reliably show the four Verification-Principle behaviors — specify before generating, evaluate against the spec rather than against "seems fine," explain why a verified solution is correct, identify its limits — after a quarter, and do they report that their actual work changed?* If the answer is no — if the behaviors don't take, or take but don't transfer to the participants' jobs — the framework is revised and the pilot is re-run before anything moves downward. Nothing is adapted for high school until Phase 0 has cleared its gate. That sequencing is the whole point of starting here, and this plan is built to produce the evidence the gate requires.

---

## 2. Cohort

**Open enrollment, working professionals, roughly 12–20, mixed fields.** The cohort target matches the course outline's [§7 logistics](./de-anza-course-outline.md): big enough for varied fields and real peer-verification pairings, small enough that one volunteer instructor can read every verification journal and run Session-8 peer verification without it degrading. "Mixed fields" is not incidental — analysts, project managers, paralegals, marketers, engineers, operations staff, clinicians, anyone who already writes specifications to an AI system whether or not they call it that. The cross-domain mix is part of what the pilot is testing: whether the same four behaviors land for a paralegal and a product manager and a clinical coordinator, or whether the course works for some professional shapes and not others.

**Recruitment** runs through De Anza's Community-Education channels — the catalog, the program's mailing list, the standard contract-ed promotion — supplemented by local professional networks: meetup groups, professional associations, alumni lists, word of mouth among working professionals in the region. Registrar copy leads with the second clause of the course title: this is a course about getting AI tools to do what you actually meant, and knowing — before the consequences land — whether they did. (See §7 below: recruitment copy is also where the "this is a thinking course, not a tips list" framing has to be set, and it has to be set there, not corrected later in Session 1.)

**Backup if enrollment is short.** If open enrollment comes in under roughly 12, the fallback is an **employer-sponsored cohort**: a single organization releasing a group of its own staff to take the course together. This is a viable substitute, not a degraded one — an employer cohort brings a built-in shared context and a built-in incentive to apply the field assignments. It also pairs naturally with the alternative course format the outline already describes: the **two-day weekend intensive plus four follow-up weekday evenings** (course outline §1), which suits an organization that can release people for two consecutive days but not for eight consecutive weeks. The default remains open enrollment with the weekly evening format; the employer-sponsored variant is the contingency, triggered by an enrollment shortfall, and it does not change the pedagogy — only the packaging.

---

## 3. Informed Consent / Co-Designer Framing

Participants are told, up front and in writing at registration and again in Session 1, exactly what this is:

- This is a **pilot**. The course is being run for the first time, and they are the first cohort.
- Their **verification journals and feedback**, anonymized, inform the K-12 framework — specifically, the material that will be adapted downward into the high-school and middle-school bands.
- They **may opt out** of having their artifacts used in the evaluation or in any downstream materials, at any time, with no effect on their participation in the course or on a pass/fail outcome.
- **Standard adult-education consent language applies** — voluntary participation, the right to withdraw, anonymization of any quoted material, no penalty for opting out of the research use while still completing the course.

This is not a formality bolted onto the front of the course. It **operationalizes the ethics argument in [`../index.md`](../index.md) §13.2** — the "autonomy and consent" reason for starting at a community college — and the plan says so explicitly. The framework's position is that the "experiment" here is *iteration with consenting co-designers*, not experimentation on people who cannot consent. Adults enroll voluntarily, can drop a course they find unhelpful, can push back on an exercise that misses, and can give informed feedback as peers rather than as subjects. That is precisely why the program begins here and not in a kindergarten classroom: the obligation owed to a child who cannot say no is discharged by getting the pedagogy right — with adults who *can* say no — before it ever reaches the child. The co-designer framing is not a courtesy; it is the mechanism by which the framework moves fast without moving fast on anyone unable to object. The instructor's stance toward the room follows from this: participants are treated as co-designers (course outline §10.5 of [`../index.md`](../index.md), "Teacher's role"), bringing real artifacts from their jobs and shaping the course as they go, not as recipients of finished content.

**What consent specifically covers:**

- Use of **anonymized excerpts from the verification journals** — quoted specs, gaps, traces, revisions — in evaluation write-ups and in materials for later bands.
- Use of the **sanitized artifact catalog** (see §4, *Pedagogy data*) as example material for the high-school and middle-school bands — that is, the redacted workplace artifacts participants bring, stripped of identifying and confidential content and organized for downstream use.
- Use of **pre/post survey responses**, in aggregate and (for short-answer items) as anonymized quotations.
- The **right to participate fully in the course while opting out of all of the above** — to take every session, do every field assignment, submit a complete journal, pass, and have none of it used for anything beyond the course itself.

Opting out is per-item, reversible, and recorded at registration with a reminder in Session 1. A participant who opts out of artifact use can still bring real artifacts to work on in class; the opt-out governs *downstream use*, not *in-class use*.

---

## 4. Success Criteria

There are three kinds of evidence, and Phase 0's gate is cleared only when all three point the same way.

### 4.1 Behavioral — the four Verification-Principle behaviors

By the end of the quarter, can participants **reliably**:

(a) **Specify** — write a spec with explicit success criteria *before* anything is generated, rather than asking for output and accepting whatever comes back;
(b) **Evaluate** — check generated work against that spec, claim by claim and criterion by criterion, rather than against "seems fine" / "looks reasonable";
(c) **Explain** — say why a verified solution is correct, with a real trace for the code-thread entries (a finger on the page, an argument that covers all the cases), not merely observe that it works;
(d) **Identify limits** — name the preconditions the solution requires, the cases it does not handle, the tradeoffs it embodies, and who the result is and is not correct for.

These are the four Verification-Principle behaviors of [`../index.md`](../index.md) §4 — *specify, evaluate, explain, identify limits* — and they are the same four the course outline is built to develop and assesses on. Behavioral success is scored from the **verification journals** (one entry per field assignment, in the [per-entry template](./de-anza-course-outline.md) the course outline §4 specifies) plus the **Session-8 capstone** (a real before/after with the spec revision and the verification on the record), against a simple rubric. The rubric is below, inline, because "a simple rubric" should be exactly that — four rows, two levels, one line each.

| Behavior | Demonstrated | Not yet demonstrated |
|---|---|---|
| **1. Specify** | At least one journal entry (and the capstone) shows a spec written *with explicit, checkable success criteria* before anything was generated — the artifact was rewritten from "give me output" into "give me a thing that meets (a), (b), (c)…". | Specs are still requests for output; success criteria are absent, vague ("make it good"), or written after the fact. |
| **2. Evaluate** | At least one entry shows the generated result checked *against the spec* — criterion by criterion, with the places it met, missed, or exceeded the spec named — not waved through on "looks reasonable." | Verification consists of "I read it and it looked fine"; no comparison to stated criteria; gaps, where noted at all, are noted impressionistically. |
| **3. Explain** | At least one entry — the code-thread trace is the natural home, but a document entry can carry it — shows *why* the correct result is correct: a trace that covers the cases, or a mechanism-level argument, not "it ran" / "the AI is usually right." | The participant can say *that* the result is correct but not *why*; "the AI wrote it" or "it passed my spot-check" stands in for an account of the mechanism. |
| **4. Identify limits** | At least one entry names the preconditions, the un-handled cases, the tradeoffs, and — for the bias/defaults work (course outline Session 7) — who the result is and is not correct for. | Limits, preconditions, and "correct for whom" go unmentioned; the result is treated as correct full stop. |

Scoring is **pass/fail per behavior**. The course's pass condition, from the course outline §4, is **all four behaviors demonstrated across the journal as a whole, plus the capstone delivered** in Session 8. For the *pilot*, the unit of analysis is the cohort: Phase 0's behavioral gate is met when the great majority of participants who complete the course clear all four — not a token few. A cohort where most people demonstrate one or two behaviors but not all four is a signal to revise the course, not to declare the gate cleared.

### 4.2 Self-report / transfer — a pre/post survey

A short survey administered at Session 1 (pre) and after Session 8 (post). The point is not satisfaction; it is **transfer** — whether the disposition shows up in the participant's actual work. Items below are the instrument, not a placeholder.

**Likert items** (1 = strongly disagree … 5 = strongly agree; asked both pre and post):

1. I notice when an instruction I write — a prompt, a brief, a ticket, a delegation email — could be read more than one way.
2. When I get AI output, I check it against criteria I set in advance, not just against whether it looks reasonable.
3. When something I delegate or prompt for comes back wrong, my first thought is "what did I leave unsaid?" rather than "the tool/person got it wrong."
4. Work I delegate or prompt for comes back needing fewer revision cycles than it used to.
5. When I sign off on something, I can say *why* it's right, not just that it looked right.
6. I can tell the difference between work I can actually verify and work I can only spot-check — and I treat the two differently.

**Short-answer items:**

7. *(Post only.)* Describe a time in the last month you caught an underspecification in your own work — a prompt, a brief, a clause, a handoff — *before* it caused a problem. What did you notice, and what did you change?
8. *(Pre and post.)* In a sentence or two: what's the most recent time something you asked for — from an AI tool or a person — came back not quite right? What went wrong?

**Recommend item:**

9. Would you recommend this course to a colleague? Why or why not?

The **transfer signal** is: (i) the **pre/post deltas** on the Likert items — items 1–3 measure whether the diagnostic habit took, items 4–6 whether it changed the work; and (ii) the **presence and quality of the post-survey short answers**, especially item 7 — a participant who can produce a concrete, recent instance of catching their own underspecification before it bit them is reporting transfer; a blank or generic answer is not. Item 8's pre-vs-post shift (does the post answer name a *specification* gap where the pre answer named a tool failure?) is a secondary read on the same thing. Item 9's prose answers feed §4.3 below.

### 4.3 Pedagogy data — what landed, and the artifact catalog

Three streams of data about the course as taught:

- **Which sessions and exercises landed and which didn't.** Captured from the instructor's session notes, the recommend-item prose (survey item 9), the Session-8 closing debrief ("what transfers, what you'll keep doing on Monday, and where"), and an optional short mid-course check after Session 4. The question for each session and each in-class exercise: did it do its job, did it run long or short, did it work for the non-technical participants as well as the technical ones?
- **Where the read-and-trace code thread helped and where it confused** — tracked specifically, because the code thread (Sessions 4–5, the ~30% of the course where verification is *provable*) is the part most at risk of alienating the non-technical participants while being, for them, the most novel. The data wanted: did every participant — including the ones who have never written a line of code — get the one solid taste of provable verification the medium is built around (course outline §2)? Where did the trace lose people? Was the scaffolding enough? This feeds directly into the Phase 1 hand-off (§6, item c).
- **A catalog of the real artifacts participants brought** — sanitized, with consent, organized **by domain** (law, marketing, software, operations, analytics, management, …) and **by which Assumption-Audit question they failed** (types / boundaries / defaults / context — the four questions of the adult Assumption Audit, course outline §3, Session 2). This is a **deliverable, not just notes**: a structured collection of redacted real-world underspecification — the prompt that misfired, the brief that produced the wrong thing, the contract clause that got litigated, each with the gap it contained named — that becomes example material for the high-school and middle-school bands. It is the single most important thing Phase 0 produces for the phases below it, and §6 treats it as the primary hand-off artifact.

---

## 5. Iteration Cadence

The cycle is **run → debrief → revise → re-run the next quarter.** After each run: a structured debrief against §4's three streams (behavioral rubric results, survey deltas and short answers, pedagogy data including the artifact catalog), then a revision pass on the course materials, then the next cohort the following quarter. The contract / Community-Education pathway exists precisely so this can happen in consecutive quarters rather than across academic years (course outline §7; [`../index.md`](../index.md) §13.2, "low institutional friction").

**Two or three cycles** before Phase 0 is declared complete and Phase 1 (high school) begins. "Declared complete" means all of:

- **Stable materials** — the session arc, the in-class exercises, the field assignments, the journal template, and the code thread have settled; a revision pass produces tweaks, not redesigns.
- **A cohort reliably hitting all four behaviors** — the behavioral rubric (§4.1) comes back with the great majority of completers clearing all four Verification-Principle behaviors, not a token few, and it does so across cohorts, not in one lucky run.
- **A positive transfer signal** — the §4.2 survey shows real pre/post movement on the Likert items and the post-survey short answers contain concrete, recent instances of participants catching their own underspecification.
- **Evidence that someone other than the author can run it** — this is the real gate, and it is the framework's, not this plan's invention: [`../index.md`](../index.md) §13.3's Phase 1 gate is "high-school teachers can run it without the course author in the room." Phase 0 is not complete until there is evidence the *adult* course transfers off its author — a second instructor, observing and then co-teaching and then teaching a cohort, with the journals, this plan, and the course outline as the transfer mechanism (§7, instructor-dependence). A course that only works because of who is teaching it has not been validated; it has been performed.

---

## 6. Hand-off to Phase 1 (High School)

When Phase 0 clears its gate, **three concrete artifacts flow downward** into the high-school phase:

**(a) The sanitized artifact catalog → high-school examples.** The catalog from §4.3 — redacted real workplace artifacts, organized by domain and by failed Assumption-Audit question — is adapted into the kind of domain-specific, age-appropriate examples that populate [`../index.md`](../index.md) §10.4 (the 9–12 band: "type checking in physics, conservation laws in chemistry, statistical assumptions, design briefs in art, API contracts in computer science"). A litigated "reasonable efforts" clause becomes a worked legal-studies example; an underspecified data pull becomes a statistics or analytics example; a misfired campaign brief becomes a design example. The catalog is the raw material; the high-school phase does the age-adaptation.

**(b) The 8-session arc → compressed for a high-school semester.** The course outline's eight-session arc — gap → Assumption Audit → specifying to an AI that acts → verification I (plausible work) → verification II (when proof is possible) → specifying across people and orgs → bias and defaults → capstone — is the skeleton of the high-school unit, re-paced for a semester rather than an evening-class quarter and re-leveled for adolescents rather than working professionals (formal-operational, [`../index.md`](../index.md) §10.4, not post-formal, §10.5).

**(c) Lessons on the code thread → how much "provable verification" a high-school pilot needs.** Phase 0's pedagogy data on where the read-and-trace code thread helped and where it confused (§4.3) tells the high-school phase how much *provable* verification a high-school pilot should carry, and in what form — read-and-trace as in the adult course, or something nearer the full architect-the-spec model, and at what scaffolding level.

**The De Anza materials are written to be ported down, not redesigned.** The course outline and this plan are built from the start as the upstream source for the bands below; adapting them downward is editing and re-leveling, not reinvention. And the high-school phase does not start from those adapted-down materials alone: it already has [`ap-cs-a-capstone`](https://github.com/davidwkeith/ap-cs-a-capstone) — "The Java Architect Capstone," in which students architect a text-adventure game as a written specification, hand it to a custom AI builder, and must explain every line at a walkthrough, with "the AI wrote it" graded as the lowest band — as an existing, worked high-school instance of the student-as-architect model. So Phase 1's job is to **reconcile** the adapted-down adult course with that capstone into one coherent high-school unit — to merge the two, not to invent from scratch. The adult course supplies the cross-domain artifact catalog and the eight-session diagnostic-to-verification arc; the capstone supplies a proven, AP-aligned, code-anchored project with a working rubric. Phase 1 fits them together.

---

## 7. Risks and Mitigations

| Risk | Mitigation |
|---|---|
| **Low enrollment** — open enrollment comes in under ~12, the floor at which the cohort still has enough field variety and the journals/peer-verification still scale. | Fall back to an **employer-sponsored cohort** — one organization releasing a group of its staff — which brings a built-in shared context and incentive to apply the field assignments. Pair it with the **two-day weekend intensive + four follow-up evenings** format (course outline §1), which suits an organization that can release people for two consecutive days but not eight consecutive weeks. The intensive still gives the field-assignment loop four iterations. |
| **Confidential-data exposure** — participants bring real workplace artifacts, and some of that material is client data, personnel data, unreleased financials, anything under NDA or covered by HIPAA / FERPA / GLBA / attorney-client privilege. | Enforce the course's standing **"bring the real thing, redacted"** rule (course outline §6, §7): keep the structure and the language that made the artifact underspecified, strip the identifying and confidential content. Pair it with **explicit no-paste-into-consumer-AI-tools guidance** and a **check-your-employer's-AI-use-policy instruction** before each session. When in doubt, leave it out and bring a different artifact. The instructor states this in Session 1 and repeats it at every session that calls for brought artifacts. |
| **The read-and-trace code thread alienates non-technical adults** — the ~30% code thread (Sessions 4–5) is, for a paralegal or a marketer, the most foreign part of the course, and it can land as "this isn't for me." | Keep the code thread **≤30% of contact time**, **read-only** (participants trace AI-written code; they never write it — [`../index.md`](../index.md) §6.1), **fully scaffolded** (a short program handed out with the one-paragraph spec it was built from, walked through line by line in the room), with **optional depth** for those who want more. The thread's job is one solid taste of *provable* verification per participant and the felt contrast with the merely-plausible verification that dominates the other 70%; it is not a coding course inside the course, and it is framed that way. Track in the pedagogy data (§4.3) whether every participant actually gets that taste. |
| **The "this is just prompt-engineering tips" misperception** — recruits and participants expect a list of tool tricks, treat it as one, and miss that it is a thinking course. | Lead **recruitment copy and Session 1** with the [`../index.md`](../index.md) §3 framing — AI makes underspecification *visible*; this is a course about the precision of your own thinking and how you know whether you got what you meant — **not** with tool tricks. Session 1 is the Adult Sandwich Challenge (course outline §3, Session 1): everyone watches their own "clear" prompt diverge from what they meant, and the word on the whiteboard is *unconsciously*. The course is positioned as the workplace instance of a K-12 framework, not as a productivity webinar; the registrar copy and the first hour both have to carry that, because it cannot be corrected later. |
| **Instructor-dependence** — only the author can teach it, so it never scales and never reaches the bands below. | Treat the transfer mechanism as a deliverable, not an afterthought: the **verification journals**, **this plan**, and the **course outline** together document what the course is and how it is run, in enough detail for a second person to run it. "A second person can run it" is an explicit **Phase 1 gate** ([`../index.md`](../index.md) §13.3 — "high-school teachers can run it without the course author in the room") and is built into §5's definition of "Phase 0 declared complete": a second instructor observes, then co-teaches, then teaches a cohort, before the framework moves downward. A course that only works because of who teaches it has not been validated. |

---

## 8. Cross-References

- [`../index.md`](../index.md) — the Specification Literacy framework. Most-cited sections here: **§3** (why algorithms / AI makes underspecification visible — the Session-1 and recruitment framing), **§4** (the Verification Principle and its four behaviors — the spine of the behavioral success criteria), **§10.4** (the 9–12 band — the target shape for the adapted-down examples), **§10.5** (Band 5: Adult Learners — the band this whole pilot instantiates), **§13** (Deployment: Where to Start — this pilot is its Phase 0; §13.2 supplies the consent/ethics argument, §13.3 the phase gates).
- [`./de-anza-course-outline.md`](./de-anza-course-outline.md) — the course this plan evaluates. Cited here for its **§1** (format, including the 2-day-intensive variant), **§3** (the session arc and the four Assumption-Audit questions), **§4** (assessment — the verification journal, the per-entry template, the pass condition), **§6** (AI access, the no-paste rule), and **§7** (logistics — cohort size, pathway, instructor).
- [`ap-cs-a-capstone`](https://github.com/davidwkeith/ap-cs-a-capstone) — "The Java Architect Capstone," the existing worked high-school instance of the student-as-architect model that Phase 1 must reconcile the adapted-down adult course with (§6).
