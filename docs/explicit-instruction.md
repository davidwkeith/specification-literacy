# Explicit Instruction and Specification Literacy

## Why a specification-literate teacher writes better lesson plans

Companion to [`../index.md`](../index.md)

---

> **Summary:** *Explicit Instruction* is the research tradition behind Rosenshine's *Principles of Instruction*, Rosenshine and Stevens's six teaching functions, and Archer and Hughes's sixteen elements. It holds that new skills should be taught in an unambiguous, step-by-step way, with modeling, guided practice, frequent checks for understanding, and support that is withdrawn gradually. This document argues that Explicit Instruction and specification literacy describe the same problem from two sides. A lesson is a specification, students are its interpreters, and a misconception is a divergent interpretation, or what we call a hallucination when LLMs do the same. A teacher trained in specification literacy is therefore better equipped to carry out Explicit Instruction: to find the gaps in a lesson plan before students fall into them, to design checks for understanding as real tests, and to treat student errors as diagnostic information about the instruction rather than verdicts on the student. The document maps the two frameworks onto each other, gives a lesson-design protocol and a worked example, and marks where the overlap ends.

---

## 1. One Problem, Two Vocabularies

The framework defines specification literacy as describing a problem precisely enough that any interpreter, human or machine, will produce the same result ([`../index.md`](../index.md) §1). It locates failures in *underspecification*: descriptions that seem complete to their author because the author relies, without noticing, on context the interpreter doesn't share (§2).

Explicit Instruction begins from the same observation, made in the classroom. Archer and Hughes call it "explicit" because it is an *unambiguous* and direct approach that covers both the design of instruction and its delivery.[^archer] A literacy-practice summary puts the aim in five words: "Nothing is left to guess work."[^keys] Rosenshine, describing the approach in 1987, stressed small steps, checking for student understanding, and active, successful participation by every student.[^archer]

Put the two side by side and the correspondence is direct:

| Specification literacy | Explicit Instruction |
|---|---|
| Author | Teacher |
| Specification | Lesson: goals, explanations, models, examples, practice tasks |
| Interpreter | Each student |
| Output | What each student can actually do when the lesson ends |
| Underspecification | An explanation or model that seemed clear to the teacher and wasn't |
| Divergent interpretation (in an LLM: hallucination) | Misconception |
| Verification | Checking for understanding |
| The expert's curse (§10.5) | The teacher's fluency hiding the steps a novice needs |

The strongest evidence for this mapping comes from Rosenshine himself. In *Principles of Instruction* he explains that students who are left to construct their own summary of new material often build it wrongly, especially when their background knowledge is weak, and that these errors are best understood as students trying to be logical with incomplete information.[^rosenshine2012] That is the framework's definition of underspecification, seen from the interpreter's side: wherever the specification is silent, the interpreter fills the gap with defaults, and the defaults differ from the author's. The student isn't failing to follow the lesson. They are following it faithfully and resolving its ambiguities differently than the teacher intended.

An example from the podcast *Sold a Story* makes this concrete.[^sold] Ask a preschooler to count "to five," and they may answer "two, five." The child isn't being careless. To a child who hears "to" and "two" as the same sound, "two, five" is a reasonable reading of what was said. The teacher's meaning depended on context the child didn't have. The fix isn't to correct the child but to correct the specification: ask the child to "count until you reach five," which has only one reading.

Siegfried Engelmann, whose preschool that season begins with, built a whole theory of instruction on this idea. He developed *Direct Instruction* — capitalized, to distinguish his scripted programs from teacher-led instruction in general — and, with Douglas Carnine, set out the theory behind it around a principle they called **faultless communication**.[^engelmann] A faultless communication is a sequence of examples and non-examples designed so that only one interpretation is consistent with all of them. If a learner who has the prerequisites still learns the wrong thing, the theory looks first at the communication, not the learner: some other interpretation must also have fit the examples. That is very close to this framework's definition of specification literacy, applied to teaching: a description precise enough that any interpreter produces the same result. Engelmann's version is more demanding than most explicit instruction, because it treats the design of the example sequence as the main way to remove ambiguity, not just the explanation that goes with it.

So Explicit Instruction is, in practice, a mature discipline's answer to underspecification. It belongs alongside the law, science, and engineering practices described in §2.4, built for the case where the interpreter is a learner. Its sixteen elements are a checklist for closing specification gaps before they reach students.

---

## 2. The Sixteen Elements as Specification Practices

Archer and Hughes list sixteen elements of Explicit Instruction, drawn from several decades of teacher-effectiveness research.[^archer] Each one corresponds to a specification-literacy concept, and in each case the specification-literate teacher has a sharper diagnostic question to ask.

| # | Element (Archer & Hughes) | Specification-literacy reading | The question a specification-literate teacher adds |
|---|---|---|---|
| 1 | Focus instruction on critical content | State the requirement: what must the interpreter be able to do? | Can I write the success criterion as an observable behavior, not "understand X"? |
| 2 | Sequence skills logically | Dependency ordering; preconditions before what depends on them | What does each step assume has already been established? |
| 3 | Break complex skills into smaller units | Decomposition | Is every unit small enough that a novice can't misread it? |
| 4 | Design organized, focused lessons | Scope: what is in the spec and what is out | What have I included that an interpreter might take as a requirement? |
| 5 | Begin with a clear statement of goals and expectations | Publish the acceptance criteria before work starts (§12.3, "Spec before you start") | Could a student predict how their work will be judged from my statement alone? |
| 6 | Review prior skills and knowledge | Check preconditions | Which prerequisites am I assuming without checking? (Assumption Audit: *Context*) |
| 7 | Provide step-by-step demonstrations, thinking aloud | Make the hidden decision procedure visible | Which decisions do I make automatically that I haven't said out loud? (the expert's curse) |
| 8 | Use clear and concise language | Consistent terms, used one way only | Do I use two words for one idea, or one word for two? |
| 9 | Provide a range of examples and non-examples | **Boundary specification and edge cases** | Where exactly is the boundary, and have I shown cases on both sides of it? (Assumption Audit: *Boundaries*) |
| 10 | Provide guided and supported practice | Supervised execution while the spec is still being tested | Which practice items are designed to expose a specific misreading? |
| 11 | Require frequent responses | Sample the interpreter's output often | Will every student's output be visible, or only the volunteers'? |
| 12 | Monitor student performance closely | Compare output against the spec | What exactly am I comparing against? |
| 13 | Provide immediate affirmative and corrective feedback | Close the loop before a wrong interpretation sets | When an error repeats across students, is it a student error or a gap in my spec? (§12.1) |
| 14 | Deliver the lesson at a brisk pace | Time is a constraint on the spec | Does the pace leave room to check output, not only to deliver input? |
| 15 | Help students organize knowledge | Name the structure explicitly | Have I stated how this connects to what students already know, or left them to infer it? |
| 16 | Provide distributed and cumulative practice | Regression testing | Does later practice re-check earlier skills, so I'd notice if they decayed? |

Rosenshine and Stevens group these elements into six teaching functions: review, presentation, guided practice, corrections and feedback, independent practice, and weekly and monthly reviews.[^archer] [^rs1986] In specification terms, those are: check preconditions, deliver the specification, run supervised tests, revise, let the interpreter run alone, and run regression tests.

Two of the correspondences deserve emphasis, because they are where specification literacy adds the most.

**Element 9 is the Assumption Audit's *Boundaries* question.** Archer and Hughes justify non-examples as the way to set the boundaries of when a skill or rule applies and when it doesn't. Wide examples prevent underuse; wide non-examples prevent misuse. That is edge-case specification in a teacher's vocabulary. A teacher who has practiced the Assumption Audit ([`de-anza-course-outline.md`](de-anza-course-outline.md), Session 2) chooses non-examples systematically, at the boundary, rather than whichever ones come to mind.

**Archer and Hughes's three forms of knowledge correspond to the *Types* question.** They separate declarative knowledge (what something is), procedural knowledge (how to do it), and conditional knowledge (when and where to use it).[^archer] A lesson goal that doesn't say which type is required is underspecified in exactly the way "summarize this" is underspecified at work. The interpreter has to guess what kind of thing was asked for. "Students will understand rounding" leaves the type open. "Students will decide, for a given number, whether rounding is appropriate and to which place" asks for conditional knowledge, and the lesson has to teach it.

---

## 3. Checking for Understanding Is the Verification Principle

Rosenshine's sixth principle is to check for student understanding, and his seventh is to obtain a high success rate. He reports that the most effective teachers aimed for a success rate of about 80 percent during practice: high enough that students are not practicing errors, low enough to show the material is still challenging.[^rosenshine2012] Archer and Hughes cite the same figure, rising to 90–95 percent once students work independently.[^archer]

The framework's Verification Principle (§4) says: *the output is the beginning, not the end.* For a teacher, the output is what students do after the lesson, and the Verification Principle says the lesson isn't finished when it has been delivered. It is finished when the teacher has compared what students can do with what the lesson specified, and explained any difference.

Specification literacy changes how a teacher checks for understanding in four practical ways.

1. **Checks are written before the lesson, as tests against the specification.** "Any questions?" isn't a test. "Round 3.96 to the nearest tenth and write how you know" is a test, because the teacher knows in advance which answer reveals which misreading. A specification-literate teacher designs each check to *discriminate* between the intended interpretation and a specific likely misinterpretation.

2. **The success rate measures the specification, not the class.** When a check shows that 40 percent of students got an item wrong *in the same way*, that is the signal §12.1 describes: the instruction could be read another way, and many students read it that way. The correct response is to revise the explanation or the model, which is Rosenshine's reteaching, rather than to tell students they made careless errors. Rosenshine's own wording points this way: errors appear when too much material is presented at once without enough guidance, which locates the cause in the instruction.[^rosenshine2012]

3. **Every student's output is visible.** Specification literacy treats each interpreter's divergence as information. That is why Explicit Instruction asks for frequent responses from *all* students (whiteboards, choral responses, written answers traded with a partner) rather than from volunteers. A spec tested only on the interpreters most likely to read it correctly hasn't really been tested.

4. **Check in early on extended work.** Students, like LLMs, don't only misread gaps in the instruction. Even when the instruction is clear, they fill gaps in their own knowledge with plausible material: weak sources, half-remembered facts, a confident answer to a question nobody asked. On a multi-week project, a misinterpretation or bad research made in the first days compounds into everything built on it, and it surfaces only at the final deadline, when it is most expensive to fix. That is the failure pattern of §2.4 on a classroom scale. Rosenshine and Stevens's guidance to monitor students' *initial* practice attempts applies here.[^archer] Check in at the start of a project and ask each student to state back what they think the task is, what a finished result looks like, and where their information is coming from. This is "Spec before you start" (§12.3) used as a checkpoint. It catches divergence while correcting it is still cheap.

---

## 4. A Lesson-Design Protocol

The following protocol uses specification-literacy practices to produce an Explicit Instruction lesson plan. It can be used at any grade band and in any subject. It adds no content to the lesson. It changes how the plan is written and checked.

1. **Write the success criterion as observable behavior.** State what a student who has learned the material can *do*, and specify the knowledge type: declarative, procedural, or conditional (§2 above). *(Elements 1 and 5.)*

2. **Run the Assumption Audit on your own plan.** Apply the four questions from the adult course to the lesson itself:
   - **Types:** what kind of knowledge, and what kind of response, counts as success?
   - **Boundaries:** where exactly does the rule stop applying? List the edge cases.
   - **Defaults:** where the plan is silent, what will a student fill in? Notation, format, rounding conventions, what counts as "showing work"?
   - **Context:** what do I know that I haven't said? Prerequisites, vocabulary, the step I no longer notice myself doing.

   *(Elements 2, 3, 6, and 7.)*

3. **Script the think-aloud from the audit.** Every decision found under *Context* goes into the modeled demonstration, said out loud. If the audit found a decision you make automatically, the model has to show it. *(Element 7.)*

4. **Choose examples and non-examples at the boundaries.** Use the *Boundaries* list. Include the near-misses that look like the target but aren't, and the targets that look like near-misses. *(Element 9.)*

5. **Write the checks as discriminating tests.** For each likely misinterpretation found in steps 2–4, write one check item that a student holding that misinterpretation would get wrong *in a predictable way*. Note in the plan what each wrong answer means. *(Elements 11, 12, and 13.)*

6. **Peer-verify the plan.** Give the plan to a colleague who didn't write it and ask them to predict what a struggling student will do with each practice item. This is §12.3's peer verification applied to teaching: if the colleague's predictions differ from yours, the plan has a gap.

7. **Teach, compare, and revise the specification.** After the lesson, compare student output with the success criterion. Where errors cluster, revise the plan, not the class's reputation, and record the change so the next delivery starts from a better specification. *(Corrections and feedback; weekly and monthly review.)*

Steps 2, 5, and 6 are the ones a teacher without specification-literacy training most often skips. They aren't extra Explicit Instruction elements. They are the *quality control* that makes the existing elements work.

---

## 5. Worked Example: Rounding Decimals (Grade 5)

### 5.1 The first draft

> **Objective:** Students will understand how to round decimals to the nearest tenth.
> **Model:** Teacher demonstrates rounding 4.37 and 2.81 on the board.
> **Practice:** Worksheet, problems 1–20.
> **Check:** Exit ticket, three problems.

This draft contains most of the elements of Explicit Instruction: a goal, a model, practice, and a check. It is still underspecified, and an Assumption Audit shows where.

### 5.2 The audit

- **Types.** "Understand" doesn't say whether students must carry out the procedure (procedural), explain why it works (declarative), or decide when rounding to tenths is appropriate (conditional). The draft only practices the first kind.
- **Boundaries.** Both modeled examples are easy cases. Neither shows:
  - a digit of exactly 5 in the hundredths place (2.45);
  - a round-up that carries into the ones place (3.96 → 4.0);
  - a number with more than two decimal places (7.349, where students sometimes round twice, 7.349 → 7.35 → 7.4, instead of once, giving 7.3);
  - a number already at the tenths place (6.2).
- **Defaults.** Is "4" an acceptable answer for 3.96, or must it be "4.0"? The draft doesn't say, so students will choose, and they will choose differently. Truncation (4.37 → 4.3) is the default procedure many students already have, and nothing in the draft separates rounding from it.
- **Context.** The teacher no longer notices that rounding to the tenths depends on identifying which digit *is* the tenths digit, a place-value prerequisite the draft never reviews. The teacher also looks only at the hundredths digit without saying so, and that unspoken step is what students who round twice are missing.

### 5.3 The revised plan

> **Success criterion (procedural and conditional):** Given any decimal with up to three decimal places, students round it to the nearest tenth, write the answer with exactly one decimal place, and state which digit they looked at to decide.
>
> **Review (precondition check):** Three quick whiteboard items: *underline the tenths digit* in 5.672, 0.48, and 12.3. Every student's board is visible. If more than a few students miss these, reteach place value before continuing.
>
> **Model (think-aloud script):** "I find the tenths digit. Now I look at *only* the next digit to the right, the hundredths, and nothing past it. If that digit is 5 or more, the tenths digit goes up by one; otherwise it stays the same. Then I drop everything after the tenths. I always write one decimal place, even if it's a zero."
> Modeled examples, in order: 4.37 (stays), 2.81 (stays), 2.45 (exactly 5, goes up), 3.96 (carries into the ones), 7.349 (look only at the 4).
>
> **Non-examples, named aloud:** "4.37 → 4.3 is *cutting off*, not rounding; it ignores the next digit." "7.349 → 7.35 → 7.4 is rounding *twice*; we only ever look at one digit." "3.96 → 4 is the right value but doesn't show the tenths place."
>
> **Guided practice:** Six items done together, one targeting each boundary. Students answer on whiteboards before the teacher shows the reasoning.
>
> **Check for understanding (discriminating items):**
> | Item | Correct | Wrong answer → what it means |
> |---|---|---|
> | 5.26 | 5.3 | 5.2 → truncating, not rounding |
> | 8.95 | 9.0 | 8.10 → carry not understood; 8.9 → truncating |
> | 1.349 | 1.3 | 1.4 → rounding twice |
> | 6.2 | 6.2 | 6.20 or 6 → output format not specified clearly enough; revisit the model |
>
> **Success threshold:** About 80 percent correct on guided practice before moving to independent practice. If one wrong answer accounts for most of the errors, revise the corresponding part of the model and reteach it, rather than assigning more of the same practice.

The revision adds no new content and takes only a few minutes longer to teach. It replaces "the teacher hopes the examples generalize" with "the teacher has specified the boundary, shown both sides of it, and written a test that tells them which misreading each student holds." That is the difference specification literacy makes to an Explicit Instruction lesson.

---

## 6. Where the Overlap Ends

The correspondence is close, but not complete, and the gaps run in both directions.

**Where Explicit Instruction is weakest, specification literacy has something to add.** Critics of how Rosenshine's principles are applied in schools point out that the evidence is strongest for well-structured skills: knowledge and procedures that can be broken into clear steps.[^ttk] It is weaker for ill-structured domains, and for teaching students to approach problems they haven't seen before. Rosenshine and Stevens themselves warned against assuming the procedures apply to all subjects, all learners, all the time.[^ttk] Noticing what you didn't say is a classic ill-structured skill: the gap is invisible from the inside (§2). Much of this framework, especially the Assumption Audit, is an attempt to give that skill teachable steps, so that it *can* be taught explicitly. Specification literacy doesn't depend on Explicit Instruction being right about every domain. It extends the range of skills Explicit Instruction can reach.

**Where specification literacy is incomplete, Explicit Instruction has something to add.** The framework says what students should be able to do at each band (§10) but says little about *how* to sequence, model, and practice those skills. Section 10.3 already notes that the 6–8 band is "where explicit instruction becomes most powerful." The sixteen elements are a ready-made delivery method for the framework's own anchor courses: model the Assumption Audit with a think-aloud, give examples and non-examples of underspecified instructions, guide practice on peer artifacts, check discriminating items, and fade support until students audit their own work unprompted.

**On authority, the two frameworks pull in different directions.** In common practice, Explicit Instruction positions the teacher as the source of correct interpretation. Specification literacy insists that when an instruction is ambiguous, the error belongs to the instruction, and that students who ask for clearer instructions are showing the skill working (§12.5, §12.6). A specification-literate teacher practicing Explicit Instruction keeps both: they deliver clear, structured instruction *and* invite students to find its gaps. The second habit is the better test of the first.

**On scaffolding, the endpoints differ.** Explicit Instruction fades support until students perform the taught skill independently. In specification literacy, the endpoint is students *writing* specifications for others: becoming authors as well as interpreters. A lesson on the Assumption Audit can be taught explicitly, but its last independent-practice task should be a student auditing someone else's specification, and eventually their own.

**On overuse.** The same critics warn that Rosenshine's principles have hardened into a fixed methodology in many schools and are sometimes judged by observation checklists.[^ttk] A specification-literate reading of that warning is that the sixteen elements are themselves a specification, and can be applied without understanding just as easily as a student can round without understanding. The protocol in §4 is designed to prevent this. Its emphasis is on finding gaps in a particular lesson for a particular group of students, not on showing that each element was present.

---

## 7. Implications for the Framework

1. **Specification literacy is a teacher competency, not only a student outcome.** The framework's practical guide (§12) already asks teachers to name underspecification when it appears. This document goes a step further: teachers can apply the Assumption Audit to their own lesson plans. Teacher professional development in specification literacy should include auditing and peer-verifying lesson plans, using the protocol in §4.

2. **The anchor courses can borrow Explicit Instruction's delivery structure.** The 6–8 course and the adult course already teach the Assumption Audit as a named diagnostic. Organizing each session around Rosenshine and Stevens's six teaching functions — review, presentation with think-aloud and non-examples, guided practice, correction, independent practice, cumulative review — would give the courses a well-studied delivery model without changing what they teach.

3. **Lesson plans are good material for teaching specification literacy to adults.** For the adult cohort, a lesson plan is an unusually clear specification: its interpreters are real, its output is observable, and its failures (misconceptions) are well documented. A short exercise in which participants audit a lesson plan for a skill they know well would make the expert's curse concrete.

---

## Notes

[^archer]: Anita L. Archer and Charles A. Hughes, *Explicit Instruction: Effective and Efficient Teaching* (Guilford Press, 2011), ch. 1, "Exploring the Foundations of Explicit Instruction," https://www.guilford.com/excerpts/archer_ch1.pdf. The chapter gives the sixteen elements (Figure 1.1), reproduces Rosenshine and Stevens's six teaching functions (Figure 1.2), describes three forms of knowledge (declarative, procedural, conditional; Figure 1.3), and cites Brophy and Evertson (1976) for success rates of about 80 percent during initial instruction and 90–95 percent during independent work. Also summarized by Reading Rockets, "16 Elements of Explicit Instruction," https://www.readingrockets.org/topics/curriculum-and-instruction/articles/16-elements-explicit-instruction.

[^keys]: Keys to Literacy, "What Is Direct, Systematic and Explicit Instruction?," https://keystoliteracy.com/blog/what-is-direct-systematic-and-explicit-instruction/. The post distinguishes *direct* instruction (a teaching sequence), *systematic* instruction (planned progression from simple to complex), and *explicit* instruction (clarity of explanation and modeling).

[^rosenshine2012]: Barak Rosenshine, "Principles of Instruction: Research-Based Strategies That All Teachers Should Know," *American Educator* 36(1), 12–19, 39 (Spring 2012), https://www.aft.org/sites/default/files/Rosenshine.pdf. The ten principles draw on cognitive science, observation of effective teachers, and studies of cognitive supports such as modeling, worked examples, and scaffolds.

[^rs1986]: Barak Rosenshine and Robert Stevens, "Teaching Functions," in M. C. Wittrock (ed.), *Handbook of Research on Teaching*, 3rd ed. (Macmillan, 1986), 376–391. The six functions are cited here as reproduced in Archer and Hughes (2011), Figure 1.2.

[^sold]: *Sold a Story*, season 2, episode 2, "The Remedy Is Always Teaching" (APM Reports, 2026), at 00:12:10, https://features.apmreports.org/sold-a-story/. The season looks at teaching more broadly, beginning with Siegfried "Zig" Engelmann's experimental preschool in Illinois in the 1960s.

[^engelmann]: Siegfried Engelmann and Douglas Carnine, *Theory of Instruction: Principles and Applications* (Irvington, 1982; rev. ed. ADI Press, 1991). The book develops faultless communication through the analysis of three systems: the communication, the learner, and the knowledge being taught.

[^ttk]: TeacherToolkit, "Potential Pitfalls of Rosenshine's Principles," https://www.teachertoolkit.co.uk/?p=261020.
