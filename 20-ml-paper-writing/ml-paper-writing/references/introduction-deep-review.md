# Deep Introduction review: computer science first

## Contents

- [Scope and protocol](#scope-and-protocol)
- [Sampling and extraction](#sampling-and-extraction)
- [Coverage and case index](#coverage-and-case-index)
- [What changed in the guidance](#what-changed-in-the-guidance)
- [Additional primary writing sources](#additional-primary-writing-sources)
- [Review and evaluation](#review-and-evaluation)
- [Evidence boundaries](#evidence-boundaries)

## Scope and protocol

Started 2026-10-30 after the user rejected the three-case pilot as insufficient.
The user then specified **computer science as the main domain, mathematics as a
secondary domain**. This supersedes treating clinical writing as the main case base.
Public papers only; no private manuscript or research result enters the corpus.

Question: how do Introduction sentences establish reader context, delimit a claim,
connect evidence or assumptions to a design/theorem/measurement, and manage novelty
and scope across different CS and mathematical contributions?

Mode: purposive, comparative Evidence Review. It is neither a systematic review nor
a measured ranking of writing methods. The objective is inspectable argument
patterns and conditional guidance, not evidence that a particular structure causes
publication acceptance. Existing uncommitted skill edits are retained as the pilot.

## Sampling and extraction

Initial target: about 30 complete Introductions, with three complementary lanes:

1. Diagnostic findings, robustness and changed assumptions: ten candidates.
2. Methods, representations and computer systems: ten candidates.
3. Theory/mathematics and benchmarks/measurement: ten candidates.

The parent investigator may add recent or contrasting cases where these strata
leave a concrete gap. Versions of one paper are one case. EOE, ZS-NTTA and Transformer
are reread members of the expanded corpus, not counted again as additional papers.
An inaccessible Introduction is not counted as read; replacements retain reasons.

Primary access is fixed-version arXiv full text or original author/venue copies.
Paper discovery is purposive by research contribution, followed by metadata checks;
it is not a database-complete search. Guidance discovery additionally examines
original CS/math writing advice and rhetorical research on computer-science papers.
Do not treat copied skill collections or search snippets as independent evidence.

For every included case record title, source/version, domain, exact reading scope,
segmentation convention and a complete functional map of the stated scope. Distinguish
sentences from colon announcements, clauses, theorem statements and grouped moves.
Use stable paragraph/sentence IDs or PDF page plus a short anchor. Do not equate a
move count with a sentence count. Preserve sources as links and original commentary;
full texts/PDFs belong only in external runtime, not this repository.

Each case must examine two or three pivotal transitions, their implicit warrant,
what evidence or assumptions they rely on, and what stronger conclusion is not
established. Inspect the cited body location where feasible; record partial checks
honestly. This is not replication of experiments or independent proof verification.

Extraction schema: one JSONL object per case, including `units` and
`pivotal_transitions`, plus a readable lane synthesis. Rhetorical labels are analyst
interpretations, not asserted author intent. Review whether multiple route labels
are needed rather than forcing each paper into exactly one predefined box.

Stopping condition: usable full-text coverage across the selected contribution
families, explicit contrary structures, an audited sample of original-source
locators, actionable changes to the guide, and behavior checks on previously
underrepresented genres. A paper-count target alone does not pass this condition.

## Coverage and case index

The expanded corpus contains **33 unique papers**: **31 CS-related papers and two
pure-mathematics papers** (T04 and C03). CS coverage concentrates on ML/AI, systems,
theory and evaluation; this is not comprehensive coverage of all CS subfields.
The years represented are 2004–2025. The inclusion of historical papers is deliberate:
they supply structural contrasts, not a claim about current technical leadership.

All 33 declared Introduction scopes were read in full. Depth is counted separately:

| Lane | Papers | Annotation units | Granularity | Pivotal transition records |
|---|---:|---:|---|---:|
| [Diagnosis, phenomena and audits](introduction-corpus-diagnostic.md) | 10 | 149 | Contiguous statement groups with sentence-span locators; not 149 individual sentences. | 30 |
| [Methods and systems](introduction-corpus-methods.md) | 10 | 266 | Individual sentences, with explicitly split contribution clauses in ReAct. | 29 |
| [Theory and benchmarks](introduction-corpus-theory-benchmarks.md) | 10 | 448 | Sentences, declared lead-ins/nominal items and formal mathematical blocks. | 30 |
| [Recent CS and mathematics](introduction-corpus-contrasts.md) | 3 | 119 | 115 prose sentences, three theorem blocks and one composite definition. | 9 |
| **Total** | **33** | **982** | **23 sentence/formal-unit maps and 10 grouped maps; not 982 plain sentences.** | **98** |

Each JSONL companion records fixed source/version, scope, segmentation, function,
dependency, reason for placement, evidence status, pivotal warrants, suitability,
counterexample and verification limits. The 98 transitions are selected high-value
bridges, not every adjacent sentence pair. Their original body locations were
inspected by extractors; this does not certify the underlying scientific results.

| ID | Paper | Unit count | Primary source |
|---|---|---:|---|
| D01 | Envisioning Outlier Exposure (EOE) | 15 groups | [2406.00806v1](https://arxiv.org/pdf/2406.00806v1) |
| D02 | Noisy Test-Time Adaptation in Vision-Language Models | 18 groups | [2502.14604v1](https://arxiv.org/pdf/2502.14604v1) |
| D03 | Deep Double Descent | 12 groups | [1912.02292v1](https://arxiv.org/pdf/1912.02292v1) |
| D04 | Understanding Deep Learning Requires Rethinking Generalization | 22 groups | [1611.03530v1](https://arxiv.org/pdf/1611.03530v1) |
| D05 | Lost in the Middle | 13 groups | [2307.03172v1](https://arxiv.org/pdf/2307.03172v1) |
| D06 | Are We Really Making Much Progress? Neural Recommendation Analysis | 14 groups | [1907.06902v1](https://arxiv.org/pdf/1907.06902v1) |
| D07 | The Pitfalls of Simplicity Bias in Neural Networks | 18 groups | [2006.07710v1](https://arxiv.org/pdf/2006.07710v1) |
| D08 | Rethinking ImageNet Pre-training | 14 groups | [1811.08883v1](https://arxiv.org/pdf/1811.08883v1) |
| D09 | Source Hypothesis Transfer for Unsupervised Domain Adaptation | 14 groups | [2002.08546v1](https://arxiv.org/pdf/2002.08546v1) |
| D10 | Intriguing Properties of Neural Networks | 9 groups | [1312.6199v1](https://arxiv.org/pdf/1312.6199v1) |
| M01 | Attention Is All You Need | 11 | [1706.03762v1](https://arxiv.org/pdf/1706.03762v1) |
| M02 | Deep Residual Learning for Image Recognition | 36 | [1512.03385v1](https://arxiv.org/pdf/1512.03385v1) |
| M03 | Denoising Diffusion Probabilistic Models | 13 | [2006.11239v1](https://arxiv.org/pdf/2006.11239v1) |
| M04 | LoRA | 25 | [2106.09685v1](https://arxiv.org/pdf/2106.09685v1) |
| M05 | Retrieval-Augmented Generation | 20 | [2005.11401v1](https://arxiv.org/pdf/2005.11401v1) |
| M06 | ReAct | 26 | [2210.03629v1](https://arxiv.org/pdf/2210.03629v1) |
| M07 | FlashAttention | 38 | [2205.14135v1](https://arxiv.org/pdf/2205.14135v1) |
| M08 | PagedAttention / vLLM | 49 | [2309.06180v1](https://arxiv.org/pdf/2309.06180v1) |
| M09 | MapReduce | 15 | [Original Google/OSDI paper](https://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf) |
| M10 | Ray | 33 | [1712.05889v1](https://arxiv.org/pdf/1712.05889v1) |
| T01 | Computing Nonvacuous Generalization Bounds | 69 | [1703.11008v2](https://arxiv.org/pdf/1703.11008v2) |
| T02 | Neural Tangent Kernel | 24 | [1806.07572v4](https://arxiv.org/pdf/1806.07572v4) |
| T03 | Turing Completeness of Modern Neural Network Architectures | 45 | [1901.03429v1](https://arxiv.org/pdf/1901.03429v1) |
| T04 | Interlacing Families II / Kadison–Singer | 32 formal/prose units | [1306.3969v4](https://arxiv.org/pdf/1306.3969v4) |
| T05 | GLUE | 21 | [1804.07461v3](https://arxiv.org/pdf/1804.07461v3) |
| T06 | SuperGLUE | 22 | [1905.00537v3](https://arxiv.org/pdf/1905.00537v3) |
| T07 | WILDS | 32 | [2012.07421v3](https://arxiv.org/pdf/2012.07421v3) |
| T08 | HELM | 154 | [2211.09110v2](https://arxiv.org/pdf/2211.09110v2) |
| T09 | Measuring Massive Multitask Language Understanding | 29 | [2009.03300v3](https://arxiv.org/pdf/2009.03300v3) |
| T10 | SWE-bench | 20 | [2310.06770v3](https://arxiv.org/pdf/2310.06770v3) |
| C01 | AlphaEvolve | 29 | [2506.13131v1](https://arxiv.org/html/2506.13131v1) |
| C02 | DeepSeek-R1 | 53 | [2501.12948v1](https://arxiv.org/html/2501.12948v1) |
| C03 | On a Conjecture of Marton | 37 formal/prose units | [2311.05762v1](https://arxiv.org/html/2311.05762v1) |

The pilot's EOE 29-unit map and expanded D01 15-group map use different granularity,
not different paper counts. The pilot Transformer used v7; M01 fixes v1. Both are
one paper in the unique-case count. The full scope includes nested subsections:
Zhang's related-work subsection, HELM's nine-page §1 including 25 findings, and
DeepSeek-R1's contributions/evaluation summary are not silently omitted. Figures,
captions and footnotes are excluded from unit totals but relevant figures can be
inspected as evidence for a pivotal inference.

Access exceptions: MapReduce's USENIX endpoint returned 403; the original Google
archive supplied the full paper. No paper was counted from an abstract alone or
replaced by a secondary summary. The diagnostic notes explicitly exclude stray
editorial text inside D02's v1 figure from the main-prose map.

## What changed in the guidance

The pilot had seven proposed routes and eighteen sentence jobs. The expansion
supports a more useful **nine-route selector**, **twenty-three jobs**, eleven
sentence-pair construction patterns and nine detailed cards in
[the route playbook](introduction-route-playbook.md). Counts describe this guide,
not a discovered universal number of writing structures.

| Observation from cases | Change to authoring guidance | Suitable use / boundary |
|---|---|---|
| D03/D04/D05/D10 can end with a phenomenon, explanatory challenge or hypothesis. | Separate phenomenon/explanation from diagnosis leading to intervention. | Do not fabricate a new method to finish a valid finding paper. |
| D06/D08 revisit conclusions through controls and comparisons. | Add a controlled-audit route distinct from a repair algorithm. | The audit revises the tested conclusion, not every related field claim. |
| D01/D02 require a bridge between informative diagnosis and available inputs. | Spell out observation → inference → feasibility → design as different claims. | Oracle evidence does not directly validate a deployable method. |
| M07/M08/M09/M10 derive requirements from resource behavior and workloads. | Explain the resource mechanism before claiming efficiency. | Asymptotic work, kernel latency and serving throughput are different evidence. |
| M05/M06/C01 use distinct interfaces or search representations. | Require an operation-to-representation warrant and an evaluation contract. | An exposed object is not automatically faithful; automatic evaluation is not universally sound. |
| T04/C03 contain exact statements and meaningful reformulations. | Add formal-result, equivalence/reduction and proof-obstacle jobs. | Preserve quantifiers, direction, constants and existence/algorithmic distinctions. |
| T05/T06/T07/T08/T09/T10 operationalize different capabilities. | Explain construct → observable → instrument → validity before advertising scale. | Benchmark novelty, difficulty and construct validity are distinct. |
| M03/M02/C02 retain adverse or mixed evidence. | Put non-implications beside the affected claim. | Acknowledged trade-offs can sharpen the story rather than weaken it. |
| D10 branches; T08/C02 contain long structured summaries. | Permit branches, cycles and purposeful restatement. | Do not turn report-specific length into a conference-paper prescription. |

Each card now specifies when it fits, when it does not, the proposition each local
sentence needs to establish, what it enables next, the missing-premise failure to
avoid, and contrasting real cases. This is the main practical deliverable. The
corpus is inspectable evidence and a source of counterexamples, not text to imitate.

**One fully worked contrast:** a diagnostic sentence can establish that a changed
input improves discrimination; the next sentence should say what this supports,
not declare the only cause. A following feasibility sentence explains why that
input is unavailable. Only then does a question about an attainable substitute
follow. In a theorem paper, the corresponding pivotal bridge may instead be why an
equivalent formulation exposes the structure used by the proof. Neither bridge
can be supplied by writing “therefore, we propose” more fluently.

## Additional primary writing sources

These supplement the pilot source register; they are **three evidence units**, not
additional paper-case counts. Multiple Tao pages remain one author-guidance unit.
The twelve papers inside Anthony's study were not individually read for this corpus
and are not added to 33.

| ID | Primary source and exact reading scope | Use and limitation |
|---|---|---|
| A1 | Laurence Anthony (1999), *Writing Research Article Introductions in Software Engineering: How Accurate Is a Standard Model?*, IEEE Transactions on Professional Communication 42(1), 38–46, [DOI](https://doi.org/10.1109/47.749366); [author-uploaded full text](https://www.researchgate.net/publication/3230053_Writing_research_article_introductions_in_software_engineering_how_accurate_is_a_standard_model). Read method and results, especially step ambiguity, cyclicity, definitions/examples and evaluation of applicability/novelty, pp. 39–44. | A twelve-article SE corpus and four specialist consultations challenge an overly rigid linear model. This historical purposive study supports sensitivity to audience and mixed functions, not optimality of our nine routes or acceptance prediction. Its selection assumptions are not adopted as writing-quality labels. |
| G6 | Terence Tao, [On writing](https://terrytao.wordpress.com/advice-on-writing-papers/), [Introduction key points](https://terrytao.wordpress.com/advice-on-writing-papers/use-the-introduction-to-%E2%80%9Csell%E2%80%9D-the-key-points-of-your-paper/) and [Be considerate of your audience](https://terrytao.wordpress.com/career-advice/be-considerate-of-your-audience/). Relevant author-written advice about motivation, comparison, novelty, hypotheses and audience; comments are not evidence. | Supports making the mathematical advance and difficulty visible to the intended reader. Practitioner/editorial advice, not a controlled effectiveness study. |
| G7 | Timothy Gowers (2007), [My favourite pedagogical principle: examples first!](https://gowers.wordpress.com/2007/10/19/my-favourite-pedagogical-principle-examples-first/), the comparison of two explanations of fields and the ensuing reader-knowledge argument. | Supports examples before abstraction when the reader lacks the object. Transfer from teaching to Introduction design is our inference; this is not a mandatory opening rule. |

Anthony's full text was readable through the web tool's author-uploaded page while
the direct context fetch returned 403. Bibliographic identity was checked against
the author's publications page; the article itself begins at page 38. Knuth's
writing booklet and Goldreich's writing page were leads only, not used as appraised
support. The pilot's unavailable/unused leads remain documented in its register.

## Review and evaluation

Original-source checks and behavior checks answer different questions. Independent
review samples exact source locations and warrants; synthetic transfer tasks check
whether the loaded guidance preserves facts and fits a genre. Neither measures
acceptance rates or establishes writing SOTA. Exact scopes, findings, corrections,
artifact hashes and verification results are retained in
[`evaluations/introduction-deep-results.md`](../evaluations/introduction-deep-results.md).

## Evidence boundaries

- Favor source access and informative contrasts, not citations or prestige as proof
  of prose quality. Selection and survivorship bias remain.
- Historical papers illuminate argument structure, not current technical SOTA.
  Include recent contrasts where feasible without inventing a claim of currency.
- Do not infer route prevalence or acceptance probability from this purposive sample.
- Independent checking samples original text and pivotal warrants; not every
  annotation is independently double-coded. No inter-rater agreement is claimed.
- Preserve the pilot and its validation scope. Its synthetic cases do not count as
  real-paper research. New corpus entries do not themselves demonstrate skill efficacy.
- Retain the existing prohibition on installation, commit, push and publication for
  this task. Source changes stay on `docs/sentence-level-introductions`.
- No route-frequency estimates, causal writing-effect estimates or complete current
  research survey follow from 33 selected cases. No new 2026 paper was included;
  this is a contemporary review of selected accessible sources, not a claim to have
  exhausted the newest literature. Security, HCI, programming languages and many
  mathematical traditions remain outside the case coverage.
- Rhetorical annotations are interpretations; specialist proof review and experiment
  replication would require different work. Full reading, map granularity, sampled
  source checking and skill behavior results must remain separate reported quantities.
