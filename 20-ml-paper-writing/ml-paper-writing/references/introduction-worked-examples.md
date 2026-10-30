# Introduction argument maps: three contrasting papers

## Contents

- [How to read these maps](#how-to-read-these-maps)
- [EOE: complete sentence-function map](#eoe-complete-sentence-function-map)
- [ZS-NTTA: targeted transition analysis](#zs-ntta-targeted-transition-analysis)
- [Transformer: a contrasting architecture argument](#transformer-a-contrasting-architecture-argument)
- [What transfers and what does not](#what-transfers-and-what-does-not)

## How to read these maps

These are our critical readings of rhetorical functions, not claims about private
author intent, reproductions of the introductions, or proof that acceptance resulted
from the writing. Consult the linked original beside each map. A prestigious paper
can contain redundant, overbroad or awkward sentences; learn from the argument rather
than declaring every original sentence indispensable.

Versions are fixed below. Paragraph indices refer to non-figure text blocks in the
arXiv HTML Introduction, counting question blocks and contribution items. Sentence
indices ignore abbreviations and citation punctuation. A colon-led announcement
counts as a discourse unit; semicolon clauses do not become new sentences. HTML
paragraph breaks can differ from the PDF, especially where a figure intervenes.

## EOE: complete sentence-function map

Chentao Cao et al., *Envisioning Outlier Exposure by Large Language Models for
Out-of-Distribution Detection*, [arXiv:2406.00806v1, Section 1](https://arxiv.org/html/2406.00806v1#S1)
and [PDF pp. 1–2](https://arxiv.org/pdf/2406.00806v1), ICML 2024.

The central argumentative maneuver is to distinguish a model limitation from a
limitation of its use, then turn an informative but unavailable intervention into a
feasible research question. This interpretation motivates the diagnostic route.

There are **29 units** under the stated convention, including two colon-led
announcements. The maps describe jobs and dependencies rather than translating the
paper sentence by sentence.

| Unit / HTML locator | Main rhetorical job | Dependency and consequence in the argument |
|---|---|---|
| E01 / P1.S1 | Establish conditional success. | Creates the condition that E02 can challenge; success is not asserted without a setting. |
| E02 / P1.S2 | Make a boundary consequential. | Turns E01's condition into a deployment concern; stakes motivate study, not method efficacy. |
| E03 / P1.S3 | Define the research task. | Converts concern into a criterion that later methods must address. |
| E04 / P2.S1 | Credit a successful method family. | Establishes a fair baseline before identifying dependencies. |
| E05 / P2.S2 | Narrow a portability limitation. | Prepares a reason to consider a different task/model setup. |
| E06 / P2.S3 | Identify an unused information channel. | Makes the next methodological development relevant instead of a historical detour. |
| E07 / P2.S4 | Introduce the closest advance. | Answers the objection that earlier limitations have already been addressed. |
| E08 / P2.S5 | Combine credit with a diagnostic target. | The successful design contains the very restriction interrogated next. |
| E09 / P3.S1 | Establish a failure to explain. | Figure 1(a) gives E10 an empirical object, rather than a generic improvement wish. |
| E10 / P3.S2 | Open competing explanations. | Reframes weak performance as a question about capacity versus usage; not an exhaustive dichotomy. |
| E11 / P3.S3 | Supply a discriminating intervention. | Figure 1(b) changes how the same backbone is used; this informs, but does not settle, E10. |
| E12 / P4.S1 | Interpret the intervention. | Bridges observed improvement to a design direction; the inference needs a scope limit. |
| E13 / P4.S2 | Block direct deployment of the oracle. | Without this boundary, readers could mistake E11 for the final solution. |
| E14 / P4.S3 | Signal the question's arrival. | Adds pacing, not independent scientific evidence; could be merged in a shorter version. |
| E15 / P5.S1 | State a constrained research question. | Preserves the useful direction from E12 while respecting E13. |
| E16 / P6.S1 | Introduce a candidate resource. | Follows an established need, so the technology does not have to serve as its own motivation. |
| E17 / P6.S2 | Name the response and its boundary. | Figure 1(c) closes the diagnostic-to-feasible-method sequence. |
| E18 / P6.S3 | Specify a generation criterion. | Converts an appealing resource into a task-directed operation. |
| E19 / P6.S4 | Make that operation concrete. | Lowers interpretation cost; the example is not evidence of broad effectiveness. |
| E20 / P6.S5 | Complete the decision pathway. | Explains that producing intermediate material is not the whole detection method. |
| E21 / P6.S6 | Face nearest-work objections. | A specific comparison axis is stronger than an unsupported uniqueness claim. |
| E22 / P6.S7 | Compress the decisive distinction. | A short sentence fixes the input boundary after a denser comparison. |
| E23 / P7.S1 | Convert design into practical claims. | Each advantage should repay an earlier requirement and later receive evidence. |
| E24 / P8.S1 | Change presentation mode. | Signals a scan-friendly summary; has navigational rather than scientific value. |
| E25 / P9.S1 | State the conceptual contribution. | Recovers the changed perspective, rather than listing a component. |
| E26 / P10.S1 | State the constructive contribution. | Makes the perspective operational. |
| E27 / P10.S2 | Retain the second mechanism. | Keeps the contribution summary aligned with the complete proposed method. |
| E28 / P11.S1 | Announce an empirical claim. | Mostly a lead-in; broad praise adds little without E29's particulars. |
| E29 / P11.S2 | Make the claim inspectable. | Named settings and measurements create obligations for the experimental section. |

### Three bridges to learn

**E08 → E10:** introduce the relevant design choice while crediting prior success.
Then a failure can interrogate that choice. Without E08, readers must reconstruct
why the suggested explanation concerns this baseline.

**E11 → E15:** observation, interpretation, deployment constraint and research
question are distinct jobs. Omitting the interpretation leaves the method unmotivated;
omitting the constraint makes the oracle appear usable; omitting the question makes
the proposed technology appear arbitrary. These jobs can be combined into fewer
sentences, but their logical dependencies cannot be replaced by transition words.

**E18 → E22:** show both how intermediate material is produced and how it is used,
then differentiate from close alternatives along a concrete axis. A list of modules
without this correspondence would not explain the design.

### Figure 1 and evidence limits

Read the three panels as failure, informative idealization, and feasible response.
They are not three equally deployable competitors. The oracle-label experiment
does not establish that backbone capacity is irrelevant or that generated labels
will necessarily reproduce the oracle's benefit. The latter needs its own evidence.
Do not use this example to justify hidden test information in a proposed method.

### What could be shorter or more careful

E14/E16 could be compressed if the question-to-resource transition remains clear.
E28's evaluative praise could yield to specific evidence. Broad claims about earlier
method families should be read in their historical scope, not copied into a new
paper as timeless facts. A minimal outline should preserve the inference chain,
not the original count of sentences or occurrences of “however.”

## ZS-NTTA: targeted transition analysis

Chentao Cao et al., *Noisy Test-Time Adaptation in Vision-Language Models*,
[arXiv:2502.14604v1, Section 1](https://arxiv.org/html/2502.14604v1#S1).
This is a selected-move analysis, **not** a complete sentence inventory.
Noise here concerns membership outside the ID label space; do not silently change
it into mislabeled training data or image corruption when reusing the pattern.

| Locator | Job | Why it matters to the next move |
|---|---|---|
| P1.S1–S3 | Move from a useful adaptation task to an assumption boundary. | An altered setting is motivated before being named. |
| P2.S1–S2 | Define and distinguish the new task. | Readers can see why simply relabeling an existing detection task is insufficient. |
| P2.S3–S5 | Credit adjacent work and delimit compatibility. | The gap is about particular requirements, not absence of all related research. |
| P3.S1–S3 | Establish the comparison and strengthen baselines. | Explaining the filtering provision pre-empts an obvious remedy before presenting failure. |
| P3.S4–S5 | Make the frozen comparator consequential. | The unexpected ranking creates a need for diagnosis, not just another adaptation module. |
| P4.S1–S4 | Connect an analysis procedure to distinct update behaviors. | Intermediate measurements help motivate a mechanism-level explanation. |
| P4.S5–S6 | Consolidate the diagnosis and expose coupled responsibilities. | The proposed separation has a reason tied to the preceding observations. |
| P4.S7 + P5 | Formulate the actionable question. | The question narrows the broad task to the intervention target. |
| P6.S1–S4 | Explain a separation principle before implementation detail. | A frozen component is a deliberate response, not an omission from the system. |
| P6.S5–S6 | Introduce a boundary case and the corresponding repair. | The extra mechanism is justified by a named failure condition. |

Transfer: make obvious alternatives and boundary cases part of the argument before
adding mechanisms. Limit: gradient observations and a few analyses are not license
to infer a universal causal law. Decoupling is one paper's supported design direction,
not a compulsory architectural principle for clinical systems or all adaptation tasks.

## Transformer: a contrasting architecture argument

Ashish Vaswani et al., *Attention Is All You Need*,
[arXiv:1706.03762v7, Section 1](https://arxiv.org/html/1706.03762v7#S1).
This historical version is used for structural contrast, not as a current model
performance recommendation. Its Introduction has eleven sentences in four paragraphs.

| Unit / locator | Function | Dependency to preserve |
|---|---|---|
| T01 / P1.S1 | Credit the established family. | Establishes what later changes must still accomplish. |
| T02 / P1.S2 | Recognize continued progress. | Avoids confusing a structural constraint with a stagnant field. |
| T03 / P2.S1 | Expose how computation is organized. | Makes the coming limitation mechanistic. |
| T04 / P2.S2 | Explain the dependency. | Supplies the premise for a computational consequence. |
| T05 / P2.S3 | Derive the consequential bottleneck. | Connects mechanism to the practical optimization target. |
| T06 / P2.S4 | Acknowledge mitigations. | Addresses the objection that efficiency work already exists. |
| T07 / P2.S5 | Identify what those mitigations leave intact. | Establishes the residual requirement for an alternative. |
| T08 / P3.S1 | Introduce an available capability. | Gives the proposed change a technical basis. |
| T09 / P3.S2 | State the prevailing coupling with an exception. | Avoids claiming that no prior exception exists. |
| T10 / P4.S1 | Present the architectural response. | Answers the specific computational constraint. |
| T11 / P4.S2 | Preview capability and empirical support. | Makes promises for subsequent analysis and experiments to substantiate. |

There is no EOE-style oracle diagnostic, explicit research-question block or
contribution bullet list here. Do not add them to every paper just because another
successful Introduction uses them. The bridge can be a mechanistic argument rather
than a preliminary experiment, provided its premises and scope are supported.

## What transfers and what does not

Across these cases, the useful invariant is a warranted transition from a relevant
limitation to a design and then to evidence. The exact order, sentence count, figure
role and amount of background vary. Historical publication is not a causal experiment
on prose quality. The route names and annotations are our synthesis, not quotations
or labels supplied by the original authors.
