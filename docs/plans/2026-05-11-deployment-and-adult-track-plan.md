# Deployment Strategy & Adult / Continuing-Education Track — Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Extend the Specification Literacy framework with a fifth ("adult learner") developmental band and a top-down deployment strategy, and produce two standalone operational documents — a De Anza contract-ed course outline and a pilot/evaluation plan.

**Architecture:** Follow the existing seam in the project — *philosophy* stays in `index.md` (thin additions in the framework's voice), *operational artifacts* (week-by-week course design, pilot mechanics) go in separate files under `docs/`. Mirrors how the 8th-grade anchor course is already "documented separately."

**Tech Stack:** Plain Markdown. No build, no tests in the code sense. "Verification" here = `grep` checks for stale section numbers, read-backs against the spec, and link checks.

**Spec:** `docs/specs/2026-05-11-deployment-and-adult-track-design.md` — read it before starting. Section references below (§4.1, §4.2, etc.) point into that spec.

**Reference artifact:** [`davidwkeith/ap-cs-a-capstone`](https://github.com/davidwkeith/ap-cs-a-capstone) — "The Java Architect Capstone." Cited in several places below; skim its README before Task 4 and Task 6.

**Note on version control:** This directory is not currently a git repo. The `git` steps below are written as if it were. If you run `git init .` first (recommended — it lets `index.md` and these docs be versioned together), follow them as written; otherwise treat each "Commit" step as a checkpoint marker (stop, eyeball the diff, move on) and skip the `git` commands.

**Note on real-world dependency (non-blocking):** Task 5 fixes the De Anza course format at "8 weekly evening sessions × 3 hours = 24 contact hours" per the approved spec. Before *offering* the course, the author should confirm De Anza's Community Education / contract-ed program parameters (minimum/maximum contact hours, room booking, enrollment minimums). That confirmation is out of scope for this plan — do not block on it; note it in the course outline's "Logistics" section as a to-confirm item.

---

## File Structure

| File | Responsibility | This plan's action |
|---|---|---|
| `index.md` | The philosophical framework (Draft v3). | Modify: add §10 intro sentence; add §10.5 (Band 5); renumber old §10.5 → §10.6 + add a table row; add new §13 "Deployment: Where to Start"; renumber old §13 "Conclusion" → §14; fix cross-references; add an `ap-cs-a-capstone` footnote in §9/§10.4. |
| `docs/de-anza-course-outline.md` | The adult anchor course — the De Anza contract-ed cohort's course design (format, session arc, assessment, prerequisites, logistics). The adult parallel to the separately-documented 8th-grade course. | Create. |
| `docs/pilot-plan.md` | The pilot & evaluation plan — cohort, informed consent, success criteria, iteration cadence, hand-off to the high-school phase, risks. | Create. |
| `docs/specs/2026-05-11-deployment-and-adult-track-design.md` | The approved design. | Read-only (already exists). |
| `docs/plans/2026-05-11-deployment-and-adult-track-plan.md` | This plan. | Read-only (this file). |

Task order: do the `index.md` edits first (Tasks 1–4) so section numbers are stable, then write the two standalone docs (Tasks 5–6), then a final cross-file consistency pass (Task 7).

---

## Task 1: `index.md` — §10 intro forward-pointer + new Band 5 (§10.5)

**Files:**
- Modify: `index.md` — §10 introduction (around the paragraph that introduces "four developmental bands"); insert new §10.5 immediately after the end of §10.4 ("Band 4: 9–12 — Domain-Specific Rigor") and before the current §10.5 ("The Through-Line").

- [ ] **Step 1: Re-read the model sections.** Read `index.md` §10 intro, §10.3 ("Band 3: 6–8"), and §10.4 ("Band 4: 9–12") in full. Note the exact structural template each band uses: a one-line **Central cognitive operation:**, a **Developmental stage:** paragraph, a **What specification literacy looks like at this stage:** block, **Cross-curricular manifestations:** (here it will be **Cross-domain manifestations:** since adults aren't in school) with *italic sub-headers* per domain, and a **Teacher's role:** paragraph. Match this template exactly.

- [ ] **Step 2: Add the §10 intro forward-pointer.** In the §10 introduction, after the sentence that says the framework "identifies four developmental bands," add one sentence: that a fifth band — adult learners and continuing education (§10.5) — extends the same progression past formal schooling, and that while the disposition *develops* bottom-up, the framework is *deployed* top-down (forward-pointer to the new §13). Keep it to one or two sentences; do not rewrite the paragraph.

- [ ] **Step 3: Write the new §10.5 "Band 5: Adult Learners — Specification Under Stakes".** Use the content points in spec §4.1, in the bands' template:
  - **Central cognitive operation:** Writing, delegating, and verifying specifications in real organizational contexts — where the interpreter (an AI, a colleague, a vendor) acts on your behalf with autonomy, and the cost of underspecification lands immediately on you.
  - **Developmental stage:** Post-formal / pragmatic reasoning. Adults can hold that a specification is *simultaneously* precise and negotiated, that "correct" is stakeholder-dependent, and that specs are revisable artifacts. The catch: deep domain expertise comes with *low* meta-awareness of one's own tacit assumptions — the expert's curse. The pedagogical opportunity is that the expertise *is* the underspecification.
  - **What specification literacy looks like at this stage:** No grades, no teacher resolving ambiguity — the stakes are intrinsic (their actual work improves or doesn't). State the band's verification question: *"When I hand this to an AI that will act on it, how do I know — before the consequences land — that it did what I needed?"*
  - **Cross-domain manifestations:** (italic sub-headers, parallel to §10.4) — *Knowledge work / drafting:* prompting an LLM is spec-writing — the Sandwich Challenge at work; "summarize this for the board" — for whom, deciding what? *Law:* AI-assisted contract review and e-discovery search terms — "relevant" is the new "room temperature." *Software / IT:* tickets, PRDs, acceptance criteria; reviewing AI-generated code at work. *Marketing / comms:* a campaign brief vs. "make it pop." *Data / analytics:* "pull our top customers" — top by what, over what period, excluding what — the SQL encodes choices the requester never stated. *Operations / procurement:* RFPs, SOWs, "reasonable efforts" — §10.4's legal-studies content, now lived. *Management:* delegating to a person is writing a spec — the manager surprised by the result has an underspecification problem, not a bad employee. *Civic / personal (adult stakes):* insurance claims, disputing a bill, instructing a contractor.
  - **Teacher's role:** Surface the expert's buried assumptions ("you said 'obviously the Q3 numbers' — obvious to whom?"). Treat learners as **co-designers**: they bring real artifacts from their jobs; the class works on those. Note that the formal vehicle for this band is documented separately — the De Anza contract-ed course outline (`docs/de-anza-course-outline.md`) — exactly as §10.3 notes the 8th-grade course is documented separately.

- [ ] **Step 4: Verify the insertion.** Read `index.md` from the end of §10.4 through the start of §10.6-to-be ("The Through-Line"). Confirm: the new section is numbered §10.5; it sits *after* Band 4 and *before* "The Through-Line"; the template matches bands 1–4; nothing in §10.4 was disturbed.

- [ ] **Step 5: Commit.**

```bash
git add index.md
git commit -m "docs: add Band 5 (adult learners) to the developmental progression"
```

---

## Task 2: `index.md` — renumber old §10.5 → §10.6 and add the fifth table row

**Files:**
- Modify: `index.md` — the section currently titled §10.5 "The Through-Line" (heading + the summary table inside it).

- [ ] **Step 1: Renumber the heading.** Change the `### 10.5 The Through-Line` heading (and any "§10.5" text inside that subsection that refers to itself) to `### 10.6 The Through-Line`.

- [ ] **Step 2: Add the fifth row to the capacity/verification-question table.** The table currently has rows for K–2, 3–5, 6–8, 9–12 with columns *Band | Capacity | Verification Question*. Add a fifth row:
  - **Band:** Adult / Continuing Ed
  - **Capacity:** Specify, delegate, and verify under real stakes — when the interpreter acts with autonomy on your behalf
  - **Verification Question:** "When I hand this off and it acts for me, how do I know — before the consequences land — that it did what I needed?"

- [ ] **Step 3: Update the prose around the table if needed.** The paragraph after the table currently says things like "A high school student who has practiced all four arrives at college, at a job, or at a voting booth…". Adjust lightly so it acknowledges the fifth capacity (e.g., "…and the adult learner who never developed the earlier capacities now builds them under stakes"). Do not rewrite the paragraph wholesale — a clause or sentence is enough.

- [ ] **Step 4: Verify.** `grep -n "10\.5\|10\.6" index.md` — confirm there is exactly one `### 10.6 The Through-Line` heading, the only remaining `§10.5`/`10.5` references point at the *new* Band 5 (from Task 1), and no reference to "§10.5" still means "The Through-Line." Read the table and confirm it has five rows.

- [ ] **Step 5: Commit.**

```bash
git add index.md
git commit -m "docs: renumber Through-Line to 10.6, add adult-band row to summary table"
```

---

## Task 3: `index.md` — new §13 "Deployment: Where to Start"; renumber Conclusion → §14

**Files:**
- Modify: `index.md` — insert a new top-level section between the current §12 ("A Practical Guide for Every Teacher", which has subsections through §12.6) and the current §13 ("Conclusion"). Renumber "Conclusion" from §13 to §14. Check the "Notes" / footnotes section and the table of contents (if any) for references to "§13" or "Section 13."

- [ ] **Step 1: Scan for cross-references to §13 and the section count.** Run `grep -n "13\.\|Section 13\|§13\|Conclusion" index.md`. Note every place that will need updating: the Conclusion heading itself, any "see Section 13" text, and any intro/abstract sentence that enumerates the document's sections.

- [ ] **Step 2: Write the new §13 "Deployment: Where to Start".** Use the content points in spec §4.2, in the framework's prose voice (full paragraphs, like §11–§12, not bullet-heavy). Cover, in order:
  1. **The developmental order is not the deployment order.** Spec literacy *develops* bottom-up (K → 12 → adult); the framework should be *built and validated* top-down. Name the tension and resolve it in one tight paragraph.
  2. **Why community college specifically — four reasons:** *urgency* (the labor market is repricing skills now; the people who need this *this year* are working adults, served by the open-access, workforce-facing community college); *autonomy & consent* (adults enroll voluntarily, can drop, push back, give informed feedback — piloting a new pedagogy on minors raises consent/equity/IRB concerns an adult cohort sidesteps; we iterate fast *and* ethically before anything reaches a child who can't consent — the "easier to experiment with adults" intuition stated responsibly: "experiment" → "iterate with consenting co-designers"); *tight feedback loop* (adults bring real work artifacts, so the §4 verification loop closes in a quarter, not the ~13 years a K cohort takes to mature); *low institutional friction* (contract/continuing-ed launches without curriculum-committee approval, so you can run-revise-rerun in consecutive quarters). Name **De Anza College** as the concrete first instance, with a pointer to `docs/de-anza-course-outline.md` and `docs/pilot-plan.md`.
  3. **The top-down sequence, with a gate between phases:** Phase 0 (now) — De Anza contract-ed pilot, open professional cohort; *gate*: do adults reliably show the four Verification-Principle behaviors after a quarter and report their work changed? Phase 1 — adult track scales (more sections, employer cohorts, a transfer-credit version) *and* high-school pilots begin: the §10.4 band already exists and the HS phase does **not** start from zero — [`ap-cs-a-capstone`](https://github.com/davidwkeith/ap-cs-a-capstone) is an existing worked HS instance (architect a spec → an AI builds it → students verify and must explain everything at a walkthrough), and the De Anza materials adapt *down* to HS alongside it; *gate*: HS teachers can run it without the course author present. Phase 2 — stand up the already-designed 8th-grade anchor course (§10.3) using lessons from the HS pilots — this is where the "named introduction" lands, as the framework already says. Phase 3 — elementary (3–5): the §12 "practices that cost nothing" become a structured strand; train elementary teachers (some of whom came through the adult track). Phase 4 — K–2: by now there's a decade of materials, a trained-teacher pipeline, and evidence; the kindergartner who draws a different house meets a teacher who knows exactly what's happening. Close with: each phase feeds the next — adult learners who are also teachers and parents carry the disposition downward — so the pilot cohort is itself part of the rollout mechanism.
  4. **Why not bottom-up (addressing the obvious alternative):** start in K and the first beneficiaries graduate in ~13 years — the AI transition won't wait; bottom-up also experiments on those least able to consent, with the longest feedback loop and the hardest approval path (state standards, textbook adoption). Top-down de-risks all of it.
  Number it `## 13. Deployment: Where to Start` (matching the document's existing `## N. Title` heading style) with subsections `### 13.1`…`### 13.4` if the four parts above each warrant a header — match the granularity of §11/§12.

- [ ] **Step 3: Renumber the Conclusion.** Change `## 13. Conclusion` to `## 14. Conclusion`.

- [ ] **Step 4: Fix the cross-references found in Step 1.** Update the abstract/intro section enumeration if it counts sections; update any "see Section 13" that meant the Conclusion to "Section 14"; leave alone (or repoint) anything that legitimately should now point to the new §13.

- [ ] **Step 5: Verify.** `grep -n "^## 1[0-4]\." index.md` — confirm the sequence is §10, §11, §12, §13 (Deployment), §14 (Conclusion) with no gaps or duplicates. Read the new §13 end-to-end: does it read in the framework's voice (paragraphs, not a slide deck)? Does it resolve the developmental-vs-deployment tension explicitly? Does it name De Anza and link the two new docs?

- [ ] **Step 6: Commit.**

```bash
git add index.md
git commit -m "docs: add Section 13 (deployment strategy), renumber Conclusion to 14"
```

---

## Task 4: `index.md` — cite `ap-cs-a-capstone` in §9 / §10.4

**Files:**
- Modify: `index.md` — §9 (the bullet beginning "**The anchor course supersedes AP Computer Science A, not supplements it.**") and/or §10.4's *Computer science:* manifestation (the sentence about "Post-AP capstone projects can assess specification literacy directly…"). Add to the "Notes" section if you use a footnote.

- [ ] **Step 1: Skim the repo.** Read the README of [`davidwkeith/ap-cs-a-capstone`](https://github.com/davidwkeith/ap-cs-a-capstone). Key facts to reflect accurately: students architect a text-adventure game as a written "blueprint"/spec, hand it to a custom AI builder, then verify and iterate; the final walkthrough requires students to explain every line — "the AI wrote it" scores the lowest band; "students who rush the blueprint get broken games."

- [ ] **Step 2: Add the citation.** In §10.4's *Computer science:* paragraph, after the sentence about post-AP capstones assessing specification literacy directly, add a clause/sentence pointing to the repo as a concrete worked example, with a footnote in the "Notes" section: `[^7]: David W. Keith, "The Java Architect Capstone," https://github.com/davidwkeith/ap-cs-a-capstone — a high-school AP CS A capstone in which students architect a text-adventure game as a written specification, an AI builder generates it, and students verify and must explain every line at a walkthrough.` (Use the next free footnote number; the document currently ends at `[^6]`.) Optionally add a one-clause nod in the §9 "supersedes AP CS A" bullet that a worked instance of the student-as-architect model already exists at the HS level (same footnote).

- [ ] **Step 3: Verify.** `grep -n "ap-cs-a-capstone\|Java Architect" index.md` — confirm the link and footnote appear and the footnote number is unique and sequential. Confirm the footnote marker in the body matches the definition in "Notes."

- [ ] **Step 4: Commit.**

```bash
git add index.md
git commit -m "docs: cite ap-cs-a-capstone as a worked HS-band example"
```

---

## Task 5: Create `docs/de-anza-course-outline.md` — the adult anchor course

**Files:**
- Create: `docs/de-anza-course-outline.md`

- [ ] **Step 1: Re-read the model.** Re-read `index.md` §10.3 (the 8th-grade anchor-course description) and §3, §4, §6.1, §6.2, §7 — the De Anza course is the adult parallel and must echo their language ("Verification Principle," "Assumption Audit," "verification journals," "model-agnostic," "read and trace, do not write"). Re-read spec §4.3.

- [ ] **Step 2: Write the document.** Structure:
  1. **Title + one-paragraph framing.** Pick one working title — *"Problem Architecture for Working Professionals: Specifying, Verifying, and Directing AI at Work"* or *"Specification Literacy: Telling AI What You Actually Mean"* (note in the doc that the title is provisional). Framing paragraph: this is the adult parallel to the 8th-grade anchor course (§10.3), built for a De Anza contract / Community-Education cohort of working professionals from mixed fields; the formal vehicle for §10.5's Band 5.
  2. **Format.** 8 weekly evening sessions × 3 hours = 24 contact hours; each session followed by a between-session **field assignment** (apply it at your actual job; bring the artifact back). Note the alternative: a 2-day intensive + 4 follow-up evenings.
  3. **The medium, and why it differs from the 8th-grade course.** The 8th-grade course uses five sorting algorithms (immediate feedback + formal verification + AI-makes-underspecification-visible, §3). Adults aren't all coders, so: **~70% real workplace specification artifacts** of increasing stakes (prompts → briefs → tickets/PRDs → contracts/SOWs) **+ ~30% one running read-and-trace code thread** (per §6.1: trace only, never write) — so every adult tastes *provable* verification and feels the contrast with the merely-plausible verification that dominates their work. State that the code thread adapts the structure of [`ap-cs-a-capstone`](https://github.com/davidwkeith/ap-cs-a-capstone) (architect a spec → an AI builds it → you must explain every line), scaled down to read-and-trace.
  4. **Session-by-session arc** (8 sessions; for each: in-class focus + the field assignment). Use spec §4.3's arc verbatim as the skeleton:
     1. *The gap.* Adult Sandwich Challenge — everyone writes a real prompt/delegation email, runs it, examine the divergence; name underspecification; introduce the Verification Principle. Field: bring a real prompt/brief/ticket from work that "didn't quite work."
     2. *The Assumption Audit, adult version.* §10.3's diagnostic re-aimed: *types* (what kind of thing did I ask for?), *boundaries* (how much, by when, for whom?), *defaults* (what did I leave the interpreter to pick?), *context* (what do I know that I didn't say — the expert's curse). Worked on participants' brought artifacts.
     3. *Specifying to an AI that acts.* Prompts as specs; system/standing instructions as standing specs; asking for *output* vs. asking for *a thing that meets criteria*; acceptance criteria. Field: rewrite your artifact as a spec with explicit success criteria; run it; journal the gap.
     4. *Verification I — checking plausible work.* Evaluating an AI-generated document/analysis/plan against your spec; "looks reasonable" vs. "meets the spec"; red-teaming your own spec. Introduce the code thread: a short AI-written function — trace it.
     5. *Verification II — when proof is possible.* Code thread continues: trace a sort or a search; *prove* it correct or find the bug; contrast with the document case where you can only spot-check. Why a few domains let you prove and most don't — and what to do in the "most" case.
     6. *Specifying across people and orgs.* Delegation, RFPs/SOWs, handoffs, "reasonable efforts," tickets/PRDs; defined terms = type declarations, conditions = preconditions (§10.4's legal content as professional practice). Field: bring a real contract clause or work handoff.
     7. *Bias, defaults, and "correct for whom."* §7, lived: when the AI's output reflects a default you didn't choose, that's an underspecified objective — "whose perspective was the default?" Applied to participants' real tools and workflows.
     8. *Capstone share-out.* Each participant: one before/after — an artifact from their job, the underspecification they found, the revised spec, the verification they ran, what changed. Peer verification of each other's specs (§12.3). Debrief: what transfers to the rest of your work.
  5. **Assessment.** Pass/fail (it's contract-ed) on a **verification journal** — the same instrument as the 8th-grade course (§10.3) — documenting each field assignment's spec / generation / trace / gap / revision, plus the capstone. No grades. (Sketch the journal's per-entry template: *what I asked for · what I expected · what I got · the gap · the revised spec · how I checked.*)
  6. **Prerequisites.** None beyond "you use (or expect to use) AI tools in your work." The code-trace thread is read-only and scaffolded — explicitly *not* a coding prerequisite. Bring real work artifacts, with confidential material redacted.
  7. **AI access.** Model-agnostic (§6.2): participants likely bring their employer's sanctioned tool; the course specifies the *interaction*, not the tool. Include the note absent from the 8th-grade course: don't paste confidential data into consumer AI tools — and have participants check their employer's policy.
  8. **Logistics (De Anza).** Contract / Community-Education pathway (no curriculum-committee approval); 24 contact hours; cohort ~12–20 (so journals + peer verification stay manageable); room with whiteboards + participant laptops; instructor = the author, volunteering. Flag as **to confirm**: De Anza Community Ed program parameters (min/max contact hours, enrollment minimums, room booking) before offering the course.

- [ ] **Step 3: Verify.** Read the file end-to-end. Checklist: 8 sessions, each with an in-class focus *and* a field assignment? Assessment is pass/fail on a verification journal (matches §10.3)? Prerequisites say "no coding required" and "redact confidential material"? The 70/30 split and the `ap-cs-a-capstone` reference are present? Logistics flags the De Anza-parameters confirmation? Cross-references to `index.md` sections (§3, §4, §6.1, §6.2, §7, §10.3, §10.4, §10.5, §12.3) are accurate.

- [ ] **Step 4: Commit.**

```bash
git add docs/de-anza-course-outline.md
git commit -m "docs: add De Anza contract-ed course outline (adult anchor course)"
```

---

## Task 6: Create `docs/pilot-plan.md` — pilot & evaluation plan

**Files:**
- Create: `docs/pilot-plan.md`

- [ ] **Step 1: Re-read the model.** Re-read spec §4.4 and `index.md` §4 (the Verification Principle's four behaviors: specify / evaluate / explain / identify-limits) and §13's deployment phases (after Task 3, these are in `index.md`).

- [ ] **Step 2: Write the document.** Structure:
  1. **Purpose.** This is Phase 0 of the deployment strategy (`index.md` §13): validate the framework with an autonomous adult cohort before anything reaches K-12. Names the vehicle: the De Anza contract-ed course (`docs/de-anza-course-outline.md`).
  2. **Cohort.** Open enrollment, working professionals, ~12–20, mixed fields; recruited via De Anza Community-Education channels + local professional networks. Backup if enrollment is short: an employer-sponsored cohort.
  3. **Informed consent / co-designer framing.** Participants told up front: this is a pilot; their (anonymized) verification journals and feedback inform the K-12 framework; they may opt out of having their artifacts used; standard adult-ed consent language. This operationalizes §13's ethics argument — say so explicitly.
  4. **Success criteria.**
     - *Behavioral* — by quarter's end, can participants reliably (a) write a spec with explicit success criteria *before* generating, (b) evaluate generated work against the spec rather than "seems fine," (c) explain why a verified solution is correct (a real trace, for the code thread), (d) name the limits/preconditions? Scored from verification journals + capstone against a simple rubric: the four Verification-Principle behaviors, pass/fail per behavior. Include the rubric inline (four rows, "demonstrated / not yet demonstrated," with a one-line descriptor of what "demonstrated" looks like for each).
     - *Self-report / transfer* — pre/post survey: do they now catch underspecification in their own work? has a work artifact measurably improved (fewer revision cycles, fewer misfires)? would they recommend it? Include the ~6–8 survey items inline.
     - *Pedagogy data* — which sessions/exercises landed; where the code thread helped vs. confused; **a catalog of the real artifacts participants brought** (sanitized) — this catalog becomes example material for the HS and MS bands.
  5. **Iteration cadence.** Run → debrief → revise → re-run next quarter; two or three cycles before Phase 0 is declared complete and Phase 1 (HS) begins.
  6. **Hand-off to Phase 1 (high school).** The artifact catalog → adapted into §10.4-style HS examples; the 8-session arc → compressed for a HS semester; lessons on the code thread → how much "provable verification" a HS pilot needs. State explicitly: the De Anza materials are *written to be ported down*, not redesigned — and the HS phase also has [`ap-cs-a-capstone`](https://github.com/davidwkeith/ap-cs-a-capstone) as an existing instance to reconcile with.
  7. **Risks & mitigations** (table): low enrollment → employer cohorts as backup; confidential-data exposure → redaction guidance + no-paste rule; the code thread alienating non-technical adults → keep it ≤30%, read-only, optional depth; "this is just prompt-engineering tips" misperception → lead with §3's "AI makes underspecification visible" framing, not "tricks"; instructor-dependence (only the author can teach it) → the verification journals + this plan are the transfer mechanism; treat "a second person can run it" as a Phase 1 gate.

- [ ] **Step 3: Verify.** Read end-to-end. Checklist: consent section explicitly ties to §13's ethics argument? Behavioral success criteria are the four Verification-Principle behaviors with an inline rubric? Pre/post survey items are written out (not "TBD")? Artifact catalog is named as the hand-off to HS/MS? Risks table has ≥4 rows with mitigations? Cross-references to `index.md` (§3, §4, §10.4, §13) and to `docs/de-anza-course-outline.md` are accurate.

- [ ] **Step 4: Commit.**

```bash
git add docs/pilot-plan.md
git commit -m "docs: add pilot and evaluation plan for the De Anza Phase 0 cohort"
```

---

## Task 7: Cross-file consistency pass

**Files:**
- Read-only review of: `index.md`, `docs/de-anza-course-outline.md`, `docs/pilot-plan.md`, `docs/specs/2026-05-11-deployment-and-adult-track-design.md`.

- [ ] **Step 1: Section-number sweep.** `grep -n "§1[0-4]\|Section 1[0-4]\|## 1[0-4]\.\|### 10\." index.md` — confirm: §10.1–§10.4 (the original bands) unchanged; §10.5 = Band 5; §10.6 = The Through-Line; §11, §12 unchanged; §13 = Deployment; §14 = Conclusion. No dangling reference to "§13 Conclusion."

- [ ] **Step 2: Footnote sweep.** `grep -n "\[\^[0-9]" index.md` — confirm every `[^N]` marker in the body has exactly one matching `[^N]:` definition in "Notes," numbers are sequential, and the new `ap-cs-a-capstone` footnote is included.

- [ ] **Step 3: Link sweep.** `grep -rn "de-anza-course-outline\|pilot-plan\|ap-cs-a-capstone" index.md docs/` — confirm: `index.md` §10.5 and §13 link the two new docs; the two new docs link back to `index.md` and to each other where the plan calls for it; every `ap-cs-a-capstone` mention uses the full URL `https://github.com/davidwkeith/ap-cs-a-capstone`.

- [ ] **Step 4: Spec-coverage check.** Open the spec (`docs/specs/2026-05-11-deployment-and-adult-track-design.md`) and walk its §4.1–§4.4 and "Files Touched" table. For each item, point to where it landed. Expected mapping: §4.1 → Task 1 + Task 2; §4.2 → Task 3; §4.3 → Task 5; §4.4 → Task 6; the `ap-cs-a-capstone` "reference artifact" → Tasks 3, 4, 5, 6. List any gaps; if a spec item has no home, add it now.

- [ ] **Step 5: Voice check.** Read the new `index.md` §10.5 and §13 against a neighboring original section (e.g., §10.4 and §12). Do they sound like the same author — full paragraphs, measured tone, concrete examples, no bullet-dump? If not, revise.

- [ ] **Step 6: Final commit.**

```bash
git add -A
git commit -m "docs: cross-file consistency pass for deployment + adult track"
```

---

## Self-Review (completed by plan author)

**Spec coverage:** spec §4.1 (Band 5) → Tasks 1–2; §4.2 (deployment section) → Task 3; §4.3 (De Anza course) → Task 5; §4.4 (pilot plan) → Task 6; the `ap-cs-a-capstone` reference artifact → Tasks 3, 4, 5, 6; spec "Files Touched" table → File Structure table here + Tasks 1–6; spec "Open Questions" (title, field assignments, Python-vs-pseudocode, survey instrument, git) → surfaced as decisions inside Tasks 5–6 and the version-control note. No uncovered spec items.

**Placeholder scan:** No "TBD/TODO/implement later." Content steps carry the actual material to write (drawn from the approved spec) rather than deferring it; for the prose docs that means detailed section skeletons with mandatory content points, which is the right granularity for a writing task (pre-writing ~5k words of final prose in the plan would be wasteful and is not what "no placeholders" means here). The one explicit "to confirm" item (De Anza Community Ed parameters) is a genuine real-world external dependency, flagged as non-blocking with a home in the course outline's Logistics section.

**Type/name consistency:** Section numbers are consistent across tasks (§10.5 Band 5 created in Task 1, referenced as such in Tasks 2/5/6; old §10.5 → §10.6 in Task 2; §13 Deployment / §14 Conclusion in Task 3, referenced consistently after). Artifact names (`docs/de-anza-course-outline.md`, `docs/pilot-plan.md`) are spelled identically everywhere. The four Verification-Principle behaviors (specify / evaluate / explain / identify-limits) are referenced with the same wording in Task 5 (assessment), Task 6 (rubric), and the spec.
