# Specification Literacy

## A K–12 Framework for Teaching Precise Thinking Across Subjects and Developmental Stages

**Draft v3 · April 2026**

---

> **Abstract:** This document presents the philosophical foundation for teaching specification literacy across K–12 education — the discipline of describing problems precisely enough that any interpreter, human or machine, will produce the same result. We argue that specification literacy is a foundational skill on par with information literacy and data literacy, and that it develops across a progression from early childhood ("what I meant vs. what I said") through high school ("formal verification of complex systems"). The framework identifies four developmental bands (K–2, 3–5, 6–8, 9–12), maps specification literacy to existing subjects at each band, and presents an anchor course — *Introduction to Problem Architecture*, a year-long 8th-grade course using algorithms and AI — as a proof-of-concept for explicit instruction. The underlying phenomenon — underspecification — is universal across disciplines, and the skills this framework develops transfer to science, law, engineering, communication, and civic life. Specification literacy is not a new subject to be added to an already overcrowded curriculum; it is a disposition that strengthens every subject already taught.

---

## 1. The Case for Specification Literacy

Reading, writing, and arithmetic became universal educational requirements not because every student would become a novelist, essayist, or mathematician. They became requirements because these skills are prerequisite to meaningful participation in society. A citizen who cannot read cannot evaluate the claims made by those who govern them. A citizen who cannot write cannot articulate their own needs. A citizen who cannot reason quantitatively cannot assess whether a policy's promised benefits are plausible.

Over the past two decades, the concept of foundational literacy has expanded. Information literacy — the ability to find, evaluate, and use information — is now recognized as essential in an age of abundant and often unreliable media. Data literacy — the ability to read, interpret, and reason with quantitative evidence — has gained traction as decisions in every domain become increasingly data-driven. These are not niche technical skills; they are baseline competencies for informed citizenship.

We propose that a new foundational literacy is emerging with equal urgency: **specification literacy** — the ability to describe a problem, process, or desired outcome with sufficient precision that any interpreter will produce the same result.

This is not a new practice. Specification has been exercised in specialized domains for centuries. Legal drafting, engineering requirements, scientific protocols, and architectural blueprints are all forms of specification. What is new is the *universality* of the need. As artificial intelligence systems become general-purpose interpreters of human intent — generating code, writing documents, making decisions, and operating in the physical world — every person who interacts with these systems is, whether they know it or not, writing specifications.

The gap between what a person *means* and what they *specify* is where failures occur. This gap is not a technical problem. It is a human problem with technical consequences.

---

## 2. The Underspecification Problem

We define **underspecification** as a description that appears complete to its author because they unconsciously rely on context, assumptions, or defaults not shared by the interpreter. The critical word is *unconsciously*. The author of an underspecified description does not believe they have been ambiguous. The ambiguity is invisible from the inside. It becomes visible only when an interpreter — a colleague, a court, a different laboratory, an AI system — makes a different choice than the author intended.

This phenomenon is documented across every discipline that has studied it.

### 2.1 In Law

In 2017, the U.S. Court of Appeals for the First Circuit ruled that a missing Oxford comma in a Maine overtime statute created sufficient ambiguity to change the statute's meaning. The law exempted workers involved in "the canning, processing, preserving, freezing, drying, marketing, storing, packing for shipment or distribution of" certain foods. Without a comma after "shipment," it was unclear whether "distribution" was a separate exempt activity or part of "packing for shipment or distribution." The resulting settlement cost the employer $5 million.[^1]

The legal philosopher H.L.A. Hart described this phenomenon in 1958: natural language has a "core of certainty" and a "penumbra of doubt."[^2] Contract law exists, in substantial part, to manage the penumbra — to force parties to specify their assumptions before disputes arise. The entire field of statutory interpretation is a systematic response to underspecification in legal texts.

### 2.2 In Science

The reproducibility crisis in science is, in significant measure, an underspecification crisis. A 2016 survey in *Nature* found that more than 70% of researchers had failed to reproduce another scientist's experiments.[^3] While some irreproducibility reflects fraud or statistical errors, a substantial portion stems from methods sections that appear complete to their authors but contain unspecified parameters.

A 2021 paper in *BioTechniques* demonstrated that the common instruction "incubate at room temperature" is a specification failure. Laboratories vary from 18°C to 25°C depending on geography, season, and building design. For temperature-sensitive reactions — enzyme kinetics, microbial growth, RNA degradation — this range can alter experimental outcomes.[^4] The researcher writing "room temperature" believed the instruction was clear because their own laboratory's temperature felt obvious to them. The underspecification was invisible from the inside.

### 2.3 In Engineering

On September 23, 1999, NASA's Mars Climate Orbiter was destroyed during orbital insertion. The proximate cause was a unit mismatch: ground software produced by Lockheed Martin calculated thruster impulse in pound-force seconds, while NASA's trajectory software expected newton-seconds. The error was a factor of 4.45, accumulated over months of small trajectory corrections, and ultimately sent the spacecraft into the Martian atmosphere at 57 kilometers altitude instead of the intended 226 kilometers.[^5]

The interface specification did not explicitly state which unit system to use. Both teams used valid units. Both teams' software was internally correct. The failure was in the specification of the interface between them — a gap that both teams assumed was obvious and neither team documented. The cost was $125 million.

NASA's subsequent investigation identified the root cause not as a unit error but as a failure in systems engineering: the processes and reviews that should have caught the underspecification did not. The specification was not wrong — it was incomplete. And its incompleteness was invisible to the people who wrote it.

### 2.4 The Common Pattern

These examples span law, science, and engineering, but the underlying phenomenon is identical. In each case:

1. An author produced a description they believed was complete.
2. The description contained an ambiguity invisible to the author because they relied on context or assumptions they did not articulate.
3. An interpreter resolved the ambiguity differently than the author intended.
4. The divergence was discovered only after consequences materialized — a lawsuit, an irreproducible result, a destroyed spacecraft.

Every mature discipline has developed systematic practices for finding and eliminating underspecification. Law uses defined-terms sections. Science uses structured reporting guidelines (ARRIVE, CONSORT, PRISMA). Engineering uses requirements review processes and interface control documents. Aviation uses standardized phraseology and readback protocols. These practices share a common structure: they force the author to address known categories of ambiguity before the description reaches an interpreter.

We propose that **specification literacy** — the systematic practice of identifying and resolving underspecification — is a teachable, transferable skill, and that it merits recognition as a foundational literacy alongside information literacy, data literacy, and media literacy.

---

## 3. Why Algorithms Are the Ideal Medium

If specification literacy is the skill, why teach it through algorithms rather than through legal drafting, scientific protocol design, or technical writing?

Three properties of algorithmic problems make them uniquely suited as a pedagogical medium.

### 3.1 Immediate, Unambiguous Feedback

When a student writes a specification for an algorithm and an AI generates code from it, the code either meets the specification or it does not. The feedback is immediate, concrete, and unambiguous. A legal specification's ambiguity may not surface for years; a scientific protocol's underspecification may not be discovered until someone in a different laboratory attempts replication. An algorithmic specification's gaps are revealed in seconds when the program is executed against test cases.

This rapid feedback loop allows students to iterate on their specification skills in a single class session — write a spec, generate a solution, discover gaps, revise, regenerate. The cognitive cycle that takes months or years in professional practice can be compressed into minutes.

### 3.2 Formal Verification Is Possible

Algorithms are one of the few domains where correctness can be proved rather than merely estimated. A student can trace through a binary search on paper and explain why it must find the target if the target exists in a sorted list — or why it must correctly report "not found" if it does not. This is a genuine proof, accessible to a middle school student, that develops the habit of requiring justification rather than accepting plausibility.

Most domains that require specification literacy do not permit this level of formal verification. You cannot prove that a law will be interpreted correctly in all future cases. You cannot prove that a scientific protocol will reproduce in all possible laboratories. But you can prove that a binary search algorithm is correct, and in doing so, you develop the disposition to seek proof wherever it is available and to recognize its absence where it is not.

### 3.3 AI Makes the Underspecification Visible

The introduction of AI coding assistants creates a pedagogical opportunity that did not exist when algorithms were taught through traditional programming instruction. When a student writes code themselves, they resolve their own ambiguities unconsciously as they type. They never see the ambiguity because they resolve it in real time without noticing.

When a student writes a specification and hands it to an AI, the AI resolves the ambiguities independently — and may resolve them differently than the student intended. The gap between intent and specification becomes visible. The student discovers that their "clear" description of the problem was, in fact, ambiguous. This discovery is the central learning event of the anchor course — and in age-appropriate forms, a recurring experience at every grade band.

In this sense, AI is not a shortcut or a crutch. It is a *pedagogical instrument* that makes underspecification observable. The AI's role is analogous to the role of a laboratory microscope: it makes visible what was previously invisible.

---

## 4. The Verification Principle

The framework's central pedagogical norm, formalized in the anchor 8th-grade course and expressed in developmentally appropriate forms at every grade band, is:

> **The Verification Principle:** The output is the beginning, not the end. Whether the interpreter is an AI, a classmate, or a younger sibling following your instructions, your job is to check whether the result matches what you meant — and to figure out why it didn't.

In its formal expression for the algorithmic context: *Working code is the beginning of the assignment, not the end. The AI can write the code. Your job is to prove it's correct, explain why it works, and know its limits.*

This principle addresses the central concern educators raise about AI in the classroom: that students will outsource thinking to AI systems and fail to develop understanding. The Verification Principle does not pretend AI does not exist. It does not restrict AI use. Instead, it redefines what constitutes evidence of learning.

Under traditional instruction, evidence of understanding is the ability to produce a correct solution. Under the Verification Principle, evidence of understanding is the ability to:

1. **Specify** what a correct solution would look like, including edge cases and constraints, before any solution is generated.
2. **Evaluate** a generated solution against the specification, identifying where the solution meets, fails, or exceeds the requirements.
3. **Explain** why the solution is correct — not merely that it is correct, but what mechanism ensures its correctness.
4. **Identify limits** — the preconditions the solution requires, the cases it does not handle, the tradeoffs it embodies.

These four skills — specify, evaluate, explain, identify limits — require deeper understanding than production does. A student who can write a sorting algorithm from memory may be performing a rehearsed procedure. A student who can evaluate an unfamiliar sorting algorithm, explain why it works, and identify the conditions under which it fails has demonstrated genuine comprehension of the underlying principles.

### 4.1 The Calculator Analogy and Its Limits

The introduction of calculators in mathematics education was met with concern that students would stop learning arithmetic. What occurred was more nuanced: calculators shifted the locus of required understanding. Mental computation became less critical; the ability to determine which operation to apply, to estimate whether an answer is reasonable, and to interpret results in context became more critical.

AI and algorithms represent a similar shift, but at greater scale. The calculator automated arithmetic. AI automates a far broader range of cognitive tasks — writing, analysis, code generation, pattern recognition. The corresponding shift in educational emphasis must be proportionally broader. It is no longer sufficient to teach students to perform procedures. It is necessary to teach them to specify what procedures should accomplish, to verify that they accomplish it, and to understand why they work.

The Verification Principle is our answer to the question every educator must now confront: what does learning mean when AI can generate the outputs we traditionally used as evidence of learning?

---

## 5. Specification Literacy as Transferable Skill

Jeannette Wing's influential 2006 paper introduced the concept of "computational thinking" as a universally applicable skill set.[^6] We build on this foundation but propose a more specific claim: the transferable skill is not computational thinking broadly construed, but specification literacy specifically — the discipline of making assumptions explicit, testable, and verifiable.

The following table illustrates how specification literacy, as developed through the anchor course's algorithmic medium, transfers to other domains:

| In This Course | In Science | In Law & Civics | In Daily Life |
|---|---|---|---|
| Write a specification before asking the AI to generate code | Write a hypothesis and methods section before conducting an experiment | Draft contract terms before entering an agreement | Write precise instructions before delegating a task |
| Test against your spec, not against "does it seem to work" | Test against predicted outcomes, not against "do the results look reasonable" | Evaluate a policy against its stated objectives, not against anecdotal evidence | Evaluate whether a product does what the advertisement claimed |
| Find the ambiguities — places where your spec could be interpreted two ways | Identify uncontrolled variables that could confound results | Identify terms in a law that could be interpreted multiple ways | Recognize when instructions could be misunderstood |
| Explain why an algorithm is correct by tracing its logic | Explain why a result supports a hypothesis by tracing the evidence | Explain why a legal argument holds by tracing the reasoning | Explain why a decision was the right one by tracing the criteria |
| Identify what the algorithm cannot do or where it fails | Identify limitations of a study and conditions for external validity | Identify loopholes or unintended consequences of a policy | Identify what could go wrong with a plan |

The structural parallels are not metaphorical. They reflect the same cognitive operation applied in different contexts. A student who has practiced finding underspecification in their algorithmic specs is practicing the same skill a scientist uses when identifying uncontrolled variables, a lawyer uses when finding ambiguities in contract language, and a citizen uses when evaluating whether a policy's stated goals match its actual mechanisms.

---

## 6. AI as Collaborator, Not Crutch

The anchor course positions students as lead collaborators with AI — not passive consumers of AI output and not adversaries trying to catch AI in errors. The relationship is modeled on the professional practice of code review, in which a senior engineer evaluates the work of a junior colleague. The AI generates. The student specifies, evaluates, and decides.

This framing is deliberately chosen to be future-proof. The specific AI tools available to schools will change year to year. A curriculum built around a particular tool's capabilities or limitations will become obsolete as the tool evolves. A curriculum built around the human skills of specification and verification remains valid regardless of how capable the AI becomes.

If the AI is imperfect and produces buggy code, the student practices debugging and correction. If the AI is flawless and produces perfect code, the student practices explanation and justification — proving that the code is correct, not just observing that it works. In either case, the student's task requires genuine understanding. The pedagogy does not depend on any particular level of AI capability.

### 6.1 The Question of Programming Languages

The anchor course currently uses Python because it is widely supported, readable, and well-suited to STEM applications. However, the choice of programming language is explicitly secondary to the specification and verification skills the course teaches.

Crucially, students in the anchor course *read and trace* code — they do not write it from scratch. The prerequisite is the ability to follow Python's logic, not the ability to produce syntactically correct programs. AI generates the code from student specifications; students verify, trace, and explain it. This distinction is fundamental. Writing code requires students to manage syntax, debugging, and language idioms simultaneously with the specification and verification skills the course teaches. Reading code isolates the skills that matter: understanding what the code does, why it is correct, and where it fails. The mechanical act of code production is delegated to AI, just as the mechanical act of arithmetic is delegated to a calculator in a statistics course.

A programming language is, at its core, a subset of human language that has been defined without ambiguity. It is a language in which every statement has exactly one interpretation. This is precisely what makes it useful as a medium for teaching specification: the contrast between the ambiguity of natural language specifications and the precision required by code makes the underspecification problem viscerally apparent to students.

If a new language emerges that is better suited to the anchor course's pedagogical goals — or if AI systems evolve to accept natural language specifications directly — the course can adopt it without altering its philosophy. The foundational skill is specification literacy, not proficiency in any particular programming language.

### 6.2 The Question of AI Model Access

The anchor course is designed to be model-agnostic. Lessons specify the nature of the AI interaction ("prompt the AI to generate a sorting algorithm that meets your specification") without prescribing a particular tool. A companion technical guide maps these interactions to specific tools and provides setup instructions for each.

Practical options for public school deployment include browser-based AI services with free tiers, locally hosted open-source models maintained by school IT departments, and education-specific AI tools as they become available. The curriculum accommodates any of these and can adapt as the landscape evolves. The guiding constraint is that the AI tool should be accessible, reliable, and appropriate for student use under applicable privacy and data protection regulations.

---

## 7. Ethics, Bias, and Specification

Questions of AI ethics and algorithmic bias are important and are addressed within the anchor course. However, the framework's philosophical perspective offers a distinctive lens: bias in AI systems is, in substantial part, an underspecification problem.

When a training dataset reflects demographic imbalances, the specification of that dataset was underspecified — it did not define the population it was intended to represent with sufficient precision, or the assumptions about representativeness were not made explicit. When a model produces outputs that reflect societal prejudices, the specification of the model's objectives was underspecified — the criteria for "correct" output did not account for equity, fairness, or the diversity of contexts in which the model would be deployed.

This is not to say that all bias is accidental or that specification alone can prevent it. Structural inequities, historical injustices, and power dynamics are substantive issues that exceed the scope of a specification. But the specification lens gives students a concrete, actionable framework for engaging with these issues: when an AI system produces biased outputs, one of the first questions to ask is "what was specified, what was assumed, and whose perspective was treated as the default?" This is the underspecification question applied at societal scale.

The course weaves ethical considerations into its existing pedagogy rather than treating them as a separate module. When students evaluate AI-generated solutions, they are asked not only "is this correct?" but "correct for whom, under what assumptions, and with what consequences?"

---

## 8. What Success Looks Like

### 8.1 For the Student

A student who develops specification literacy across K–12 can approach any problem — in STEM, in their community, in their future career — and ask: What exactly am I trying to solve? What would a correct solution look like? How would I verify that I got one? What assumptions am I making that I haven't stated?

They can work productively with AI tools without being dependent on them or deceived by them. They understand that AI-generated output requires the same verification as any other source of claimed truth — and they possess the skills to perform that verification.

They have developed the intellectual habit of seeking precision in their own communication and identifying imprecision in others'. This habit transfers to every discipline they encounter.

### 8.2 For the Institution

This framework demonstrates that specification literacy can be taught as a core competency, not as an elective for students with pre-existing interest in technology. The anchor course provides a replicable model; the cross-curricular integration shows how the competency strengthens every department without adding to their burden.

The framework also demonstrates a viable approach to AI in education — one that neither bans AI tools nor surrenders learning outcomes to them. The Verification Principle provides a framework that administrators, teachers, and parents can understand and endorse: AI is a tool, and we are teaching students to use it rigorously.

### 8.3 For Society

The long-term aspiration is a citizenry equipped to direct AI toward beneficial outcomes. This requires people who can specify what "beneficial" means in concrete, verifiable terms — who can translate values into specifications, evaluate AI systems against those specifications, and hold developers and deployers accountable for the gap between specification and reality.

A population that cannot specify what it wants from AI systems will get whatever the systems' developers specify for them. A population that can specify, verify, and evaluate will be able to participate meaningfully in decisions about how AI is developed, deployed, and governed.

---

## 9. What This Framework Is Not

**This is not vocational training.** The framework does not prepare students to be software engineers, though some will pursue that path. It prepares them to be precise thinkers and effective collaborators with AI tools, regardless of their career direction. Specification skills are no more specific to software engineering than essay-writing skills are specific to journalism.

**This is not "vibe coding."** In the grade bands where AI tools are used (6–8 and 9–12), students do not prompt an AI and accept whatever it produces. The Verification Principle ensures that AI use deepens rather than replaces understanding.

**This is not anti-AI.** The framework does not teach students to fear or reject AI tools. It teaches them to use these tools with the same critical rigor they would apply to any powerful instrument — the same rigor a scientist applies to a microscope, an engineer to a simulation, or a lawyer to a precedent.

**This is not a new subject.** Specification literacy is a disposition — a habit of precise thinking — not a body of content. At most grade bands, it is developed *within* existing subjects, not alongside them. The explicit anchor course at 8th grade is the exception: a dedicated course that names the skill, provides the vocabulary, and builds the formal methods. But even this course is a proof of concept for the competency, not the only pathway to it.

**The anchor course supersedes AP Computer Science A, not supplements it.** Every generation of programming abstraction has redefined the human's role. Assembly programmers managed registers and memory addresses. C programmers managed types and pointers. Java programmers managed objects and inheritance. At each transition, the previous generation's core skill became a detail handled by the new abstraction layer, and the human's job moved up — from managing machine state, to managing program structure, to managing system design. Specification with AI is the next such transition. The human specifies *what* the solution must do and *why* it is correct. The AI handles *how* — the syntax, the implementation details, the language-specific idioms.

AP CS A remains anchored at the Java layer. It teaches students to be the translator — to convert algorithmic intent into syntactically correct code in a specific language. The anchor course teaches students to be the architect — to define what needs to be built, verify that it was built correctly, and understand why the design works. A student who completes the anchor course covers the same algorithmic topics as AP CS A — and more broadly, since the course is not constrained by a single language's idioms. But they engage with those topics at the specification and verification layer rather than the syntax layer. A worked instance of this student-as-architect model already exists at the high-school level, layered onto AP CS A itself: students architect a text-adventure game as a written specification, an AI builder generates it, and the team must explain every line at a walkthrough.[^7]

---

## 10. The K–12 Developmental Progression

Specification literacy is not a skill introduced at a single grade level. It is a cognitive capacity that develops across childhood and adolescence, mapped to the same concrete-to-formal operational transition that Piaget identified and that every subject area navigates in its own way. Children are already practicing proto-specification in kindergarten; by high school, they can engage with formal verification. What changes across the K–12 span is not the *kind* of thinking but its *precision*, *scope*, and *abstraction*.

The framework identifies four developmental bands. Each band describes what specification literacy looks like at that stage, what the central cognitive operation is, and how it manifests across subjects. The bands are not curriculum units — they are lenses through which existing instruction can be recognized, named, and strengthened. A fifth band — adult learners and continuing education (§10.5) — extends the same progression past the end of formal schooling, where the disposition meets real organizational stakes. And although the disposition *develops* bottom-up, from kindergarten upward, the framework is best *deployed* top-down, beginning with adult learners and pushing validated materials down one band at a time — a deliberate inversion taken up in §13.

### 10.1 Band 1: K–2 — The Gap Between What I Meant and What I Said

**Central cognitive operation:** Noticing that the same instruction produces different results from different interpreters.

**Developmental stage:** Pre-operational to early concrete operational. Children at this stage think in terms of specific instances, not categories. They can observe that "draw a house" produced different drawings from different classmates, but they cannot yet systematically identify *why* — they can only notice *that*.

**What specification literacy looks like at this stage:**

Everything at this age is the Sandwich Challenge. "Draw a house" — every child draws a different house because the instruction is underspecified and they each fill in assumptions from their own experience. This isn't a failure; it is the starting point. The teachable moment is noticing the variation: "look, everyone drew something different from the same instruction. What would we need to say to make everyone draw the *same* house?"

The Verification Principle at this level is simple and concrete: "did what happened match what you asked for? If not, what could you say differently next time?" There is no formal language, no abstract framework — just the repeated experience of discovering that your words didn't fully capture your intention.

**Cross-curricular manifestations:**

*Math:* "Put the numbers in order" assumes ascending. A teacher who asks "from smallest to biggest, or biggest to smallest?" is modeling specification refinement. Word problems are specifications for mathematical operations — children who get word problems "wrong" are often reading the specification correctly but interpreting an ambiguity differently than the teacher intended. The teachable moment is not "you got it wrong" but "you read it a different way than I meant — let's figure out where the instruction was unclear."

*Writing:* Even in first grade, "tell me about your weekend" vs. "tell me one thing that happened this weekend, who was there, and how you felt" — the second is a more complete specification for the writing task. Children who "don't know what to write" often have a specification problem, not a creativity problem. They need the constraints tightened, not loosened.

*Art:* "Paint a picture of your family" is expressive art with no verification criterion. "Paint a picture of your family that someone who doesn't know them could use to find them at the airport" is functional art with a specification to verify against. The difference between expressive and functional art is whether there's a specification. Both are valuable; noticing the difference is specification literacy.

*Following directions:* Every game of Simon Says, every recipe in cooking class, every set of instructions for a craft project is a specification. When the result doesn't match the teacher's expectation, the first question should be "was the instruction clear enough?" before "did the child follow it correctly?"

**Teacher's role:** Name the phenomenon. When instructions produce unexpected results, resist the assumption that the child failed to listen. Ask: "was my instruction clear enough, or could it be read two ways?" Model specification refinement by revising your own instructions in front of the class. The vocabulary is simple: "I wasn't specific enough" and "let me try again with more detail."

### 10.2 Band 2: 3–5 — Procedures, Recipes, and Rules

**Central cognitive operation:** Writing multi-step instructions and discovering sequence dependencies and hidden assumptions.

**Developmental stage:** Concrete operational. Children at this stage can follow and produce sequential procedures, classify objects by multiple criteria, and reason about concrete examples — but they generalize from specific instances rather than reasoning about abstract categories.

**What specification literacy looks like at this stage:**

Children begin writing their own multi-step procedures and experiencing what happens when someone else follows them. The feedback loop tightens: it's no longer just "we drew different houses" but "you followed my instructions exactly and it still came out wrong — something was missing from my instructions."

The Verification Principle at this level: "write down the steps. Have someone else follow them. Watch what happens. Fix the steps."

**Cross-curricular manifestations:**

*Science:* Science fair procedures are specifications. "Pour the water into the cup" — how much water? Which cup? What temperature? A 4th grader who writes "pour some water" and a 4th grader who writes "pour 200mL of room-temperature tap water into the 500mL plastic cup" have different specification literacy. The second student's experiment is reproducible; the first's is not. The gauge swatch in knitting, the calibration step in a measurement lab, and the "check your equipment" step in any procedure are all verification steps — the student confirms that the preconditions are met before execution begins.

*Math:* Long division is an algorithm. Children learn it as a procedure, but the specification is implicit — "divide 847 by 3" specifies the operation and the operands but not the expected form of the output. Remainder? Decimal? Fraction? "Show your work" is a verification requirement — it asks the student to make their execution traceable. Children who "show their work" poorly often don't know what level of detail makes a trace useful to someone else. This is a specification problem: the instruction "show your work" is itself underspecified.

*Social studies:* When a 4th-grade class writes their own classroom rules, they are writing specifications for behavior. "Be respectful" is underspecified. "Raise your hand before speaking during class discussion" is verifiable. The arguments that erupt ("I *was* being respectful!") are specification gaps. A class that rewrites "be respectful" as three specific, observable behaviors has done specification refinement.

*Games:* Children at this age invent games constantly, and the games fall apart when two players interpret a rule differently. "You can't do that!" / "The rules don't say I can't!" — this is a state machine gap. Every playground argument about rules is a specification literacy lesson waiting to be named. The child who writes a complete rule set for a game they invented is practicing specification; the arguments that arise during playtesting are the verification feedback loop.

*Music:* Reading sheet music is reading a specification. Playing in a round ("Row, Row, Row Your Boat") is a simple concurrency specification: same code, staggered start times, shared resource (the listener's attention). When it falls apart, it's a synchronization failure.

**Teacher's role:** Make the connection explicit. When a science fair procedure fails to reproduce, say "your instructions had a gap — what did you assume that you didn't write down?" When a classroom rule produces an argument, say "the rule wasn't specific enough — how can we rewrite it so there's no argument?" The vocabulary grows: "assumption," "specific," "step," "what's missing?"

### 10.3 Band 3: 6–8 — The Formal Transition

**Central cognitive operation:** Moving from "here's one specific case that went wrong" (concrete operational) to "here's the *category* of things that could go wrong" (formal operational).

**Developmental stage:** Concrete-to-formal operational transition. Most students at this stage are developing the ability to reason about hypothetical cases, consider multiple possibilities simultaneously, and generalize from specific instances to abstract principles. The transition is uneven — some students are fully formal operational, others are still strongly concrete. The curriculum must scaffold the transition rather than assume it.

**What specification literacy looks like at this stage:**

This is where explicit instruction becomes most powerful. Students are developmentally ready to move beyond "my instructions had a gap" to "what *kinds* of gaps should I look for in every set of instructions?" The Assumption Audit — a systematic method for searching for hidden assumptions — becomes teachable because students can reason about categories (types, boundaries, edge cases) rather than only about specific instances.

The Verification Principle at this level reaches its full formal expression: "Specify. Generate. Trace. Compare. Explain. Find the limits." Algorithms and AI provide the ideal medium because the feedback is immediate and the verification is formal — you can *prove* correctness, not merely observe it.

**The anchor course:** *Introduction to Problem Architecture: Specification Literacy Through Algorithms and AI* is designed for this band. It is a year-long 8th-grade course using a modern block schedule (225 minutes/week, 88 sessions across 36 weeks). The full course outline is documented separately. The course uses five sorting algorithms as vehicles for five design strategies, introduces the Assumption Audit as a growing diagnostic checklist, and culminates in a student-directed capstone research pipeline. Assessment is pass/fail based on verification journals. AI generates all code; students specify, trace, verify, and explain. The course is the proof-of-concept for explicit specification literacy instruction and the foundation for the high school bands.

**Cross-curricular manifestations:**

*Science:* Lab reports are specification documents. The hypothesis is a pre-condition. The procedure is an algorithm. The expected results are post-conditions. The actual results are execution output. The discussion section is the gap analysis. When a student writes "the experiment didn't work," the specification-literate response is "what specifically did you observe that differed from what you predicted, and what assumption might explain the difference?" Every science teacher already teaches this; they don't call it specification literacy.

*Writing/ELA:* A thesis statement is a specification for an essay. "The Great Gatsby is about the American Dream" is underspecified — it doesn't constrain what the essay will argue, only what it will be about. "Fitzgerald uses Gatsby's parties to show that the American Dream is hollow because it substitutes spectacle for substance" is a tighter specification — a reader can predict what the body paragraphs will contain and verify whether they deliver. Peer review of essays is specification verification: does the essay do what the thesis promised? The rubric is the test suite.

*Math:* Proofs. A geometric proof is a verified specification — each step must follow from the previous step by a named rule, and the chain must connect the given to the conclusion with no gaps. Students who struggle with proofs often struggle with the specification, not the geometry — they can *see* that the angles are equal but can't *specify* the chain of reasoning that proves it. Two-column proofs are literally a verification journal format: statement on the left, justification on the right.

*Foreign language:* Translation is specification interpretation across cultural contexts. The student who translates "I'm cold" as "Soy frío" (I am a cold person, personality-wise) instead of "Tengo frío" (I have coldness, physically) has made a specification error — the English sentence was ambiguous and they picked the wrong interpretation.

*History:* Primary source analysis is specification forensics. "All men are created equal" — what did "men" mean in 1776? What did "equal" mean? Historians do specification archaeology — recovering intended meaning from an ambiguous text by examining context, usage, and consequences. When students debate whether the Constitution "specifies" a right to privacy, they are arguing about underspecification in a 230-year-old document.

### 10.4 Band 4: 9–12 — Domain-Specific Rigor

**Central cognitive operation:** Applying specification literacy with discipline-specific formalism — type checking in physics, conservation laws in chemistry, statistical assumptions, design briefs in art, API contracts in computer science.

**Developmental stage:** Formal operational. Students can reason hypothetically, consider multiple interacting systems, and engage with abstract formalisms. The specification literacy disposition developed in earlier bands now encounters domain-specific notation, conventions, and professional standards.

**What specification literacy looks like at this stage:**

Students don't need a dedicated specification literacy course at this level — they need every course to leverage the specification thinking they've already developed. The vocabulary transfers: "what are the preconditions?" is the same question in a physics lab, a statistics class, a design studio, and a courtroom simulation. The habit of asking "what did I assume that I didn't state?" has been practiced for years. Now it encounters the specific ways each discipline handles assumptions.

**Cross-curricular manifestations:**

*Physics:* Dimensional analysis is type checking. If the answer to a velocity problem comes out in kilograms, the specification (equation) has a type error. Unit conversion is type casting. Significant figures are precision specifications — "3.0" and "3.00" are different specifications for the same number because they encode different precision guarantees. The Mars Climate Orbiter is the canonical example of a unit specification failure.

*Chemistry:* A balanced equation is a specification with conservation invariants. The law of conservation of mass is a post-condition that every chemical equation must satisfy. Stoichiometry is verifying that the specification (equation) matches the execution (actual yields) — and the discrepancy (percent yield) is the gap analysis.

*Statistics:* Every statistical test has preconditions (assumptions) that must be satisfied before the test is valid. "Is the data normally distributed?" is a pre-condition check. "Is n > 30?" is a boundary condition. Students who run a t-test without checking assumptions are executing code without reading the specification. P-hacking is a specification violation — the specification says "choose your hypothesis before looking at the data" and the p-hacker violates the precondition.

*Visual art and design:* A creative brief is a specification. "Design a logo for a coffee shop" is underspecified. A proper brief specifies target audience, brand personality, color constraints, size requirements, media where it will appear, and competitive differentiation. Students in AP Art who write artist statements are writing post-hoc specifications — "here's what I intended" — and the viewer's interpretation is the verification.

*Music:* Musical notation is a specification for performance — famously underspecified. "Allegro" means fast, but how fast? Two pianists playing the same Chopin score produce different performances, both "correct." MIDI quantizes this further: every note becomes a number (pitch, velocity, duration). A student who writes a melody in notation and hears it rendered as MIDI experiences the specification gap — technically correct, musically dead. Where did the meaning go? It was never in the spec. At the advanced level, orchestration is specification for a distributed concurrent system: multiple independent performers executing different parts of the same specification, coordinated by a conductor (scheduler) with a shared resource (the audience's attention).

*English/composition:* A research paper's methodology section is a specification for how evidence was gathered and analyzed. "I searched the internet" is underspecified. "I searched JSTOR and Google Scholar for peer-reviewed articles published between 2015 and 2024 using the search terms X, Y, and Z, excluding editorials and opinion pieces" is a reproducible specification. A student who can write the second version can also *read* a research methodology critically — which is media literacy.

*Computer science:* AP CS A teaches specification literacy implicitly through Java: students read specifications (APIs, Javadocs) and implement them. The anchor course's reversal — write the spec and tests first, hand to someone else to implement, assess where the spec broke — is the natural progression. Students who took the anchor course in 8th grade arrive at AP CS A understanding *why* Javadoc specifies preconditions, postconditions, and exception behavior — they've written these contracts themselves. Post-AP capstone projects can assess specification literacy directly: define a data structure, file format, simulation, API, or transformation pipeline precisely enough that a classmate can implement it from the spec alone. A worked instance of this already exists at the high-school level — students architect a text-adventure game as a written specification, an AI builder generates it, and the team must verify the result and explain every line of it at a walkthrough, with "the AI wrote it" graded as the lowest band.[^7]

*Legal studies / civics:* Contract drafting is specification. Defined terms are type declarations. Conditions precedent are preconditions. Indemnification clauses are error handling. "Reasonable efforts" is the legal equivalent of "room temperature" — underspecified until litigated. Mock trial preparation is specification-and-verification applied to argumentation: the prosecution specifies a theory of the case, the defense tests it against the evidence, and the jury verifies.

*Architecture and engineering:* Blueprints and BIM (Building Information Modeling) are computational specifications where every element has properties and relationships. An architect who specifies a window opening without specifying the structural header above it discovers the gap when the BIM clash detection runs — the computational Sandwich Challenge. CAD/CAM manufacturing chains are specification pipelines where each stage's output must satisfy the next stage's input contract.

*Typography and graphic design:* A type designer specifies letterforms as Bézier curves, but the specification must also include hinting instructions for low-resolution rendering. CSS font stacks are priority-ordered specifications with graceful degradation. Color specification (Pantone, sRGB, Display P3) is an attempt to specify a perceptual phenomenon unambiguously across media — and the specification gaps (metamerism, gamut mapping) are visible in every print-vs-screen color mismatch.

*Translation and localization:* A localization spec goes beyond "translate these words" — it specifies date formats, number formats, text direction, pluralization rules (English has 2 forms; Arabic has 6), and cultural adaptation. Unicode's CLDR (Common Locale Data Repository) is a massive specification for how every locale formats every kind of data.

*Choreography:* Labanotation specifies body position, direction, and timing on a vertical staff — but cannot capture weight, quality of movement, or spatial relationship. A dance reconstructed from notation alone is to the original what MIDI is to a live performance. The specification captured the structure but lost the meaning.

*Knitting and fiber arts:* "K2, P2, repeat to end" is a specification in a domain-specific language with zero ambiguity for the practitioner — and total opacity for anyone who doesn't know the language. The gauge swatch is literally a verification step: knit a test sample and measure it against the specification before committing to the full project. This is the Verification Principle enacted in fiber.

### 10.5 Band 5: Adult Learners — Specification Under Stakes

**Central cognitive operation:** Writing, delegating, and verifying specifications in real organizational contexts — where the interpreter, whether an AI, a colleague, or a vendor, acts on your behalf with autonomy, and the cost of underspecification lands immediately on you.

**Developmental stage:** Post-formal, pragmatic reasoning. Adults can hold several things at once that earlier bands cannot: that a specification is *simultaneously* precise and negotiated, that "correct" is stakeholder-dependent rather than fixed, and that a specification is a revisable artifact rather than a final answer. The catch is a developmental irony — deep domain expertise tends to come with *low* meta-awareness of one's own tacit assumptions. The expert knows so much that has become automatic that the knowledge no longer feels like an assumption at all; it feels like the way things obviously are. This is the expert's curse, and it is the precise mechanism of underspecification described in §2, now operating in someone who is, by every other measure, highly competent. The pedagogical opportunity is that the expertise *is* the underspecification: the more an adult knows about their field, the more they leave unsaid, and the more there is to surface.

**What specification literacy looks like at this stage:**

There are no grades and no teacher to resolve an ambiguity by fiat. The stakes are intrinsic — the adult's actual work either improves or it does not, and the feedback comes from clients, managers, vendors, regulators, and the AI systems they direct, not from a rubric. The disposition shows up as a habit: before handing something off, the adult pauses to ask what the interpreter will have to decide that was left undecided. The verification question at this band is: *"When I hand this to an AI that will act on it, how do I know — before the consequences land — that it did what I needed?"*

**Cross-domain manifestations:**

*Knowledge work and drafting:* Prompting an LLM is spec-writing — the Sandwich Challenge moved to the desk of a working professional. "Summarize this for the board" leaves the interpreter to decide for whom, at what level of detail, foregrounding what and dropping what. The adult who is surprised by the summary wrote an underspecified prompt; the adult who got what they needed had already decided those things and said so.

*Law:* AI-assisted contract review and e-discovery search-term design are specification tasks with immediate consequences. "Relevant" is the new "room temperature" — it feels obvious to the attorney who wrote it and resolves differently in the hands of the tool that runs it. The cost of the gap is measured in privilege review and sanctions, not in a returned assignment.

*Software and IT:* Tickets, product requirements documents, and acceptance criteria are specifications handed to implementers — increasingly AI implementers. Reviewing AI-generated code at work is the §4 Verification Principle as a daily professional obligation: the code is the beginning, not the end, and the engineer who merges it without being able to explain why it is correct has not finished the job.

*Marketing and communications:* A campaign brief that specifies audience, message, channel, constraints, and what success looks like is a specification; "make it pop" is not. The difference is who gets to decide — the person who wrote the brief, or whoever or whatever executes it.

*Data and analytics:* "Pull our top customers" — top by revenue, by margin, by lifetime value; over what period; excluding what segments — leaves the analyst to encode choices the requester never stated. The SQL that comes back is a correct execution of an underspecified request, and the disagreement that follows is a specification gap, not a query error.

*Operations and procurement:* RFPs, statements of work, service-level agreements, and "reasonable efforts" clauses are §10.4's legal-studies content, now lived rather than simulated. The defined-terms section is still a set of type declarations; the conditions precedent are still preconditions; but the dispute is real and the money is real.

*Management:* Delegating to a person is writing a specification. The manager who is surprised by what an employee delivered has an underspecification problem, not a bad employee — the instruction relied on context the manager never made explicit, exactly as a methods section relies on a laboratory's unstated room temperature. Recognizing this reframes a great deal of supervisory friction as a specification literacy issue with a specification literacy fix.

*Civic and personal life, at adult stakes:* Filing an insurance claim, disputing a bill, instructing a contractor — each is a specification handed to an interpreter with their own defaults and incentives. The adult who can state precisely what they are claiming, what they are disputing, and what "done" looks like fares better than the one who assumes the other party will fill the gaps the way they would.

**Teacher's role:** Surface the expert's buried assumptions — "you said 'obviously the Q3 numbers'; obvious to whom, and which Q3?" — and do it relentlessly, because the assumptions are invisible to the person who holds them. Treat the learners as **co-designers** rather than students receiving content: they bring real artifacts from their jobs — a prompt that misfired, a brief that produced the wrong thing, a contract clause that got litigated — and the class works on those. The formal vehicle for this band is documented separately, exactly as the 8th-grade anchor course is — the De Anza contract-education course outline (`docs/de-anza-course-outline.md`) — which adapts the framework's pedagogy to working adults: a verification-journal assessment, between-session field assignments at the learner's actual workplace, and a running read-and-trace code thread so that every adult gets at least one taste of *provable* verification and feels its contrast with the merely-plausible verification that dominates professional life.

### 10.6 The Through-Line

The through-line from kindergarten to 12th grade is: **how precisely can you describe what you mean, and how do you know whether what happened matches what you meant?** Every subject teaches this. The framework names it. The anchor course formalizes it. And every subsequent class benefits because students arrive knowing how to ask "what did I assume that I didn't say?"

The developmental progression is not a sequence of courses. It is a sequence of *capacities*:

| Band | Capacity | Verification Question |
|------|----------|----------------------|
| K–2 | Notice the gap between intention and result | "Did it come out the way you wanted?" |
| 3–5 | Write multi-step instructions and test them | "Did someone else get the same result from your steps?" |
| 6–8 | Systematically audit assumptions and categorize failure modes | "What kinds of gaps should you look for?" |
| 9–12 | Apply formal specification methods within each discipline | "What does this domain's notation leave unspecified?" |
| Adult / Continuing Ed | Specify, delegate, and verify under real stakes — when the interpreter acts with autonomy on your behalf | "When I hand this off and it acts for me, how do I know — before the consequences land — that it did what I needed?" |

Each capacity builds on the previous one. A high school student who has never noticed the gap between intention and result (K–2 capacity) cannot systematically audit assumptions (6–8 capacity). A student who has practiced all four arrives at college, at a job, or at a voting booth with the disposition and the method to think precisely about what they want and whether they got it. And an adult who never developed the earlier capacities — who arrives in the workforce without them — can still build them, now under stakes that make the lesson land hard and fast; the fifth capacity is the same skill, exercised where the consequences are no longer hypothetical.

---

## 11. Cross-Curricular Integration

### 11.1 What Improves Without Any Curriculum Changes

Specification literacy is not domain-specific knowledge that conflicts with existing instruction. It is a *disposition* — a habit of precise thinking that students bring with them. In practice, this means:

**In science,** students arrive already understanding that "heat the solution" is underspecified and that a reproducible protocol requires exact temperatures, durations, and equipment. Lab reports improve. The perennial teacher complaint that students cannot write a clear methods section is partially addressed before the student walks through the door. The science teacher does not need to teach specification — they benefit from it having been taught.

**In mathematics,** the transition from computation to proof is one of the most difficult conceptual shifts in secondary education. Students with specification literacy have spent years practicing "explain *why* this is correct, not just *that* it is correct." The disposition toward formal justification — the expectation that a claim requires a mechanism, not just a demonstration — transfers directly to geometric proofs, algebraic reasoning, and statistical inference.

**In English language arts,** argumentative writing requires precisely stated claims supported by evidence that addresses those specific claims — not adjacent ones. The specification discipline ("does my thesis say what I think it says, or could a reader interpret it differently?") maps directly to thesis construction and evidence evaluation. The peer review skills transfer to writing workshops.

**In social studies and civics,** policy analysis requires evaluating whether a law's mechanisms actually achieve its stated objectives — which is the specification-verification loop applied to governance. Students who have studied the Oxford comma case and the Mars orbiter arrive with concrete examples of how imprecise language produces unintended consequences. These examples enrich civics instruction without requiring curriculum changes.

In each case, the effect is additive. Teachers receive students with stronger analytical habits. No existing lesson needs to be removed or modified to accommodate this.

### 11.2 The CS Curriculum Will Need to Evolve

The one area where specification literacy creates productive tension is in existing computer science instruction. A student who has spent a year specifying requirements and verifying AI-generated solutions at the architect level may find it less engaging to hand-write Java syntax for a sorting algorithm they could specify in three sentences and have an AI produce in seconds.

This is not a problem with the student or with this framework. It is signal that the CS curriculum is teaching at an abstraction layer that is becoming, like assembly language before it, a specialist concern rather than a general requirement.

This has happened before. When students arrived at high school proficient with calculators, math courses that spent weeks on long division by hand felt misaligned. The response was not to stop teaching arithmetic — it was to evolve the curriculum upward, spending less time on mechanical computation and more time on problem formulation, estimation, and interpretation. The same evolution is due in computer science education.

Over time, we anticipate that high school CS courses will shift emphasis from code production toward specification, verification, and system design — the same shift the anchor course introduces at the middle school level. This framework may accelerate that transition by producing students who expect and benefit from instruction at the specification layer.

### 11.3 What This Does Not Require of Other Teachers

To be explicit about what this framework does *not* ask of colleagues in other departments:

- **No new content.** Other courses do not need to add specification or algorithms to their curriculum.
- **No new tools.** Other teachers do not need to adopt AI tools or learn Python.
- **No coordination overhead.** The framework's effects transfer through student disposition, not through mandated cross-curricular alignment.
- **No additional assessment burden.** The specification skills transfer passively. No teacher is asked to assess specification literacy — they simply benefit from students who think more precisely.

The only ask of the broader faculty is awareness: if students begin asking more precise questions about assignments, pushing back on ambiguous instructions, or requesting clearer evaluation criteria, that is the specification literacy at work. It should be welcomed, not treated as insubordination.

---

## 12. A Practical Guide for Every Teacher

Section 11 describes what specification literacy improves without curriculum changes. This section describes what any teacher can *do* — tomorrow, in any subject, at any grade level — to develop specification literacy in their students. Nothing here requires new curriculum, new technology, or coordination with other departments. These are teaching practices, not lesson plans.

### 12.1 The One-Sentence Shift

Most teachers already teach specification literacy. They just don't name it, so students don't transfer it across subjects. The science teacher fixes underspecified lab procedures. The English teacher fixes underspecified thesis statements. The math teacher fixes underspecified "show your work." Each teacher solves the problem in isolation, and the student never realizes it's the same skill.

The shift is one sentence. When a student's work doesn't match expectations, before saying "that's wrong," ask: **"Was my instruction clear enough, or could you have read it a different way?"**

Half the time, the answer is yes — the instruction was ambiguous. Name it: "that was underspecified." The student's error was not in execution but in interpretation, and the source of the error was in the instruction, not in the student. Now the concept exists in the classroom. It has a name. It will recur.

This is not a lowering of standards. It is a raising of diagnostic precision. "You got it wrong" tells the student nothing about *why*. "My instruction was ambiguous and you picked a different interpretation than I intended" tells them exactly what happened and shifts the emphasis from blame to clarity. The next time the student encounters an ambiguous instruction — in any class — they have a word for what they're experiencing and a strategy for resolving it: ask for clarification, or state their interpretation before proceeding.

### 12.2 The 15-Minute Sandwich Challenge

The Sandwich Challenge — write instructions, have someone else follow them literally, watch the gap — takes 15 minutes and works in any subject. It is the single most portable specification literacy activity.

**In science:** "Write the procedure for your experiment so that a student in another school could reproduce it without talking to you." Have a classmate attempt to follow the procedure literally. Where they get stuck or do something unexpected, the procedure was underspecified. Fix it.

**In English:** "Write instructions for someone who hasn't read the book to write a paragraph arguing your thesis." Have a partner attempt it from the instructions alone. If the partner's paragraph argues something different from what the student intended, the thesis was underspecified.

**In math:** "Write a set of steps that would let someone else solve this type of problem." Have a partner follow the steps on a new problem. Where the steps break or produce a wrong answer, the instructions had a gap.

**In art:** "Write a brief describing the poster you're going to make — who it's for, what it needs to communicate, what it should look like." After making the poster, compare it to the brief. Where did it diverge? Was that a creative choice or a specification gap?

**In PE/games:** "Write the complete rules for the game we just played." Have another group play from the written rules. Where arguments arise, the rules were underspecified.

**In music:** "Write instructions for how to play this melody so that someone who can read music but has never heard the piece would play it the way you want." Have another student play from the instructions. What was missing?

**In foreign language:** "Translate this English sentence into Spanish." When different students produce different translations, identify the ambiguity in the English that allowed multiple interpretations. The specification problem is in the source language, not in the students' translation skill.

The format is universal because the underlying phenomenon is universal. The subject-specific content changes; the cognitive operation — discovering the gap between what you meant and what you said — does not.

### 12.3 Three Practices That Cost Nothing

These are ongoing classroom habits, not one-time activities. They compound over time as students internalize the questions.

**Practice 1: Spec before you start.**

Before any project, assignment, or lab, have students write what they think a successful outcome looks like — not what they'll *do*, but what the *result* will be.

"My poster will have three sections, each with a claim supported by two pieces of evidence, with source citations for each piece of evidence" is a specification. "I'll make a poster about the water cycle" is not.

The specification becomes the student's own rubric. Students who write their own success criteria before beginning produce better work because they know what they're aiming at. They also self-assess more accurately because they have something concrete to assess against.

This practice scales from kindergarten ("I'm going to draw my house with the red door and the two big trees") through high school ("My research paper will argue that X, using evidence from three peer-reviewed sources published after 2020, addressing the counterargument that Y"). The sophistication of the specification grows with the developmental band; the habit of specifying before executing is the same at every level.

**Practice 2: Peer verification.**

Hand a student's instructions, lab procedure, recipe, proof, thesis, or design brief to another student. Can they reproduce the result or predict the argument from the specification alone, with no conversation with the author?

This is not peer editing — the question is not "is this good?" It is peer *verification* — the question is "could I produce the same result from these instructions?" Where it breaks is where the specification was incomplete. The author then revises not the *work* but the *specification*, and the cycle repeats.

This practice is more rigorous than traditional peer review because it has a concrete success criterion: did the verifier produce the same result? There is no subjective judgment involved. Either the specification was sufficient for independent reproduction or it was not. This clarity makes the feedback actionable and reduces the social discomfort of peer critique — the verifier is not saying "your work is bad," they are saying "your instructions had a gap at step 3."

**Practice 3: Name the assumptions.**

When something goes wrong in class — an experiment fails, an essay misses the point, a group project falls apart, a game produces an argument — ask: **"What did we assume that we didn't say out loud?"**

Post this question on the wall. Make it a classroom refrain. Apply it every time results don't match expectations. Over time, students start asking it *themselves* before things go wrong. They begin to anticipate the gap between intention and instruction. That anticipation is specification literacy.

This practice requires no lesson time. It is a diagnostic question applied in moments that already occur in every classroom — the moments when things don't go as planned. The teacher's only change is to redirect those moments from "who made a mistake?" to "what assumption was hiding?"

### 12.4 Subject-Specific Entry Points

The following practices require zero curriculum change. They are modifications to existing activities, not additions.

**Science.** Add one line to every lab report template: "List three things someone in a different school would need to know to reproduce this experiment that aren't already in your procedure." This is the Assumption Audit in one sentence. Students discover that they've assumed room temperature, local water pressure, specific brands of equipment, the altitude of their school, or the calibration state of their instruments. Each discovery is a specification lesson embedded in existing lab work.

**Mathematics.** When students write solutions, ask: "Would this explanation convince someone who disagrees with you, or only someone who already believes you?" That is the difference between a demonstration and a proof — between showing that a result is correct for one case and specifying the mechanism that makes it correct for all cases. This question bridges the gap between computation and justification without requiring formal proof notation.

**English language arts.** After students write a thesis statement, have a partner predict what the body paragraphs will argue — from the thesis alone, without reading the essay. If the partner can't predict accurately, the thesis is underspecified. This takes five minutes and immediately improves thesis quality because the student sees, in real time, that their "clear" thesis could be read multiple ways. The same practice works for topic sentences within body paragraphs: can a reader predict the paragraph's content from the topic sentence alone?

**Social studies.** When studying a law, policy, or historical document, ask: "What does this *not* say that someone could exploit or interpret differently?" The Oxford Comma Case is memorable, but the same exercise works with the Second Amendment, the school dress code, the cafeteria rules, or the student government constitution. Students find genuine ambiguities in documents that govern their daily lives. This is civic literacy through specification literacy.

**Art and design.** Before starting a project, have students write a brief: audience, purpose, constraints, materials, success criteria. After the project, verify: does the finished work meet the brief? Where did it diverge? Was the divergence an intentional creative choice or an unplanned deviation? This is professional practice in every design studio, and it distinguishes intentional artistic decisions from unexamined assumptions.

**Music.** After learning a piece from notation, ask: "What did the notation *not* tell you that you had to decide for yourself?" Tempo range within a marking, dynamic balance between voices, phrasing at ambiguous boundaries, tone color, rubato — these are all underspecifications in the notation system. The student's performance choices are their resolution of those ambiguities. Naming them as specification gaps gives students language for discussing interpretation and for understanding why two performances of the same piece sound different while both being "correct."

**Physical education and coaching.** Game rules are specifications. When disputes arise during a game, pause and ask: "What does the rule say? What *doesn't* it say? How should we close the gap?" Then have students write the missing rule. This is specification refinement as a five-minute classroom management moment that teaches more about precise language than many formal lessons. It also models democratic governance: the class collectively specifies the rules under which they'll operate, and disputes are resolved by improving the specification rather than by authority.

**Foreign language.** When a translation produces an unintended meaning, name the source: "The English was underspecified — it could mean two things in Spanish, and you picked the other one." This reframes translation errors as specification problems in the *source* language rather than failures of the student's target-language skill. It validates the student's translation ability while teaching them that natural language is inherently ambiguous — which is why specification literacy matters in every language, not just in code.

### 12.5 What Not to Do

**Don't add a unit.** Specification literacy is a disposition, not a body of content. Adding a "specification literacy unit" to a science or English course misses the point. The skill develops through repeated application across contexts, not through isolated instruction. The practices above work precisely because they are integrated into existing activities, not separated from them.

**Don't grade it separately.** "Specification clarity: B+" makes the skill feel like an add-on. Instead, let specification quality be reflected in the work itself: a clearer thesis produces a better essay, a more precise procedure produces a more reproducible experiment. The specification is the means, not the end.

**Don't use the jargon unless it helps.** "Underspecified" is useful because it names a specific phenomenon. "Pre-conditions," "post-conditions," "verification," and "Assumption Audit" are useful in the anchor course where students build formal methods. In a 3rd-grade classroom, "what did we forget to say?" works better than "what was underspecified?" Use the language that serves the students. The concept transfers regardless of the vocabulary.

**Don't correct the student when the instruction was ambiguous.** If a student interpreted an ambiguous instruction differently than you intended, that is a specification failure, not a student failure. Correcting the student without acknowledging the ambiguity teaches them that the authority's interpretation is always right — which is the opposite of specification literacy. Acknowledging the ambiguity teaches them that instructions can be unclear and that asking for clarification is a sign of precision, not confusion.

### 12.6 The Faculty Meeting Version

If a principal or curriculum coordinator wanted to introduce specification literacy to the entire faculty in a single meeting, the message is:

1. **You're already teaching it.** Every time you fix an ambiguous instruction, clarify a rubric, or help a student understand why their work didn't match expectations, you're teaching specification literacy. The only change is to *name* it so students can transfer it.

2. **One question changes everything.** When work doesn't match expectations: "Was my instruction clear enough, or could it be read a different way?" Say it enough times and students start asking it before they begin.

3. **Three free practices.** Spec before you start. Peer verification (not peer editing). Name the assumptions when things go wrong.

4. **It makes your job easier.** Students who write their own success criteria before starting produce better work. Students who verify each other's specifications before working catch problems earlier. Students who name their assumptions make fewer "careless" errors — because most careless errors are actually specification gaps.

5. **The side effect is better questions.** Students may start asking for clearer instructions, pushing back on ambiguous rubrics, or requesting explicit evaluation criteria. This is not insubordination. It is the skill working.

---

## 13. Deployment: Where to Start

A framework that describes a developmental progression invites an obvious assumption: that it should be built in the order children encounter it — start with the kindergartners, then the elementary grades, then middle school, then high school, and let the adult extension follow whenever it follows. That assumption is wrong, and getting it wrong would cost a generation. This section names the tension between the order in which the disposition *develops* and the order in which the framework should be *deployed*, and argues that deployment must run top-down: begin with adult learners at a community college, validate the pedagogy there, and push the proven materials down one band at a time.

### 13.1 The Developmental Order Is Not the Deployment Order

Specification literacy develops bottom-up. A high school senior cannot apply domain-specific formalism if they never learned, in elementary school, to write a procedure someone else could follow; an adult cannot specify under stakes if no one ever named the gap between intention and result. The bands in §10 describe a real cognitive sequence, and nothing in this section disputes it.

But the order in which a capacity matures in a person is not the order in which a curriculum should be created, tested, and rolled out. The two are easily conflated and must not be. A piece of pedagogy is only as good as the evidence that it works, and evidence is generated fastest where the feedback loop is shortest, the participants can consent, and the institutional path to running the next revision is clearest. Those conditions are met not in kindergarten but in adult and continuing education. So the resolution is straightforward: build and validate from the top — adult learners first — and migrate downward as each band's materials are proven. The disposition is constructed in a child from the bottom up; the framework that teaches it is constructed by its authors from the top down. There is no contradiction, only a distinction that has to be held clearly.

### 13.2 Why Community College, Specifically

The first instance of this framework outside the already-designed 8th-grade anchor course should be an adult cohort at a community college. Four reasons converge on that choice.

*Urgency.* The labor market is repricing skills now, not in thirteen years. The people who most need specification literacy *this year* are working adults who are already, untrained, writing specifications to AI systems that act on their behalf — and the institution built to serve exactly those people is the open-access, workforce-facing community college. To start anywhere else is to start with the population whose need is least immediate.

*Autonomy and consent.* Adults enroll voluntarily, can drop a course they find unhelpful, can push back on an exercise that misses, and can give informed feedback as peers rather than as subjects. Piloting a new pedagogy on minors raises consent, equity, and human-subjects concerns that an adult cohort sidesteps entirely. The instinct that it is "easier to experiment with adults" is correct, but the right way to state it is not "experiment on" — it is *iterate with consenting co-designers*. We can move fast precisely because we are not moving fast on anyone who cannot say no; the obligation to a child who cannot consent is discharged by getting the thing right before it ever reaches them.

*A tight feedback loop.* Adults bring real work artifacts — a prompt that misfired, a brief that produced the wrong thing, a contract clause that got litigated — so the §4 verification loop closes inside a single quarter. A kindergarten cohort, by contrast, will not reveal whether the framework produced specification-literate adults for roughly thirteen years. One of those timescales permits revision; the other does not.

*Low institutional friction.* A contract or continuing-education offering launches without curriculum-committee approval, without a Course Outline of Record, without state-standards alignment or textbook adoption. That means the cycle of run, debrief, revise, and run again can happen in consecutive quarters rather than across academic years. Speed of iteration is the whole point, and the contract-education pathway is where iteration is fastest.

The concrete first instance is **De Anza College**, where the author intends to teach an open-enrollment cohort of working professionals from mixed fields as a volunteer, through the contract and Community-Education pathway. The course outline for that cohort and the plan for evaluating it are documented separately, as the 8th-grade anchor course is — see `docs/de-anza-course-outline.md` for the course and `docs/pilot-plan.md` for the pilot and evaluation design.

### 13.3 The Top-Down Sequence

Deployment proceeds in phases, with a gate between each phase: the next phase does not begin until the current one has produced the evidence that justifies it.

**Phase 0, now.** The De Anza contract-education pilot — an open professional cohort, real workplace artifacts, a verification-journal assessment. *Gate:* do adults reliably show the four Verification-Principle behaviors — specify before generating, evaluate against the spec rather than against "seems fine," explain why a verified solution is correct, identify its limits — after a quarter, and do they report that their actual work changed? If not, the framework is revised and the pilot is re-run before anything moves downward.

**Phase 1: the adult track scales, and high-school pilots begin.** The adult course expands — more sections, employer cohorts, a transfer-credit version — and, in parallel, high-school pilots start. The high-school phase does not start from zero: the 9–12 band already exists in §10.4, and there is already a worked high-school instance of the student-as-architect model — [`davidwkeith/ap-cs-a-capstone`](https://github.com/davidwkeith/ap-cs-a-capstone), "The Java Architect Capstone"[^7] — in which students architect a text-adventure game as a written specification, hand the specification to a custom AI builder, and then verify and iterate, with a final walkthrough at which they must explain every line and "the AI wrote it" earns the lowest band. The De Anza materials adapt *down* to the high-school band — its nearest neighbor — alongside that capstone as a template. *Gate:* high-school teachers can run it without the course author in the room.

**Phase 2: stand up the 8th-grade anchor course.** The already-designed *Introduction to Problem Architecture* (§10.3) launches, informed by the lessons of the high-school pilots. This is where the "named introduction" lands — the dedicated course that gives the skill its vocabulary and formal methods — exactly where the framework already says it belongs, but now reached after the bands above it have been validated rather than before.

**Phase 3: elementary, grades 3–5.** The §12 "practices that cost nothing" — spec before you start, peer verification, name the assumptions — become a structured strand rather than a set of optional habits, and elementary teachers are trained to run it. Some of those teachers will have come through the adult track themselves.

**Phase 4: K–2.** By the time the framework reaches kindergarten, there is a decade of materials, a trained-teacher pipeline, and accumulated evidence behind it. The kindergartner who draws a different house from the same instruction meets a teacher who knows exactly what is happening and exactly what to do with it.

Each phase feeds the next in a way that is more than sequential. Adult learners who are also teachers and parents carry the disposition downward into their own classrooms and homes; the pilot cohort is therefore not merely the first audience but part of the rollout mechanism. The framework propagates the way the disposition itself does — through people who have it teaching people who do not.

### 13.4 Why Not Bottom-Up

The obvious alternative is to start in kindergarten and build upward, matching the developmental order. It fails on every dimension that matters. The first beneficiaries of a K-first rollout graduate in roughly thirteen years, and the AI transition will not wait thirteen years for them. A K-first rollout also conducts its first experiments on the population least able to consent, with the longest feedback loop of any band, and through the hardest institutional path — state standards, curriculum committees, textbook adoption — so revisions that an adult cohort absorbs in a quarter take years to reach a classroom. Top-down deployment de-risks all of it: it puts the unproven version in front of consenting adults whose feedback is immediate, validates the pedagogy where validation is cheap and fast, and only then carries the proven version to the children for whom the stakes of getting it wrong are highest and the ability to object is lowest.

---

## 14. Conclusion

The question this framework answers is not "should students learn to code?" It is: in a world where AI systems interpret human intent at scale, what skills must every person have to maintain agency over the systems that act on their behalf?

Our answer is specification literacy: the ability to describe what you want precisely enough that any interpreter — human or machine — will produce the same result. The ability to find the assumptions you didn't know you were making. The ability to verify that what you received is what you needed, not merely what you asked for.

This ability does not emerge fully formed in high school. It develops across childhood — from a kindergartner noticing that "draw a house" produced different drawings, through a 5th grader whose science fair procedure failed to reproduce, through an 8th grader systematically auditing assumptions in algorithmic specifications, to a high school senior applying domain-specific formalism in physics, statistics, legal reasoning, or design.

Algorithms provide an ideal medium for the formal anchor course because they offer immediate feedback, permit formal verification, and — when combined with AI coding assistants — make the underspecification problem viscerally visible. But the skill itself is not about algorithms. It is about the precision of thought and communication that every discipline demands and that the age of AI makes indispensable.

Reading gave citizens access to the ideas of others. Writing gave citizens the ability to articulate their own. Numeracy gave citizens the ability to evaluate quantitative claims. Specification literacy gives citizens the ability to direct the most powerful tools humanity has ever built — and to verify that those tools are doing what was asked of them, not merely what was assumed.

---

## Notes

[^1]: O'Connor v. Oakhurst Dairy, 851 F.3d 69 (1st Cir. 2017). Settled for $5 million in 2018.

[^2]: H.L.A. Hart, "Positivism and the Separation of Law and Morals," *Harvard Law Review* 71(4), 593–629 (1958).

[^3]: Baker, M. "1,500 scientists lift the lid on reproducibility." *Nature* 533, 452–454 (2016).

[^4]: Teixeira da Silva, J.A. "Room Temperature in Scientific Protocols and Experiments Should be Defined: a Reproducibility Issue." *BioTechniques* 70(6), 307–309 (2021).

[^5]: Mars Climate Orbiter Mishap Investigation Board Phase I Report, NASA, November 10, 1999.

[^6]: Wing, J.M. "Computational Thinking." *Communications of the ACM* 49(3), 33–35 (2006).

[^7]: David W. Keith, "The Java Architect Capstone," https://github.com/davidwkeith/ap-cs-a-capstone — a high-school AP CS A capstone in which students architect a text-adventure game as a written specification, an AI builder generates it, and students verify and must explain every line at a walkthrough.
