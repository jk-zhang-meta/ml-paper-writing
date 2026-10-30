# Introduction route playbook: sentence-level decisions

Use one relevant card with the [sentence-design guide](introduction-sentence-design.md).
These are conditional planning aids synthesized from the [CS-first case review](introduction-deep-review.md),
not scripts to reproduce. A row is a **possible sentence job**, not a mandatory
sentence, and a theorem/definition may need a block. Keep only supported steps.
The ordering expresses reader dependencies; an informed audience can receive the
answer first, followed by its motivation. Sample wording below is synthetic.

## Contents

- [1. Consequential capability gap](#1-consequential-capability-gap)
- [2. Diagnostic finding to feasible intervention](#2-diagnostic-finding-to-feasible-intervention)
- [3. Phenomenon or explanatory hypothesis](#3-phenomenon-or-explanatory-hypothesis)
- [4. Changed assumption or task setting](#4-changed-assumption-or-task-setting)
- [5. Controlled audit or negative finding](#5-controlled-audit-or-negative-finding)
- [6. Representation or interface](#6-representation-or-interface)
- [7. Workload and computational bottleneck](#7-workload-and-computational-bottleneck)
- [8. Theorem or mathematical result](#8-theorem-or-mathematical-result)
- [9. Benchmark or measurement](#9-benchmark-or-measurement)
- [Choosing, mixing and compressing](#choosing-mixing-and-compressing)

## 1. Consequential capability gap

**Use when:** the evidence establishes a useful operation that named alternatives
do not adequately support. **Do not use to invent novelty:** a missing citation or
an untested benefit does not establish a field-wide gap.

| Step | Proposition the reader needs | Why this sentence belongs / next dependency |
|---|---|---|
| 1 | The task, object and success criterion. | Makes later claims about improvement interpretable. |
| 2 | The strongest relevant capability already available. | Establishes a fair baseline, with its conditions. |
| 3 | The remaining failure or unresolved requirement in a defined regime. | Changes the argument from general progress to this paper's problem. |
| 4 | The operational consequence of that boundary. | Explains why this gap matters beyond being unstudied. |
| 5 | The property a useful response would need. | Bridges the problem to a design without choosing modules arbitrarily. |
| 6 | The mechanism and how it realizes that property. | Makes the proposal an answer to the established requirement. |
| 7 | The decisive comparison and the observed outcome or planned test. | Grounds efficacy separately from plausibility. |
| 8 | The retained contribution and its scope. | Gives the reader a bounded claim to carry into the body. |

**Fine-grained repair:** “Earlier systems are inadequate. We propose X” omits both
the inadequacy criterion and the design warrant. Supply the operation, condition
and requirement before claiming that X addresses it. If only an interface is
implemented, use “supports operation Y”; do not add “improves accuracy.”

**Case contrast:** ResNet's degradation observation sharpens the requirement beyond
a generic capability gap; DDPM balances generative modeling objectives rather than
claiming dominance on every metric. See M02/M03 in the methods corpus.

## 2. Diagnostic finding to feasible intervention

**Use when:** there is an actual diagnostic comparison, a bounded inference and a
response motivated by it. **Avoid when:** the contribution ends with a phenomenon
or negative result; use card 3 or 5 instead.

| Step | Proposition the reader needs | Why this sentence belongs / next dependency |
|---|---|---|
| 1 | A relevant capability and the expectation it creates. | A surprising observation needs a stated expectation. |
| 2 | The measured failure, including setting and comparator. | Defines what requires explanation. |
| 3 | One plausible explanation and what it predicts. | Turns a vague failure into a discriminable claim. |
| 4 | A meaningful rival explanation or untested alternative. | Prevents the preferred story from being assumed in advance. |
| 5 | What the diagnostic intervention changes and holds fixed. | Allows the reader to assess what the test can distinguish. |
| 6 | The result of that intervention. | Supplies evidence before interpretation. |
| 7 | The narrow inference and unresolved alternatives. | Separates a useful clue from unique causal identification. |
| 8 | Why the diagnostic/oracle configuration cannot simply be deployed. | Establishes the practical constraint for the method. |
| 9 | The capability required using available information. | Converts diagnosis into a feasible research question. |
| 10 | The design principle, then the operation that implements it. | Connects the method to the clue instead of jumping to an acronym. |
| 11 | Evaluation of the actual deployable configuration. | Prevents oracle evidence from standing in for method evidence. |

**The pivotal bridge:** a diagnostic result can show that useful information exists
without showing that the proposed method can recover it. Those are two claims and
normally need different evidence. Name the unavailable oracle input locally.

**Case contrast:** EOE (D01) is the main close reading; ZS-NTTA (D02) combines a new
setting with diagnosis and boundary-case handling. Neither licenses attributing
every failure to a single component. DeepSeek-R1 (C02) shows a related second cycle:
the authors' own exploratory model produces the usability limitation motivating
the practical pipeline. The gap need not always be a defect of prior literature.

## 3. Phenomenon or explanatory hypothesis

**Use when:** the scientific contribution is discovering, characterizing or
organizing behavior. A new training algorithm is optional.

| Step | Proposition the reader needs | Why this sentence belongs / next dependency |
|---|---|---|
| 1 | The expectation, conventional account or open empirical question. | Defines the intellectual target without exaggerating consensus. |
| 2 | The variables and observable pattern of interest. | Makes “surprising behavior” operational. |
| 3 | The first observation and the conditions in which it occurs. | Establishes a finding, not yet a general law. |
| 4 | Which variations test its robustness or boundary. | Explains why the result is more than one anecdote. |
| 5 | A second observation that distinguishes plausible accounts. | Adds discriminating information when it exists. |
| 6 | The proposed explanation or organizing hypothesis. | Gives the observations meaning without upgrading conjecture to proof. |
| 7 | A consequence or prediction, with its test status. | Makes the explanation useful and potentially falsifiable. |
| 8 | What the evidence revises and what remains unexplained. | Closes on knowledge, not a fabricated repair. |

**Sentence distinction:** “We observe pattern P” reports a result. “P is consistent
with account H” interprets it. “H predicts Q” introduces a consequence. “We confirm
Q in regime R” requires a separate test. Do not compress all four into “we prove H.”

**Case contrast:** Deep Double Descent (D03) develops a phenomenon and hypothesis;
Understanding Generalization (D04) challenges explanatory accounts; Intriguing
Properties (D10) carries two surprise branches. Lost in the Middle (D05) documents
a limitation without establishing its unique mechanism. These cases counter a
universal failure → new solver → state-of-the-art result template.

## 4. Changed assumption or task setting

**Use when:** the target setting changes an assumption material to existing
capability. **Avoid when:** the only change is a name or an arbitrary restriction
that has not been connected to a real use or scientific question.

| Step | Proposition the reader needs | Why this sentence belongs / next dependency |
|---|---|---|
| 1 | The established task and relevant capability. | Gives a recognizable starting point. |
| 2 | The assumption enabling that capability. | Identifies precisely what is about to change. |
| 3 | A concrete reason the target setting violates it. | Establishes relevance without pretending every use case differs. |
| 4 | The new setting's inputs, permissions and evaluation objective. | Prevents a silent switch of task. |
| 5 | What direct reuse does under those conditions. | Tests the assumption's consequence rather than asserting inadequacy. |
| 6 | The behavior the response must preserve and change. | Avoids fixing the new condition by abandoning the old objective. |
| 7 | A mechanism compatible with the available information. | Makes feasibility visible. |
| 8 | Evaluation under both the changed regime and relevant boundary cases. | Checks that the new definition did not manufacture an easy success. |

**Fine-grained repair:** attach “without source data,” “with contamination,” or a
similar condition to the capability it qualifies. Introduce a new task name after
its distinguishing condition, unless the audience already knows it.

**Case contrast:** ZS-NTTA (D02) and source-hypothesis transfer (D09) make materially
different assumption changes. WILDS (T07) also changes the evaluation setting but
contributes a measurement resource; the same premise can lead to another route.

## 5. Controlled audit or negative finding

**Use when:** revisiting baselines, protocols or confounds changes a prevailing
interpretation. “No new architecture” can be the point of a good comparison.

| Step | Proposition the reader needs | Why this sentence belongs / next dependency |
|---|---|---|
| 1 | The claim or practice under examination. | Defines what the audit may revise. |
| 2 | Why its validity matters for later research or use. | Establishes consequence without demanding a positive method result. |
| 3 | The comparison vulnerability or missing control. | Gives a concrete reason to re-examine the claim. |
| 4 | The aligned protocol, tuning or resource conditions. | Makes the audit fair and reproducible in principle. |
| 5 | The comparison outcome, including unfavorable or mixed results. | Supplies the actual finding. |
| 6 | Which part of the earlier interpretation survives. | Avoids turning a scoped correction into blanket dismissal. |
| 7 | The revised conclusion and unresolved alternatives. | States what is learned rather than only what failed. |
| 8 | An evaluation recommendation or open question, if supported. | Gives a useful consequence without inventing a repair algorithm. |

**Critical distinction:** reproducing a published configuration, tuning a baseline,
and comparing matched compute answer different questions. Name the relevant one.
Failure to reproduce alone does not identify the cause of a published advantage.

**Case contrast:** the neural-recommendation analysis (D06) concerns evaluation and
baselines; Rethinking ImageNet Pre-training (D08) examines the role of pre-training
under training conditions. Do not generalize either to “deep learning does not work.”

## 6. Representation or interface

**Use when:** an explicit object, decomposition or retrieval/action interface
enables a consequential operation. **Avoid when:** a representation's existence
is being substituted for evidence that it is faithful, correct or beneficial.

| Step | Proposition the reader needs | Why this sentence belongs / next dependency |
|---|---|---|
| 1 | The operation that the research needs to perform. | Starts with a purpose rather than a list of components. |
| 2 | How the closest existing representation/interface supports it. | Gives credit and a concrete comparator. |
| 3 | The specific boundary or coupling that obstructs the target operation. | Defines the missing capability without calling all prior work opaque. |
| 4 | The information or responsibility that must become explicit or separate. | Converts the boundary into a design principle. |
| 5 | The proposed object and its input/output contract. | Explains what the new representation actually contains and exposes. |
| 6 | How a reader or system uses it in one minimal example. | Makes the operation intelligible, not empirically validated. |
| 7 | What is equivalent to or different from the nearest approach. | Bounds novelty by mechanism and assumptions. |
| 8 | Separate tests for interface capability and downstream efficacy. | Prevents inspectability from being equated with correctness. |

**Fine-grained repair:** replace “all state is hidden inside models” with a
source-supported description of the specific interface being compared. Then state
the exact new operation. A visible object can still contain unverified assertions.

**Case contrast:** RAG (M05), ReAct (M06) and AlphaEvolve (C01) expose different
objects and feedback paths. AlphaEvolve's evaluator makes search possible and also
limits admissible tasks; its optional LLM feedback and user-defined evaluation do
not constitute universal correctness verification. LoRA (M04) combines a constrained
parameterization with an efficiency argument. None validates an unrelated system's
claimed state fidelity.

## 7. Workload and computational bottleneck

**Use when:** the central limitation follows from resource behavior under a
specified workload. **Avoid when:** a smaller model or lower operation count is
being assumed to imply lower latency without a resource model or measurement.

| Step | Proposition the reader needs | Why this sentence belongs / next dependency |
|---|---|---|
| 1 | The workload and user-visible objective. | Defines what throughput, latency, cost or capacity means here. |
| 2 | The operation and state that consume the limiting resource. | Grounds the problem in a mechanism. |
| 3 | How workload structure creates serialization, movement or waste. | Explains why the resource becomes a bottleneck. |
| 4 | Why existing mitigations leave part of this constraint. | Distinguishes the proposal from simply using known optimization. |
| 5 | The required property under the actual resource model. | Converts the bottleneck into a design requirement. |
| 6 | The algorithm or system mechanism that changes the resource behavior. | Connects an architectural choice to the problem. |
| 7 | What semantics or objective the change preserves and trades off. | Prevents speed from silently changing the task. |
| 8 | The matched workload/hardware comparison and result. | Establishes practical value at a declared scope. |
| 9 | The portability boundary or untested regime. | Separates this measured configuration from universal efficiency. |

**Sentence distinction:** an asymptotic resource bound, wall-clock measurement and
service-level outcome are different evidence. If the body contains all three,
explain their relationship. A lower bound across memory sizes need not establish
pointwise optimality at every size. A reimplemented comparator is not the original
production system; retain that fact when it affects interpretation.

**Case contrast:** Transformer (M01) foregrounds sequential computation;
FlashAttention (M07) models memory traffic; PagedAttention (M08) targets serving
memory management. MapReduce (M09) and Ray (M10) start from workload needs and
distributed execution. These mechanisms require different premises despite sharing
an efficiency route.

## 8. Theorem or mathematical result

**Use when:** the primary contribution is a theorem, bound, impossibility result,
equivalence or proof technique. Choose **problem-first** for readers needing the
question, or **result-first** when the precise result itself supplies orientation.

| Step | Proposition the reader needs | Why this sentence or block belongs / next dependency |
|---|---|---|
| 1 | The question or main result in a recognizable domain. | Gives a specialist a concrete target immediately. |
| 2 | Minimal definitions and material assumptions. | Makes the target intelligible without a full preliminaries section. |
| 3 | The best relevant result and the unresolved regime. | Locates the gain by assumptions, strength or constructiveness. |
| 4 | The exact theorem, with quantifiers and computational model where relevant. | Replaces vague “strong guarantees” with an assessable claim. |
| 5 | The obstacle to extending the nearest proof or technique. | Explains difficulty without using prestige as evidence. |
| 6 | A useful reformulation, reduction or proof idea. | Supplies the conceptual contribution; say why this changes the obstacle. |
| 7 | The key intermediate obligation and where it is discharged. | Gives a reader a route through the body. |
| 8 | A corollary or interpretation, retaining its assumptions. | Explains significance without strengthening the theorem. |
| 9 | A relevant non-implication or unresolved neighboring problem. | Prevents an attractive but invalid extension of the claim. |

**Formal versus informal:** an informal statement can introduce the idea before a
technical theorem, but it must not erase a decisive condition. Infinite-width and
finite-width claims, arbitrary and fixed precision, existence and efficient
construction, asymptotic and finite-sample results are not interchangeable.

**Examples as scaffolding:** if a reader lacks the object, a small instance may
precede the definition. If the audience already knows it, the formal statement can
come first. Gowers's examples-first teaching argument and Tao's audience-oriented
advice support this conditional choice; neither justifies requiring an anecdote in
every mathematical Introduction.

**Case contrast:** nonvacuous generalization bounds (T01), NTK (T02), Turing
completeness (T03), Interlacing Families II (T04) and Marton (C03) pose different
proof obligations. Marton moves from a combinatorial theorem to an equivalent
entropic formulation and preserves an adjacent unsolved question. The formulation
is doing argumentative work, not merely decorating an overview with notation.

## 9. Benchmark or measurement

**Use when:** the contribution makes a capability measurable or reveals a validity
boundary in existing evaluation. A hard or large dataset is not enough by itself.

| Step | Proposition the reader needs | Why this sentence belongs / next dependency |
|---|---|---|
| 1 | The intended capability or use being assessed. | Defines the construct before the metric. |
| 2 | What existing evaluation successfully measures. | Preserves credit and avoids a straw man. |
| 3 | The omitted behavior, saturation or mismatch. | Establishes the measurement need. |
| 4 | A concrete consequence of drawing conclusions from that proxy. | Explains why another score or dataset matters. |
| 5 | The operational distinction a useful test must make. | Bridges the construct to an instrument. |
| 6 | The task/data/protocol design and its validity controls. | Shows how the instrument implements the requirement. |
| 7 | Baselines and evidence that the test discriminates relevant behaviors. | Goes beyond advertising dataset size. |
| 8 | How to interpret scores, coverage and exclusions. | Prevents the instrument from claiming the entire capability. |
| 9 | The resource and the scientific question it enables. | Separates releasing an artifact from establishing a substantive result. |

**Fine-grained repair:** “Existing benchmarks are saturated, so our benchmark
measures intelligence” skips construct definition and validity. State what behavior
the earlier test no longer distinguishes, how the new task operationalizes it, and
what a score still cannot establish. Human baselines, contamination and execution
tests supply different kinds of evidence; none automatically validates all use.

**Case contrast:** GLUE (T05) and SuperGLUE (T06) form a useful renewal pair;
WILDS (T07) changes distribution-shift coverage; HELM (T08) expands dimensions and
transparency; MMLU (T09) and SWE-bench (T10) operationalize different capabilities.
HELM's long nested Introduction is a report structure, not a word-count prescription.

## Choosing, mixing and compressing

1. Identify what the paper actually contributes: a response, phenomenon, correction,
   formulation, guarantee or instrument. If multiple claims exist, give each its
   own evidence rather than using one result to validate the whole bundle.
2. Choose the route whose pivotal bridge can be supported. A diagnostic route
   without a diagnostic test should become a hypothesis or use another route.
3. Borrow a local move when needed. A systems paper may need a theorem; a benchmark
   may begin with an assumption change; a mathematical paper may lead with an example.
4. Compress by removing already-known context and repeated inventories. Keep
   definitions, decisive assumptions, warrants and boundaries that make the central
   inference valid. Do not compress by silently enlarging the claim.
5. Map the Abstract onto the resulting claim contract. It can start with the
   finding or theorem and need not reproduce paragraph order or a fixed sentence count.

The case maps describe what authors wrote and our interpretation of its function.
These cards prescribe choices for a new manuscript. The latter are synthesis, not
measured causal effects of writing style. A counterexample defeats a mandatory
template; it does not establish the opposite template as mandatory.
