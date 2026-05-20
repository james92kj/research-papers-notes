# Research-engineer mindset

How a senior research engineer at DeepMind / OpenAI / Anthropic reads a paper. This file is the **rotating catalog** of lenses for Phase 3 step 4. Pick a lens for each paragraph; do not repeat the same lens two paragraphs in a row.

The qualities to embody, drawn from how good research engineers actually think:

- **Skepticism by default.** A claim is a claim. The numbers in the table are evidence for it — not proof of it.
- **First principles.** Strip the paper down to: what input, what mechanism, what output, what supervision signal?
- **Ablations are the whole game.** A method that works without ablations is luck. Ablations are how you know which piece is load-bearing.
- **Baselines are doing more work than you think.** A "5% gain over baseline" depends entirely on whether the baseline was tuned.
- **Scale changes everything.** Things that look smart at 100M parameters often vanish at 70B (and vice versa).
- **Failure modes matter more than success modes.** Where does the method break? That's the paper's true contribution.
- **Find the load-bearing assumption.** Every paper has one. If you removed it, the result collapses. Hunt for it.
- **Isolate the variable.** If they changed two things at once, the result is uninterpretable. Watch for this.
- **What would falsify this?** If no result could falsify the claim, the claim isn't doing real work.
- **Distribution shift.** Does the eval set look like the train set? If yes, gains may not transfer.
- **Compute / cost reality.** Every method has a price. Is the gain worth the cost?
- **Evaluation validity.** Does the metric actually measure what you care about? Goodhart is everywhere.
- **Generalization claims.** "Works on X" ≠ "works in general." Watch for over-generalized conclusions.
- **Prior-art delta.** What is genuinely new here vs what is repackaged from prior work?

---

## The 14 lenses — pick one per paragraph

For each lens: the **mindset**, plus a few **example questions** to ask of the paragraph in front of you.

### 1. Skepticism

> A claim is just a claim. Where is the evidence?

- What is the strongest claim in this paragraph?
- What would I need to see to actually believe it?
- Are the authors hedging here? If so, why?

### 2. First principles

> What is this actually doing, mechanically?

- If I had to explain this to a smart undergraduate in one sentence, what would I say?
- What's the input, what's the output, what's the loss?
- Strip away the marketing. What's left?

### 3. Ablation reasoning

> Which piece is load-bearing?

- If we removed *this* component, what would happen?
- Did the authors run that ablation? If not, why not?
- Are the ablations showing that the method works, or that the *story* works?

### 4. Baseline rigor

> Is the baseline a fair fight?

- Was the baseline tuned with the same compute budget?
- Did the authors pick a weak baseline to look better?
- What baseline would have made this comparison most honest?

### 5. Scaling intuition

> Does this still work at the next scale?

- The result is at scale X. What happens at 10X? At 1/10X?
- Is the gain growing, shrinking, or flat as scale increases?
- Did the authors run a scaling sweep? (Most papers should.)

### 6. Failure-mode hunting

> Where does this break?

- What's an input where this method will fail?
- Did the authors show any failure cases?
- If they didn't, what failures are they likely hiding?

### 7. Load-bearing assumption

> What does the whole paper rest on?

- What is the one assumption that, if false, kills the result?
- Is the paper transparent about that assumption?
- How robust is that assumption to real-world settings?

### 8. Isolate-the-variable

> Did they change one thing or three?

- Is this gain coming from the method, or from data, or from compute, or from training tricks?
- Could the result be explained by any of those alone?
- What experiment would isolate the variable cleanly?

### 9. Falsifiability

> What would falsify this claim?

- If the claim is "X causes Y", what observation would mean "no, it doesn't"?
- Is the claim falsifiable in principle? In practice?
- If not, it's not really a scientific claim — it's a slogan.

### 10. Distribution shift

> Does the eval look like training?

- Does the test set actually test generalization, or is it i.i.d. with train?
- What real-world distribution is the eval supposed to stand in for?
- Where does the method break under distribution shift?

### 11. Compute / cost reality

> Is the gain worth the price?

- How much compute did this take? How much inference cost?
- Is the gain over the baseline worth the compute multiplier?
- At what cost-per-call does this stop being practical?

### 12. Evaluation validity

> Does the metric measure what you care about?

- Is the metric a proxy for the real thing, or the real thing?
- What's the Goodhart failure mode here? (Optimizing the metric without improving the underlying quality.)
- Would a human grader agree with the metric?

### 13. Generalization claim

> Works on X ≠ works in general.

- The headline says "Method works." But works *on what*?
- Would I bet this works on a new domain? A new language? A new modality?
- What's the authors' strongest evidence for generalization?

### 14. Prior-art delta

> What's actually new here?

- Strip away the parts that are standard practice. What's left?
- How much of this method existed in prior work?
- Is the contribution the method, the engineering, the data, or the framing?

---

## How to use this catalog in Phase 3

- For each paragraph, **pick the lens that is most natural for the content of that paragraph.** Intro paragraphs → motivation/first principles; method paragraphs → ablations/load-bearing; results paragraphs → baselines/evaluation validity; experiments → isolate-the-variable, scaling, distribution shift.
- **Do not repeat the same lens twice in a row.** Variety is the point — the user is building reflexes across all 14.
- **State the lens explicitly** in the heading, e.g. *Research-engineer lens — Ablation reasoning*. Over time the user starts to recognize the moves.

## How to use this catalog in Phase 4

After the user reconstructs the paper, ask: "If you had to write the **one most uncomfortable question** to ask the authors, what would it be?" That question almost always lives in one of these 14 lenses. Push the user to name which one.
