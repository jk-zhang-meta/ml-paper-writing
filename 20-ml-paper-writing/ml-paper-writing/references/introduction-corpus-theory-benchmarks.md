# Introduction corpus: theory, mathematics, benchmarks and measurement

This bounded Evidence Review examines 10 deliberately selected primary papers for **sentence-level rhetorical guidance**, with computer science primary and mathematics as a contrast case. All 10 full Introductions were read from the fixed arXiv PDF versions below on 2026-10-30; no candidate was replaced. This is a purposive teaching corpus, not a representative sample, systematic review, proof verification, or scientific replication. Rhetorical labels and dependency links are analyst interpretations; reported results, assumptions and definitions remain attributed to their papers.

The companion [JSONL](introduction-corpus-theory-benchmarks.jsonl) contains 448 annotated units and 30 pivotal transitions. Units are sentences or explicitly declared prose/statement units, **not 448 uniformly defined sentences**. In particular, T04 has 32 mathematical statement units; T02 includes a standalone colon-terminated lead-in; nominal contribution items and run-in labels follow the per-paper conventions. Captions, figure labels, table cells, footnotes, abstracts and page furniture are excluded from every map. Definitions and equations embedded in T04's theorem/proof units are retained as part of those units, never silently counted as sentences.

Each JSONL unit provides a local locator, function, rhetorical dependencies, reason for placement and evidence status. Read units in order against the declared section boundary. Dependency links describe what a reader needs to understand the move; they are **not a proof dependency graph or a claim of logical entailment**. Pivotal transitions add the predecessor, new claim, warrant, checked source locator and limit. The full unit map is intentionally in JSONL rather than duplicating hundreds of rows here.

## Source register and scope

“Year” is first arXiv submission year; the revision year is separate. All title/identifier pairs were checked against primary arXiv records and fixed PDF title pages. Version histories were inspected; a separate exhaustive correction/retraction search was not performed. No source-access failure or paper substitution occurred. PDF bytes were piped into pdftotext and extracted working text stayed outside OneDrive under /tmp; these two files contain original annotations, metadata and locators rather than redistributed full text.

| ID | Primary source | Year / revision | Full Introduction | Units |
|---|---|---|---|---:|
| T01 | [Computing Nonvacuous Generalization Bounds for Deep (Stochastic) Neural Networks with Many More Parameters than Training Data](https://arxiv.org/pdf/1703.11008v2) | 2017 / 2017 | §1–1.2, pp. 1–3 | 69 |
| T02 | [Neural Tangent Kernel: Convergence and Generalization in Neural Networks](https://arxiv.org/pdf/1806.07572v4) | 2018 / 2020 | §1–1.1, pp. 1–2 | 24 |
| T03 | [On the Turing Completeness of Modern Neural Network Architectures](https://arxiv.org/pdf/1901.03429v1) | 2019 / 2019 | §1, pp. 1–2 | 45 |
| T04 | [Interlacing Families II: Mixed Characteristic Polynomials and the Kadison-Singer Problem](https://arxiv.org/pdf/1306.3969v4) | 2013 / 2014 | §1, pp. 2–4; theorem and proof included | 32 |
| T05 | [GLUE: A Multi-Task Benchmark and Analysis Platform for Natural Language Understanding](https://arxiv.org/pdf/1804.07461v3) | 2018 / 2019 | §1, pp. 1–2 | 21 |
| T06 | [SuperGLUE: A Stickier Benchmark for General-Purpose Language Understanding Systems](https://arxiv.org/pdf/1905.00537v3) | 2019 / 2020 | §1, pp. 1–2 | 22 |
| T07 | [WILDS: A Benchmark of in-the-Wild Distribution Shifts](https://arxiv.org/pdf/2012.07421v3) | 2020 / 2021 | §1, pp. 4–6 | 32 |
| T08 | [Holistic Evaluation of Language Models](https://arxiv.org/pdf/2211.09110v2) | 2022 / 2023 | §1–1.3, pp. 2–10; all 25 findings | 154 |
| T09 | [Measuring Massive Multitask Language Understanding](https://arxiv.org/pdf/2009.03300v3) | 2020 / 2021 | §1, pp. 1–2 | 29 |
| T10 | [SWE-bench: Can Language Models Resolve Real-World GitHub Issues?](https://arxiv.org/pdf/2310.06770v3) | 2023 / 2024 | §1, pp. 1–2 | 20 |

## Comparative observations

1. **Select a route from the actual warrant.** T01 starts with an achieved numerical certificate and then explains why it matters. T02 first establishes a kernel connection that makes its new mathematical object intelligible. T03 separates formal capacity from practical learning. T04 states a problem and follows a chain of reductions, including an embedded proof. These are different solutions to readers' information needs, not imperfect instances of one mandatory funnel. See [T01 §1](https://arxiv.org/pdf/1703.11008v2), [T02 §1](https://arxiv.org/pdf/1806.07572v4), [T03 §1](https://arxiv.org/pdf/1901.03429v1), and [T04 §1](https://arxiv.org/pdf/1306.3969v4).

2. **The sentence after a claim often carries its permission to be believed.** In T03 the strong bounded-architecture claim is immediately constrained by arbitrary precision and simulation details (U012–U016). In T02 convergence is followed by the sphere-conditioned positive-definiteness result (U018–U019). A useful editing question is which assumption or mechanism makes the preceding claim legitimate; an interchangeable transition phrase does not supply that warrant. These are theorem assumptions, not empirical observations. [T03 §§2–4](https://arxiv.org/pdf/1901.03429v1); [T02 Theorem 2 and Proposition 2](https://arxiv.org/pdf/1806.07572v4).

3. **Benchmark novelty and measurement validity are separate arguments.** GLUE explicitly reuses datasets and explains the transfer incentives and diagnostic layer (U005–U011). WILDS ties realism to data, task/metric and split, while selecting cases for a performance drop (U017–U024). SWE-bench pairs repository-scale work with an executable success criterion (U004–U012). A new task count alone cannot warrant the intended capability claim. [GLUE §§1,3–4](https://arxiv.org/pdf/1804.07461v3); [WILDS §1 and Appendix A](https://arxiv.org/pdf/2012.07421v3); [SWE-bench §§1–2](https://arxiv.org/pdf/2310.06770v3).

4. **A successful predecessor can create the next measurement problem.** SuperGLUE credits GLUE's role before arguing that saturation reduces its utility; MMLU uses repeated saturation to motivate knowledge domains that previous suites undermeasure. Preserve this distinction when writing a gap: a saturated metric is not proof that the underlying scientific objective has been achieved. [SuperGLUE §1, Figure 1](https://arxiv.org/pdf/1905.00537v3); [MMLU §1](https://arxiv.org/pdf/2009.03300v3).

5. **Lists need internal logic and different jobs.** NTK's contribution bullets progress from dynamics to a convergence condition to a special loss and numerical illustration. HELM separately lists evaluation principles, 25 empirical findings, and contributions. A compulsory list of three contributions would erase either the design rationale or the evidence interpretation in these examples. HELM's nine-page Introduction is an observed genre choice, not a general length recommendation. [NTK §1.1](https://arxiv.org/pdf/1806.07572v4); [HELM §§1–1.3](https://arxiv.org/pdf/2211.09110v2).

6. **Put boundaries beside the claim that might otherwise overreach.** T01 contrasts an informative but loose certificate with held-out error; T03 distinguishes existence from learnability; MMLU follows aggregate progress with uneven subject performance and calibration; HELM acknowledges prompt suitability and contamination before its findings. These qualifications perform argumentative work rather than serving as generic final disclaimers. [T01 §1.1 and Table 1](https://arxiv.org/pdf/1703.11008v2); [T03 §1](https://arxiv.org/pdf/1901.03429v1); [MMLU §1 and Figure 8](https://arxiv.org/pdf/2009.03300v3); [HELM §1.1](https://arxiv.org/pdf/2211.09110v2).

7. **Distinguish why the paper is worth reading from what has been proved.** Qualified priority claims in T01 and T02 are not theorem evidence. A benchmark's low score does not prove its construct validity. T04 earns the bridge to its famous problem by stating quantified results and reductions, not by historical prominence alone. The reading guide should therefore ask for the source of the warrant and its scope, not insist that every Introduction contain the same diagnosis, explicit question, or final bullets. [T01 §1](https://arxiv.org/pdf/1703.11008v2); [T02 §1](https://arxiv.org/pdf/1806.07572v4); [T04 §1](https://arxiv.org/pdf/1306.3969v4).

## Case notes and pivotal transitions

### T01 — Computing Nonvacuous Generalization Bounds for Deep (Stochastic) Neural Networks with Many More Parameters than Training Data

[Fixed primary PDF](https://arxiv.org/pdf/1703.11008v2); [version metadata](https://arxiv.org/abs/1703.11008v2). Dziugaite & Roy; first version 2017, inspected revision 2017.

**Reading boundary:** Full §1, including §1.1 Understanding SGD and §1.2 Approach, PDF pp. 1–3; ends before §2 Preliminaries.

**Route:** Result-first certificate → quantitative inadequacy of existing explanation → SGD phenomenon → candidate structure → qualified stochastic guarantee → historical mechanism → scalable algorithm.

**Why use this case:** Use for computational theory where the paper must exhibit an actual informative certificate, not merely an asymptotic rate.

**What a fixed template misses:** A mandatory broad opening delays the achieved result; a diagnosis-only middle loses the distinction between explaining existence and explaining magnitude. Prior work is part of the warrant, not a detachable survey.

1. **T01-U012, T01-U013, T01-U015, T01-U016.** Norm-based accounts and implicit regularization are plausible explanations. → Computed contemporary bounds do not yet establish nontrivial generalization in the tested regime. **Warrant:** A numerical upper bound above the trivial error ceiling supplies no informative certificate; the paper actually evaluates the competing bound rather than inferring failure from model size. **Checked locator:** Appendix D, Theorems D.1–D.2, §D.1 experiment setup and §D.2 results; Figure 1. **Limit:** Failure of these calculations is not a proof that all norm-based bounds are vacuous.

2. **T01-U021, T01-U022, T01-U023, T01-U024, T01-U025, T01-U026, T01-U028.** A structural account of SGD needs an informative associated bound. → A broad low-error posterior provides a candidate certificate, with limited numerical tightness. **Warrant:** PAC-Bayes connects posterior empirical error and divergence from a fixed prior to expected population error; Table 1 instantiates the bound and distinguishes stochastic from deterministic error. **Checked locator:** Theorem 2.3; Table 1 (true-label architectures, PAC-Bayes bounds 0.161–0.223 and SNN test-error rows). **Limit:** The table is a computational certificate under iid/bound conditions, not evidence that SGD always finds this structure or that the mean network has the same guarantee.

3. **T01-U060, T01-U063, T01-U064, T01-U065, T01-U066, T01-U067.** The predecessor estimates coordinate sensitivities and scales a diagonal posterior. → Joint direct optimization replaces an uninformative coordinate procedure. **Warrant:** In highly overparameterized networks, one coordinate may scarcely affect classification error; optimizing the bound jointly searches an informative posterior instead. **Checked locator:** §1.2 final three paragraphs; §3 optimization objective and Table 1 feasibility results. **Limit:** The asserted coordinate failure motivates design; no universal optimality or causal explanation of flatness is established.

**Verification ceiling:** Reported numerical bounds are for stochastic classifiers on a binary MNIST variant; Table 1 is not a universal explanation of SGD or a guarantee for the unperturbed mean network. Priority is qualified by the authors and not proved here.

### T02 — Neural Tangent Kernel: Convergence and Generalization in Neural Networks

[Fixed primary PDF](https://arxiv.org/pdf/1806.07572v4); [version metadata](https://arxiv.org/abs/1806.07572v4). Jacot, Gabriel & Hongler; first version 2018, inspected revision 2020.

**Reading boundary:** Full §1 and §1.1 Contribution, PDF pp. 1–2; ends before §2 Neural networks.

**Route:** Optimization gap → generalization puzzle → kernel analogy → function-space object → conditional results → finite-width illustration.

**Why use this case:** Use when a new mathematical object unifies a problem and makes subsequent claims intelligible.

**What a fixed template misses:** A question followed immediately by contribution bullets would omit the kernel bridge. The contribution list itself has internal dependencies: dynamics, definiteness, squared-loss specialization, numerical comparison.

1. **T02-U010, T02-U011, T02-U012, T02-U013, T02-U017.** Networks share an initialization/kernel connection and an overfitting puzzle with kernels. → The function's training evolution can also be represented by a kernel. **Warrant:** The NTK is defined from parameter derivatives; its infinite-width limit becomes fixed under the theorem's conditions, making function-space dynamics analyzable. **Checked locator:** §4 Theorems 1–2 and the differential equation following Theorem 2. **Limit:** A limiting theorem does not assert every finite network behaves exactly as a fixed kernel.

2. **T02-U018, T02-U019, T02-U020.** Kernel dynamics alone leaves convergence conditional. → Positive definiteness can establish the required convergence condition in a specified setting. **Warrant:** Proposition 2 verifies positivity for non-polynomial Lipschitz activation on the unit sphere and depth at least two; §3 explains the kernel-gradient implication. **Checked locator:** §3 kernel-gradient convergence discussion; §4 Proposition 2, proof in Appendix A.4. **Limit:** Sphere support, activation and depth are assumptions, not empirical findings; broad finite-network generalization is not proved by this bridge.

3. **T02-U021, T02-U022, T02-U023, T02-U024.** Squared-loss dynamics have a spectral solution in the limit. → Early stopping is theoretically motivated and wide-network behavior is illustrated numerically. **Warrant:** §5 decomposes learning into kernel eigendirections; §6 compares finite networks with the limit. **Checked locator:** §5 Least-squares regression; §6 numerical experiments, Figures 1–2. **Limit:** Early-stopping motivation is an interpretation of learning rates, not a universal validated stopping rule; illustrations do not remove theorem assumptions.

**Verification ceiling:** Theorem 2 assumes smooth/Lipschitz nonlinearity, bounded second derivative and bounded integrated training direction in an infinite-width limit. Proposition 2 adds sphere support and non-polynomial activation. Numerical agreement does not remove these assumptions.

### T03 — On the Turing Completeness of Modern Neural Network Architectures

[Fixed primary PDF](https://arxiv.org/pdf/1901.03429v1); [version metadata](https://arxiv.org/abs/1901.03429v1). Pérez, Marinković & Barceló; first version 2019, inspected revision 2019.

**Reading boundary:** Full §1 including the unnumbered Background work passage, PDF pp. 1–2; ends before §2 Preliminaries.

**Route:** Algorithm-learning aspiration → two notions of computational resources → architectural gap → formal result → precision disclosure → theory/practice reconciliation → failed analogy repaired.

**Why use this case:** Use for expressivity papers where capacity, learnability and implementation resources can be conflated.

**What a fixed template misses:** A fixed failure-diagnosis template may imply the theorem cures empirical length generalization. Here the Introduction deliberately reconciles apparently conflicting results by comparing assumptions.

1. **T03-U012, T03-U013, T03-U014, T03-U015, T03-U016.** The two architectures are claimed universal without additional external memory. → The capacity result uses explicit precision and simulation assumptions. **Warrant:** The proof constructs a Transformer simulation and reduces uniform Neural GPU computation to a seq-to-seq RNN; it does not infer capacity from benchmark success. **Checked locator:** §2 arbitrary-precision convention; Theorem 3.4 and Figure 1; Theorem 4.1. **Limit:** The formal Transformer includes positional encodings and uses hard attention in the construction; arbitrary rational precision is essential to the stated model.

2. **T03-U031, T03-U032, T03-U033, T03-U034, T03-U035, T03-U036.** Existing models can fail to generalize to longer sequences in practice. → The formal completeness result can coexist with that empirical failure. **Warrant:** Representational existence under arbitrary precision/hard attention differs from learning under fixed precision/soft attention. **Checked locator:** §3.3 discussion following Theorem 3.4, plus §2 precision convention. **Limit:** Neither theorem falsifies the empirical failure nor proves that training will discover the simulated algorithm.

3. **T03-U040, T03-U041, T03-U042, T03-U043, T03-U044, T03-U045.** A cellular-automaton analogy appears to establish Neural GPU universality. → Input-bounded cells make that analogy insufficient; dense representations provide another route. **Warrant:** Unbounded-cell capacity does not transfer automatically to a model with input-sized state; Theorem 4.1 supplies a different simulation. **Checked locator:** §1 final paragraph; §4 definition of uniform Neural GPU and Theorem 4.1. **Limit:** The repair concerns formal resource models, not an empirical claim of better algorithm learning.

**Verification ceiling:** Completeness is an existence claim under arbitrary-precision rational activations and architecture choices including hard attention for the construction. It neither establishes finite-precision universality nor practical learnability.

### T04 — Interlacing Families II: Mixed Characteristic Polynomials and the Kadison-Singer Problem

[Fixed primary PDF](https://arxiv.org/pdf/1306.3969v4); [version metadata](https://arxiv.org/abs/1306.3969v4). Marcus, Spielman & Srivastava; first version 2013, inspected revision 2014.

**Reading boundary:** Full §1 Introduction, PDF pp. 2–4, including Question 1.1, Conjectures 1.2–1.3, Theorem 1.4, Corollary 1.5 and its proof; ends before §2 Overview. §2 and the named proof locators were additionally inspected.

**Route:** Named problem → implication network → sufficient conjecture → technical theorem → quantitative comparison → explicit reduction → short proof.

**Why use this case:** Use for theorem papers whose significance is carried by a precise chain of implications and assumptions.

**What a fixed template misses:** A compulsory motivating failure paragraph or contribution bullets would obscure the actual proof obligation. The Introduction already performs mathematics; it is not solely a sales pitch or a roadmap.

1. **T04-U003, T04-U006, T04-U007, T04-U008.** The historic operator-algebra question is linked to several conjectures. → It suffices to prove the precisely stated Weaver formulation. **Warrant:** The Introduction names the implication through projection paving and keeps its source explicit, replacing a broad importance claim with an implication chain. **Checked locator:** Question 1.1; Conjecture 1.2; sentence citing Weaver p. 229; Corollary 1.5 specialization. **Limit:** External equivalence proofs were not independently checked; their cited role is distinguished from the paper's new theorem.

2. **T04-U016, T04-U017, T04-U018, T04-U020.** Concentration inequalities supply larger bounds with high probability. → A sharper existence bound can yield a partition theorem. **Warrant:** Theorem 1.4 trades a high-probability assertion for positive probability under independence, finite support and covariance/norm constraints; Corollary 1.5 converts that existence into partitions. **Checked locator:** Theorem 1.4; Corollary 1.5; proof of Theorem 1.4 at end of §5 using Theorems 4.5 and 5.1. **Limit:** This is not a concentration improvement at the same probability level. Proof locations and statements were read, not formally certified.

3. **T04-U020, T04-U021, T04-U022, T04-U023, T04-U024, T04-U025.** The partition corollary has free constants and arbitrary partition count. → The original conjectures follow with explicit parameters. **Warrant:** The Introduction exhibits the KS2 substitution and normalization; the second paving implication is separately routed to §6. **Checked locator:** Corollary 1.5; immediately following r=2, delta=1/18 specialization; §6 paving result. **Limit:** The constants and quantifiers matter; a priority announcement or informal 'solves the problem' sentence cannot replace this bridge.

**Verification ceiling:** Read statements and implication/proof locations, not an independent proof verification. Theorem 1.4 is a positive-probability existence bound for independent finitely supported random vectors; it is not a high-probability concentration result.

### T05 — GLUE: A Multi-Task Benchmark and Analysis Platform for Natural Language Understanding

[Fixed primary PDF](https://arxiv.org/pdf/1804.07461v3); [version metadata](https://arxiv.org/abs/1804.07461v3). Wang et al.; first version 2018, inspected revision 2019.

**Reading boundary:** Full §1, PDF pp. 1–2; ends before §2 Related Work. Table 1 and footnote 1 are excluded from unit count.

**Route:** Generality criterion → task-specific shortfall → suite design → transfer incentive → diagnostics → baseline behavior → artifact inventory.

**Why use this case:** Use for benchmarks that curate existing datasets but add a measurement regime and analysis capability.

**What a fixed template misses:** Treating dataset novelty as the sole contribution misses model eligibility, scarcity-based transfer incentives, private tests and diagnostics. The design-to-incentive inference needs explanation before the closing list.

1. **T05-U005, T05-U006, T05-U007.** The suite permits diverse architectures but varies data quantity and genre. → Knowledge sharing is intended to become advantageous. **Warrant:** Data-scarce and mismatched tasks create pressure for sample-efficient transfer without mandating a particular architecture. **Checked locator:** §3 Tasks and Table 1; §6 benchmark results and Table 4. **Limit:** This is a design incentive supported by baseline behavior, not a theorem that any high score requires a unified model.

2. **T05-U008, T05-U009, T05-U010, T05-U011.** Most underlying tasks already exist and aggregate scores alone are limited. → Private tests and expert diagnostics create distinct evaluation contributions. **Warrant:** Held-out evaluation addresses reuse integrity; targeted examples inspect linguistic behavior beyond an overall ranking. **Checked locator:** §4 Diagnostic Dataset; Tables 2–3; Table 5 diagnostic results. **Limit:** Curation novelty, leakage resistance and construct coverage are different claims; none proves comprehensive language understanding.

3. **T05-U012, T05-U013, T05-U014, T05-U015, T05-U016.** Multitask baselines improve aggregate performance. → Substantial headroom and logical weaknesses remain. **Warrant:** Table 4 evaluates the comparison; Table 5 separates diagnostic categories, preventing a modest average improvement from being presented as robust understanding. **Checked locator:** §6 Benchmark Results and §7 diagnostic analysis; Tables 4–5. **Limit:** The evidence is about selected baselines and selected diagnostic examples; it is not a universal model limitation.

**Verification ceiling:** A low suite score or diagnostic weakness is evidence about evaluated baselines, not proof that the suite measures all language understanding. Architecture freedom does not force knowledge sharing; it creates an intended incentive.

### T06 — SuperGLUE: A Stickier Benchmark for General-Purpose Language Understanding Systems

[Fixed primary PDF](https://arxiv.org/pdf/1905.00537v3); [version metadata](https://arxiv.org/abs/1905.00537v3). Wang et al.; first version 2019, inspected revision 2020.

**Reading boundary:** Full §1, PDF pp. 1–2; ends before §2 Related Work. Figure 1 and author footnote excluded from map.

**Route:** Successful research trajectory → old measurement success → demonstrated headroom loss → replacement with continuity → concrete design repairs.

**Why use this case:** Use for benchmark replacement where the predecessor was useful and progress has changed measurement needs.

**What a fixed template misses:** The predecessor is not portrayed as a failed method. A mandatory deficiency paragraph can misrepresent the warrant: success caused saturation, while broader understanding remains unresolved.

1. **T06-U008, T06-U009, T06-U010, T06-U011.** Rapid progress pushes the old score beyond a non-expert human estimate. → A successor is needed even though language understanding remains unsolved. **Warrant:** The paper separates metric headroom from the underlying scientific goal and supplies both task-level scores and diagnostics. **Checked locator:** Figure 1; Appendix B Figure 2; §1 July 2019 score comparison. **Limit:** An estimated human score is not an upper bound on human competence or an exhaustive validity test.

2. **T06-U015, T06-U016, T06-U017, T06-U018, T06-U019.** Harder tasks and broader formats are proposed. → Human and model measurements must establish usable headroom. **Warrant:** Task selection criteria and measured human/BERT baselines make difficulty operational instead of relying on novelty adjectives. **Checked locator:** §3 task design; Table 1 task formats; §5 experiments and Table 3 human/BERT/BERT++ results. **Limit:** The selected baselines establish contemporary headroom, not guaranteed longevity.

3. **T06-U019, T06-U020, T06-U021.** Measurement quality requires more than a difficult task list. → Tooling and usage rules are parts of the contribution. **Warrant:** Shared evaluation support and explicit participation/credit rules make comparative measurement usable and interpretable. **Checked locator:** §4 Benchmark Usage and corresponding toolkit/leaderboard rules. **Limit:** Software release and rules support adoption; the paper does not experimentally prove their long-term governance effect.

**Verification ceiling:** Human comparison uses the paper's non-expert performance estimate and contemporaneous submissions, not universal human capability. Table 3 demonstrates measured headroom for selected baselines, not permanent benchmark difficulty.

### T07 — WILDS: A Benchmark of in-the-Wild Distribution Shifts

[Fixed primary PDF](https://arxiv.org/pdf/2012.07421v3); [version metadata](https://arxiv.org/abs/2012.07421v3). Koh, Sagawa et al.; first version 2020, inspected revision 2021.

**Reading boundary:** Full §1 Introduction, PDF pp. 4–6; ends before §2 Existing ML benchmarks for distribution shifts. Figures 1–2 and captions excluded.

**Route:** Define deployment shifts → distinguish constructs → identify proxy mismatch → justify complementary benchmark → specify admission criteria → disclose exclusions → support adoption.

**Why use this case:** Use for evaluations where deployment relevance depends on splits, metrics and domain definitions rather than dataset size alone.

**What a fixed template misses:** A fixed novel-dataset story misses that most data are inherited and restructured. A performance-drop result is partly selected by the admission criterion; it cannot by itself establish realism or prevalence.

1. **T07-U009, T07-U010, T07-U011, T07-U012, T07-U013.** Synthetic shifts are useful controlled testbeds. → They need complementary deployment-linked evaluations. **Warrant:** Robustness can be specific to the shift; the proposed response changes data, metrics and train/test partitions together rather than merely enlarging a dataset. **Checked locator:** §2 existing benchmarks; Appendix A Dataset realism; §4 dataset definitions. **Limit:** The motivating nontransfer examples are cited prior work, not replications in this review.

2. **T07-U017, T07-U018, T07-U019, T07-U020, T07-U021, T07-U022.** Realistic difficulty is the design aim. → Three admission criteria operationalize challenge, relevance and possible leverage. **Warrant:** Performance loss, domain-informed splits/metrics and training metadata address different validity requirements; metadata is an opportunity, not demonstrated algorithmic success. **Checked locator:** §1 three criteria; Appendix A; §5 and Table 1; §6 and Table 2. **Limit:** Selecting datasets for performance drops means the observed drops do not estimate prevalence across all real-world shifts; Table 2 also reports adaptation omissions.

3. **T07-U023, T07-U024, T07-U025, T07-U026, T07-U027.** A broad curated portfolio is assembled. → Exclusions and standardized access are needed for an inspectable benchmark. **Warrant:** The paper discloses candidate domains without appreciable drops and explains modifications/package defaults, making scope and reuse visible. **Checked locator:** §8 survey; Appendix F excluded no-drop datasets; §10 package. **Limit:** Breadth does not imply representativeness; baseline defaults are a reproducibility aid, not a replication performed here.

**Verification ceiling:** Appendix A supplies a realism framework, not a universal realism proof. Table 1 compares dataset-specific ID/OOD settings; Table 2 covers selected methods with explicitly omitted detection adaptations. No claim of exhaustive real-world shifts follows.

### T08 — Holistic Evaluation of Language Models

[Fixed primary PDF](https://arxiv.org/pdf/2211.09110v2); [version metadata](https://arxiv.org/abs/2211.09110v2). Liang et al.; first version 2022, inspected revision 2023.

**Reading boundary:** Full §1, including §1.1 HELM, all 25 findings of §1.2, §1.3 Contributions and the final attribution passage, PDF pp. 2–10. Ends before Contents and §2. Figures 1–4, captions and footnotes excluded.

**Route:** Normative role of benchmarks → define holistic evaluation → operationalize three principles → audit comparability → specify adaptation → acknowledge validity threats → extensive findings → contribution inventory and credit.

**Why use this case:** Use for measurement infrastructure papers whose claims require explicit coverage, constructs, protocols and known omissions.

**What a fixed template misses:** HELM has three different lists doing different jobs: design principles, 25 findings, and contributions. Collapsing them into one contribution list erases the criterion-to-operation-to-observation argument. Its long Introduction is a genre case, not a universal length recommendation.

1. **T08-U015, T08-U016, T08-U024, T08-U028, T08-U029, T08-U033, T08-U036, T08-U037.** Exhaustive holistic evaluation is impossible and constructs are contested. → A taxonomy plus explicit coverage/missingness can still support a bounded holistic claim. **Warrant:** The authors distinguish the design space from the implemented subset and report a scenario-metric matrix rather than equating a long dataset list with completeness. **Checked locator:** §1.1; Figure 2; Table 4 (98 of 112 core pairs); §10 missing evaluations. **Limit:** Measured coverage concerns chosen categories only; omitted pairs can be undefined or judged invalid, and quantified fairness is not the whole social construct.

2. **T08-U053, T08-U054, T08-U056, T08-U057, T08-U058, T08-U060, T08-U061, T08-U062.** Previous models lack common datasets and comparable adaptation conditions. → Dense standardized evaluation improves cross-model interpretability. **Warrant:** A documented audit shows missing overlap; Figure 4 compares prior and new coverage, while the prompting analysis demonstrates why nominally shared datasets are insufficient. **Checked locator:** Figure 4 and Appendix F; §8.2 prompting analysis; Figure 33. **Limit:** Standardization controls a protocol; it does not prove that the protocol is equally suitable for every model or remove training-data/compute confounds.

3. **T08-U065, T08-U066, T08-U069, T08-U070, T08-U132, T08-U133, T08-U134.** Generic shared prompts are chosen for comparability, with caveats. → Adaptation can reverse measured accuracy and complicate fairness of comparison. **Warrant:** Figure 33 and its discussion show the OPT/HellaSwag contrast and an Anthropic exception on other multiple-choice scenarios; a common prompt is not a universal optimum. **Checked locator:** §8.2, Figure 33 and the following 'Formulation of multiple choice scenarios' discussion; §1.2 findings 22–23. **Limit:** The HellaSwag adaptation ordering is consistent across the tested models; model-dependent exceptions occur in other scenarios. Do not generalize the rank-reversal claim to every scenario.

**Verification ceiling:** Full Introduction read; only pivotal evidence locators inspected, not all 25 findings independently checked. Findings are a fixed historical snapshot conditional on model access, prompt choices, metric operationalizations and uncertain contamination. Uniform prompts are not proven equally suitable.

### T09 — Measuring Massive Multitask Language Understanding

[Fixed primary PDF](https://arxiv.org/pdf/2009.03300v3); [version metadata](https://arxiv.org/abs/2009.03300v3). Hendrycks et al.; first version 2020, inspected revision 2021.

**Reading boundary:** Full §1, PDF pp. 1–2; ends before §2 Related Work. Figure 1 panels/captions and page furniture excluded.

**Route:** Repeated saturation → unmeasured pretraining knowledge → zero/few-shot test design → subject breadth → scale result → unevenness → calibration and consequential blind spots.

**Why use this case:** Use for construct-expansion benchmarks that need to explain both what to test and why the protocol tests it.

**What a fixed template misses:** Simply replacing an easy benchmark with a harder one misses the pretraining-exposure warrant and protocol choice. Aggregate improvement is immediately qualified by subject-level and calibration failures.

1. **T09-U008, T09-U009, T09-U010, T09-U011, T09-U012, T09-U013.** Existing benchmarks cover only part of the knowledge encountered in pretraining. → A broad subject test with zero/few-shot evaluation targets that missing ability. **Warrant:** The argument ties the new construct to training exposure and constrains the protocol to reduce task-specific learning during evaluation. **Checked locator:** §3 A Multitask Test; §4.1 evaluation setup and few-shot prompt description. **Limit:** No protocol completely isolates pretraining knowledge from contamination, prompting skill or question-format effects.

2. **T09-U019, T09-U020, T09-U021, T09-U022, T09-U023, T09-U024.** A large model exceeds chance on aggregate. → The gain does not amount to balanced subject competence. **Warrant:** Size comparisons quantify aggregate improvement; subject disaggregation shows unevenness and specific weak areas. **Checked locator:** Table 1; §4.2 results; Figure 6 and Appendix Figure 9. **Limit:** The 43.9% figure is a particular few-shot model result; no present-day ranking is implied.

3. **T09-U024, T09-U025, T09-U026, T09-U027, T09-U028.** Some weak subjects matter for consequential decisions. → Accuracy alone misses whether the model knows its limitations. **Warrant:** The calibration analysis adds a confidence/accuracy relationship to the subject score inventory. **Checked locator:** §4.2 calibration discussion and Figure 8; Appendix Figure 11. **Limit:** Figure 8 is zero-shot GPT-3 calibration, while the earlier headline is few-shot. Professional exam questions are not a complete safety or competence assessment.

**Verification ceiling:** Table 1's 43.9% is the specified GPT-3 few-shot result; Figure 8 concerns zero-shot calibration. Subject-test performance is not comprehensive professional competence, and saturation alone does not prove a construct-valid replacement.

### T10 — SWE-bench: Can Language Models Resolve Real-World GitHub Issues?

[Fixed primary PDF](https://arxiv.org/pdf/2310.06770v3); [version metadata](https://arxiv.org/abs/2310.06770v3). Jimenez, Yang et al.; first version 2023, inspected revision 2024.

**Reading boundary:** Full §1, PDF pp. 1–2; ends before §2 SWE-bench. Figure 1, its caption and author/resource footnote excluded.

**Route:** Deployment need → benchmark saturation → challenge/verifiability tension → code tests → repository realism → input/output/oracle → baseline result → training resources.

**Why use this case:** Use when benchmark validity depends on a realistic work unit and a checkable success oracle.

**What a fixed template misses:** A generic task-gap-bullets route misses the two-constraint design argument. The execution oracle is part of the contribution and must be explained before a low solve rate has meaning.

1. **T10-U004, T10-U005, T10-U006, T10-U007, T10-U008, T10-U009.** A benchmark needs both challenging tasks and verifiable predictions. → Repository issue resolution offers a more realistic unit while retaining executable evaluation. **Warrant:** The paper pairs a richer input/action space with repository tests, rather than relying only on longer prompts or a harder score. **Checked locator:** §2.1 construction pipeline, Figure 2; §2.2 Task Formulation; Figure 1 overview. **Limit:** Merged PRs and tests operationalize success but do not prove the benchmark captures every aspect of engineering.

2. **T10-U010, T10-U011, T10-U012, T10-U015, T10-U016.** Input, patch output and test oracle are specified. → The reported baseline solve rate indicates difficulty under that setup. **Warrant:** Evaluation applies patches and runs issue-linked tests; Table 2 ties the result to BM25 retrieval and maximum context content. **Checked locator:** §2.2 evaluation metrics; §4.1 retrieval; Table 2 (Claude 2, BM25, 13k: 1.96%). **Limit:** Retrieval/context limits are part of the result. This rate must not be presented as a model-intrinsic ceiling or a current best score.

3. **T10-U017, T10-U018, T10-U019, T10-U020.** The test is difficult for existing models. → Separate training data and tuned baselines provide a development route. **Warrant:** The paper distinguishes test and non-test task collections and reports conditional model comparisons rather than only issuing a challenge. **Checked locator:** §3 SWE-Llama; §4.3 Models; Table 4 context coverage and §5 results. **Limit:** Training-artifact availability is not evidence that benchmark realism or all issue semantics are solved.

**Verification ceiling:** Table 2 binds 1.96% to Claude 2 with BM25 and 13k maximum content. It is not a current best-system claim. Passing selected repository tests is the benchmark's operational resolution criterion, not a proof of complete issue semantics.

## Review limitations and handoff

The ten supplied candidates define the review boundary. There was one primary-text reader/annotator in this lane; the parent workflow may independently spot-check these annotations. There was no independent duplicate extraction, comprehensive cited-literature audit, formal bias rating, statistical synthesis, proof replay, model execution or benchmark replication. For HELM, reading the full Introduction does not mean independently validating all 25 reported findings: the three pivotal transition checks are the explicit evidence-audit scope. The same distinction between full rhetorical reading and selective scientific verification applies to every case.

To reuse the corpus, select a case by contribution type and required warrant, inspect its full local sequence, and compare the assumptions and evidence with the new manuscript. Treat routes as alternatives to reason about, not scripts to copy. A draft's scientific claims still need their own verified evidence.

