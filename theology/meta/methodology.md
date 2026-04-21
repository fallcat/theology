# Methodology

This document describes the principles and working norms governing the theology research system. It is derived from the Core Principles and Agent Behavior Guidelines in `CLAUDE.MD` and should be updated as the system evolves.

## Core Principles

1. **Questions are atomic units.** Every investigation begins with a specific question, stored as its own file. Questions link to modules, comparative analyses, and other questions — but each question stands on its own as a self-contained research artifact.

2. **Observation and interpretation are strictly separated.** Observations record what a source says — direct statements, textual data, historical facts. Interpretations record what those observations mean according to a given tradition, scholar, or line of reasoning. These two activities occupy separate sections in every question file. This separation is not optional; it is the epistemic backbone of the system.

3. **Multiple interpretations are preserved, not collapsed.** Where genuine disagreement exists, the system tracks each view explicitly with its supporting sources. Premature harmonization is a research failure. A question file with only one interpretation is incomplete unless the matter is truly uncontested.

4. **Every claim is cited.** "Tradition says" is not a citation. Scripture references use book:chapter:verse format. Secondary sources cite author, title, and (where feasible) chapter or page. Uncited claims should be flagged for future sourcing.

5. **Traditions are studied on their own terms first.** Each religion has its own directory with its own modules, questions, and sources. Cross-tradition comparison happens only in the `comparative/` layer, after each tradition's internal logic has been understood. Premature comparison distorts both sides.

6. **Synthesis is explicit and traceable.** Higher-level conclusions belong in `synthesis/` and must show their derivation: which questions, which evidence, which reasoning. Synthesis files are not summaries — they are arguments, and their premises must be checkable.

## Working Norms

- **Append-only mindset.** Never overwrite past reasoning. If a view changes, add a new dated entry or a revision note rather than deleting the old position. The research log in `meta/research_log.md` tracks all significant additions.
- **Preserve uncertainty.** If something is unresolved, say so. Use the Confidence field in question files honestly. "Medium" is not a failure; it is information.
- **Evolve incrementally.** When a new question arises, create a question file. When related questions cluster, propose a module. When cross-tradition patterns emerge, write a comparative analysis. Do not build structure in advance of content.
- **Flag ambiguity.** When a source, doctrine, or term is genuinely ambiguous, note the ambiguity rather than resolving it silently. Ambiguity is data.
