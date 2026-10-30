# Designing an Introduction sentence by sentence

Use for an Introduction outline, draft, reverse outline, or substantive revision.
The deliverable is an intelligible argument, not a completed template. Follow the
author's requested scope and language; do not rewrite the research thesis silently.

## Contents

- [Start from the evidence and reader](#start-from-the-evidence-and-reader)
- [Choose a route](#choose-a-route)
- [Use the case base at the needed depth](#use-the-case-base-at-the-needed-depth)
- [Assign sentence jobs](#assign-sentence-jobs)
- [Connect adjacent sentences](#connect-adjacent-sentences)
- [Build paragraphs that change the argument](#build-paragraphs-that-change-the-argument)
- [Draft and revise](#draft-and-revise)
- [Worked repair](#worked-repair)
- [Audit the argument](#audit-the-argument)
- [Align the Abstract](#align-the-abstract)

## Start from the evidence and reader

Before arranging sentences, identify the target reader, task and setting, strongest
supported takeaway, closest alternatives, available evidence, and unresolved claims.
Use supplied material first. If a fact is missing, mark that fact; continue drafting
what is supported. A working Introduction does not require completed experiments.

Keep five distinctions visible in planning:

| Status | Permitted treatment |
|---|---|
| Established background | Attribute to a source supporting this exact scope. |
| Measured observation or proved result | Name the comparison/assumptions and locator. |
| Interpretation | Explain the inference; preserve plausible alternatives. |
| Proposed design or hypothesis | State what is proposed or will be tested. |
| Unknown | Mark a citation/result need; never turn it into a finding. |

An implementation can support an interface claim without proving empirical benefit.
A diagnostic intervention may motivate a design without uniquely identifying the
cause of failure. A benchmark advantage is not a deployment or clinical guarantee.

Choose the narrowest opening that lets the intended reader understand the stakes.
A specialized ML audience may need the unresolved constraint immediately; an
interdisciplinary audience may need a concrete use case and one definition first.
Neither a broad background opening nor a contribution-first opening is universally
correct. Do not infer an ideal sentence count from a published example.

## Choose a route

These are fork-maintainer design patterns, synthesized from the sources and cases;
they are not a validated taxonomy or instructions to manufacture the missing steps.
Choose one dominant route, borrowing another move only when the argument needs it.

| Route | Use when | Dependency order | Evidence needed / avoid |
|---|---|---|---|
| Specific gap | A consequential requirement remains unmet by named alternatives. | Task → relevant progress → residual limitation → consequence → response → evidence. | Establish the limitation within a defined scope; absence from a short search is not proof of novelty. |
| Diagnostic finding to intervention | There is a surprising failure, an informative comparison and a supported response. | Expectation → observation → plausible explanations → intervention → bounded inference → practical constraint → design → evaluation. | Distinguish observed failure from an explanation. If no response is established, end at the finding or hypothesis instead. |
| Phenomenon or explanatory hypothesis | The contribution is revealing or organizing a behavior, not fixing it. | Relevant expectation → operationally defined phenomenon → varied tests → bounded explanation/hypothesis → implications and open questions. | Separate finding, explanation and conjecture; a phenomenon can be a complete contribution without a new solver. |
| Controlled audit or negative finding | A prevailing conclusion changes under a fairer comparison, omitted baseline or controlled protocol. | Existing conclusion → evaluation vulnerability → aligned comparison → result → revised conclusion → scope. | Explain what was controlled; failure of selected methods does not refute a whole research direction. No repair algorithm is required. |
| Assumption change | A familiar task's assumptions differ from the intended setting. | Existing capability → assumption → concrete violation → new setting → inadequacy of direct reuse → response → evidence. | Cite the original assumption and establish the new setting's relevance. Redefining a task alone does not demonstrate usefulness. |
| Representation or interface | A missing explicit object or separation obstructs a specific operation. | Needed operation → current interface boundary → consequence → representation/contract → what it enables → tests and limits. | Show an actual interface difference. Inspectability, traceability, fidelity and correctness are different claims. Do not declare all earlier reasoning hidden. |
| Trade-off or computational bottleneck | A mechanism constrains cost or competing objectives. | Capability → mechanism → bottleneck → existing mitigations → remaining constraint → alternative → matched evaluation. | Explain why mitigations do not remove the constraint. Compare resources and objectives fairly; no free-lunch claim. |
| Theory or mathematical result | A precise question can be answered under explicit assumptions. | Problem or main theorem → relevant prior result → unresolved regime → precise statement → useful reformulation/proof obstacle → proof idea → consequence and limits. | Keep upper/lower bounds, existence/constructive results and worst/average cases distinct. Theorem-first and problem-first are alternatives. |
| Benchmark or measurement | The missing contribution is a valid measurement, not a new solver. | Intended capability → existing measurement boundary → missed behavior → operational definition → instrument/data → validation and use. | Establish construct validity, leakage controls and scope; a new dataset is not automatically a new scientific finding. |

These **nine** routes are overlapping planning choices, not nine mutually exclusive
paper classes. EOE uses diagnosis; ZS-NTTA also changes assumptions. Deep Double
Descent introduces a phenomenon and hypothesis without a repair algorithm. The
neural-recommendation audit and Rethinking ImageNet Pre-training reconsider a
conclusion through comparisons. Transformer, FlashAttention and PagedAttention
develop different computational constraints. Marton presents a theorem before its
history, then changes to an entropic formulation. GLUE, WILDS and HELM make different
measurement arguments. Read the relevant case and its limits before transferring a
pattern; occurrence in a successful paper does not establish optimality.

## Use the case base at the needed depth

For routine drafting, use the route table and the relevant card in
[the route playbook](introduction-route-playbook.md). For close reverse outlining,
use [the corpus index](introduction-deep-review.md) to select one primary case and
one structurally different case. Each corpus entry links the fixed source, complete
map of its declared Introduction scope, pivotal warrants and evidence limits.
The [three pilot worked examples](introduction-worked-examples.md) remain a compact
entry point; they are not the entire evidence base.

Read at three resolutions: paragraph entry/exit; individual sentences or explicitly
identified formal blocks; and the pivotal bridge into a result, design or proof.
A full map does not mean every sentence deserves the same commentary. Spend most
attention where claim strength, assumptions, objects or comparison axes change.
Do not report grouped theorem blocks, clauses or bullet fragments as plain sentences.

## Assign sentence jobs

A job is a reader-facing function, not a mandatory sentence slot. One sentence may
do two compatible jobs (e.g., credit prior success and introduce the disputed design).
One complex claim may need several sentences. Do not split a condition away from
the claim it qualifies simply to satisfy a one-idea slogan.

| Job | Reader question it answers | What must already be available | What it licenses next / common failure |
|---|---|---|---|
| Orient | What task and setting are we discussing? | Audience model. | A concrete stake; avoid generic field celebration. |
| Make the stake concrete | What operation or decision suffers? | Task and user/objective. | A meaningful requirement; importance is not evidence of method efficacy. |
| Define a consequential term | What precisely counts as noise, state, correctness, etc.? | A reason the distinction matters. | Fair comparisons; define before exploiting ambiguity. |
| Credit prior capability | What already works? | Relevant source and scope. | A residual problem, not a straw man. |
| Expose an assumption/mechanism | What does that success depend on? | Named approach or family. | A testable boundary; do not substitute “black box” for a mechanism. |
| State a bounded limitation | Where does the approach fall short? | Setting, criterion and evidence. | A consequence or question; qualify “all,” “cannot,” and “always.” |
| State a consequential gap | Why does that limitation obstruct our objective? | Limitation plus objective. | A design requirement; “not studied before” alone is insufficient. |
| Pose explanations | What could account for the observation? | An observation to explain. | A discriminating test; alternatives need not be exhaustive or mutually exclusive. |
| Describe a diagnostic contrast | What was held fixed and what changed? | Hypotheses, comparator and observed result. | Bounded inference; an idealized intervention is not a deployable method. |
| Supply the warrant | Why does this evidence favor this design direction? | Evidence and its scope. | A justified requirement; do not confuse correlation, possibility and unique cause. |
| State a feasibility boundary | Why not deploy the diagnostic/oracle solution directly? | The useful intervention. | A constrained research question; make unavailable inputs explicit. |
| Formulate the question | What useful capability is needed under what constraint? | Gap and feasibility conditions. | A method that answers it; avoid a question that just spells the acronym. |
| State the design principle | What property should the solution preserve/change? | The justified requirement. | Mechanism selection; a component list is not a principle. |
| Introduce the method | How does the mechanism realize that property? | Principle and minimum vocabulary. | Evaluation; distinguish implemented behavior from hoped-for benefit. |
| Give a minimal example | What would this operation look like? | Defined mechanism. | Understanding, not a claim of typical performance. |
| Differentiate closest work | What changes relative to the strongest relevant alternative? | Comparable inputs, assumptions and mechanism. | Scoped novelty; avoid attacking an entire field. |
| Preview evidence | How will the reader know whether the claim holds? | Main claim and evaluation/proof. | Calibrated confidence; say what remains untested. |
| Summarize contributions | What knowledge, artifact or capability should be retained? | The preceding argument and evidence. | A compact claim contract; avoid “extensive experiments” without a finding. |
| State a formal result | Exactly what is quantified, assumed and guaranteed? | Defined objects or an immediately attached definition. | Comparison and proof; an informal paraphrase cannot replace material hypotheses. |
| Change to an equivalent formulation | Why is this another route to the same target? | The original target and a justified equivalence/reduction. | A more tractable argument; preserve direction, constants and changed assumptions. |
| Explain a proof obstacle | Why does the closest argument not directly extend? | A specific earlier method and the target regime. | The new proof idea; “technically challenging” names no obstacle. |
| State a non-implication | What tempting conclusion does the result not give? | A likely overreading of the central claim. | Calibrated novelty; put this beside the affected result, not in a generic disclaimer. |
| Define an evaluation contract | What observable outcome counts as success? | The intended capability, object or workload. | A defensible test; a convenient score is not automatically the construct itself. |

For a detailed outline or audit, use a small sentence map:

| ID | Sentence or intended proposition | Main job | Depends on | Evidence/status | What this enables next |
|---|---|---|---|---|---|
| S1 | ... | ... | reader knowledge / S0 | source, result, proposal or unknown | ... |

Use explicit IDs for difficult dependencies; ordinary prose is enough for a local
edit. The map is an authoring aid, not manuscript content or a required machine schema.

## Connect adjacent sentences

Identify the logical relationship before adding a transition word. A connective
cannot repair a missing premise. Ask what a skeptical reader would need to accept
the next sentence, and whether it is stated, cited, or genuinely common knowledge.

| Relationship | Test before using it | Repair when it fails |
|---|---|---|
| Elaboration | Does the next sentence explain the same object at greater resolution? | Keep the object explicit; move an unrelated detail. |
| Qualification | Does the limitation apply to the success just described? | Name the setting or assumption; avoid switching populations silently. |
| Contrast | Are the compared alternatives aligned on a relevant axis? | State that axis, e.g., available training data, not merely “however.” |
| Inference | Do the evidence and assumptions warrant the asserted conclusion? | Supply the missing premise, narrow the claim, or mark a hypothesis. |
| Design response | Does this mechanism address the named requirement? | Explain the operation that connects them; naming a framework is insufficient. |
| Example | Is the example an instance of the preceding idea? | Explain the correspondence; do not promote the example to validation. |
| Scope boundary | Does the qualification travel with the affected claim? | Attach it locally rather than burying it in the final limitations paragraph. |

Three practical passes:

1. **Topic continuity:** read sentence subjects and their referents alone. A jump
   from evidence availability to model architecture needs a bridge. Reusing a word
   does not establish a logical relationship.
2. **New-information placement:** put the entity needed to orient the reader early,
   and give the new distinction room to be noticed. The sentence end is a useful
   emphasis location, not a rule requiring inversion of every sentence.
3. **Unpaid inference:** read each “therefore,” “because,” “despite,” and “suggests.”
   Write the missing premise in plain language. If it is unknown, the solution is
   evidence or weaker wording, not a more persuasive transition.

Pronouns are acceptable when their referents are unique. Passive voice is acceptable
when the affected object should remain the topic. Keep exact scientific verbs:
“combine,” “extend,” or “modify” may accurately describe a contribution; replacing
them with “introduce” cannot make it novel. Preserve justified uncertainty.

### Sentence-pair construction patterns

These are optional language shapes, not facts to fill in without evidence. The
bracketed slots are authoring placeholders, never submission-ready claims.

| Pair's purpose | Possible construction | Check before using |
|---|---|---|
| Credit → boundary | “[Approach] supports [operation] when [condition]. In [target setting], [specific condition] is unavailable, leaving [operation] unresolved.” | Verify both the earlier capability and the target constraint. |
| Observation → interpretation | “Holding [factors] fixed, [intervention] changed [outcome] in [scope]. This supports [limited inference], while leaving [alternative] unresolved.” | Report only controls actually held fixed; do not imply unique cause. |
| Constraint → question | “[Useful intervention] requires [unavailable input]. Can [useful property] be obtained under [available-input boundary]?” | The question preserves the task instead of quietly weakening it. |
| Principle → mechanism | “The design separates [responsibilities]. [Mechanism] implements this separation by [concrete operation].” | Architectural separation is not itself evidence of better outcomes. |
| Nearest work → difference | “Like [prior method], we [shared operation]. We differ in [specific mechanism/assumption], which targets [requirement].” | Cite the actual comparator; do not claim superiority from difference alone. |
| Result → scope | “Under [assumptions], [proof/comparison] establishes [claim]. It does not address [relevant untested regime].” | Keep the condition next to the claim; include a limitation only when it matters. |
| Phenomenon → hypothesis | “Across [tested variations], we observe [defined pattern]. We hypothesize [organizing explanation], which predicts [untested or separately tested consequence].” | Mark the hypothesis and its testing status; do not retrofit a mechanism as proved. |
| Audit → revised conclusion | “With [specific comparator/protocol] aligned, [reported contrast] changes. This narrows the earlier conclusion to [supported scope].” | Do not imply controls or baseline tuning that were not performed. |
| Workload → resource consequence | “During [workload operation], [state/resource] must [behavior]. Under [resource model], this induces [bottleneck], limiting [user-visible objective].” | Connect the hardware mechanism to a measured or derived constraint; parameter count alone may not predict cost. |
| Theorem → reformulation | “The target can be expressed as [equivalent statement] under [conditions]. This form exposes [structure], which permits [proof step].” | Equivalence, one-way reduction and heuristic analogy are different claims. |
| Capability → instrument | “To assess [construct], an evaluation must distinguish [behaviors]. We therefore measure [operational observable] while controlling [confound].” | Supply validity reasoning; a benchmark's size or difficulty is not sufficient. |

Vary syntax to fit the manuscript. Explicitly naming every relationship is useful
while planning, but the final text need not repeat these same constructions.

## Build paragraphs that change the argument

Give each paragraph an entry question and an exit takeaway. The middle supplies
the explanation, comparison or evidence needed to get from one to the other.
A topic sentence can state the takeaway first; a diagnostic paragraph can instead
build to a warranted inference. Both are legitimate.

Useful local sequences (choose only what the argument needs):

- **Fair limitation:** demonstrated capability → enabling assumption → condition
  outside that assumption → specific unresolved consequence.
- **Diagnostic paragraph:** observation → explanations → controlled contrast →
  bounded interpretation → what is still unknown.
- **Design paragraph:** requirement → principle → mechanism → correspondence to
  the requirement → nearest alternative or scope limit.
- **Evidence paragraph:** claim → comparison or theorem conditions → result →
  implication at the tested/proved scope.
- **Proof-navigation paragraph:** precise target → obstacle in a familiar route →
  useful formulation or lemma → how it changes the proof → remaining obligation.
- **Measurement paragraph:** construct → failure of an existing proxy → observable
  distinction → instrument/control → what the resulting score can and cannot mean.

The next paragraph should use the previous exit takeaway, not restart the field.
Two consecutive paragraphs with the same exit takeaway may be redundant; a paragraph
with multiple unrelated exits may need restructuring. Do not delete a useful
definition, concession or limitation merely because it adds no new experiment.
Repetition can serve navigation: a long technical report may restate a result in a
contribution list and an evaluation summary. Judge whether the repeated occurrence
serves a distinct reader need; do not copy that length into a short conference paper
or delete all restatement by rule. HELM's nested Introduction and DeepSeek-R1's
evaluation summary are genre-specific contrasts, not length targets.

Place prior work where it does argumentative work: establish capability, identify
an assumption, delimit a gap, or compare the proposed mechanism. A comprehensive
history can go in Related Work. Cite the clause supported by the source, not an
entire mixed paragraph whose claims have different evidence.

Figure 1 is optional. Decide whether it orients, diagnoses, explains a mechanism,
or summarizes results. If it supports a diagnostic inference, the prose must tell
the reader what comparison to inspect and what that comparison does **not** establish.

## Draft and revise

### Drafting from notes

1. Write a one-sentence takeaway at the available evidence strength. If results are
   pending, state a proposed question/design rather than a fictional discovery.
2. Select a route and explain the choice briefly. Identify the strongest plausible
   objection that the Introduction must address; do not invent an adversary.
3. Outline paragraph entry questions and exit takeaways. Resolve the central bridge
   from gap to principle before polishing the opening.
4. For the requested fine-grained pass, assign sentence jobs, dependencies and
   evidence statuses. Missing evidence belongs beside the affected sentence.
5. Draft connected prose. Introduce a method name after, or together with, enough
   purpose for it to mean something. Put implementation inventory in Methods.
6. Read as a newcomer, then as a skeptical expert. Deliver the requested prose or
   outline, a compact explanation of substantive choices, and unresolved needs.

Do not require a contribution approval round if the user already supplied the thesis
or authorized drafting. A local sentence edit does not require this entire workflow.

### Revising an existing Introduction

Reverse-outline what the text actually does before replacing it with a template.
Preserve useful claims, examples, voice, citations, assumptions and their provenance.
For each substantive revision, identify the faulty relationship and repair it:

| Symptom | Underlying problem | Targeted action |
|---|---|---|
| Abrupt “we propose” | Missing design warrant | Explain why the requirement motivates this mechanism. |
| Endless background | No consequential gap | Keep facts needed for the specific unresolved operation. |
| Repeated “however” | Comparisons change axis | Align the comparator/condition, then decide if contrast remains. |
| Many modules, no insight | Architecture substituted for argument | Lead with the operation/principle; retain only essential mechanisms. |
| Strong rhetoric, weak support | Evidence status inflated | Restore scope or a testable hypothesis; do not invent a result. |
| Detailed outline, no requested prose | Analysis displaced the task | Convert the warranted sequence to the requested manuscript form. |
| Every paragraph ends “more research needed” | Gap repeated instead of narrowed | Give each paragraph a different, necessary exit takeaway. |

## Worked repair

**Synthetic exercise; these are invented premises, not a clinical finding.** Supplied:
a candidate-state interface is implemented; one toy example demonstrates inspectable
logs; fidelity evaluation is absent. No broad survey of prior methods is supplied.

Weak: “LLMs revolutionize medicine. Existing methods hide everything. We combine
three modules and solve hallucination.”

An evidence-preserving alternative:

1. “How can a clinical-generation interface expose the candidate assertions it
   passes between processing stages?” — states a design question, not a field-wide gap.
2. “We address this question with an explicit candidate-state interface.” — answers
   the named question before listing implementation components.
3. “The interface makes intermediate candidates available for inspection.” — states
   the supplied interface capability, without claiming they are correct.
4. “A toy example illustrates inspection of the resulting logs.” — attaches the
   demonstration to its actual scope.
5. “Whether this interface improves fidelity remains untested.” — separates the
   design contribution from an unresolved empirical benefit.

Why the repair works: the question introduces the object used by the proposal;
the capability explains the proposal; the example illustrates that capability;
the final sentence limits a likely overinterpretation. A clinical motivation and
comparison to prior interfaces would still require evidence before release.

Do not add a positive result to make this paragraph more exciting. If actual fidelity
measurements become available, rewrite the evidence sentence and reconcile every
dependent contribution and Abstract claim.

## Audit the argument

Use counterfactual questions, not a count of desirable words:

- **Removal:** if this sentence disappears, what definition, premise, distinction,
  evidence or useful orientation is lost? Pure redundancy can go.
- **Swap:** if two sentences swap, does the reader encounter an undefined object or
  unsupported inference? If neither order matters, inspect their relationship.
- **Alternative explanation:** does the diagnostic result exclude the proposed rival,
  merely weaken it, or not test it? Do not upgrade motivation to identification.
- **Obvious alternative:** why not use the strongest existing method or the oracle
  configuration? If there is no supported answer, the gap is not established yet.
- **Mechanism correspondence:** which requirement does each named component satisfy?
  Do not claim causal efficacy merely because the design is plausible.
- **Claim ceiling:** do the comparison, metric, population and uncertainty survive
  compression into the opening, contribution bullets and Abstract?
- **Prior-work fairness:** would an author of the closest work recognize the description?
  A failed search cannot justify “no previous work.”
- **Reader retelling:** can a reader state the question, rationale, method, evidence
  and boundary without reconstructing an unstated premise? For a finding/theory
  paper, substitute the finding, theorem or proof idea for a nonexistent method.
- **Formal scope:** does an informal theorem or consequence retain quantifiers,
  domain, precision/computation model and material constants? Does a reduction run
  in the claimed direction?
- **Measurement scope:** does the evaluation measure the intended construct, or
  merely a convenient proxy? Have benchmark limitations become method promises?

A fluent Introduction with unsupported pivotal claims needs scientific work, not
cosmetic approval. A cautious Introduction that never explains the design rationale
needs argument repair, not just more disclaimers.

## Align the Abstract

Compress the same claim and evidence contract; do not mechanically select each
paragraph's first sentence. A diagnostic paper may lead with the surprising finding;
a design paper may lead with the unmet operation; a theory paper may lead with its
result and assumptions. Keep decisive conditions and unresolved status intact.
The upstream five-sentence Abstract recipe is an option, not a required ordering.

## Provenance and limits

The sentence-job inventory, route table, tests and synthetic repair are original
fork-maintainer synthesis. They operationalize reader-oriented and claim-oriented
guidance; no study establishes this exact workflow as optimal or acceptance-improving.
See `introduction-evidence.md` for the pilot provenance, `introduction-deep-review.md`
for the CS-first expansion and source boundaries, and the linked corpus maps for
critical readings rather than templates to copy. The expanded set informs the nine
routes and twenty-three jobs; neither count is a validated universal inventory.
