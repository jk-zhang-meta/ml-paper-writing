# Ten complete Introductions: diagnostic and reassessment cases

This note compares **10 complete Introductions**, not ten abstracts or selected
opening paragraphs. The purpose is to improve sentence-level argumentative
decisions: what a statement contributes, which earlier statement licenses it, and
where an attractive transition exceeds its evidence. The companion
[introduction-corpus-diagnostic.jsonl](introduction-corpus-diagnostic.jsonl)
contains **149 manually segmented argument statement groups**, dependencies,
locators and evidence-status labels.

This is a bounded **Evidence Review**, accessed on **2026-10-30**. The ten supplied
candidates were retained after title/identifier checks against arXiv and the
original PDFs. No candidate was inaccessible or replaced. All sources below are
fixed **v1** versions; later revisions exist for several papers and were not
silently substituted. Source PDF bytes were fetched and piped to text extraction
in memory; no source PDF, full Introduction copy or extraction file was written
to this repository.

The corpus is purposive and entirely computer-science/ML-centered. Several papers
mix theory and experiments; it does **not** supply a pure-mathematics sample, a
representative sample of CS writing, or evidence that an observed rhetorical
pattern causes acceptance. Historical model and benchmark claims are bounded to
the paper versions, not claims about current systems.

## Scope and use of the maps

A map unit is a **contiguous statement group**, sometimes one sentence and
sometimes several sentences performing the same argumentative job. It is not
claimed to be a machine-counted sentence. PDF pages plus paragraph/sentence
ranges identify the source; complete paragraph, numbered-clause and list-item
units are explicitly marked. Paragraph numbers follow prose reading order,
excluding headings, captions, footnotes, affiliations and running matter.
Two-column order was restored before analysis. The maps cover the entire
Introduction body under these conventions.

The distinction matters: **149 is a count of analytical groups, not a count of
source sentences**. Each group is paraphrased rather than reproduced. Function,
dependency and compression judgments are the analyst's interpretations.

| Case | Fixed primary source | Introduction boundary | Contribution genre |
|---|---|---|---|
| D01 | [Cao et al., EOE (2024)](https://arxiv.org/pdf/2406.00806v1) | §1, pp.1–2, all three contribution bullets | Oracle-motivated method |
| D02 | [Cao et al., Noisy Test-Time Adaptation (2025)](https://arxiv.org/pdf/2502.14604v1) | §1, pp.1–3, all contribution bullets | Setting, diagnosis and method |
| D03 | [Nakkiran et al., Deep Double Descent (2019)](https://arxiv.org/pdf/1912.02292v1) | §1, pp.1–2; §2 excluded | Phenomenon and conjectural unification |
| D04 | [Zhang et al., Rethinking Generalization (2016)](https://arxiv.org/pdf/1611.03530v1) | §1 including **§1.1 and §1.2**, pp.1–3 | Explanatory stress test and theory |
| D05 | [Liu et al., Lost in the Middle (2023)](https://arxiv.org/pdf/2307.03172v1) | §1, pp.1–3, through code/data release | Controlled behavioral evaluation |
| D06 | [Ferrari Dacrema et al., Are We Really Making Much Progress? (2019)](https://arxiv.org/pdf/1907.06902v1) | §1, pp.1–2, through organization paragraph | Reproducibility/baseline audit |
| D07 | [Shah et al., Pitfalls of Simplicity Bias (2020)](https://arxiv.org/pdf/2006.07710v1) | §1, pp.1–3, including Summary/Organization | Operationalized mechanism testbed |
| D08 | [He et al., Rethinking ImageNet Pre-training (2018)](https://arxiv.org/pdf/1811.08883v1) | §1, pp.1–2; p.2 right-column §2 excluded | Controlled removal of a standard component |
| D09 | [Liang et al., SHOT (2020)](https://arxiv.org/pdf/2002.08546v1) | §1, pp.1–2, before Related Work | Changed information constraint and method |
| D10 | [Szegedy et al., Intriguing Properties (2013)](https://arxiv.org/pdf/1312.6199v1) | §1, pp.1–2, before Framework | Two parallel empirical surprises |

D02 v1 contains stray editorial annotations within Figure 1. They were excluded
with figure material, not treated as Introduction sentences. D04's Related Work
is numbered **1.2**, so omitting it would falsely label a partial reading complete.

## Pivotal transitions, case by case

### D01 — An oracle comparison creates a constrained research question

**Pivots.** D01.U04→U05 separates a failure from two possible explanations, then
changes the label space while retaining the VLM. The new claim is that the
interface can be improved; the warrant is the actual-OOD-name comparison in
Fig.1(a,b). U05→U06 then denies deployment access to that oracle information.
Only after that boundary does U07 propose generated substitutes. This ordering
makes the research question a consequence of evidence and constraints.
[EOE §1 and Fig.1, pp.1–2](https://arxiv.org/pdf/2406.00806v1)

U08→U09 adds scoring because a list of names alone is not a detector. The prompt
and score commitments have distinct evaluation destinations: §3.1–3.2,
§4.3/Fig.6, and §4.2/Tables1–4. The near-OOD discussion also records an extra
similarity filter for ImageNet-20. That qualification should survive a compressed
claim of broad success. The single oracle illustration does not establish that
model capacity is irrelevant or that label restriction is the unique cause.
[EOE §§3–4](https://arxiv.org/pdf/2406.00806v1)

**Writing lesson.** Preserve the oracle-to-feasibility transition. The advantages
paragraph and contribution bullets repeat some mechanism and scope information;
they offer more compression room than that transition. This pattern is useful
when an informative unavailable input can be approximated. It fails when the
diagnostic comparison is absent or the proposed surrogate has no warranted
connection to the oracle.

### D02 — A new setting and a diagnosis are different contributions

**Pivots.** U01→U03 first changes the task contract: zero-shot operation, online
noise detection and classification obligations. U04→U06 then gives adapting
baselines filtering and an adaptive threshold, observes their failures, and
varies the data admitted to updating. The GT-clean, filtered and all-update
pipelines in Table1 make a more informative comparison than the ranking figure
alone. The reported ordering has exceptions: SoTTA is near frozen CLIP under the
ordinary pipeline. [Noisy TTA §§1–3, Fig.2 and Table1](https://arxiv.org/pdf/2502.14604v1)

U06→U09 turns contamination/coupling evidence into a proposed update boundary.
The detailed gradient trajectory in Fig.4 is for Tent; it does not establish one
cause for every adaptation method. U10→U11 then introduces a **new failure of the
proposed detector** on all-clean streams and a second remedy. This nested branch
would disappear in a one-problem/one-solution rewrite.
[Noisy TTA §3.2 and §4](https://arxiv.org/pdf/2502.14604v1)

**Writing lesson.** Compress repeated advantages and contribution recaps before
cutting the all-clean boundary case. Use this structure when a setting change
requires both a new benchmark and a method. Do not present a method-specific
trajectory as a general causal law. The complete clean-stream ablation suite
was not independently audited in this note.

### D03 — A diagnostic contribution need not culminate in a repair

**Pivots.** U01→U05 reconciles two size intuitions by introducing interpolation
regimes. U08→U10 changes the explanatory coordinate from parameter count to a
training-dependent effective complexity, then checks epoch-wise behavior.
The paper explicitly calls the generalized account a hypothesis; §2 leaves
epsilon and regime boundaries informal. The observations do not prove that
hypothesis. [Deep Double Descent §§1–2, §6/Figs.9–10](https://arxiv.org/pdf/1912.02292v1)

U11→U12 predicts sample non-monotonicity from a shifted peak and supplies
translation examples. §7/Fig.11 varies training sample count while retaining the
model/procedure; the counterexample rejects unconditional monotonicity, not the
usual usefulness of additional data. Label noise strengthens many peaks, and
the paper also discusses plateaus and noiseless settings.
[Deep Double Descent §§5–7](https://arxiv.org/pdf/1912.02292v1)

**Writing lesson.** A contribution may be a shared variable and a set of
falsifiable predictions. Preserve observation/hypothesis distinctions. Historical
examples can be shortened before the definition and conditions. A required
method-design ending would manufacture a contribution the paper does not make.

### D04 — Negative evidence needs an explicit discrimination criterion

**Pivots.** U03→U06 asks whether proposed explanations distinguish unchanged
architectures trained on true versus randomized labels. The comparison is
informative because the explanatory account must change when the behavior
changes. §2.2 addresses particular complexity/stability accounts; this is not a
refutation of all learning theory.
[Rethinking Generalization §2, Fig.1](https://arxiv.org/pdf/1611.03530v1)

U12→U14 tests regularization separately and preserves the distinction between
being useful and being a sufficient explanation. The results contain
heterogeneity: the v1 text says AlexNet with weight decay did not converge on
random labels. U15→U19 adds finite-sample expressivity, then explicitly leaves
algorithmic choice and architecture-dependent generalization open. Existence of
a fitting network is not a guarantee that SGD finds it.
[Rethinking Generalization §3/Table1 and §1.1](https://arxiv.org/pdf/1611.03530v1)

**Writing lesson.** The three randomization implications are not interchangeable:
capacity, optimization and experimental control do different work. Compress the
citation inventory or repeated framing first. Use this approach to test
explanatory sufficiency; it fails if a local negative result is inflated into
universal impossibility or a complete replacement theory.

### D05 — A second task can narrow an explanation without establishing it

**Pivots.** U02→U05 separates usable context from maximum accepted context and
tests answer position using controlled prompt changes. U05→U08 removes much of
QA's semantic burden through a key-value task. Similar curves motivate a shared
question, but do not establish a shared internal mechanism.
[Lost in the Middle §3/Fig.5 and §4](https://arxiv.org/pdf/2307.03172v1)

U09→U11 keeps probes preliminary. Encoder-decoder robustness depends on sequence
length relative to training, while query-aware prompts strongly improve the
synthetic task without similarly repairing QA. These divergent results constrain
a tidy single-cause narrative. The architecture comparison also changes models
and training histories; it is not a clean intervention on architecture alone.
[Lost in the Middle §5, Figs.11–12](https://arxiv.org/pdf/2307.03172v1)

**Writing lesson.** Preserve why the simpler second task is needed and why its
repair does not settle the first task. Lists of model names can move to setup.
This route suits evaluative contributions that end in protocols and evidence,
not a solved mechanism or new algorithm.

### D06 — The sample-selection flow belongs in the argument

**Pivots.** U08→U10 makes reproducibility operational: eligible papers,
artifact availability, reconstructible data/splits and reasonable effort.
The 18 considered papers and seven reproduced papers are different denominators.
Eleven unavailable cases cannot become eleven negative algorithmic results.
[Progress audit §2.1 and Table1](https://arxiv.org/pdf/1907.06902v1)

U10→U12 asks a second question: whether reproduced results beat tuned simple
alternatives. CMN and MCRec provide concrete examples, but U12→U13 must retain
the Mult-VAE exception. Tables8–9 show that its comparison with SLIM depends on
metric and cutoff. Possible incentive problems discussed in the Introduction
are contextual hypotheses, not causes measured by this audit.
[Progress audit §3, Tables2–3 and8–9](https://arxiv.org/pdf/1907.06902v1)

**Writing lesson.** Compress multiple historical illustrations before the
eligibility rules, denominators or exception. Use this pattern for replication
and evaluation audits. It fails when artifact accessibility is mistaken for a
random sample or failure to reproduce is equated with falsity.

### D07 — Operationalization is a necessary bridge, not background detail

**Pivots.** U03→U06 separates feature simplicity from predictive strength and
constructs a dataset where both can vary. Without that bridge, saying that a
network prefers simple features is too vague to test. U08→U10 compares a
realizable multi-feature boundary with what training selects, combining a
restricted theorem and controlled feature-randomization evidence.
[Pitfalls of Simplicity Bias §§3–4, Theorem1 and Fig.3](https://arxiv.org/pdf/2006.07710v1)

U11→U13 extends the implications from robustness to in-distribution
generalization by making the simple feature less predictive. §5/Table2 tests
that case. The natural-world extension remains conditional: §4.3 explicitly
hypothesizes that spurious features are simple. §6 also notes that ensembles may
combine several simple features while remaining insensitive to complex ones;
a blanket no-benefit paraphrase would lose this qualification.
[Pitfalls of Simplicity Bias §§4.3–6](https://arxiv.org/pdf/2006.07710v1)

**Writing lesson.** The testbed definition earns space because it licenses the
inference. Repeated summary and roadmap prose is easier to shorten. This
structure suits operationalization papers; it fails when a tractable synthetic
notion is silently made universal.

### D08 — Removing a component can be the contribution

**Pivots.** U03→U08 reports successful training without ImageNet initialization
and identifies the normalization/time conditions needed for comparison. The
learning curves distinguish early speed from final accuracy. Holding a short
fine-tuning schedule fixed can disadvantage scratch training; equal local
iteration counts and equal total computation are different comparisons.
[Rethinking ImageNet Pre-training §3 and §5.1, Figs.1,3–4/Table1](https://arxiv.org/pdf/1811.08883v1)

U05→U09 addresses the low-data escape clause by retuning the pretrained baseline
and reusing those settings for scratch. U10→U11 interprets localization-sensitive
differences as a possible task-gap effect, not a uniquely identified cause.
COCO subsets with thousands of labels do not establish results for every
small-data transfer task.
[Rethinking ImageNet Pre-training §5.2/Fig.7 and Fig.6/Table2](https://arxiv.org/pdf/1811.08883v1)

**Writing lesson.** Preserve the matched baseline, schedules and resource
conditions. Generic opening praise and broad future speculation can be shorter.
The template fails if it insists on a new architecture or turns a conditional
counterexample into a universal recommendation against pretraining.

### D09 — A changed access rule is not a privacy guarantee

**Pivots.** U03→U06 defines source-model-only access before describing SHOT,
then distinguishes hypothesis-transfer predecessors. Table1 supports smaller
transmission size in its examples; it does not support a formal privacy
guarantee. U08→U11 contains a separate inferential safeguard: confident outputs
can still align to the wrong class, so target structure motivates pseudo-labels.
[SHOT §1/Table1 and §3.2–3.3](https://arxiv.org/pdf/2002.08546v1)

U12→U14 requires separate architecture ablations and task comparisons.
The digit discussion says pseudo-labeling adds limited gains in easy cases;
the Office results are not uniformly best and identify small target sets as a
possible constraint. These qualifications matter when the Introduction presents
broad versatility.
[SHOT §4.3–4.4, Tables2–7](https://arxiv.org/pdf/2002.08546v1)

**Writing lesson.** Shorten the catalog of standard adaptation methods before the
information boundary or confident-misalignment problem. Use this structure for
constraint-changing formulations. Do not copy a motivation's privacy language
into an unsupported security claim.

### D10 — Parallel findings need not form one causal funnel

**Pivots.** U02→U03 tests the implicit privileged-basis premise by comparing
unit directions with random directions. Qualitatively coherent exemplars are
evidence against a simple unit-inspection argument, not a proof that no unit
has meaning. The stability branch starts afresh at U05; it is not derived from
the representation branch.
[Intriguing Properties §3, Figs.1–4](https://arxiv.org/pdf/1312.6199v1)

U06→U08 asks whether perturbations are run-specific accidents, then tests
cross-model and cross-training-set transfer. Tables2–4 show variable transfer,
especially lower effectiveness for minimally perturbed inputs on disjoint
training sets. The optimization in §4.1 approximates a minimum. Neither
mathematical discontinuity of continuous logits nor universal transfer follows.
v1 also explicitly lacks quantitative MNIST convolutional-model results.
[Intriguing Properties §4.1–4.2, Tables2–4](https://arxiv.org/pdf/1312.6199v1)

**Writing lesson.** Preserve two branch-specific premises and the transfer
follow-up. The word-vector analogy is more compressible. This form suits
related discoveries sharing an interpretive question; forcing one chain would
invent a causal relation between unit semantics and adversarial sensitivity.

## What this corpus changes about sentence-level guidance

The corpus does not validate a fixed seven-route taxonomy. Its useful
counterexamples instead support a few **conditional editing tests**:

1. **Identify the inference, not only the sentence role.** A result sentence
   followed by a mechanism sentence needs a warrant. EOE's label intervention,
   noisy-TTA's update pipelines and Lost in the Middle's query placement
   support different strengths of inference.

2. **Let the contribution determine the ending.** D03 can end in a prediction,
   D05 in evaluation protocols, D06 in an audit and D10 in unresolved
   interpretation. A method or repair is not compulsory.

3. **Separate feasibility, operationalization and causality.** D01 needs an
   unavailable-oracle boundary; D07 needs a measurable construct; D09 needs a
   changed access contract. None is interchangeable with a causal explanation.

4. **Allow branching when the evidence branches.** D02's clean-stream failure,
   D09's confident misalignment and D10's paired findings each defeat a rigid
   single-funnel order. A dependency map should represent these branches.

5. **Use negative controls and exceptions to size the claim.** The Mult-VAE
   exception, architecture-dependent random-label fitting, task-dependent
   query-placement effects and small-target SHOT results prevent universal
   paraphrases.

6. **Compress repetition before warrants.** Advantage lists, contribution
   recaps, historical inventories and roadmaps are often candidates. A
   comparator definition, unavailable-input statement, constructed feature
   distinction or acknowledged alternative explanation is usually carrying
   more argumentative weight.

These are analyst-derived design heuristics. Their applicability must be
checked against a new paper's actual evidence, venue budget and intended reader;
the corpus does not establish a single optimal order or paragraph count.

## Verification and remaining limits

Identity checks used the fixed-version arXiv records and original PDF title
pages. Every mapped Introduction was read through its stated ending. For each
paper, two or three pivotal transitions were followed into original methods,
figures, tables or result discussions far enough to distinguish observed
behavior from a proposed explanation. The JSONL records exact evidence
destinations and unresolved limits.

This was a single-analyst extraction and source check, not dual independent
rhetorical coding. It does not claim experiment replication, proof
verification, exhaustive source-method comparison or systematic
correction/retraction surveillance. The explicit reading boundaries and
dependencies make a separate spot-check possible. Full raw text is intentionally
not reproduced; the fixed sources remain the authority.

