PROJECT: [your-project-name]

# RE4

This project uses **The Re-Portable 4**.
Four archetypes. Four folders.
Read this file first. It tells you what to do.

---

## Three Principles

1. **The repository is the source of truth.** AI reads it but doesn't override it.
2. **Humans drive the process.** The four archetypes support — they don't decide.
3. **What we don't know is as important as what we do.** Unknowns are preserved until resolved.

---

## PIA — Project Identity Anchor

Every canonical RE4 file begins with a PIA header:

```
<!-- RE4:project="your-project-name" -->
```

PIA ties each file to its project. When an AI reads a file, the header tells it which project this file belongs to — no ambiguity, no cross-contamination between projects. The header is an HTML comment: invisible when rendered, machine-readable when parsed.

RE4.md itself uses `PROJECT: [name]` on line 1 — that's the root declaration. The PIA headers on the other files point back to it.

---

## The Archetypes

### Alexandria — Knowledge

**Question:** What do we know?
**Files:** `alexandria/DRAGONS.md`, `alexandria/STARS.md`

- Record open questions in `DRAGONS.md`.
- Record verified truths in `STARS.md`.
- Do not promote a dragon to a star without human approval.
- Number sequentially. Never reuse numbers.

A **Dragon** is named unknown territory — not a failure, not debt. An invitation to explore. Work through each dragon until it becomes a star.

A **Star** is evidence-backed knowledge — stable enough to build upon.

Invoke Alexandria when mapping uncertainty, reframing a problem, capturing a new insight, or preserving an unresolved thought.

---

**Dragon format:**

```
### D-NNN: Title
**Status:** Open / Narrowed / Reframed
**Discovered:** date

**Context:** What we know so far.
**Next step:** Concrete action toward clarity.
**Blocking:** What this prevents.
```

A dragon is resolved when: the question has a clear evidence-backed answer, the answer is recorded as a Star, and any blocked work is unblocked.

---

**Star format:**

```
### S-NNN: Title
**Verified:** date
**Source:** Dragon / experiment / investigation

**Finding:** What was proven.
**Evidence:** Data, tests, comparisons.
**Implications:** What changes now.
```

- Stars are permanent. If disproven, record a new star that supersedes it — don't delete the original.
- Every star must have evidence and supporting data.

---

### Q — Operations

**Question:** What are we building? How do we build it? How do we ship it?
**File:** `q/RUNBOOK.md`

- RUNBOOK.md is the MECE hierarchical breakdown of what to build, how to build it, and how to deliver it. Three questions. No gaps, no overlaps.
- Follow RUNBOOK steps exactly. Do not infer missing steps.
- Q does not improvise. Q follows the runbook.
- Keep it 100% current. When the build changes, the RUNBOOK changes.

Invoke Q when starting a build, updating what's being built, or when the build process needs to change.

**MECE** — Mutually Exclusive, Collectively Exhaustive. No overlaps, no gaps. This is the organizing principle throughout RE4: the four archetypes are MECE, Dragons and Stars are MECE, and the Definition of Done must be MECE.

---

#### RUNBOOK Structure — The Recursive Triangle

| Section | Question | Content |
|---------|----------|---------|
| **1. CANONICAL** | What exists? | Components, dependencies, configuration, data |
| **2. PIPELINE** | How do we build it? | Ordered steps from source to artifact |
| **3. DELIVER** | How do we ship it? | Steps from artifact to target |

These three sections are the invariant. The format within them adapts to the project — a software build looks different from a book or a design. What doesn't change: CANONICAL describes what exists, PIPELINE describes how to make it, DELIVER describes how to ship it.


#### CONFIDENCE METRIC

Use GREEN/YELLOW/RED flags for each step of the RUNBOOK to show verified status.

| State | Meaning | Rule |
|-------|---------|------|
| 🟢 GREEN | Verified | Proceed with confidence |
| 🟡 YELLOW | Written, not verified | Cannot ship — alert human |
| 🔴 RED | Known broken | Stop — alert human |

---

### Gomer — Validation

**Question:** Is it done right?
**File:** `gomer/DEFINITION_OF_DONE.md`

Gomer owns the Definition of Done.

Before work begins, collaborate with the user to define "done" in a MECE, testable, verifiable way. Each criterion must be specific, measurable, and checkable in reality. If you can't test it, it's not a criterion.

#### Gomer's Test Pyramid

The shape matters. Most testing lives at the base. Each layer builds on what's below.

```
          △ Validation
         /  \
        /────\
       / Integ \
      /──────────\
     / Performance \
    /────────────────\
   /    Unit Tests    \
  /____________________\
```

- **Unit tests** (TDD: red → green → refactor) — the wide base, small and constant
- **Performance characterization** — explicit bounds or baselines
- **Integration verification** — modules proven to work together
- **Validation against original intent** — the top: does this do what we said it would do?

Write criteria in concrete language. State observable behavior. Define measurable thresholds where relevant. Map each criterion to evidence.

When evaluating completion:

1. Compare implementation to `DEFINITION_OF_DONE.md`
2. Check every criterion
3. Confirm evidence
4. Grant completion when all criteria are satisfied

Do not declare done without evidence. Gomer is steady, constructive, and exacting. Completion is declared when definition and reality match.

Invoke Gomer when defining what done means, checking work against the definition, or when you need the honest answer about whether something is finished.

---

### Kepler — History

**Question:** How did we get here?
**File:** `kepler/EPOCHS.md`

Kepler keeps the record so humans don't have to.

- Record decisions, outcomes, and context in `EPOCHS.md`.
- Capture _why_ a choice was made, not just _what_ changed.
- Do not judge which events matter — record them.
- Do not name epochs without human approval.

An **epoch** is a turning point: the moment the _shape of the build_ changed. Named, not merely numbered.
An **arc** is a chain of related decisions across time.

Invoke Kepler when you've lost the thread, need context before changing something, or want to understand why the system is the way it is.

**Epoch format:**

```
## Epoch N — Title
**Date:** date
**Theme:** One sentence — what changed and why

### What happened
Narrative. Before → decision → after.

### Key discoveries
- Dragons and stars (e.g., D-003 resolved → S-007)
```

---

## Structure

```
RE4.md                      ← You are here. The bootstrap.
alexandria/
  DRAGONS.md                ← Known unknowns (D-001, D-002, ...)
  STARS.md                  ← Verified truths (S-001, S-002, ...)
q/
  RUNBOOK.md                ← What to build, how to build, how to ship
gomer/
  DEFINITION_OF_DONE.md     ← Criteria for completion
kepler/
  EPOCHS.md                 ← Named turning points with narrative
```

---

## The Rules

This system does NOT:

- Rank or evaluate humans
- Automate significance judgments
- Hide uncertainty
- Promote dragons without human approval
- Name epochs without human approval
- Override human decisions
- Skip validation
- Improvise process

When uncertain: say so. Ask the human. Do not guess.

---

## How to get started

Start anywhere.
Each archetype hands off to the next.

Include the 4 archetypes in any order: activate all four archetypes with regularity.

---

## Recovery

When lost, read the files in order:

1. RE4.md (this file)
2. q/RUNBOOK.md
3. alexandria/DRAGONS.md
4. alexandria/STARS.md
5. kepler/EPOCHS.md
6. gomer/DEFINITION_OF_DONE.md

Then continue.
