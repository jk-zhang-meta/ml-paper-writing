# ML Paper Writing Philosophy & Best Practices

This reference compiles writing advice from prominent ML researchers including Neel Nanda, Andrej Karpathy, Sebastian Farquhar, Zachary Lipton, and Jacob Steinhardt.

---

## Contents

- [The Narrative Principle](#the-narrative-principle)
- [Time Allocation](#time-allocation)
- [Abstract Writing Formula](#abstract-writing-formula)
- [Introduction Structure](#introduction-structure)
- [Sentence-Level Clarity](#sentence-level-clarity)
- [Word Choice and Precision](#word-choice-and-precision)
- [Mathematical Writing](#mathematical-writing)
- [Figure Design](#figure-design)
- [Common Mistakes to Avoid](#common-mistakes-to-avoid)

---

## The Narrative Principle

### From Neel Nanda

"A paper is a short, rigorous, evidence-based technical story with a takeaway readers care about."

The narrative rests on three pillars that must be crystal clear by the end of your introduction:

**The "What"**: One to three specific novel claims fitting within a cohesive theme. Vague contributions like "we study X" fail immediately—reviewers need precise, falsifiable claims.

**The "Why"**: Support appropriate to the claim. For empirical work this includes
fair baselines and informative comparisons; for theory it may be a proof under stated
assumptions. Implementation evidence supports implemented behavior, not unmeasured
benefits. In a working draft, explicitly distinguish hypotheses from known results.
This broader routing is the fork's adaptation, not a verbatim quotation from Nanda.

**The "So What"**: Why readers should care, connecting your contribution to problems the community recognizes as important.

### From Andrej Karpathy

"A paper is not a random collection of experiments you report on. The paper sells a single thing that was not obvious or present before. The entire paper is organized around this core contribution with surgical precision."

This applies whether you're presenting a new architecture, a theoretical result, or improved understanding of existing methods—NeurIPS explicitly notes that "originality does not necessarily require an entirely new method."

**Practical exercise**: try expressing the main takeaway in one sentence to focus
the paper. Difficulty doing so can reveal an unresolved question; it does not prohibit
an early outline or require inventing a positive result.

---

## Time Allocation

### From Neel Nanda

Spend approximately **the same amount of time** on each of:
1. The abstract
2. The introduction
3. The figures
4. Everything else combined

This isn't hyperbole—most reviewers form preliminary judgments before reaching your methods section. Readers encounter your paper in a predictable pattern: **title → abstract → introduction → figures → maybe the rest.**

### Reviewer Reading Patterns

Studies of reviewer behavior show:
- Abstract is read 100% of the time
- Introduction is skimmed by 90%+ of reviewers
- Figures are examined before methods by most reviewers
- Full methods are read only if interest is established

**Implication**: Front-load your paper's value. Don't bury the contribution.

---

## Abstract Writing Formula

### Sebastian Farquhar's 5-Sentence Formula

Treat this as a contribution-first option, not a required count or order. A diagnostic,
theoretical or design paper may need a different opening. Preserve the same scope and
evidence strength as the Introduction; unknown results remain unknown in the Abstract.

1. **What you achieved**: "We introduce...", "We prove...", "We demonstrate..."
2. **Why this is hard and important**
3. **How you do it** (with specialist keywords for discoverability)
4. **What evidence you have**
5. **Your most remarkable number/result**

### Example (Good Abstract)

```
We prove that gradient descent on overparameterized neural networks
converges to global minima at a linear rate. [What]
This resolves a fundamental question about why deep learning works
despite non-convex optimization landscapes. [Why hard/important]
Our proof relies on showing that the Neural Tangent Kernel remains
approximately constant during training, reducing the problem to
kernel regression. [How with keywords]
We validate our theory on CIFAR-10 and ImageNet, showing that
predicted convergence rates match experiments within 5%. [Evidence]
This is the first polynomial-time convergence guarantee for
networks with practical depth and width. [Remarkable result]
```

### What to Avoid

From Zachary Lipton: "If the first sentence can be pre-pended to any ML paper, delete it."

**Delete these openings**:
- "Large language models have achieved remarkable success..."
- "Deep learning has revolutionized..."
- "In recent years, neural networks have..."

**Start with your specific contribution instead.**

---

## Introduction Structure

### Argument design, not mandatory paragraph slots

Explain the task, consequential limitation, warranted response, and available evidence.
Their order and granularity depend on the paper. Contribution bullets and compact
page counts are options, not universal requirements. An Introduction can expose a
computational constraint, diagnose a failure, change a task assumption, or formulate
a representation/theory contribution; these routes need different transitions.

Use the directly routed references in `SKILL.md`:

- `introduction-sentence-design.md`: reader/evidence intake, nine overlapping routes,
  twenty-three sentence jobs, dependency and inference checks, and a worked repair.
- `introduction-route-playbook.md`: sentence-level decisions for each route, including
  findings without a new method, systems constraints, theorem formulations and measurement validity.
- `introduction-deep-review.md`: CS-first 33-case index, annotation granularity,
  cross-case findings, evidence boundaries and review coverage.
- `introduction-worked-examples.md`: critical maps of EOE, ZS-NTTA and Transformer.
- `introduction-evidence.md`: source locators and the limits of this synthesis.

For an outline, state what each paragraph lets the reader conclude, then design the
sentences needed to earn that conclusion. For revision, diagnose the existing argument
before replacing it. If evidence is missing, mark the affected claim rather than
inventing a finding or refusing all early drafting.

### Contribution Bullets: Good vs Bad

**Good:**
- We prove that X converges in O(n log n) time under assumption Y
- We introduce Z, a 3-layer architecture that reduces memory by 40%
- We demonstrate that A outperforms B by 15% on benchmark C

**Bad:**
- We study the problem of X (too vague without the question and resulting knowledge)
- We provide extensive experiments (too vague)
- We make several contributions to the field (says nothing)

---

## Sentence-Level Clarity

### From Gopen & Swan: "The Science of Scientific Writing"

The seminal 1990 paper by George Gopen and Judith Swan establishes that **readers have structural expectations** about where information appears in prose. Violating these expectations forces readers to spend energy on structure rather than content.

> "If the reader is to grasp what the writer means, the writer must understand what the reader needs."

#### The 7 Principles of Reader Expectations

**Principle 1: Subject-Verb Proximity**

Keep grammatical subject and verb close together. Anything intervening reads as interruption of lesser importance.

**Weak**: "The model, which was trained on 100M tokens and fine-tuned on domain-specific data using LoRA with rank 16, achieves state-of-the-art results"

**Strong**: "The model achieves state-of-the-art results after training on 100M tokens and fine-tuning with LoRA (rank 16)"

**Principle 2: Stress Position (Save the Best for Last)**

Readers naturally emphasize the **last words of a sentence**. Place your most important information there.

**Weak**: "Accuracy improves by 15% when using attention"
**Strong**: "When using attention, accuracy improves by **15%**"

**Principle 3: Topic Position (First Things First)**

The beginning of a sentence establishes perspective. Put the "whose story" element first—readers expect the sentence to be about whoever shows up first.

**Weak**: "A novel attention mechanism that computes alignment scores is introduced"
**Strong**: "To address the alignment problem, we introduce a novel attention mechanism"

**Principle 4: Old Information Before New**

Put familiar information (old) in the topic position for backward linkage; put new information in the stress position for emphasis.

**Weak**: "Sparse attention was introduced by Child et al. The quadratic complexity of standard attention motivates this work."
**Strong**: "Standard attention has quadratic complexity. To address this, Child et al. introduced sparse attention."

**Principle 5: Coherent Purpose Within a Unit**

Give each unit a recognizable purpose. A sentence can both credit prior capability
and qualify its scope, or state a result together with its assumptions. Split unrelated
claims when that improves comprehension; do not separate a claim from its conditions.

**Principle 6: Articulate Action in the Verb**

Express the action of each sentence in its verb, not in nominalized nouns.

**Weak**: "We performed an analysis of the results" (nominalization)
**Strong**: "We analyzed the results" (action in verb)

**Principle 7: Context Before New Information**

Provide context before asking the reader to consider anything new. This applies at all levels—sentence, paragraph, section.

**Weak**: "Equation 3 shows that convergence is guaranteed when the learning rate satisfies..."
**Strong**: "For convergence to be guaranteed, the learning rate must satisfy the condition in Equation 3..."

#### Summary Table

| Principle | Rule | Mnemonic |
|-----------|------|----------|
| Subject-Verb Proximity | Keep subject and verb close | "Don't interrupt yourself" |
| Stress Position | Emphasis at sentence end | "Save the best for last" |
| Topic Position | Context at sentence start | "First things first" |
| Old Before New | Familiar → unfamiliar | "Build on known ground" |
| Coherent Purpose | Each unit advances an intelligible takeaway | Keep related conditions; split unrelated claims |
| Action in Verb | Use verbs, not nominalizations | "Verbs do, nouns sit" |
| Context Before New | Explain before presenting | "Set the stage first" |

---

---

## Micro-Level Writing Tips

### From Ethan Perez (Anthropic)

These practical micro-level tips improve clarity at the sentence and word level.

#### Pronoun Management

**Minimize pronouns** ("this," "it," "these," "that"). When pronouns are necessary, use them as adjectives with a noun:

**Weak**: "This shows that the model converges."
**Strong**: "This result shows that the model converges."

**Weak**: "It improves performance."
**Strong**: "This modification improves performance."

#### Verb Placement

**Position verbs early** in sentences for better parsing:

**Weak**: "The gradient, after being computed and normalized, updates the weights."
**Strong**: "The gradient updates the weights after being computed and normalized."

#### Apostrophe Unfolding

Transform possessive constructions for clarity:

**Original**: "X's Y" → **Unfolded**: "The Y of X"

**Before**: "The model's accuracy on the test set"
**After**: "The accuracy of the model on the test set"

This isn't always better, but when sentences feel awkward, try unfolding.

#### Words to Eliminate

Delete these filler words in almost all cases:
- "actually"
- "a bit"
- "fortunately" / "unfortunately"
- "very" / "really"
- "quite"
- "basically"
- "essentially"
- Excessive connectives ("however," "moreover," "furthermore" when not needed)

#### Sentence Construction Rules

1. **Manage sentence load** - Split competing claims when helpful, but keep a claim
   with the condition that makes it true; one sentence may perform compatible jobs.
2. **No repeated sounds** - Avoid similar-sounding words in the same sentence
3. **Every sentence adds information** - Delete sentences that merely restate
4. **Choose voice for clarity** - Name the actor when it matters; passive voice can
   preserve a useful topic without hiding responsibility.
5. **Expand contractions** - "don't" → "do not" for formality

#### Paragraph Architecture

- Establish an entry question or topic, provide the needed explanation/evidence,
  and leave a clear exit takeaway.
- A topic-first paragraph and a paragraph building toward a diagnostic inference
  can both work. Do not force every final sentence to restate the first.
- Make the next paragraph depend on that takeaway instead of restarting the background.

---

## Word Choice and Precision

### From Zachary Lipton

**Eliminate hedging** unless genuine uncertainty exists:
- Delete "may" and "can" unless necessary
- "provides *very* tight approximation" drips with insecurity
- "provides tight approximation" is confident

**Avoid vacuous intensifiers**:
- Delete: very, extremely, highly, significantly (unless statistical)
- These words signal insecurity, not strength

### From Jacob Steinhardt

**Precision over brevity**: Replace vague terms with specific ones.

| Vague | Specific |
|-------|----------|
| performance | accuracy, latency, throughput |
| improves | increases accuracy by X%, reduces latency by Y |
| large | 1B parameters, 100M tokens |
| fast | 3x faster, 50ms latency |
| good results | 92% accuracy, 0.85 F1 |

**Consistent terminology**: Referring to the same concept with different terms creates confusion.

**Choose one and stick with it**:
- "model" vs "network" vs "architecture"
- "training" vs "learning" vs "optimization"
- "sample" vs "example" vs "instance"

### Vocabulary Signaling

Describe the actual contribution: a combination, extension or modification can be
valuable. Explain the new capability, result or insight and its evidence. Replacing
an accurate verb with “introduce” does not establish novelty and can obscure credit.

---

## Mathematical Writing

### From Ethan Perez

**Unfold apostrophes** for clarity:
- Weak: "X's Y"
- Strong: "The Y of X"

Example: "the model's accuracy" → "the accuracy of the model"

### General Principles

1. **State all assumptions formally** before theorems
2. **Provide intuitive explanations** alongside proofs
3. **Use consistent notation** throughout the paper
4. **Define symbols at first use**

### Notation Conventions

```latex
% Scalars: lowercase italic
$x$, $y$, $\alpha$, $\beta$

% Vectors: lowercase bold
$\mathbf{x}$, $\mathbf{v}$

% Matrices: uppercase bold
$\mathbf{W}$, $\mathbf{X}$

% Sets: uppercase calligraphic
$\mathcal{X}$, $\mathcal{D}$

% Functions: roman for named functions
$\mathrm{softmax}$, $\mathrm{ReLU}$
```

---

## Figure Design

### From Neel Nanda

Figures should tell a coherent story even if the reader skips the text. Many readers DO skip the text initially.

### Design Principles

1. **Figure 1 is crucial**: Often the first thing readers examine after abstract
2. **Self-contained captions**: Reader should understand figure without main text
3. **No title inside figure**: The caption serves this function (ICML/NeurIPS rule)
4. **Vector graphics**: PDF/EPS for plots, PNG (600 DPI) only for photographs

### Accessibility Requirements

8% of men have color vision deficiency. Your figures must work for them.

**Solutions**:
- Use colorblind-safe palettes: Okabe-Ito or Paul Tol
- Avoid red-green combinations
- Verify figures work in grayscale
- Use different line styles (solid, dashed, dotted) in addition to colors

### Tools

```python
# SciencePlots: Publication-ready styles
import matplotlib.pyplot as plt
plt.style.use(['science', 'ieee'])

# Or for Nature-style
plt.style.use(['science', 'nature'])
```

---

## Common Mistakes to Avoid

### Structure Mistakes

| Mistake | Solution |
|---------|----------|
| Introduction repeats background without advancing the argument | Remove duplication or move detail; use the actual venue limit |
| Reader cannot identify the approach | Explain the mechanism earlier once its purpose is clear |
| Contributions are unclear | State specific supported contributions in prose or bullets as appropriate |
| Experiments without explicit claims | State what each experiment tests |

### Writing Mistakes

| Mistake | Solution |
|---------|----------|
| Generic abstract opening | Start with your specific contribution |
| Inconsistent terminology | Choose one term per concept |
| Passive voice overuse | Use active voice: "We show" not "It is shown" |
| Hedging everywhere | Be confident unless genuinely uncertain |

### Figure Mistakes

| Mistake | Solution |
|---------|----------|
| Raster graphics for plots | Use vector (PDF/EPS) |
| Red-green color scheme | Use colorblind-safe palette |
| Title inside figure | Put title in caption |
| Captions require main text | Make captions self-contained |

### Citation Mistakes

| Mistake | Solution |
|---------|----------|
| Paper-by-paper Related Work | Organize methodologically |
| Missing relevant citations | Reviewers authored papers—cite generously |
| AI-generated citations | Always verify via APIs |
| Inconsistent citation format | Use BibLaTeX with consistent keys |

---

## Pre-Submission Checklist

Before submitting, verify:

**Narrative**:
- [ ] Can state contribution in one sentence
- [ ] Three pillars (What/Why/So What) clear in intro
- [ ] Every experiment supports a specific claim

**Structure**:
- [ ] Abstract and Introduction preserve the same claim scope and evidence strength
- [ ] Introduction length fits the audience, argument and verified venue requirements
- [ ] Approach is identifiable without an unexplained jump from problem to modules
- [ ] Contributions are explicit; bullets are optional unless the venue requires them
- [ ] Limitations section present

**Writing**:
- [ ] Consistent terminology throughout
- [ ] No generic opening sentences
- [ ] Hedging removed unless necessary
- [ ] All figures have self-contained captions

**Technical**:
- [ ] All citations verified via API
- [ ] Error bars included with methodology
- [ ] Compute resources documented
- [ ] Code/data availability stated
