# Evidence and provenance for the Introduction extension

This document preserves the **three-paper pilot** and its source trail. The
[expanded CS-first review](introduction-deep-review.md) now supplies 33 unique
paper cases, revised route guidance and additional CS/math writing sources. Do not
add the three pilot cases to that total: they are reread members of the corpus.

## Contents

- [Scope and search](#scope-and-search)
- [Source register](#source-register)
- [Guidance-to-evidence mapping](#guidance-to-evidence-mapping)
- [Limits and maintenance](#limits-and-maintenance)

## Scope and search

Review date: **2026-10-30**. Mode: bounded **Evidence Review** for design input,
not a systematic review, author-success predictor or established writing SOTA.
Question: what operational guidance helps an agent build and revise sentence-level
Introduction arguments while preserving evidence strength and prior-work fairness?

Use public first-hand researcher guidance, original teaching/editorial materials,
a relevant writing-evaluation study, and contrasting paper introductions. Exclude
skill mirrors as independent evidence, commercial writing claims without primary
support, and abstract-only access when the target is the Introduction itself.
Paper examples are purposive, not a representative sample of accepted/rejected work.

Discovery used web search plus backward tracing of the upstream skill's sources.
Representative exact queries executed on the review date:

- `site.sebastianfarquhar.com "How to write ML papers"`
- `site.alignmentforum.org Neel Nanda highly opinionated advice write ML papers narrative`
- `site.journals.plos.org "Ten simple rules for structuring papers" Mensh Kording`
- `site.amstat.org Gopen Swan science scientific writing topic stress`
- `research paper introduction writing advice 2026 2025 machine learning author narrative`
- `site.arxiv.org "Noisy Test-Time Adaptation" Cao`

Primary retrieval: author sites, MIT Communication Lab, PLOS, the Gopen–Swan
reprint, and fixed-version arXiv full text. We inspected the relevant original
sections, not search snippets alone. No exhaustive database export, screening
denominator, recall estimate, or formal risk-of-bias instrument was used. Stop when
sentence cohesion, evidence-to-design warrants, reader orientation and contrasting
routes have sources/examples and behavioral tests; further unsystematic collection
would not establish optimality.

One author-guide lane, Jennifer Widom's Stanford page, failed retrieval (TLS/reset
and timeout) and is **not** used as supporting evidence. A later urllib reread of
MIT returned 403; the earlier successful full-page retrieval supplied its content.
The Microsoft-hosted Peyton Jones slide deck was located but is not needed for
the retained rule set. Do not imply these leads were fully appraised.

## Source register

Each ID identifies an evidence unit for this extension. Other versions of the same
paper are not independent support. Teaching advice and rhetorical analysis are not
controlled evidence that a technique improves acceptance rates.

| ID | Primary source and locator | Kind and use | Limit / status |
|---|---|---|---|
| G1 | Neel Nanda, [Highly Opinionated Advice on How to Write ML Papers](https://www.alignmentforum.org/posts/eJGptPbbFPZGLpjsp/highly-opinionated-advice-on-how-to-write-ml-papers), 2025-05-12; “The Essence of a Paper,” “Crafting a Narrative,” “Paper Structure Summary.” | First-hand practitioner advice: coherent claims, supporting evidence and reader relevance. | Opinionated advice, not a causal writing study; do not universalize its prescriptions. |
| G2 | Sebastian Farquhar, [How to Write ML Papers](https://sebastianfarquhar.com/on-research/2024/11/04/how_to_write_ml_papers/), 2024-11-04; “Outlining your paper / Introduction” and “Miscellaneous Points / How to write.” | Practitioner advice: evidence expectations, closest-work fairness, recursive outlining down to sentences. | Its compact lengths and opening preference are stylistic defaults, not venue laws. |
| G3 | George D. Gopen and Judith A. Swan, *The Science of Scientific Writing*, American Scientist, 1990; [authorized reprint](https://cseweb.ucsd.edu/~swanson/papers/science-of-writing.pdf), PDF pp. 3–9 and 11–12. | Original rhetorical teaching: topic continuity, emphasis, subject–verb relation and missing logical connections. | Worked revisions, not a randomized trial. The inference-audit protocol here is our extension. |
| G4 | Brett Mensh and Konrad Kording, [Ten simple rules for structuring papers](https://doi.org/10.1371/journal.pcbi.1005619), 2017; Rules 2–3, 6 and 10. | Editorial guidance: reader orientation, context/content/conclusion at multiple scales, consequential gaps and feedback. | Mainly scientific-article guidance, not ML-specific. Publisher correction checked; see below. |
| G5 | MIT Biological Engineering Communication Lab, [Journal Article: Introduction](https://mitcommlab.mit.edu/be/commkit/journal-article-introduction/); “Criteria for Success,” “Skills / Orient outside readers,” and the narrowing-background guidance. | Institutional teaching: audience-dependent background and a balanced path from context to the research question. | Broader opening than G2 may suit a different audience; do not erase this difference by averaging rules. |
| E1 | Chentao Cao et al., [EOE, arXiv:2406.00806v1](https://arxiv.org/html/2406.00806v1#S1), Section 1 and Figure 1; ICML 2024. | Primary paper: complete sentence-function case of a diagnostic-to-feasible-method argument. | Rhetorical roles are our interpretation; no claim that its intervention establishes a unique failure cause. |
| E2 | Chentao Cao et al., [Noisy Test-Time Adaptation in Vision-Language Models, arXiv:2502.14604v1](https://arxiv.org/html/2502.14604v1#S1), Section 1, Figures 1–2. | Primary paper: selected transitions from assumption change through diagnosis to separation and boundary-case repair. | Same first author as E1, so not an independent sample of writing traditions. |
| E3 | Ashish Vaswani et al., [Attention Is All You Need, arXiv:1706.03762v7](https://arxiv.org/html/1706.03762v7#S1), Section 1. | Primary paper: eleven-sentence contrast case built on a computational bottleneck. | Historical architecture paper; not evidence for today's technical SOTA or universal writing practice. |
| V1 | Krishna Garg, Firoz Shaik, Sambaran Bandyopadhyay and Cornelia Caragea, [Let's Use ChatGPT To Write Our Paper! Benchmarking LLMs To Write the Introduction of a Research Paper, arXiv:2508.14273v1](https://arxiv.org/html/2508.14273v1), abstract, Section 7 and Appendix Table 7. | Original empirical preprint: treats content/faithfulness and narrative evaluation as distinct dimensions. | Section 7 uses author ratings without overlapping annotation; no inter-rater agreement is established. We borrow dimensions, not its scores or an efficacy claim for this fork. |

G4's [publisher correction](https://doi.org/10.1371/journal.pcbi.1005830),
2017-11-09, supplies a missing key in Figure 1. The correction was read; the
extension does not reproduce that figure. A comprehensive correction/retraction
database audit was not performed for the other sources. Exact arXiv versions are
used so a future text change does not silently invalidate the sentence maps.

## Guidance-to-evidence mapping

| Extension decision | Supporting source/locator | Status of our use |
|---|---|---|
| Start with claim, evidence and reader relevance. | G1, narrative sections. | Adapted practitioner principle; not proof of effectiveness. |
| Choose opening depth for the audience. | G2 Introduction; G5 success criteria and reader orientation. | Synthesis preserving the tension between contribution-first and broader context. |
| Outline paragraphs, then sentence dependencies. | G2 “How to write”; G3 missing-connection example pp. 11–12. | Operational extension with our own sentence map. |
| State the warrant between observation and design. | E1 E10–E15; E2 P3–P6; G3 pp. 11–12. | Critical case analysis, not the authors' declared private intent. |
| Do not force a diagnostic experiment into every paper. | E3 Section 1 contrasted with E1. | Counterexample to a mandatory template; does not validate all proposed routes. |
| Preserve prior capabilities and exceptions. | G2 Introduction; G5 “Orient outside readers”; E3 P2–P3. | Normative fairness guidance plus illustrative practice. |
| Separate fidelity from narrative quality in testing. | V1 evaluation dimensions and Table 7. | Design input only; local rubric is unvalidated. |
| Keep every claim within its evidence strength. | G1 “Crafting a Narrative”; G2 evidence questions. | Evidence discipline; not a ban on clearly labeled hypotheses. |

The pilot's seven-route selector, eighteen-job inventory, transition tests and
synthetic repair were **fork-maintainer synthesis**. The expanded guide now has
nine overlapping routes and twenty-three jobs, with direct theory and benchmark
cases. Neither version is attributed verbatim to one researcher or established as
a universal taxonomy. The three pilot papers illustrated only selected routes.

## Limits and maintenance

- Pilot selection favored English-language ML examples and accessible guidance.
  The expansion adds systems, theory, measurement and mathematics, while remaining
  purposive and English-language; no reader-comprehension trial was conducted.
- Publication prestige is not a prose-quality label; reviewers and methods differ.
- Source availability does not prove originality or license to reproduce full text.
  Retain links, locators and our commentary; do not vendor papers or long excerpts.
- Do not transfer upstream numerical claims about reviewer behavior or citation
  error rates into this extension without their original empirical support.
- The package remains MIT-licensed; source papers retain their own rights. Upstream
  Orchestra attribution is preserved. New annotations and exercises belong to this fork.
- Recheck evidence when expanding a route, changing a source version, or making an
  effectiveness claim. Update the case locators and tests together. Adding more
  recommendations alone is not validation.
- Local behavior evaluation lives in `evaluations/introduction-cases.md` and
  `evaluations/introduction-results.md`. Explicit-load smoke tests do not establish
  automatic activation, cross-host reliability, acceptance rates or a SOTA ranking.
