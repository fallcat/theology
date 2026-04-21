You are initializing a structured research repository for theology.

## Objective
Build a long-term, modular, and rigorous system for studying theology across multiple religious traditions.  
This is not a note-taking system. It is a **research system** designed to track questions, evidence, interpretations, and synthesis over time.

The system should support:
- Deep exploration of individual questions
- Multiple interpretations and sources
- Cross-religion comparison
- Traceable reasoning (from source → interpretation → conclusion)
- Long-term evolution of thought

---

## Core Principles

1. **Questions are atomic units**
   - Every insight starts from a question
   - Questions should be stored independently and linked

2. **Separate observation from interpretation**
   - Observation = what the text says
   - Interpretation = what it means
   - Never mix them

3. **Support multiple interpretations**
   - Do not collapse disagreements
   - Track different views explicitly with sources

4. **Modular structure**
   - Each subdomain (module) should be self-contained
   - Modules act like “mini-theses”

5. **Comparative layer**
   - Different religious traditions should not be mixed at the base level
   - Cross-religion comparison happens in a separate layer

6. **Synthesis is explicit**
   - Higher-level conclusions must be written separately
   - Track uncertainty and unresolved tensions

---

## Repository Structure

Create the following structure:

theology/
├── christianity/
│   ├── modules/
│   ├── questions/
│   └── sources/
│
├── other_religions/
│   ├── buddhism/
│   │   ├── modules/
│   │   ├── questions/
│   │   └── sources/
│   └── islam/
│       ├── modules/
│       ├── questions/
│       └── sources/
│
├── comparative/
│   ├── themes/
│   └── analyses/
│
├── global_questions/
├── synthesis/
└── meta/

---

## File Templates

### Question Template

Each question file should follow this structure:

# QXXX: [Question]

## Motivation
Why this question matters

## Sources / Verses
- List of references

## Observations (Objective)
- Direct statements from sources

## Interpretations (Multiple Views)
### View A
- Explanation
- Supporting sources

### View B
- Explanation
- Supporting sources

## Cross-References
- Related questions / modules

## Tensions / Open Questions
- Unresolved issues

## Notes
- Optional insights

## Confidence
- High / Medium / Low

---

### Module Template

Each module should represent a focused subproject:

# Module: [Name]

## Scope
What this module covers

## Key Questions
- Links to relevant question files

## Core Concepts
- Important ideas

## Interpretations
- Major viewpoints

## Internal Tensions
- Conflicts within the module

## Current Understanding
- Summary of findings

## Next Questions
- What to explore next

---

### Comparative Analysis Template

# Topic: [Concept across religions]

## Christianity
- Summary

## Buddhism
- Summary

## Other Traditions
- Summary

## Key Differences
- Core distinctions

## Underlying Assumptions
- Differences in worldview

## Open Questions
- Unresolved comparisons

---

## Meta Tracking

Create files in `meta/`:

- research_log.md → track progress
- open_questions.md → unanswered questions
- methodology.md → how the system evolves

---

## Agent Behavior Guidelines

- When encountering a new question → create a question file
- When multiple related questions exist → suggest creating a module
- When patterns emerge → update themes or synthesis
- Never overwrite past reasoning; append and evolve
- Always preserve uncertainty and alternative views

## Git Hygiene (MANDATORY for every agent session)

This is a knowledge-research repository: the remote is the source of truth, knowledge accumulates across many short agent sessions, and the local working tree is always disposable. The pipeline below is non-negotiable.

**1. Pull first — ALWAYS.** Before doing any work at the start of a session, AND before every commit:
```
git fetch origin
git pull --rebase origin <current-branch>
```
Another session or a human may have pushed while you were planning. Working on stale state produces merge conflicts, duplicate Q-numbers, or overwritten reasoning. Resolve any conflicts before continuing — do NOT force-push to bypass them.

**2. Commit every logical unit.** One unit = one commit. Don't batch unrelated edits. Don't leave uncommitted changes at session end. Commit messages: imperative mood, one-line subject ≤ 72 chars, optional body for the "why". Follow the existing pattern (`Init: ...`, `Add: ...`, `Update: ...`, `Fix: ...`).

**3. Push after EVERY commit — not just at the end.** `git push origin <current-branch>`. "Committed but not pushed" is a failure state. If the push fails (auth, network, divergence), stop and diagnose — do not continue making more local commits on top of an un-pushed pile. Never force-push `main` or any shared branch.

**4. Exit check.** Before ending a session, both must be true:
- `git status` shows a clean tree.
- `git rev-list --left-right --count HEAD...origin/<branch>` reports `0 0` (local fully in sync with remote).

If either is violated, fix before exiting — that's the whole point of this pipeline.

---

## Output Requirement

Generate:
1. The full folder structure
2. One example question file
3. One example module
4. One example comparative analysis
5. A minimal meta folder setup

Keep everything clean, minimal, and extensible.
