# Deep-review transfer cases

Frozen 2026-10-30 before the fresh candidate run. These synthetic tasks test the
newly emphasized genres. They are not real research findings, and their stipulated
facts need no browsing. Use the supplied facts only. The length requests below are
test constraints, not universal Introduction rules. This is a qualitative transfer
check, not a paired before/after trial or automatic-trigger evaluation.

## Tasks supplied to the candidate

### E — Systems resource argument

Write six connected Introduction sentences. A request-serving prototype has a
variable-size cache; the existing contiguous allocator reserves maximum request
length and wastes memory on a supplied trace. A block allocator reduces reserved
memory by 28% and raises throughput by 18% on that trace, one GPU and unchanged
answer-quality tests. Its block lookup makes the isolated kernel 6% slower. No
other hardware/workload tests or asymptotic bound are supplied. Explain the design
motivation without claiming universal speed or treating kernel speed as system speed.

### F — Finding without a new method

Write six connected Introduction sentences and then label each sentence's job.
Across three supplied model families, a synthetic study observes error first rise
and then fall as training duration increases under one fixed data/noise setting.
One conventional account predicts only monotonic improvement in this setting.
The authors hypothesize that a changing effective-capacity regime explains the
pattern; they have not tested the mechanism. There is no new training algorithm.
Do not invent a method, a proof or broader robustness evidence.

### G — Mathematical formulation and scope

Write a seven-sentence Introduction plan, each with its job and dependency. A
supplied theorem concerns finite objects over a field of characteristic two under
assumptions A and B. It improves the bound from a supplied comparator's exponential
form to a polynomial form. An equivalent entropy formulation, with constants
tracked only up to a factor, exposes a subadditivity step used by the proof.
The argument establishes existence through compactness; no efficient construction
or extension to odd characteristic is supplied. The comparator's citation is missing.
Do not invent an experiment, exact constants, historical priority or an algorithm.

### H — Benchmark validity

Repair the following into six connected Introduction sentences using only the
supplied facts, then state the strongest unresolved validity issue:

“Existing benchmarks are saturated, so we built 5,000 software tasks that measure
real developer intelligence. Our benchmark solves evaluation.”

Facts: the selected old test no longer separates two supplied systems. The proposed
tasks pair repository issues with executable tests; two systems differ in pass rate
on 200 audited tasks. The remaining 4,800 tasks have not been audited. Contamination
and whether tests capture complete issue resolution are unresolved. There is no
human baseline and no deployment study.

## Reviewer-only rubric

Do not show this section to the candidate. Apply the six dimensions from
`introduction-cases.md`: fidelity, dependency, warrant, comparison, route fit and
requested delivery. Judge with source facts, not exact wording.

- E: distinguish memory, kernel and service metrics; retain trace/GPU scope and
  measured semantic checks without claiming universal equivalence.
- F: let a phenomenon be a complete contribution; keep the explanation a hypothesis
  and preserve the narrow evaluation conditions.
- G: retain characteristic/assumptions, bounded equivalence and existential result;
  explain the proof role of the formulation; flag the missing comparator citation.
- H: distinguish the intended construct from test passage; retain the 200/5,000
  audit denominator and unresolved contamination/coverage. Do not invent a human result.

Any invented result, citation, guarantee or proof invalidates the relevant case.
No aggregate score establishes reader benefit, publication success or SOTA status.
