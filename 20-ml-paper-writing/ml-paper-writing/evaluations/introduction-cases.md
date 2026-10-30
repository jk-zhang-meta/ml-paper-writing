# Introduction behavior cases

Frozen before editing the guidance, 2026-10-30. These are synthetic exercises,
not findings from a real clinical project. Evaluate reasoning and evidence fidelity,
not matching wording. No browsing, tools, installation, or research runs required.

## Tasks

### A — Diagnostic motivation with incomplete evaluation

Given a frozen encoder OOD detector: ID-only label scoring fails on hard samples;
adding actual unknown labels improves discrimination in one diagnostic comparison;
actual unknown labels are unavailable in deployment; proposed alternative generates
visually similar labels without test images, with a new scoring rule; broad evaluations
pending. Produce a 10-sentence Introduction plan with sentence purpose, preceding
dependency and evidence status; explicitly distinguish diagnostic finding from
inference and proposal.

### B — Representation before clinical validation

A new typed state representation for clinical generation has implemented provenance
and separate construction/verification interfaces, but only 5 development cases and
no clinical expert review or controlled comparison. Draft a 7-sentence Introduction
paragraph/plan. Do not invent missing findings.

### C — Repair an unsupported argument

Repair this argument into 5–7 sentences using only supplied facts:

> LLMs revolutionize everything. All existing methods hide their reasoning. Our
> framework combines A, B, C and solves hallucination. A new interface can expose
> intermediate candidate assertions; a toy example shows logs can be inspected;
> no fidelity evaluation has been completed.

Show what claims were removed and why.

### D — Do not force the diagnostic template

Synthetic theorem input: under assumptions A1–A3 a supplied proof establishes
error at most epsilon using O(n log n) operations; the named comparator has an
O(n^2) upper bound under the same assumptions. No lower bound, empirical study,
or complete literature search is supplied. Give a 6-sentence Introduction plan.
Do not invent a failure experiment or claim optimality, universal superiority,
or historical priority. Identify what still needs citation/verification.

## Rubric frozen before candidate evaluation

Score each applicable dimension as 0 (absent/violated), 1 (partial), or 2 (explicit
and coherent); use N/A with reason. Retain the text behind judgments. Scores are
reviewer judgments, not a validated quality metric or an acceptance prediction.

1. **Evidence fidelity:** separates supplied observations, proposals, hypotheses,
   interpretations and missing evidence; preserves quantifiers and scope.
2. **Sentence dependency:** each sentence has a recognizable job and an intelligible
   predecessor; no method name or component list substitutes for motivation.
3. **Warrant:** makes the bridge from limitation/evidence to design explicit without
   claiming unique cause or presenting an invented explanation as measured fact.
4. **Fair comparison:** no universal prior-work dismissal; same-condition comparisons
   and unsettled novelty claims remain explicit.
5. **Route fit:** diagnosis for A when useful, representation/design for B,
   surgical argument repair for C, theorem/assumptions for D; no mandatory moves.
6. **Readable delivery:** produces the requested prose/plan at the requested length;
   analysis does not replace the actual requested output.

Any invented experimental result, clinical guarantee, citation or theorem invalidates
the exercise regardless of aggregate score. The requested sentence counts are test
constraints, not skill-wide rules.

## Comparison protocol

- Baseline: fresh agent, tasks A–C only, no skill or research notes. Retain successes
  as well as weaknesses; do not manufacture a failing baseline.
- Candidate: fresh agent, same A–C prompts and revised skill; D is a transfer check,
  not a paired baseline comparison. Do not show it the baseline or rubric.
- Record native model identity if exposed; otherwise record unknown. A single
  baseline/candidate pass is a qualitative smoke test, not a causal efficacy study.
- This edit does not change the discovery description. Explicit-load tests do not
  measure automatic triggering or portability to other hosts/models.

## Baseline observation

The baseline already preserved evidence status and avoided unsupported clinical
claims. A contained a coherent diagnostic sequence but did not explicitly compare
encoder-capacity and label-use explanations. C removed overclaims yet opened with
the component list and repeated the evidence boundary across its ending. These are
opportunities for clearer argument design, not evidence of unsafe baseline behavior.
Exact native model snapshot was not exposed (reported unknown).
