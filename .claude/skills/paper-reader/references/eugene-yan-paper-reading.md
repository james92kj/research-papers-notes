# Eugene Yan's paper-reading method (condensed)

Source: https://eugeneyan.com/writing/paper-club/

This file is condensed for use inside the `paper-reader` skill. Use it when planning Phase 2 (skim) or designing the order in which to walk the user through a paper.

## The three-pass approach

| Pass | Time | What you actually do |
|---|---|---|
| 1. Skim | ~10 min | Title, abstract, intro, figures, conclusion. Get the scope. Do **not** try to understand details. |
| 2. Read for understanding | ~1 hr | Follow the narrative. Don't get bogged down in math/proofs. Identify sections that need a third pass. |
| 3. Deep dive | 3–6 hr (optional) | Methodology, proofs, replication-grade understanding. Only needed if you'll implement or critique. |

> "Most of the time, unless you're trying to replicate the paper, two passes will suffice." — Eugene Yan

For this skill, **Phase 2 = Pass 1 (skim)** and **Phase 3 = Pass 2 (read for understanding) done paragraph-by-paragraph**. We don't routinely do Pass 3 unless the user explicitly asks to go deep on a section.

## The five focus questions

When facilitating, Yan directs attention to:

1. **Motivation** — Why does this problem matter? What gap exists in the prior work?
2. **Methodology** — How was the problem actually addressed? What's the core mechanism?
3. **Results** — What were the key findings? What's the headline number?
4. **Ablations** — Which design choices worked? Which didn't? Why?
5. **Related work** — How does this advance over previous efforts?

These five are excellent anchors for **Phase 4 (synthesis)** — make sure the user can answer all five before marking a paper done.

## How to handle dense math / unfamiliar concepts

Yan's pragmatic move: **screenshot the equation or term and ask Claude to explain it.** Inside this skill, that means: when the paragraph contains math the user doesn't know, you explain the equation inline in plain English with an analogy, then add the term to the glossary. Don't make the user power through unfamiliar notation alone.

## Note-taking

Yan uses Zotero for paper management and Zotero's built-in highlighter for marginalia. He screen-shares his annotated PDF (no slides) when facilitating. This skill mirrors that: `paper.md` is the "marginalia" — the running annotated read, paragraph by paragraph.

## Author intent

The article hints rather than prescribes: when authors attend paper club, they share "behind-the-scenes insights" — e.g. *why* Molmo emphasized analog clocks. The takeaway is: papers don't always tell you why an authoring choice was made. When you can't ask the author, **infer the why from the structure** — that's exactly what Phase 3's "Bridge" section forces.

## Building intuition over time

Latent Space Paper Club covers ~50 papers/year, with a thematic spine (language modeling) plus cross-domain branches (vision, audio, RL). Coherence is deliberate. The implication for this skill: surface **cross-paper weak spots** in `~/paper-reader/index.md` so the user's reading compounds instead of feeling like one-off sessions.

## Pitfalls Yan calls out

- **Skipping the pre-read.** Yan says it costs ~80% of the value of discussion. For this skill: **don't let the user skip Phase 2.** The skim is the foundation for everything in Phase 3.
- **Implicit:** trying to read a paper without the prerequisite foundation. If the user is struggling badly on a paper, it may be the wrong paper — offer to switch to a more foundational one and come back.

## Striking lines (short quotes — safe to keep verbatim, all <15 words)

- "If you find reading academic papers challenging, you're not alone."
- "Most of the time, unless you're trying to replicate the paper, two passes will suffice."
- "Pre-reading helps you identify what you don't understand and clarify during discussion."

## How this maps to the skill's phases

| Skill phase | Yan's pass | Yan's focus questions |
|---|---|---|
| Phase 2 (skim) | Pass 1 | Motivation (high-level only) |
| Phase 3 (deep) | Pass 2 done paragraph-by-paragraph | Methodology, Results, Ablations |
| Phase 4 (synthesis) | — | All five focus questions, plus "what would you push back on?" |
