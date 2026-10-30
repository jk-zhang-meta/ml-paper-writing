# Deep Introduction extension: verification record

Date: 2026-10-30. Target: this fork's `ml-paper-writing` source, version **1.4.0**,
branch `docs/sentence-level-introductions`. Scope: a CS-first, mathematics-secondary
evidence review and finer Introduction guidance. No installation, commit, push or
publication was performed. Earlier uncommitted pilot work was retained and extended.

## Evidence inventory

The [review index](../references/introduction-deep-review.md) records **33 unique
full-Introduction cases**: 31 CS-related and two pure-mathematics cases. The three
pilot papers are included in 33, not added again. Four JSONL files contain 33 unique
case IDs, **982 heterogeneous annotation units** and **98 pivotal transitions**.

- Ten diagnostic/phenomenon/audit cases: 149 contiguous statement groups.
- Ten method/system cases: 266 sentence/contribution-clause units.
- Ten theory/benchmark cases: 448 sentence, nominal-item and formal units.
- Three contrast cases: 119 units, comprising 115 prose sentences, three theorem
  blocks and one composite definition.

Thus **23 cases have sentence/formal-unit maps and 10 have grouped maps**. Neither
the total units nor the grouped lane is presented as a count of individual sentences.
Extraction included each case's declared whole Introduction scope; original-source
independent checking was sampled, as described below.

## Independent original-source review

Two reviewers received fresh, bounded assignments against frozen files. They did
not edit the reviewed artifacts or spawn review chains. Native model identifiers
were not exposed and are not inferred. Source papers were retrieved at the fixed
versions in the records; temporary copies remained outside the repository.

### Review A: six cases

Frozen methods JSONL:
`663ab14daaafe073dbf68f4d0ee7839e063aea611b0d4b12e8faa272fd56701a`.

Frozen contrasts JSONL before correction:
`0c7e1c46738375f47197843443cb9153d6068c7b983cac131ddc1b1b0adf1a90`.

The reviewer verified both identities before and after the read. Result: **PASS
for the subset, with one low-severity correction**.

| Case | Check actually performed | Result and limit |
|---|---|---|
| C01 AlphaEvolve | Entire §1 segmentation: 29 sentences in eight paragraphs; anchors; §2.4, Table 2, §3.2 and §6 samples. | No omitted main-prose unit; evaluator dependence and selected-problem scope preserved. No evaluator execution. |
| C02 DeepSeek-R1 | Entire §1 segmentation: 53 sentences, including contributions and evaluation summary; §2.2.4 and §4.1/Table 6. | Coverage confirmed; usability motivation and distillation comparison remain conditional. No training/equal-budget verification. |
| C03 Marton | Entire §1: 33 prose sentences, three theorem blocks and composite definition; §2 compactness remark and Appendix B. | Formal boundaries and implication direction preserved; one notation annotation corrected below. No proof certification. |
| M02 ResNet | Selected Introduction and body pivots; Figure 4/Table 2 and §4.2. | Existence versus optimization and the 1202-layer counterexample preserved. Entire sentence count not independently recounted. |
| M07 FlashAttention | Proposition 3, Appendix C, Table 1 and §4.3. | Lower-bound quantifier and kernel-versus-training measures preserved. Entire sentence count not independently recounted. |
| M08 PagedAttention | §6.1–6.3 and §7.1; selected mapped pivots. | Workload/baseline qualifications and kernel-overhead versus throughput distinction preserved. Entire sentence count not independently recounted. |

**Correction:** C03.P15.U2 originally described an example about attainable versus
claimed sharpness. The second sentence of
[`#S1.SS0.SSSx1.p7.1`](https://arxiv.org/html/2311.05762v1#S1.SS0.SSSx1.p7.1)
instead explains using `C1/2` to preserve prior notation. The parent changed the
function, placement explanation and evidence label to cross-paper notation
consistency in both Markdown and JSONL; non-optimality remains in U1. This was an
exact implementation of the source review's correction, not a new scientific claim.
Final contrasts JSONL:
`eacbdd2656cc8ea215b2de1ce9aa53b1ca77873c6c4f472890d1360611239170`.

### Review B: five cases

Frozen diagnostic JSONL:
`5a0faa351e080ac21c01d45525b29c9d42df6422938d07c54f6046b96131b8c8`.

Frozen theory/benchmarks JSONL:
`ca43e7a5807724e9bef030787a3fbe5cbf36404a7b931af8970dcdfd4b50288b`.

Both identities matched before and after review. Result: **PASS for the subset;
no required correction**.

| Case | Check actually performed | Result and limit |
|---|---|---|
| D01 EOE | Complete §1 region including question and contributions; U04–U09; §3.2 Eq.3 and §4.2 similarity filter. | Diagnostic/oracle/surrogate distinctions and score interpretation match. Grouped segmentation, not a new individual-sentence recount. |
| D02 Noisy TTA | Complete §1 region, including all-clean-stream failure/repair; U06–U11; §3.2 Observations 3.1–3.3. | Pipeline and Tent-specific gradient scope, including the SoTTA exception, preserved. |
| D06 Recommendation audit | Complete §1 including questions and organization paragraph; §2.1 and §3.7/Table 9. | Eighteen-paper versus seven-reproduction denominators and metric-dependent Mult-VAE exception preserved. |
| T04 Interlacing Families II | Complete §1 formal/prose regions including Corollary 1.5 proof; U016–U025; Theorem 1.4 proof at §5 end. | Independence, finite support, positive probability and parameter reduction preserved; existence not inflated to concentration. No proof certification. |
| T08 HELM | Complete §1 regions, pp.2–10, including 25 findings and §1.3; U132–U134; §8.2 and Table 4. | Coverage and selected contrasts match; missing evaluation pairs remain explicit. Every sentence was not independently retokenized. |

The independent source sample totals **11 unique cases**. Eight received complete
Introduction-region coverage checks; the other three received selected pivotal
checks. Only the stated segmentation recounts were performed. No agreement
coefficient, exhaustive double coding, experiment replication, proof verification,
priority audit or comprehensive correction/retraction surveillance is claimed.

## Fresh explicit-load behavior check

[Tasks E–H](introduction-deep-cases.md) were frozen before the candidate run. The
candidate had the task facts, main skill and relevant guidance, but not the rubric,
prior outputs or other evaluators' findings. It performed no browsing. Its
[unaltered responses](introduction-deep-responses.md) retain loaded hashes and
report the exact native model identity as **unknown**.

A separate integration reviewer checked the six frozen artifacts below and applied
the six-dimension pilot rubric to the four new tasks. Each received **2/2 on all
six dimensions**, with no invented result, citation or guarantee found:

| Case | Fidelity | Dependency | Warrant | Comparison | Route fit | Delivery | Reason for pass |
|---|---:|---:|---:|---:|---:|---:|---|
| E — systems | 2 | 2 | 2 | 2 | 2 | 2 | Six sentences connect reservation waste to block allocation, retain the trace/GPU scope, and distinguish slower kernel from faster service. |
| F — phenomenon | 2 | 2 | 2 | 2 | 2 | 2 | Six sentences preserve the observation/hypothesis distinction and deliver a finding without inventing a solver. |
| G — mathematics | 2 | 2 | 2 | 2 | 2 | 2 | Seven planned sentences retain assumptions, characteristic, equivalence precision, compactness/existence and the missing citation. |
| H — measurement | 2 | 2 | 2 | 2 | 2 | 2 | Six sentences preserve the 200/5,000 audit boundary, test-passage proxy and unresolved coverage/contamination. |

These are qualitative judgments from one fresh candidate pass, not calibrated
scores or a causal before/after effect. The tests do not show reader comprehension,
acceptance benefit, optimal writing style, automatic activation or cross-host
reliability. The discovery description was broadened for CS/math Introduction work;
its actual automatic triggering remains **untested**. Nothing was installed.

## Integrated artifact identities

The independent integration reviewer confirmed these hashes and found the
fine-grained guidance, suitability boundaries and metadata scope coherent. The
frozen snapshot had one packaging gap: this closing-results file did not yet exist.
Creating it and checking the relative link resolves that gap without changing the
reviewed main skill, guides, protocol or candidate output.

| Artifact | SHA-256 |
|---|---|
| `SKILL.md` | `6f2d2c9f7e9766efab0b09daf69708d26616f00623f2648051c5a8fccc4690ac` |
| `references/introduction-sentence-design.md` | `4a0f630d259d3b0e2664d96ee5a651b2e00f305ed520cc718b41741807e2e990` |
| `references/introduction-route-playbook.md` | `d112d9a40b11f78f33e3cc07be2c0a6fb628448e9c92ab3767897f55790ba89e` |
| `references/introduction-deep-review.md` | `06325052c31f4202d29b022be1ac2c5c2f96fd61768a6e3b2467ea7578ffe548` |
| `evaluations/introduction-deep-cases.md` | `62ad5604b4a4910661c12c4570f6245e3f6cac2ac6b10c4e70abf1ae6ec4f7e3` |
| `evaluations/introduction-deep-responses.md` | `e6b3d8e6f7bd6dd417a0d64858f89f606a2655c8933665d6e3a06442052891ea` |

## Deterministic verification and release boundary

- Four JSONL files parse; required fields, unique case/unit IDs, declared counts,
  transition references and backward in-case dependencies pass.
- Guide tables contain nine routes, twenty-three jobs and eleven sentence-pair
  patterns. Counts match the review index and main skill routing.
- Repository frontmatter schema passes with original metadata keys retained;
  author remains Orchestra Research and license MIT. Version is 1.4.0.
- `git diff --check` passes. A separate scan includes new, untracked artifacts for
  trailing whitespace, final newline and relative-link existence.
- The main skill's inherited length remains above 500 lines; this scoped change
  uses linked references rather than refactoring the entire upstream package.
- This is source verification, not an installation compatibility claim. The earlier
  pilot record documents the generic validator's mismatch with upstream metadata
  keys; no keys were removed merely to satisfy a different schema.

No research paper body, clinical source, global profile or runtime configuration was
changed. No full paper copies, generated model outputs or scientific experiment
artifacts were placed in OneDrive. New repository files are authored guidance,
annotations, synthetic evaluation responses and review records.
