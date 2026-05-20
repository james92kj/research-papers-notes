# English-for-papers — recurring academic patterns

This file is for Phase 3 step 3 (English notes). Use it when picking which 2–3 phrases to highlight from a paragraph. The user is technical but learning English — translate the *language*, not the ideas.

This file is **a starter set**. As you encounter new patterns the user struggles with, add them here so the catalog grows over time.

---

## 1. Hedging language

Academic English avoids overclaiming. Recognizing hedges helps the user spot how strong a claim actually is.

| Pattern | What it really means |
|---|---|
| "Our results **suggest** that…" | We're not 100% sure, but the data points this way |
| "**Likely** because…" | Our best guess, not proven |
| "We **observe** that…" | We saw it; we're not yet claiming why |
| "These findings **may** indicate…" | Soft claim; we're hedging |
| "It **appears that**…" | Even softer than "suggests" |
| "To the best of our knowledge…" | Standard hedge before a "first to do X" claim |

**Teach the user:** when you see "suggest", "may", "appears", "indicate", the author is hedging. The claim is weaker than it sounds at first read.

---

## 2. Claim-strength language

The opposite of hedging — words that signal a strong claim.

| Pattern | What it really means |
|---|---|
| "We **demonstrate** that…" | Strong: we have evidence and we believe it |
| "We **prove** that…" | Strongest: usually math/formal proof |
| "We **show** that…" | Medium-strong |
| "**Clearly**, …" / "**Obviously**, …" | Author is asserting confidence (sometimes too confidently — watch this) |
| "**Strikingly**, …" / "**Surprisingly**, …" | Author wants you to notice this result |

**Teach the user:** "demonstrate" and "show" carry more weight than "suggest." Track which the author uses — it tells you how much they're willing to commit.

---

## 3. Comparison phrases

Papers constantly compare methods. The user must read these fluently.

| Pattern | What it really means |
|---|---|
| "X **outperforms** Y" | X is better than Y on the metric |
| "X **achieves comparable performance to** Y" | About the same — possibly tied |
| "X **lags behind** Y" | X is worse than Y |
| "X **is on par with** Y" | Tied / about equal |
| "X **closes the gap** with Y" | X is approaching Y's performance |
| "X **sets a new state of the art** on Z" | X is now the best on benchmark Z |
| "**Relative to** baseline…" | Comparing against baseline |
| "X **yields a Y% improvement over** Z" | X is Y% better than Z |

---

## 4. Contrast moves (transition words)

These signal a turn in the argument. Critical for following the logical flow.

| Pattern | What it really means |
|---|---|
| "**However**, …" | "But, on the other hand…" |
| "**Nevertheless**, …" / "**Nonetheless**, …" | "Despite that, …" |
| "**In contrast**, …" | "The opposite is true here…" |
| "**On the other hand**, …" | Introducing a different perspective |
| "**Whereas** X…, Y…" | X does one thing, Y does another |
| "**While** prior work assumed…, we…" | Setting up the paper's novelty |
| "**That said**, …" | Adding a caveat |

**Teach the user:** when you see these, the next clause **contradicts or qualifies** the previous one. Slow down — this is where the author's argument turns.

---

## 5. Citation language

Papers cite a lot. The verb tells you what role the citation plays.

| Pattern | Role |
|---|---|
| "Smith et al. (2023) **introduced** …" | Crediting the original work |
| "**Following** Jones (2022), we…" | We are building on / using their method |
| "**Unlike** Wang et al. (2021), we…" | We differ from them in a specific way |
| "Prior work **has shown** …" | Setting up established background |
| "**In concurrent work**, …" | Someone else did similar work at the same time (not influenced by them) |
| "We **extend** the approach of … to …" | We're adapting an existing method |

---

## 6. "We" vs. "Our method" vs. passive voice

Papers vary the agent of action. This matters for who gets credit and for clarity.

| Pattern | Reading hint |
|---|---|
| "**We** trained the model on…" | The authors are taking direct credit for the action |
| "**Our method** achieves…" | The method (not the authors) is the agent — emphasizes the contribution |
| "The model **was trained** on…" | Passive — focuses on the object, not who did it. Common in methods sections. |

---

## 7. Section-opening sentences

Each paper section follows English conventions. Knowing the convention lets the user skim faster.

| Section | Typical opening move |
|---|---|
| Abstract | One-sentence problem statement, then "We propose / present / introduce …" |
| Introduction | First paragraph = wide problem framing. Last paragraph = "In this paper, we…" (the paper's contributions). |
| Related work | "X has been extensively studied…" / "Prior work on Y can be grouped into…" |
| Method | "We propose …", "Our approach consists of three components:…" |
| Experiments | "We evaluate on …", "We compare against …" |
| Results | "Table N shows that …", "We observe that …" |
| Discussion | "Our results suggest…", "A natural question is…" |
| Limitations / Conclusion | "Despite these results, …", "Future work could…" |

**Teach the user:** these openings repeat across papers. After 5 papers, the structure becomes automatic.

---

## 8. Common noun-phrase patterns (where English gets dense)

Long noun phrases are where non-native readers most often lose the thread. Example unpacking:

> "**The performance gap between supervised baselines and self-supervised pretrained models** narrows with scale."

Unpack it left-to-right:
- "performance gap" = how much one is better than the other
- "between supervised baselines and self-supervised pretrained models" = which two things we're comparing
- "narrows" = gets smaller
- "with scale" = as we make models bigger

Rewrite in plain English: "When the model gets bigger, supervised baselines and self-supervised pretrained models become more similar in performance."

**Teach the user:** when a sentence has a long noun phrase, **read it last word first** — that's usually the main thing. Then walk back to find what's being said about it.

---

## 9. Phrasings that signal the contribution

These are sentences worth bookmarking when you spot them — they tell you what the paper is *for*.

- "**Our key contribution is** …"
- "**To this end, we propose** …"
- "**The main insight** of this paper is …"
- "**In summary, our contributions are: (1) …, (2) …, (3) …**"

When the user spots one, that paragraph is one of the most important in the paper.

---

## 10. Vocabulary the user is likely to hit early

(Add to this list over time as new ones come up.)

- **Empirical** — based on experiments / data, not theory
- **Theoretical** — based on math / proofs
- **Heuristic** — a rule of thumb that works in practice but is not proven
- **Trade-off** — gaining one thing means losing another
- **Robust** — keeps working under varied / harsh conditions
- **Generalize** — work on data the model didn't see during training
- **Pretraining** — training on a large generic dataset before specializing
- **Fine-tuning** — additional training on a specific task after pretraining
- **Downstream task** — the actual task you care about, after pretraining
- **In-context learning** — model learns from examples in the prompt, no weight updates
- **Out-of-distribution** — data unlike what the model was trained on
- **Ablation** — removing one piece of the method to measure its contribution
- **Held-out** — kept aside, not used during training
- **State of the art** (SOTA) — the current best result on a benchmark
- **Inductive bias** — what the model is biased to learn easily (built-in assumptions)
- **Saturation** — performance has stopped improving with more data / compute
- **Scaling law** — a predictable relationship between scale and performance
- **Distillation** — training a small model to imitate a larger one
- **Self-supervised** — training signal comes from the data itself, not labels
- **Zero-shot** / **few-shot** — performance with 0 / very few examples

---

## How to use this file in Phase 3

For each paragraph's "English notes" section:

1. Skim the paragraph for the kinds of patterns above (hedges, comparisons, contrast moves, long noun phrases).
2. Pick 2–3 items the user is most likely to find hard.
3. For each, give a plain-English meaning and a one-sentence example.
4. Add new items to `~/paper-reader/notes/<paper-slug>/glossary.md`.
5. If you encounter a new pattern that's not yet in this file but seems to recur across papers, **mention it** — the user can ask to add it here.
