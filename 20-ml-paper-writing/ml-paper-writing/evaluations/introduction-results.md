# Introduction extension: validation record

Date: 2026-10-30. Scope: the Introduction extension in this fork, not all inherited
conference rules, citation helpers, or templates. No packages or skills installed;
no scientific experiment or clinical evaluation was run.

## Behavioral method

The tasks and rubric in `introduction-cases.md` were frozen before guidance edits.
Two fresh native agents performed the exercises independently:

- Baseline agent `intro_baseline`: A–C, without the skill or reference material.
- Candidate agent `intro_forward_test`: same A–C plus transfer case D, explicitly
  loaded the revised skill and all three Introduction references; did not read the
  baseline, rubric or evaluation files.
- Exact native model identity: **unknown** in both sessions. No model API override
  or external-model request was made. This limits reproducibility and comparison.

The candidate used these pre-review identities (SHA-256):

| File | Digest |
|---|---|
| SKILL.md | `4b0ac425b21444efc7979caed50c4b242c04875c3425281893a080571a26b7d4` |
| references/introduction-sentence-design.md | `da005ed1090b4ffc54b619fca4f4e61a5af5042eaa0a9f3a2470d488e92ebc06` |
| references/introduction-worked-examples.md | `655ece19c9b452bc65c92dc7c50bf82e9769f74fe071969bd932ab132b1daf89` |
| references/introduction-evidence.md | `9f737299bf3267b6c047fc835374678d0719f66a08c85a0817a972bb7b5d31b6` |

One run per condition is a qualitative, unblinded authoring smoke test. It cannot
establish average improvement, statistical significance, automatic trigger rate,
cross-host behavior, or publication success. Three within-prompt repetitions were
not performed; there is no trigger-rate claim. Discovery metadata is unchanged.

## Observed behavior and scoring

Scores below are the integrating agent's judgments against the frozen rubric,
not independent human ratings. Dimension order is evidence fidelity, sentence
dependency, warrant, fair comparison, route fit, readable delivery. N/A means the
fixture does not supply a substantive comparator; absence of fabrication is still
assessed under evidence fidelity.

| Case | Baseline scores | Candidate scores | Interpretation |
|---|---|---|---|
| A | 2 / 2 / 2 / 2 / 2 / 2 | 2 / 2 / 2 / 2 / 2 / 2 | Both separate diagnostic evidence from a proposed deployable method. No demonstrated improvement on this rubric. |
| B | 2 / 2 / 2 / N/A / 2 / 2 | 2 / 2 / 2 / N/A / 2 / 2 | Both keep an implemented interface distinct from clinical/comparative validity. |
| C | 2 / 1 / 2 / 2 / 2 / 1 | 2 / 2 / 2 / 2 / 2 / 1 | Candidate opens with the intended operation rather than components. Both endings could be less repetitive. |
| D | Not run | 2 / 2 / 2 / 2 / 2 / 2 | Candidate uses a theory route and distinguishes upper-bound comparison from runtime separation. Transfer check only. |

No supplied observation was turned into a new measured result or clinical guarantee
in these outputs. This does not prove that the skill prevents such errors generally.

### Text behind the judgments

**A baseline S4–S5:** “In one diagnostic comparison, adding the actual unknown-class
labels improved discrimination. That result suggests that additional label information
may help, but it does not establish that other labels will reproduce the improvement.”

**A candidate A4:** “This contrast suggests that label information merits investigation,
without identifying a unique cause of the failures.” A9 separately retains the
surrogate-label benefit as a hypothesis. Both outputs meet the evidence ceiling.
Neither explicitly enumerates both capacity and usage explanations; this is not a
failure when the inference remains bounded and the task does not require both.

**B candidate:** “These interfaces establish an architectural capability whose effect
on fidelity and clinical correctness still requires evaluation.” It also states the
five-case development scope and absence of expert review and controlled comparison.

**C baseline S1:** “Our framework combines A, B, and C.”
**C candidate S1:** “We study how a generation interface can expose intermediate
candidate assertions.” The latter gives the reader a purpose before a mechanism.
The candidate removes the universal dismissal of earlier work and explains that
inspectability alone does not establish hallucination reduction. Its last three
sentences repeat closely related evidence limits; further compression would help.

**D candidate S5:** “The result provides a smaller asymptotic upper bound than the
comparator's stated bound, without establishing a runtime separation or optimality.”
It asks to verify the assumptions, error objective and cost model, and does not
invent a proof mechanism, empirical result or priority claim. D4 is an authoring
instruction rather than finished prose, acceptable for this plan request only.

The baseline was already strong. The evidence supports usable detailed guidance and
a small observed rhetorical improvement in C, not a general claim of superiority.

## Structural validation

- Project-required YAML keys, name, description length, retained upstream author and
  license, unchanged discovery description, and version 1.3.0 checked successfully.
- New Introduction references are directly reachable from `SKILL.md`.
- EOE IDs E01–E29 and Transformer IDs T01–T11 are consecutive and unique. This
  mechanical check does not establish semantic accuracy; independent source review
  is a separate check.
- The generic Codex `quick_validate.py` rejects the inherited top-level `author`,
  `dependencies`, `tags`, and `version` keys. The same keys exist in untouched HEAD
  and are required by this repository's conventions. We preserve upstream metadata
  and report this portability limitation; we do not claim generic-validator success.
- No Python packages were installed. The system interpreter lacked PyYAML; an existing
  local environment supplied it for project-schema validation. Bytecode writes were
  disabled and validation ran outside the synchronized source tree.

## Independent review and corrected revision

The read-only `intro_review` agent independently verified EOE's 29 units,
Transformer's eleven-sentence order, and the Farquhar outlining/prior-work locators.
It initially returned BLOCK on three inherited integration conflicts: rigid
checklists, a redundant confirmation gate, and an empirical-only evidence pillar.
All three were corrected in both entry points and relevant summary/checklist text.
Related one-sentence readiness wording was changed into a focusing exercise.

The reviewer then returned **APPROVE for the exact revised artifacts**, with no
remaining scoped correction. Its review did not assess automatic activation or
establish writing effectiveness. It regarded the long inherited entrypoint as
nonblocking size debt for this scoped revision, not as a fully optimized package.

Final reviewed SHA-256 identities:

| File | Digest |
|---|---|
| SKILL.md | `ac8cbddaeeef68792d31e919d1c3b3bb4235a631c4e2a85d67ea5522a45c2a4f` |
| references/writing-guide.md | `ac734f065889f0b0ca2afd4f14386df58ea2327740f40a96c8f8059578c57ec0` |
| references/introduction-sentence-design.md | `f97bbc3e9d356073e3cb32a2c729c2a26530e3855e6a2cdac9f5603d561d5b10` |
| references/introduction-evidence.md | `9e4f69ffe6ec36a504b8d7e44b435903bbedf54293a3dddb5cfaf974dc588f78` |
| references/introduction-worked-examples.md | `655ece19c9b452bc65c92dc7c50bf82e9769f74fe071969bd932ab132b1daf89` |
| evaluations/introduction-cases.md | `ccbdcbaf90f8bdc3cbd0538aa5b212b4b887484f12905d9e2a22429777e2472f` |

## Post-correction boundary test

A fresh agent `intro_boundary_test` explicitly loaded the final main file,
`writing-guide.md` and `introduction-sentence-design.md`. It was asked for a
six-sentence theoretical Introduction with an already-chosen thesis and drafting
authorization, no contribution bullets, no experiments, an unmatched comparator
error objective, and a sentence combining credit with qualification. It did not
read evaluation files or previous outputs. It also reported loading the host's
personal bootstrap; exact model identity remained unknown.

Observed checks:

- Delivered six prose sentences, no contribution bullets and no approval question.
- Used the supplied conditional proof; invented neither an experiment nor a proof
  mechanism, performance result or historical-priority claim.
- Retained the dual-function comparator sentence: “The comparator [name; full citation
  and result locator to verify] provides an O(n^2) operation upper bound under the same
  assumptions, but its error objective remains unchecked, so these bounds do not yet
  establish an advantage at matched accuracy.” Mathematical markup is normalized here.
- Explicitly retained unresolved empirical performance and lack of a lower bound.

This checks the corrected workflow conflicts on one new prompt. It is not a rerun of
the complete A–D comparison and does not expand the earlier effectiveness claim.
The paragraph is heavily qualified because the fixture lacks motivating context;
passing a boundary test is not a claim that it is a finished publishable Introduction.

Final local checks passed: project-schema validation, all changed/new-file relative
links and whitespace checks, consecutive example IDs, and `git diff --check`.
The generic-validator incompatibility documented above remains. The working branch
is `docs/sentence-level-introductions`; changes are uncommitted, unpushed and not
installed into any personal or global skill location.
