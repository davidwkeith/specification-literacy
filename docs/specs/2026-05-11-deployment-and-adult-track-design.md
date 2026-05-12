# Design — Deployment Strategy & the Adult / Continuing-Education Track

**Date:** 2026-05-11
**Status:** Approved (brainstorming complete; implementation plan to follow)
**Author:** David W. Keith
**Affects:** `index.md` (Specification Literacy framework, Draft v3) and two new operational documents.

**Reference artifact:** [`davidwkeith/ap-cs-a-capstone`](https://github.com/davidwkeith/ap-cs-a-capstone) — "The Java Architect Capstone," an existing high-school AP CS A capstone in which students architect a text-adventure game as a written spec ("blueprint"), hand it to a custom AI builder, then verify and iterate, with a walkthrough where they must explain every line ("the AI wrote it" is graded lowest). It is a concrete, already-built worked example of: the Verification Principle (§4), the Sandwich Challenge made visceral ("students who rush the blueprint get broken games"), and the "post-AP capstone" idea gestured at in `index.md` §9 and §10.4. It is referenced below in the deployment plan (the HS phase does not start from zero) and the De Anza course outline (its spec → AI-builds → explain-everything structure is a template for the adult course's read-and-trace thread).

---

## 1. Problem & Motivation

`index.md` presents Specification Literacy as a **K–12 developmental framework**: four developmental bands (K–2, 3–5, 6–8, 9–12) plus one fully-built anchor course at 8th grade. It argues persuasively that the disposition *develops* from kindergarten upward, but it says nothing about two things the author now wants on the record:

1. **The progression doesn't stop at grade 12.** Working adults are, right now, writing specifications to AI systems with no training in doing so. The framework's own thesis (§1, §8.3 — "a population that cannot specify what it wants from AI will get whatever the developers specify for it") applies most acutely and most urgently to adults already in the workforce. There needs to be a fifth band.

2. **The developmental order is not the deployment order.** Although the skill develops bottom-up, the framework should be *built and validated* top-down — starting with **community college / adult learners**, then pushing the validated materials down one band at a time (HS → MS → elementary → K). Adults enroll voluntarily, can opt out, push back, and give informed feedback; the verification feedback loop closes in a quarter rather than the ~13 years a K cohort takes to mature; and contract / continuing-ed launches without curriculum-committee approval. We learn fast *and* ethically before anything reaches a child who cannot consent.

The author intends to teach the first instance of this — a contract / Community-Education cohort at **De Anza College** — as a volunteer, using an open-enrollment cohort of working professionals from mixed fields.

## 2. Goals & Non-Goals

**Goals:**

- Add a fifth developmental band ("Adult Learners — Specification Under Stakes") to `index.md` §10, in the existing voice and structure of bands 1–4.
- Add a deployment-strategy section to `index.md` that names and resolves the developmental-order-vs-deployment-order tension, argues "why community college first," and lays out the top-down rollout sequence with a gate between phases.
- Produce a full, teachable course outline for the De Anza contract-ed cohort — the adult parallel to the 8th-grade "Introduction to Problem Architecture" anchor course.
- Produce a pilot & evaluation plan: cohort, informed consent, success criteria, iteration cadence, and how findings hand off to the high-school phase.

**Non-Goals:**

- Not rewriting the K–12 bands or the 8th-grade anchor course (only a one-sentence forward-pointer is added to §10's intro).
- Not designing the HS / MS / elementary / K rollout phases in detail — the deployment section sketches the sequence and gates; each later phase gets its own spec when its time comes.
- Not building a for-credit Course Outline of Record, SLOs, or curriculum-committee paperwork — the pilot runs through the contract / Community-Ed pathway specifically to avoid that.
- Not splitting the adult band into sub-bands (traditional-age CC students vs. career-changers vs. mid-job reskillers) — treated as one band.

## 3. Approach (chosen: "mirror the existing seam")

The framework already keeps *philosophy* in `index.md` and *operational artifacts* (the week-by-week 8th-grade course) "documented separately." The extension follows the same seam:

1. **Thin additions to `index.md`** — a new Band 5 in §10 and a new deployment section — written in the framework's existing voice.
2. **A standalone De Anza course outline** (`docs/de-anza-course-outline.md`) — the adult parallel to the separately-documented 8th-grade anchor course.
3. **A standalone pilot & evaluation plan** (`docs/pilot-plan.md`) — operational, not philosophical.

Approaches considered and rejected: (A) one big standalone "deployment & adult track" doc — rejected because the deployment *argument* belongs in the framework's voice inside `index.md`; (B) everything bolted into `index.md` — rejected because a week-by-week syllabus breaks the "this is a framework, not a curriculum" tone the document maintains.

## 4. Detailed Design

### 4.1 `index.md` — new Band 5 in §10

Insert after the current §10.4 as **§10.5 "Band 5: Adult Learners — Specification Under Stakes."** Renumber the current §10.5 "The Through-Line" to §10.6, and add a fifth row to its summary table. Add one sentence to the §10 intro acknowledging the post-secondary band and noting that *deployment* runs top-down (forward-pointer to the new deployment section).

Band 5 follows the exact structure of bands 1–4:

- **Central cognitive operation:** Writing, delegating, and verifying specifications in real organizational contexts — where the interpreter (an AI, a colleague, a vendor) acts on your behalf with autonomy, and the cost of underspecification lands immediately on you.
- **Developmental stage:** Post-formal / pragmatic reasoning. Adults can hold that a specification is *simultaneously* precise and negotiated, that "correct" is stakeholder-dependent, and that specs are revisable artifacts. The catch: deep domain expertise comes with *low* meta-awareness of one's own tacit assumptions — the expert's curse. The pedagogical opportunity is that the expertise *is* the underspecification.
- **What specification literacy looks like at this stage:** No grades, no teacher resolving ambiguity — the stakes are intrinsic (their actual work improves or doesn't). Verification question: *"When I hand this to an AI that will act on it, how do I know — before the consequences land — that it did what I needed?"*
- **Cross-domain manifestations** (parallel to §10.4's list, at workplace stakes): prompting an LLM is spec-writing — the Sandwich Challenge at work; "summarize this for the board" — for whom, deciding what?; AI-assisted contract review and e-discovery — "relevant" is the new "room temperature"; tickets / PRDs / acceptance criteria; campaign briefs vs. "make it pop"; "pull our top customers" — top by what, over what period, excluding what; RFPs / SOWs / "reasonable efforts" (§10.4's legal-studies content, now lived); **delegating to a person is writing a spec** — the manager surprised by the result has an underspecification problem, not a bad employee; civic/personal with adult stakes — insurance claims, disputing a bill, instructing a contractor.
- **Teacher's role:** Surface the expert's buried assumptions ("you said 'obviously the Q3 numbers' — obvious to whom?"). Treat learners as **co-designers**: they bring real artifacts from their jobs; the class works on those.

### 4.2 `index.md` — new deployment section

Insert as **§13 "Deployment: Where to Start"**; the current §13 "Conclusion" becomes §14. (Note for implementation: the document's footnote anchors and any cross-references to §13 must be updated.)

Contents, in the framework's voice:

1. **The developmental order is not the deployment order.** Spec literacy *develops* bottom-up (K → 12 → adult). The framework should be *built and validated* top-down. This paragraph names the tension explicitly and resolves it.
2. **Why community college specifically — four reasons:**
   - *Urgency.* The labor market is repricing skills now; the people who need this *this year* are working adults, and the open-access, workforce-facing institution that serves them is the community college.
   - *Autonomy & consent.* Adults enroll voluntarily, can drop, push back, and give informed feedback. Piloting a new pedagogy on minors raises consent, equity, and IRB concerns an adult cohort sidesteps — we iterate fast *and* ethically before anything reaches a child who can't consent. (This is the "easier to experiment with adults" intuition, stated responsibly: "experiment" → "iterate with consenting co-designers.")
   - *Tight feedback loop.* Adults bring real work artifacts, so the §4 verification loop closes in a quarter, not the ~13 years a K cohort takes to mature.
   - *Low institutional friction.* Contract / continuing-ed launches without curriculum-committee approval, so you can run-revise-rerun in consecutive quarters.
   - Names **De Anza College** as the concrete first instance.
3. **The top-down sequence, with a gate between phases:**
   - **Phase 0 (now):** De Anza contract-ed pilot, open professional cohort. *Gate:* do adults reliably show the four Verification-Principle behaviors after a quarter, and report that their work changed?
   - **Phase 1:** Adult track scales (more sections, employer cohorts, a transfer-credit version) *and* high-school pilots begin — the §10.4 band already exists, and the HS phase does **not** start from zero: [`ap-cs-a-capstone`](https://github.com/davidwkeith/ap-cs-a-capstone) is an existing worked HS instance (architect a spec → an AI builds it → students verify and must explain everything at a walkthrough). The De Anza materials adapt *down* to HS, the nearest neighbor, alongside that capstone as a template. *Gate:* HS teachers can run it without the course author present.
   - **Phase 2:** Stand up the already-designed 8th-grade anchor course (§10.3), using lessons from the HS pilots. This is where the "named introduction" lands, as the framework already says.
   - **Phase 3:** Elementary (3–5): the §12 "practices that cost nothing" become a structured strand; train elementary teachers (some of whom came through the adult track).
   - **Phase 4:** K–2: by now there's a decade of materials, a trained-teacher pipeline, and evidence; the kindergartner who draws a different house meets a teacher who knows exactly what's happening.
   - Each phase feeds the next — adult learners who are also teachers and parents carry the disposition downward — so **the pilot cohort is itself part of the rollout mechanism.**
4. **Why not bottom-up (addressing the obvious alternative):** Start in K and the first beneficiaries graduate in ~13 years — the AI transition won't wait; bottom-up also experiments on those least able to consent, with the longest feedback loop and the hardest approval path (state standards, textbook adoption). Top-down de-risks all of it.

### 4.3 `docs/de-anza-course-outline.md` — the adult anchor course

The adult parallel to "Introduction to Problem Architecture" (§10.3). Title to be finalized; candidates: *"Problem Architecture for Working Professionals: Specifying, Verifying, and Directing AI at Work"* or *"Specification Literacy: Telling AI What You Actually Mean."*

- **Format:** De Anza runs on quarters; this is a contract / Community-Ed cohort of working adults → **8 weekly evening sessions × 3 hours = 24 contact hours**, each with a between-session **field assignment** (apply it at your actual job; bring back the artifact). Alternative noted in the doc: a 2-day intensive + 4 follow-up evenings.
- **The medium problem and its solution:** The 8th-grade course uses five sorting algorithms because algorithms give immediate feedback, permit *formal* verification, and make underspecification visible (§3). Adults aren't all coders, so the medium can't be "five sorting algorithms." Instead: **~70% real workplace specification artifacts** of increasing stakes (prompts → briefs → tickets/PRDs → contracts/SOWs) **+ ~30% one running read-and-trace code thread** (per §6.1: trace only, never write) so every adult gets at least one taste of *provable* verification — and feels the contrast with the merely-plausible verification that dominates their work. The code thread adapts the structure of the [`ap-cs-a-capstone`](https://github.com/davidwkeith/ap-cs-a-capstone) project — architect a spec, an AI builds it, you must be able to explain every line — scaled down to read-and-trace (adults read and verify AI-generated code; they do not write it).
- **Session arc:**
  1. **The gap.** Adult Sandwich Challenge — everyone writes a real prompt / delegation email, runs it, we examine the divergence; name underspecification; introduce the Verification Principle. *Field:* bring a real prompt/brief/ticket from work that "didn't quite work."
  2. **The Assumption Audit, adult version.** §10.3's diagnostic re-aimed: *types* (what kind of thing did I ask for?), *boundaries* (how much, by when, for whom?), *defaults* (what did I leave the interpreter to pick?), *context* (what do I know that I didn't say — the expert's curse). Worked on participants' brought artifacts.
  3. **Specifying to an AI that acts.** Prompts as specs; system / standing instructions as standing specs; asking for *output* vs. asking for *a thing that meets criteria*; acceptance criteria. *Field:* rewrite your artifact as a spec with explicit success criteria; run it; journal the gap.
  4. **Verification I — checking plausible work.** Evaluating an AI-generated document / analysis / plan against your spec; "looks reasonable" vs. "meets the spec"; red-teaming your own spec. Introduce the code thread: here's a short AI-written function — trace it.
  5. **Verification II — when proof is possible.** Code thread continues: trace a sort or a search; *prove* it correct or find the bug; contrast with the document case where you can only spot-check. Why a few domains let you prove and most don't — and what to do in the "most" case (§3.2, lived).
  6. **Specifying across people and orgs.** Delegation, RFPs/SOWs, handoffs, "reasonable efforts," tickets/PRDs; defined terms = type declarations, conditions = preconditions (§10.4's legal content as professional practice). *Field:* bring a real contract clause or work handoff.
  7. **Bias, defaults, and "correct for whom."** §7, lived: when the AI's output reflects a default you didn't choose, that's an underspecified objective — "whose perspective was the default?" Applied to participants' real tools and workflows.
  8. **Capstone share-out.** Each participant: one before/after — an artifact from their job, the underspecification they found, the revised spec, the verification they ran, what changed. Peer verification of each other's specs (§12.3). Debrief: what transfers to the rest of your work.
- **Assessment:** Pass/fail (it's contract-ed) on a **verification journal** — the same instrument as the 8th-grade course (§10.3) — documenting each field assignment's spec / generation / trace / gap / revision, plus the capstone. No grades.
- **Prerequisites:** None beyond "you use (or expect to use) AI tools in your work." The code-trace thread is read-only and scaffolded — explicitly *not* a coding prerequisite. Bring real work artifacts, with confidential material redacted.
- **AI access:** Model-agnostic (§6.2) — participants likely bring their employer's sanctioned tool; the course specifies the *interaction*, not the tool. Includes a note absent from the 8th-grade course: don't paste confidential data into consumer AI tools.
- **De Anza logistics:** Contract / Community-Ed pathway (no curriculum-committee approval); 24 contact hours; cohort ~12–20 (so verification journals + peer verification stay manageable); whiteboards + participant laptops; instructor = the author, as a volunteer.

### 4.4 `docs/pilot-plan.md` — pilot & evaluation plan

- **Cohort:** Open enrollment, working professionals, ~12–20, mixed fields; recruited via De Anza Community-Ed channels + local professional networks.
- **Informed consent / co-designer framing:** Participants told up front this is a pilot, their (anonymized) journals and feedback inform the K-12 framework, and they may opt out of artifact use — standard adult-ed consent. This section operationalizes §13's ethics argument.
- **Success criteria:**
  - *Behavioral* — by quarter's end, can participants reliably (a) write a spec with explicit success criteria *before* generating, (b) evaluate generated work against the spec rather than "seems fine," (c) explain why a verified solution is correct (a real trace, for the code thread), (d) name the limits/preconditions? Scored from verification journals + capstone against a simple rubric — the four Verification-Principle behaviors, pass/fail per behavior.
  - *Self-report / transfer* — pre/post survey: do they now catch underspecification in their own work? has a work artifact measurably improved (fewer revision cycles, fewer misfires)? would they recommend it?
  - *Pedagogy data* — which sessions/exercises landed; where the code thread helped vs. confused; **a catalog of the real artifacts adults brought** — this catalog becomes example material for the HS and MS bands.
- **Iteration cadence:** Run → debrief → revise → re-run next quarter; two or three cycles before Phase 0 is declared complete.
- **Hand-off to Phase 1 (high school):** The artifact catalog → adapted into §10.4-style HS examples; the 8-session arc → compressed for a HS semester; lessons on the code thread → how much "provable verification" a HS pilot needs. Stated explicitly: the De Anza materials are *written to be ported down*, not redesigned.
- **Risks & mitigations:** Low enrollment → employer cohorts as backup; confidential-data exposure → redaction guidance + no-paste rule; the code thread alienating non-technical adults → keep it ≤30%, read-only, optional depth; "this is just prompt-engineering tips" misperception → lead with §3's "AI makes underspecification visible" framing, not "tricks."

## 5. Files Touched

| File | Change |
|---|---|
| `index.md` | Add §10.5 (Band 5); renumber old §10.5 → §10.6 and add a table row; add one sentence to §10 intro; add new §13 "Deployment: Where to Start"; renumber old §13 "Conclusion" → §14; fix any internal cross-references; add a footnote/link in §9 and/or §10.4 citing [`ap-cs-a-capstone`](https://github.com/davidwkeith/ap-cs-a-capstone) as a concrete worked example of the post-AP / HS-band capstone idea. |
| `docs/de-anza-course-outline.md` | New file — full adult contract-ed course outline (§4.3). |
| `docs/pilot-plan.md` | New file — pilot & evaluation plan (§4.4). |
| `docs/specs/2026-05-11-deployment-and-adult-track-design.md` | This document. |

## 6. Open Questions / Deferred Decisions

- Final course title (two candidates above; decide during drafting).
- Exact between-session field assignments per session (sketched above; flesh out in the course outline).
- Whether the code-trace thread uses Python (consistency with the 8th-grade course) or pseudocode (lower barrier for non-technical adults) — lean Python per §6.1; confirm during drafting.
- The pilot plan's pre/post survey instrument — drafted in `pilot-plan.md`, not in this design.
- Whether to commit these files to version control (this directory is not currently a git repo) — recommended once it is.

## 7. Next Step

Hand to the `writing-plans` skill to produce a step-by-step implementation plan for: (1) editing `index.md`, (2) writing `docs/de-anza-course-outline.md`, (3) writing `docs/pilot-plan.md`.
