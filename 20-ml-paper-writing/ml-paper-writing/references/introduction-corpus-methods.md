# Introduction corpus: methods and systems cases

This is a bounded **Evidence Review of writing decisions**, accessed 2026-10-30. It covers ten complete Introductions and 266 sentence/statement units. It is not a representative sample of CS, a ranking of writing quality, an empirical study of persuasion, or independent validation of the papers' scientific results.

The companion [JSONL](introduction-corpus-methods.jsonl) contains every unit's function, dependencies, reason for its position, evidence status, and two or three pivotal transitions per paper. Its routes were described after reading the sources; papers were not assigned to a preselected template. The corpus supplies counterexamples and design options, not rules inferred from famous papers' success.

## Scope and reading protocol

- Candidates were assigned in advance: nine named arXiv papers plus the original MapReduce paper. Inclusion required the whole Introduction and original body evidence for pivotal claims. All ten met that threshold; no paper was substituted.
- Nine records use **arXiv v1**, even where a later version is better known. MapReduce uses Google's archived 2004 author paper, marked for OSDI 2004, not the later CACM account. This is deliberate version binding, not a claim that v1 is the definitive publication.
- Source identity was checked against arXiv metadata and the original USENIX paper. The USENIX direct download returned HTTP 403; Google's original archived PDF supplied the full MapReduce reading. Full-text bytes were piped to `pdftotext`; working text remained in declared runtime files `/tmp/intro-methods-M01.txt` through `M10.txt`. No source PDFs or copied Introductions are included here.
- PDF two-column reading order was reconstructed where floating figures disrupted extraction, especially ResNet, PagedAttention, MapReduce and Ray. Captions, labels, author notes and footnotes are excluded from unit counts. LoRA's main-text Terminologies paragraph is included because it remains inside Section 1.
- The unit normally is a main-text sentence, with embedded examples kept inside it. ResNet's two result clauses and ReAct's four contribution clauses are split explicitly. Paragraph/sentence locators count visual prose order; bullets and LoRA terminology use separately named locators. The section's end is the next numbered section, recorded for every case.
- Extraction and appraisal were performed by one reader. Machine checks verify JSON structure, IDs, counts and backward dependencies; these checks cannot certify rhetorical interpretation. A parent integration review may spot-check the evidence; **no completed independent review is claimed here**.
- No systematic correction/retraction search, full backward-citation audit, proof audit or experimental replication was performed. Version histories were inspected to bind the artifact, not to claim that later corrections are absent.

## Verified reading register

| Case | Fixed primary source | Whole Introduction boundary | Units | Body evidence inspected |
|---|---|---|---:|---|
| M01 | [Vaswani et al., 2017](https://arxiv.org/pdf/1706.03762v1) | §1, PDF pp.1–2; before §2 Background | 11 | §4/Table 1; §5.2; §6.1/Table 2 |
| M02 | [He et al., 2015](https://arxiv.org/pdf/1512.03385v1) | §1, PDF pp.1–2; before §2 Related Work | 36 | §3.2; §4.1/Figure 4/Table 2; §4.2/Figure 6/Table 6 |
| M03 | [Ho, Jain and Abbeel, 2020](https://arxiv.org/pdf/2006.11239v1) | §1, PDF pp.1–2; before §2 Background | 13 | §3.2/§3.4; Tables 1–2; §4.3/Algorithms 3–4/Figure 5 |
| M04 | [Hu et al., 2021](https://arxiv.org/pdf/2106.09685v1) | §1, PDF pp.1–2, including Terminologies; before §2 Problem Statement | 25 | §3/§3.1; Table 1; §6.2/Table 4 |
| M05 | [Lewis et al., 2020](https://arxiv.org/pdf/2005.11401v1) | §1, PDF pp.1–2; before §2 Methods | 20 | §2.1–2.4; Tables 1–3; §4.5 knowledge-update experiment |
| M06 | [Yao et al., 2022](https://arxiv.org/pdf/2210.03629v1) | §1, PDF pp.1–3; before §2 ReAct | 26 | §2 formalization; §3/Tables 1–2/Figure 2; §4/Tables 3–4 |
| M07 | [Dao et al., 2022](https://arxiv.org/pdf/2205.14135v1) | §1, PDF pp.1–3; before §2 Background | 38 | §3.2/Theorem 2/Proposition 3 and Appendix C proof; §4.1/Tables 1–3; §4.3 |
| M08 | [Kwon et al., 2023](https://arxiv.org/pdf/2309.06180v1) | §1, PDF pp.1–2; before §2 Background | 49 | §6.1–6.3/Figures 12–15; §7.1/Figure 18a |
| M09 | [Dean and Ghemawat, 2004](https://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf) | §1, PDF pp.1–2; before §2 Programming Model | 15 | §3.3; §5.3–5.5/Figure 3; §6/Table 1 |
| M10 | [Moritz et al., 2017](https://arxiv.org/pdf/1712.05889v1) | §1, PDF pp.1–2; before §2 Motivation and Requirements | 33 | §2–3.2; §6.1/Figures 7–9; §6.2/Figures 10–11; §6.3.3/Table 3 |

The JSONL evidence codes distinguish **C**: cited background not independently re-audited; **D**: definition/design specification; **M**: mechanistic or mathematical reasoning, subject to stated conditions; **H**: hypothesis or forecast; **I**: interpretation/inference; **E**: illustrative example; **Q**: motivating question; **R**: recap/navigation; and **B**: original body evidence inspected at the stated locator. Mixed codes are intentional. A B label is not a reproducibility or correctness certificate. Functions, dependencies and editorial judgments are the present reader's interpretations.

## What the sentence chains actually do

### M01: remove a dependency before advertising the result

The short Introduction earns the replacement architecture through a causal chain: incumbent computation → recurrent dependency → limited parallelism → incomplete efficiency workarounds → attention as an available component. U10 therefore has something concrete to remove. U11 pays off the claim with a result, but the body separates the base model's twelve-hour schedule from the larger model's longer training. Table 1 concerns layer dependencies; it does not make autoregressive decoding parallel. The second opening sentence is a candidate for compression when its citations add no useful distinction. There is no explicit research question or contribution list. See [§1, §4 and §5.2](https://arxiv.org/pdf/1706.03762v1).

### M02: distinguish an observed failure, an existence argument and a hypothesis

ResNet does not simply say deeper networks should win. U8–U10 establish higher training error; U13–U15 construct a no-worse solution and expose the solver's failure to find it. U20 then labels easier residual optimization as a hypothesis. The matched plain/residual experiments address that claim more directly than competition rankings do. Its final generality language exceeds the tested domain, and Table 6 supplies a useful boundary: extreme depth does not guarantee better test error. Preserve this distinction when borrowing the structure; neither an identity construction nor an intuitive limiting case is an optimization theorem. See [§1, Figure 4 and Table 6](https://arxiv.org/pdf/1512.03385v1).

### M03: use a negative metric to open an explanatory contribution

DDPM moves quickly from model-family definition to a missing demonstration, then connects a parameterization to observed sample quality. The final paragraph deliberately reports weaker likelihood and explains it through rate/distortion. This is a strong counterexample to requiring the ending to announce superiority on every axis. The score connection, objective ablation and compression interpretation are different claims with different warrants. In particular, a conceptual coding procedure is not an implemented codec benchmark. Its broad generative-progress opening is compressible; the negative result is not disposable because it motivates the final contribution. See [§3.2, Tables 1–2 and §4.3](https://arxiv.org/pdf/2006.11239v1).

### M04: turn operational constraints into consequences of the mechanism

LoRA's gap is conjunctive: reduce task-specific storage and training burden while avoiding latency/context penalties and retaining quality. The intrinsic-dimension citation motivates a low-rank-update hypothesis; it does not prove it. Table 4 supplies limited empirical support. The advantages list explains operational consequences of a linear factorized update, including a merge that applies to fixed-task inference; switching and mixed-task batching remain distinct issues. Notation at the end is part of this Introduction's local design. The benefit lead-in and small-matrix restatement can be compressed, but the hypothesis-to-evidence boundary should remain. See [§3, §3.1 and §6.2](https://arxiv.org/pdf/2106.09685v1).

### M05: specify what is new in a composition

RAG identifies a representational liability, acknowledges close hybrid predecessors, and extends their scope to generation. Its explanation of components, latent documents and two marginalizations makes the novelty more precise than claiming retrieval itself is new. The subsequent from-scratch/pretrained distinction prevents another possible misreading. Evaluation closes several separate loops, including an imperfect knowledge-update demonstration. Retrieved documents offer an inspection route; they do not certify faithful generation. The FEVER comparison is deliberately weaker than a best-result claim. Keep that calibration instead of forcing one triumphant summary across all tasks. See [§2, Tables 1–3 and §4.5](https://arxiv.org/pdf/2005.11401v1).

### M06: reciprocal mechanisms need asymmetric evidence

ReAct's cooking example illustrates both directions of interaction: reasoning guides action; action supplies information. Its prior-work paragraph then assigns a different limitation to each isolated capability. That analogy is explanatory rather than evidence that LLMs implement human cognition. The body reports search failures and reasoning-loop errors, and its strongest reasoning-task setup combines methods. Visible traces also do not establish faithful access to internal computation. The contribution recap repeats much of the preceding evaluation paragraph and is a plausible compression target. An example can earn its place by explaining the interaction; it need not become mandatory decoration. See [§2–4, especially Tables 1–4](https://arxiv.org/pdf/2210.03629v1).

### M07: preserve the metric and the theorem's quantifier

FlashAttention's decisive move is from FLOPs to IO and elapsed time. The following sentences name obstacles in forward reduction and backward storage, then match techniques to each obstacle. Theory and measurements strengthen different parts of that explanation. Proposition 3 does not establish pointwise optimality at every SRAM size: its quantifier excludes an asymptotic improvement over all sizes, with the proof using a large-memory endpoint. Kernel, end-to-end training and longer-context quality results also have different comparison contracts. The Introduction explicitly concedes that some approximate methods become faster in a longer-sequence regime. See [§3.2/Appendix C and §4](https://arxiv.org/pdf/2205.14135v1).

### M08: derive the optimization target from the resource budget

PagedAttention takes more sentences because it must connect serving cost, token generation, batching, a concrete memory budget, fragmentation and duplication. Its paging analogy is useful because each property closes a previously named failure: small on-demand blocks, equal-size allocation and sharing. The body makes two limits particularly valuable for writing guidance: Orca is reimplemented under explicit reservation assumptions, and attention-kernel latency is higher even while system throughput improves. Hence the unit of improvement is the serving system under the evaluated workload. The broad social-impact opening and repeated contribution recap are more compressible than the memory diagnosis. See [§6.1–6.3 and §7.1](https://arxiv.org/pdf/2309.06180v1).

### M09: an abstraction can begin with recurring work

MapReduce starts from firsthand production computations and the mismatch between simple application intent and distributed execution machinery. The familiar functional primitives are credited; the contribution combines a usable interface with an implementation. Failure semantics in the body condition sequential-equivalent behavior on deterministic operators and commit handling. Its failure test kills worker processes on functioning machines, a narrower scenario than arbitrary machine failure. Production adoption supports practical relevance, not a controlled usability conclusion. The six roadmap sentences are navigation and a clear compression opportunity. Neither a SOTA opening nor an interrogative problem statement is necessary here. See [§1, §3.3 and §5–6](https://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf).

### M10: derive requirements before listing architecture

Ray's Introduction derives graph variability, state, throughput and latency from RL workloads, then maps abstractions and control-plane choices to those requirements. This makes the design description assessable without a result-heavy ending. The generic forecast about emerging AI is less secure than the workload examples. The scaling experiment is embarrassingly parallel; the simulated robot uses soft deadlines and fails at tighter budgets. Neither proves every RL graph scales linearly or real robots receive hard guarantees. The observed structure is requirements-driven, but that does not make a requirements list obligatory for papers with a different scientific problem. See [§2–3 and §6](https://arxiv.org/pdf/1712.05889v1).

## Transferable decisions, with boundaries

1. **Give a sentence an inferential job.** A background sentence earns space if the next step depends on it. M01 explains a dependency; M08 accounts for memory; M02 eliminates an alternative explanation. A popular field or impressive model size does not by itself establish the paper's specific problem.
2. **Choose the kind of gap that the evidence supports.** M02 diagnoses an observed failure. M03 addresses a missing demonstration. M04 proposes a structural hypothesis under practical constraints. M09 abstracts repeated experience. These are distinct warrants; none should be rewritten into a generic claim that existing work is inadequate.
3. **Explain why the intervention addresses that gap.** Name the causal premise, not merely a new component. In M07, avoiding intermediate traffic follows from an IO diagnosis. In M05, the key novelty includes pretrained access and generative output scope. This is editorial guidance inferred from the cases, not proof that one presentation causes acceptance.
4. **Match the payoff to the comparison unit.** Architecture, kernel, training run, complete serving system and deployment experience support different claims. A faster component need not make a system faster, and M08 demonstrates the converse. State configuration, workload, model and baseline conditions where they matter.
5. **Let a limitation carry argument.** DDPM's likelihood deficit motivates compression analysis; ReAct's failures motivate hybrid behavior; FlashAttention marks approximate-method crossover; ResNet's extreme-depth result limits a monotonic-depth story. Removing these limits can damage the reasoning rather than strengthen the prose.
6. **Use questions, bullets and roadmaps only when they help.** M02 and M07 contain explicit motivating questions. Other cases specify the uncertainty through an explanation or contrast. M01, M03, M05 and M09 have no contribution bullets. M09 uses a long roadmap; M10 ends with an architecture recap. These are counterexamples to mandatory surface forms, not estimates of their prevalence across CS.
7. **Compress duplication before removing warrants.** Candidate cuts include generic trend sentences, lead-ins announcing lists and recaps that merely repeat nearby claims. Preserve conditions, alternative explanations, distinct comparison axes and the sentence that makes the proposed intervention follow from the problem.

This subset is predominantly CS methods and systems. Its mathematical reasoning includes constructive arguments, distributional conditions and complexity quantifiers, but it is **not a corpus of mathematics-paper Introductions**. Any guidance for theorem-led mathematics needs separate primary examples and should not be inferred from these ten cases alone.

