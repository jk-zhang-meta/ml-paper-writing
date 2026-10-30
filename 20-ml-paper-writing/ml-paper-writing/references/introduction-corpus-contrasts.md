# Recent CS and mathematical contrast cases

These three cases extend the 30-case core review. They were read in full at the fixed versions linked below. The maps are original functional paraphrases, not reproduced Introductions. A source sentence can serve several compatible jobs; assigned jobs are interpretations. `depends_on` in the companion [JSONL](introduction-corpus-contrasts.jsonl) records reading continuity, not causal proof. No result was reproduced and no complete mathematical proof was checked.

## C01 — AlphaEvolve: A coding agent for scientific and algorithmic discovery

[Primary source](https://arxiv.org/html/2506.13131v1); Novikov et al., 2025. Accessed 2026-10-30.

**Scope:** Entire §1 prose; excludes Table 1, caption and footnote; §2.4, §3.1–3.3 and §6 inspected for pivotal claims.

**Segmentation:** 29 prose sentences in eight source paragraphs. HTML paragraph IDs fixed to v1; sentence order follows rendered prose. Dependencies record reading continuity, not causal identification.

**Observed route:** An early proposal is followed by representation rationale, predecessor comparison, an applicability boundary and a result portfolio.

**Use when:** Useful when a single evaluable representation supports multiple concrete domains and the author can name the evaluator's validity boundary.

**Counterexample to a rigid template:** Does not require a single failure experiment or postpone the method name until all prior work is reviewed.

| Unit | Source locator | Function | Why it is here / evidence boundary |
|---|---|---|---|
| C01.P1.U1 | §1 HTML #S1.p1.1, prose sentence 1 | Establish discovery as an iterative activity | Makes iteration the object that an agent could automate. author framing; interpretive rhetorical annotation. |
| C01.P1.U2 | §1 HTML #S1.p1.1, prose sentence 2 | Locate growing interest in LLM-assisted discovery | Moves from the broad activity to the relevant research community. author framing; interpretive rhetorical annotation. |
| C01.P1.U3 | §1 HTML #S1.p1.1, prose sentence 3 | Name the capability sources underlying optimism | Connects model progress and inference-time resources to that interest. cited expectation, not a measured discovery guarantee. |
| C01.P1.U4 | §1 HTML #S1.p1.1, prose sentence 4 | Credit progress on discovery-oriented tasks | Acknowledges existing capability before narrowing the claim. prior-work claim; references not exhaustively reaudited. |
| C01.P1.U5 | §1 HTML #S1.p1.1, prose sentence 5 | Distinguish benchmark progress from genuine new discoveries | Defines the harder target the proposed system will address. author framing; interpretive rhetorical annotation. |
| C01.P2.U1 | §1 HTML #S1.p2.1, prose sentence 1 | Introduce the evolutionary coding approach | Supplies the proposed answer early, before a long prior-work review. method description. |
| C01.P2.U2 | §1 HTML #S1.p2.1, prose sentence 2 | Restrict candidate tasks to automatically evaluable solutions | Defines the applicability condition that makes the feedback loop possible. explicit scope condition. |
| C01.P2.U3 | §1 HTML #S1.p2.1, prose sentence 3 | Choose programs and a population as the search representation | Turns the general approach into an operational representation. method description. |
| C01.P2.U4 | §1 HTML #S1.p2.1, prose sentence 4 | Ground candidate selection in execution and evaluation | Explains how the representation produces feedback. implementation rationale; §2.4. |
| C01.P2.U5 | §1 HTML #S1.p2.1, prose sentence 5 | Assert that evaluation filters incorrect suggestions | Explains the intended safeguard but needs a local evaluator-validity qualification. author claim; correctness is conditional on the evaluator, not universally guaranteed. |
| C01.P3.U1 | §1 HTML #S1.p3.1, prose sentence 1 | Explain how feedback supports diverse candidate exploration | Connects the evaluation mechanism to the search process. mechanism rationale, not an isolated causal test. |
| C01.P3.U2 | §1 HTML #S1.p3.1, prose sentence 2 | Extend algorithm search to objects constructible by algorithms | Expands the scope through an explicit representational bridge. author framing; interpretive rhetorical annotation. |
| C01.P3.U3 | §1 HTML #S1.p3.1, prose sentence 3 | Motivate indirect search as potentially better than direct search | Explains why evolving a constructor can be useful. prior-work-supported possibility, not dominance on every problem. |
| C01.P4.U1 | §1 HTML #S1.p4.1, prose sentence 1 | Situate the approach within evolutionary code generation | Credits the relevant technical lineage. author framing; interpretive rhetorical annotation. |
| C01.P4.U2 | §1 HTML #S1.p4.1, prose sentence 2 | Identify FunSearch as the closest predecessor | Creates a concrete comparison rather than a field-wide gap. author framing; interpretive rhetorical annotation. |
| C01.P4.U3 | §1 HTML #S1.p4.1, prose sentence 3 | List domains in which related approaches were explored | Explains that the idea has a substantial context. author framing; interpretive rhetorical annotation. |
| C01.P4.U4 | §1 HTML #S1.p4.1, prose sentence 4 | Differentiate by program scope and model capability | States the dimensions of the extension. system-design comparison; Table 1. |
| C01.P4.U5 | §1 HTML #S1.p4.1, prose sentence 5 | Infer increased scale and generality from those differences | Gives the reader the proposed consequence of the design. interpretation; empirical scope remains the tested task portfolio. |
| C01.P5.U1 | §1 HTML #S1.p5.1, prose sentence 1 | Turn automated evaluation from advantage into scope limit | Keeps the necessary condition adjacent to the promised capability. explicit exclusion of tasks requiring manual experimentation. |
| C01.P5.U2 | §1 HTML #S1.p5.1, prose sentence 2 | Explain why mathematics, CS and systems are suitable domains | Makes domain selection follow from evaluability. author framing; interpretive rhetorical annotation. |
| C01.P5.U3 | §1 HTML #S1.p5.1, prose sentence 3 | Specify the chosen discovery and optimization task portfolio | Bridges general scope to the evidence that follows. evaluation plan and scope. |
| C01.P6.U1 | §1 HTML #S1.p6.1, prose sentence 1 | Introduce matrix multiplication and a specialized AI comparator | Defines a recognizable algorithmic test case. author framing; interpretive rhetorical annotation. |
| C01.P6.U2 | §1 HTML #S1.p6.1, prose sentence 2 | Preview algorithm discoveries with a concrete arithmetic setting | Supplies a specific result while distinguishing complex-valued matrices. reported findings; §3.1 Table 2; not independently recomputed. |
| C01.P7.U1 | §1 HTML #S1.p7.1, prose sentence 1 | Introduce constructive mathematics as a second evaluation family | Explains how the same search representation transfers. author framing; interpretive rhetorical annotation. |
| C01.P7.U2 | §1 HTML #S1.p7.1, prose sentence 2 | Report matching existing constructions across a problem collection | States one outcome tier of the portfolio. reported aggregate; problem selection is not a random population. |
| C01.P7.U3 | §1 HTML #S1.p7.1, prose sentence 3 | Report improvements on a subset of those problems | Separates improvement from merely matching the prior construction. reported aggregate; not an acceptance or universal-success statistic. |
| C01.P7.U4 | §1 HTML #S1.p7.1, prose sentence 4 | Name concrete mathematical examples | Makes the aggregate result interpretable. reported examples; §3.2. |
| C01.P8.U1 | §1 HTML #S1.p8.1, prose sentence 1 | Preview applications across four engineering layers | Adds systems evidence for the claimed breadth. reported applications; §3.3.1–3.3.4. |
| C01.P8.U2 | §1 HTML #S1.p8.1, prose sentence 2 | Explain the accumulated value of small repeated savings | Connects system-level metrics to deployment relevance. scaling rationale; not a claim of identical benefit in every system. |

### Pivotal transitions checked against the body

- **C01.P2.U2 → C01.P2.U4 → C01.P5.U1:** Automatic evaluation makes feedback operational and simultaneously limits admissible tasks. Source: §1 P2/P5; §2.4 Evaluation; §6 Discussion. Limit: A passing evaluator is only as sound and complete as the task's evaluation contract.
- **C01.P3.U2 → C01.P3.U3:** Searching for a constructing program permits tackling objects as well as algorithms. Source: §1 P3; §6 discussion of direct, constructive-function and search-algorithm modes. Limit: The source explicitly notes that search representations introduce different biases.
- **C01.P6.U2 → C01.P7.U2 → C01.P8.U1:** A result portfolio supports breadth across the selected task families. Source: §3.1 Table 2; §3.2; §3.3.1–3.3.4. Limit: Complex versus real arithmetic, human seeding and workload-specific measurements remain material; selected successes do not establish universal performance.

**Scientific verification limit:** Read the Introduction and selected body evidence; no evaluator execution, algorithm reconstruction or independent correctness proof was performed.

## C02 — DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning

[Primary source](https://arxiv.org/html/2501.12948v1); DeepSeek-AI, 2025. Accessed 2026-10-30.

**Scope:** Entire §1 including §1.1 Contributions and §1.2 Evaluation Summary; §2.2.4, §2.3, §3 and §4.1 inspected for pivotal comparisons. This is the fixed v1 report, not a later publication version.

**Segmentation:** 53 prose sentences across five opening paragraphs and seven list blocks. Nested contribution and evaluation prose is included. Numeric benchmark lists within a sentence remain one unit.

**Observed route:** The narrative contains two linked design cycles: exploratory capability first, then a practical limitation and response; a separate transfer claim follows. Contributions and evaluation intentionally repeat prior content in a technical-report genre.

**Use when:** Useful for a study that actually produced an exploratory system and then an improved pipeline; distinguish the scientific finding from the usable artifact.

**Counterexample to a rigid template:** Not every later design must originate in a failure of prior literature. Broad AGI framing and repeated benchmark inventory are observed choices, not recommended requirements for a short conference Introduction.

| Unit | Source locator | Function | Why it is here / evidence boundary |
|---|---|---|---|
| C02.P1.U1 | §1 HTML #S1.p1.1, prose sentence 1 | Open with broad LLM progress and AGI framing | Supplies field orientation but contributes little to the specific technical gap. broad author framing; not endorsed as a necessary opening. |
| C02.P2.U1 | §1 HTML #S1.p2.1, prose sentence 1 | Identify post-training as the relevant stage | Narrows from the field to the intervention point. author framing; interpretive rhetorical annotation. |
| C02.P2.U2 | §1 HTML #S1.p2.1, prose sentence 2 | Enumerate post-training benefits and resource appeal | Explains why that stage matters. background generalization. |
| C02.P2.U3 | §1 HTML #S1.p2.1, prose sentence 3 | Use o1 as an inference-time scaling precedent | Creates a concrete external capability target. historical priority wording not independently verified. |
| C02.P2.U4 | §1 HTML #S1.p2.1, prose sentence 4 | Describe improvements attributed to longer reasoning | Explains the capability the report wants to reproduce. prior-system claim. |
| C02.P2.U5 | §1 HTML #S1.p2.1, prose sentence 5 | State the unresolved effective-scaling question | Converts the capability target into a research problem. author framing; interpretive rhetorical annotation. |
| C02.P2.U6 | §1 HTML #S1.p2.1, prose sentence 6 | Organize existing attempts into approach families | Credits the relevant search space. author framing; interpretive rhetorical annotation. |
| C02.P2.U7 | §1 HTML #S1.p2.1, prose sentence 7 | Claim a remaining performance gap | Motivates the proposed investigation. broad comparison requiring date, tasks and compute scope. |
| C02.P3.U1 | §1 HTML #S1.p3.1, prose sentence 1 | Announce direct reinforcement learning as the investigated step | Answers the post-training question with a concrete intervention. proposal and reported procedure. |
| C02.P3.U2 | §1 HTML #S1.p3.1, prose sentence 2 | Define the no-supervised-finetuning objective for this stage | Makes the experiment's distinguishing condition explicit. stage-specific claim; does not mean no supervised information anywhere in pretraining. |
| C02.P3.U3 | §1 HTML #S1.p3.1, prose sentence 3 | Name the base model and reinforcement-learning mechanism | Gives the minimum operational identity for the result. method description. |
| C02.P3.U4 | §1 HTML #S1.p3.1, prose sentence 4 | Describe emergent reasoning behaviors | Moves from the procedure to observed qualitative behavior. reported observation; not proof of a unique mechanism. |
| C02.P3.U5 | §1 HTML #S1.p3.1, prose sentence 5 | Preview benchmark performance | Adds quantitative evidence to the qualitative observations. reported evaluation. |
| C02.P3.U6 | §1 HTML #S1.p3.1, prose sentence 6 | Give AIME pass-at-one and majority-vote examples | Makes the gain concrete across distinct inference settings. reported results; pass@1 and voting are different comparisons. |
| C02.P4.U1 | §1 HTML #S1.p4.1, prose sentence 1 | State readability and language-mixing defects of the first system | Uses the authors' own exploratory result to create the next design requirement. reported drawback; §2.2.4. |
| C02.P4.U2 | §1 HTML #S1.p4.1, prose sentence 2 | Introduce a practical pipeline with cold-start data | Presents the response to that newly established limitation. design description. |
| C02.P4.U3 | §1 HTML #S1.p4.1, prose sentence 3 | Describe the initial supervised cold-start stage | Explains where readable traces enter the pipeline. method description; §2.3.1. |
| C02.P4.U4 | §1 HTML #S1.p4.1, prose sentence 4 | Describe reasoning-oriented reinforcement learning | Adds the stage responsible for capability development. method description; §2.3.2. |
| C02.P4.U5 | §1 HTML #S1.p4.1, prose sentence 5 | Describe rejection sampling and mixed supervised data | Explains the next transition in the staged procedure. method description; §2.3.3. |
| C02.P4.U6 | §1 HTML #S1.p4.1, prose sentence 6 | Describe the later reinforcement-learning stage | Completes the pipeline overview. method description; §2.3.4. |
| C02.P4.U7 | §1 HTML #S1.p4.1, prose sentence 7 | Preview the resulting model's benchmark comparison | Returns from mechanism to the promised evidence. reported task-dependent comparison. |
| C02.P5.U1 | §1 HTML #S1.p5.1, prose sentence 1 | Introduce distillation into smaller models | Expands the contribution from a large model to transfer. author framing; interpretive rhetorical annotation. |
| C02.P5.U2 | §1 HTML #S1.p5.1, prose sentence 2 | Contrast distillation with direct RL on a smaller base | Supplies the key comparative observation. reported Table 6 comparison; not an equal-compute theorem. |
| C02.P5.U3 | §1 HTML #S1.p5.1, prose sentence 3 | Interpret the result as evidence for learned reasoning patterns | Explains why the comparison matters scientifically. interpretation; alternative explanations and data/compute differences remain. |
| C02.P5.U4 | §1 HTML #S1.p5.1, prose sentence 4 | State the release of distilled checkpoints | Makes the artifact contribution concrete. release claim in the source; current hosting not audited. |
| C02.P5.U5 | §1 HTML #S1.p5.1, prose sentence 5 | Preview performance across selected distilled model sizes | Connects the release to measured capability. reported benchmark-specific findings. |
| C02.P6.U1 | §1.1 Contributions, HTML #S1.I1.i1.p1.1, prose sentence 1 | Repeat the absence of supervised finetuning in the exploratory stage | Reasserts the principal experimental distinction. stage-specific procedure. |
| C02.P6.U2 | §1.1 Contributions, HTML #S1.I1.i1.p1.1, prose sentence 2 | Name the resulting exploratory model | Binds the contribution summary to the earlier system. author framing; interpretive rhetorical annotation. |
| C02.P6.U3 | §1.1 Contributions, HTML #S1.I1.i1.p1.1, prose sentence 3 | Repeat qualitative reasoning behaviors | Compresses the claimed outcome into a contribution item. reported observations. |
| C02.P6.U4 | §1.1 Contributions, HTML #S1.I1.i1.p1.1, prose sentence 4 | Claim priority for the open investigation | Positions the contribution historically. priority claim not independently established. |
| C02.P6.U5 | §1.1 Contributions, HTML #S1.I1.i1.p1.1, prose sentence 5 | Offer the result as a future research direction | States anticipated downstream value. prospective implication. |
| C02.P7.U1 | §1.1 Contributions, HTML #S1.I1.i2.p1.1, prose sentence 1 | Summarize the practical model's pipeline | Contrasts the usable system with the exploratory one. author framing; interpretive rhetorical annotation. |
| C02.P7.U2 | §1.1 Contributions, HTML #S1.I1.i2.p1.1, prose sentence 2 | Count the RL and supervised stages by purpose | Compresses the method into an operational summary. method description. |
| C02.P7.U3 | §1.1 Contributions, HTML #S1.I1.i2.p1.1, prose sentence 3 | Suggest value for the wider community | States anticipated uptake. author expectation, not an evaluated outcome. |
| C02.P8.U1 | §1.1 Contributions, HTML #S1.I2.i1.p1.1, prose sentence 1 | Restate the smaller-model distillation finding | Elevates transfer into a separate contribution. reported task-specific result. |
| C02.P8.U2 | §1.1 Contributions, HTML #S1.I2.i1.p1.1, prose sentence 2 | State the planned value of released models | Connects artifacts to future community use. prospective benefit. |
| C02.P9.U1 | §1.1 Contributions, HTML #S1.I2.i2.p1.1, prose sentence 1 | Identify the distilled model families | Makes the artifact set concrete. reported release scope. |
| C02.P9.U2 | §1.1 Contributions, HTML #S1.I2.i2.p1.1, prose sentence 2 | Summarize benchmark strength | Gives the artifact claim an evaluation basis. reported comparative finding. |
| C02.P9.U3 | §1.1 Contributions, HTML #S1.I2.i2.p1.1, prose sentence 3 | Use a small-model benchmark example | Demonstrates the scale-specific claim. reported AIME comparison. |
| C02.P9.U4 | §1.1 Contributions, HTML #S1.I2.i2.p1.1, prose sentence 4 | List results for the 32B model | Supplies another quantitative anchor. reported metric-specific findings. |
| C02.P9.U5 | §1.1 Contributions, HTML #S1.I2.i2.p1.1, prose sentence 5 | Position those results against a named comparator | Makes relative performance explicit. settings and comparator versions matter. |
| C02.P9.U6 | §1.1 Contributions, HTML #S1.I2.i2.p1.1, prose sentence 6 | Restate checkpoint release | Closes the contribution on a reusable artifact. release claim; present accessibility not checked. |
| C02.P10.U1 | §1.2 Evaluation Summary, HTML #S1.I3.i1.p1.1, prose sentence 1 | Preview a reasoning benchmark comparison | Organizes evidence by capability category. reported result. |
| C02.P10.U2 | §1.2 Evaluation Summary, HTML #S1.I3.i1.p1.1, prose sentence 2 | Add a mathematical benchmark result | Extends that category's evaluation. reported result. |
| C02.P10.U3 | §1.2 Evaluation Summary, HTML #S1.I3.i1.p1.1, prose sentence 3 | Add competitive programming performance | Broadens beyond mathematical questions. reported result. |
| C02.P10.U4 | §1.2 Evaluation Summary, HTML #S1.I3.i1.p1.1, prose sentence 4 | State potential in software engineering | Moves from benchmarks to a practical task family. reported task evidence plus potential; not general reliability. |
| C02.P11.U1 | §1.2 Evaluation Summary, HTML #S1.I3.i2.p1.1, prose sentence 1 | Preview knowledge benchmark results | Opens a second evaluation family. reported result. |
| C02.P11.U2 | §1.2 Evaluation Summary, HTML #S1.I3.i2.p1.1, prose sentence 2 | Concede a remaining gap to a named model | Retains an adverse comparison locally. explicit result boundary. |
| C02.P11.U3 | §1.2 Evaluation Summary, HTML #S1.I3.i2.p1.1, prose sentence 3 | Add factual question-answering evidence | Tests an adjacent capability. reported result. |
| C02.P11.U4 | §1.2 Evaluation Summary, HTML #S1.I3.i2.p1.1, prose sentence 4 | Connect the result pattern to another observed comparison | Interprets the pattern across evaluations. author interpretation. |
| C02.P12.U1 | §1.2 Evaluation Summary, HTML #S1.I3.i3.p1.1, prose sentence 1 | Introduce non-reasoning task performance | Tests whether specialization preserves broader usefulness. reported evaluation scope. |
| C02.P12.U2 | §1.2 Evaluation Summary, HTML #S1.I3.i3.p1.1, prose sentence 2 | Preview preference-evaluation scores | Makes the broader-usefulness claim measurable. reported judge-dependent metric. |
| C02.P12.U3 | §1.2 Evaluation Summary, HTML #S1.I3.i3.p1.1, prose sentence 3 | Preview long-context performance | Closes with another capability boundary. reported benchmark result; not arbitrary-context reliability. |

### Pivotal transitions checked against the body

- **C02.P3.U4 → C02.P4.U1 → C02.P4.U2:** The exploratory system's own usability defects motivate a second, staged design. Source: §1 P3–P4; §2.2.4 Drawback of DeepSeek-R1-Zero; §2.3.1 Cold Start. Limit: Observed defects motivate the pipeline; the Introduction alone does not isolate the effect of each added stage.
- **C02.P5.U2 → C02.P5.U3:** The smaller-model comparison motivates transfer of reasoning traces. Source: §4.1 Distillation v.s. Reinforcement Learning, Table 6; §3.2. Limit: Reported distillation and RL use different training paths; do not promote the comparison to a universal or equal-budget theorem.
- **C02.P2.U7 → C02.P11.U2:** Capability claims need task-specific comparison and local acknowledgment of remaining gaps. Source: §1.2 Evaluation Summary; §3.1 evaluation tables. Limit: Historical priority and broad superiority wording were not independently established.

**Scientific verification limit:** No training rerun, benchmark recomputation, current release audit or exhaustive priority search; body checks support interpretation of reported comparisons only.

## C03 — On a conjecture of Marton

[Primary source](https://arxiv.org/html/2311.05762v1); Gowers, Green, Manners and Tao, 2023. Accessed 2026-10-30.

**Scope:** Entire §1, including Entropy methods and Notation; theorem statements and their displays retained as blocks; excludes footnotes. §2–§3 and Appendix B inspected for proof organization and implications.

**Segmentation:** 37 annotation units: 33 prose sentences, three theorem blocks, and one composite definition containing a display and its independent-copy convention. These are not 37 plain sentences. Theorem prose is not split into artificial rhetorical sentences.

**Observed route:** Result first, exact statement, prior-bound context, methodological boundary, useful equivalent formulation, consequences and notation.

**Use when:** Useful for theorem-led work with a recognizable precise problem; for a broader audience add a small motivating instance or informal statement before the formal block.

**Counterexample to a rigid template:** An Introduction can legitimately contain definitions, full theorem statements and notation. It need not invent an empirical failure, a deployable method or contribution bullets.

| Unit | Source locator | Function | Why it is here / evidence boundary |
|---|---|---|---|
| C03.P1.U1 | §1 HTML #S1.p1.1, prose sentence 1 | State the proved conjecture and characteristic immediately | Gives the specialist reader the result before a general motivation. theorem announcement. |
| C03.P1.U2 | §1 HTML #S1.p1.1, prose sentence 2 | Explain that several equivalent formulations exist | Prepares the choice of statement and its consequences. prior equivalence and consequence claims. |
| C03.P2.U1 | §1 HTML #S1.p2.1, prose sentence 1 | Introduce the selected combinatorial formulation | Provides the transition from announcement to a formal claim. author framing; interpretive rhetorical annotation. |
| C03.T1.U1 | §1 Theorem 1.1, HTML #S1.Thmtheorem1, formal theorem block 1 | State the finite-set covering theorem with hypotheses and constants | Makes the main claim precise enough to assess. formal statement; proof not independently verified. |
| C03.P3.U1 | §1 HTML #S1.p3.1, prose sentence 1 | Commit the paper to proving this and equivalent forms | Clarifies the scope of the result beyond the displayed formulation. proof commitment. |
| C03.P4.U1 | §1 HTML #S1.p4.1, prose sentence 1 | Recall Ruzsa's earlier bound | Establishes the relevant quantitative baseline. cited historical result. |
| C03.P4.U2 | §1 HTML #S1.p4.1, prose sentence 2 | Explain the conjecture's attribution | Locates the problem historically. author framing; interpretive rhetorical annotation. |
| C03.P4.U3 | §1 HTML #S1.p4.1, prose sentence 3 | Describe Sanders's improvement | Identifies the strongest relevant improvement in the narrative. cited historical result. |
| C03.P4.U4 | §1 HTML #S1.p4.1, prose sentence 4 | Mention a related Konyagin variant | Qualifies the surrounding landscape rather than erasing adjacent progress. cited historical result. |
| C03.P5.U1 | §1 HTML #S1.p5.1, prose sentence 1 | State the best known prior bound at the manuscript's date | Defines the advance against a fixed historical baseline. date-scoped author claim. |
| C03.P6.U1 | §1 HTML #S1.p6.1, prose sentence 1 | Differentiate the proof from the Bogolyubov route | Identifies a methodological change instead of merely a stronger bound. proof-strategy claim. |
| C03.P6.U2 | §1 HTML #S1.p6.1, prose sentence 2 | Preserve the unresolved status of the adjacent Bogolyubov problem | Blocks an overbroad interpretation of the new theorem. explicit non-implication. |
| C03.P7.U1 | §1 HTML #S1.p7.1, prose sentence 1 | Mention possible extension to odd characteristic | Shows a neighboring direction while retaining the present scope. prospective extension, not this paper's proved theorem. |
| C03.P7.U2 | §1 HTML #S1.p7.1, prose sentence 2 | Explain the decision to treat that extension separately | Justifies a scope boundary through notation and new ideas. author scope choice. |
| C03.P8.U1 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p1.1, prose sentence 1 | Credit earlier entropy methods | Establishes the methodological lineage. author framing; interpretive rhetorical annotation. |
| C03.P8.U2 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p1.1, prose sentence 2 | Identify recent work particularly close to this proof | Narrows the lineage to the direct technical precursor. author framing; interpretive rhetorical annotation. |
| C03.P8.U3 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p1.1, prose sentence 3 | State that those methods underlie the present proof | Connects context to the chosen approach. proof-strategy claim. |
| C03.P9.U1 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p2.1, prose sentence 1 | Refer readers to a fuller appendix discussion | Allocates background without duplicating it. author framing; interpretive rhetorical annotation. |
| C03.P9.U2 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p2.1, prose sentence 2 | Announce the entropic Ruzsa distance | Introduces the object needed for the next theorem. author framing; interpretive rhetorical annotation. |
| C03.DEF.U1 | §1 Entropy methods, #S1.SS0.SSSx1.p2.1–p2.2 and intervening display, composite definition block 1 | Define entropic distance together with its independent-copy convention | Keeps the formula and the condition that gives it meaning in one unit. formal definition. |
| C03.P10.U1 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p2.2, final sentence, prose sentence 1 | Clarify dependence on marginal distributions | Prevents a mistaken reading involving the original joint coupling. definition clarification. |
| C03.P11.U1 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p3.1, prose sentence 1 | Point to detailed properties of the distance | Provides a source for deferred technical facts. author framing; interpretive rhetorical annotation. |
| C03.P11.U2 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p3.1, prose sentence 2 | State triangle behavior and why this is not a metric | Preserves a mathematical limitation before later use. mathematical background. |
| C03.P11.U3 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p3.1, prose sentence 3 | Simplify the notation used below | Reduces recurring overhead without changing the object. author framing; interpretive rhetorical annotation. |
| C03.P11.U4 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p3.1, prose sentence 4 | Explain square-bracket notation for laws | Prevents ambiguity before stating the entropic result. author framing; interpretive rhetorical annotation. |
| C03.P12.U1 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p4.1, prose sentence 1 | Recall the equivalence of the combinatorial and entropic forms | Justifies changing representations. cited equivalence up to constants. |
| C03.P12.U2 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p4.1, prose sentence 2 | Choose the entropic formulation as the proof target | Explains which statement the body will establish. proof-organization commitment. |
| C03.T2.U1 | §1 Theorem 1.2, HTML #S1.Thmtheorem2, formal theorem block 1 | State the entropic theorem with its quantified random variables and subgroup | Makes the proof target exact. formal statement; proof not independently verified. |
| C03.P13.U1 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p5.1, prose sentence 1 | Recall the established equivalence up to constants | Reassures the reader that the new representation addresses the original problem. cited equivalence. |
| C03.P13.U2 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p5.1, prose sentence 2 | Point to the appendix implication with explicit constants | Binds the reduction to an exact proof obligation. Appendix B checked for role, not fully re-proved. |
| C03.P14.U1 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p6.1, prose sentence 1 | Derive an integer-case consequence using prior implications | Separates the new central theorem from a downstream corollary. stated consequence using prior results. |
| C03.T3.U1 | §1 Theorem 1.3, HTML #S1.Thmtheorem3, formal theorem block 1 | State the weak polynomial Freiman–Ruzsa consequence over integers | Makes the corollary's domain and strength explicit. formal statement; proof not independently verified. |
| C03.P15.U1 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p7.1, prose sentence 1 | Explain that constants are tracked without claiming optimality | Calibrates the quantitative contribution. explicit non-optimality boundary. |
| C03.P15.U2 | §1 Entropy methods, HTML #S1.SS0.SSSx1.p7.1, prose sentence 2 | Explain constant notation inherited from prior work | Clarifies that the exponent C1/2 preserves the earlier notation; non-optimality belongs to the preceding sentence. cross-paper notation clarification. |
| C03.P16.U1 | §1 Notation, HTML #S1.SS0.SSSx2.p1.1, prose sentence 1 | Fix the logarithm convention | Makes later quantitative statements unambiguous. author framing; interpretive rhetorical annotation. |
| C03.P16.U2 | §1 Notation, HTML #S1.SS0.SSSx2.p1.1, prose sentence 2 | Fix entropy and information notation | Prepares the technical exposition. author framing; interpretive rhetorical annotation. |
| C03.P16.U3 | §1 Notation, HTML #S1.SS0.SSSx2.p1.1, prose sentence 3 | Point to collected basic facts | Offers a path for readers needing background. author framing; interpretive rhetorical annotation. |

### Pivotal transitions checked against the body

- **C03.P1.U1 → C03.T1.U1 → C03.P4.U1:** A specialist can assess a theorem-first opening once its hypotheses, quantitative gain and prior bounds are supplied. Source: §1 Theorem 1.1 and following prior-bound paragraphs. Limit: A theorem announcement does not remove the need for context or proof; the intended reader already knows the problem family.
- **C03.P12.U1 → C03.P12.U2 → C03.T2.U1 → C03.P13.U2:** An equivalent entropic formulation changes the proof route while retaining the original mathematical target. Source: §1 Theorem 1.2; §2 Induction on entropy distance; Appendix B. Limit: Equivalence up to constants and the direction actually proved in Appendix B must be distinguished.
- **C03.P6.U1 → C03.P6.U2 → C03.P15.U1:** Methodological novelty is scoped by adjacent open questions and non-optimal constants. Source: §1 Bogolyubov paragraph; §2 post-proof remark on compactness and algorithmicity; §3 proof plan. Limit: The result does not automatically settle the adjacent Bogolyubov problem or give the strongest algorithmic version.

**Scientific verification limit:** No independent proof verification or attempt to evaluate the theorem's mathematical correctness; the reading checks claim scope and the role of proof sections.


