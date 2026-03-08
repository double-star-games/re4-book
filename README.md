# The Re-Portable 4

The Re-portable 4 assists the reader in professionally building with Claude Code without losing what makes the work alive. Written and designed by a non-coding software developer and a forty-year engineer shipping games and edge AI in Seattle: the RE4 offers a four-archetype framework for working with Claude Code — mapping unknowns, holding operations steady, recording history with context, and protecting the definition of done through honest testing and a shared grammar.

We built the system because we needed the assistance in our own company. As AI reshapes the scope, scale, and speed of work, we needed a way to stay tethered as our standards and creativity scaled with it—to keep the thread of decisions, standards, and history intact. RE4 lowers the cost of recovery after crashes, interruptions, and time-away, and helps teams treat the repository as a navigable place.

Rooted in Christopher Alexander's search for the quality without a name, Robert Martin's ethic of craft, and the authors' own lineage of biomimetic design, the book assumes bravery on the part of the reader — not mastery. It is written for engineers, makers, and anyone who can design and imagine but has never been invited to build.

---

## Install

To initialize RE4 in a new project, paste the following block into Claude Code:

```
Read the file RE4.md from https://raw.githubusercontent.com/double-star-games/re4-book/main/RE4.md

This is the RE4 coordination framework. Initialize it in this project:

1. Copy RE4.md to the project root. Replace [your-project-name] on line 1 with the actual project name.

2. Create the four archetype directories and their canonical files:

   alexandria/DRAGONS.md — start with:
   <!-- RE4:project="[project-name]" -->
   # Dragons
   Named unknowns. Not failures — invitations to explore.
   See RE4.md for the dragon format.

   alexandria/STARS.md — start with:
   <!-- RE4:project="[project-name]" -->
   # Stars
   Verified truths — stable enough to build upon.
   See RE4.md for the star format.

   q/RUNBOOK.md — start with:
   <!-- RE4:project="[project-name]" -->
   # Runbook
   What we're building, how we build it, and how we ship it.
   Three sections — CANONICAL, PIPELINE, DELIVER — no gaps, no overlaps.
   See RE4.md for the card format and the Recursive Triangle.
   ---
   ## 1. CANONICAL
   ## 2. PIPELINE
   ## 3. DELIVER

   gomer/DEFINITION_OF_DONE.md — start with:
   <!-- RE4:project="[project-name]" -->
   # Definition of Done
   MECE criteria for completion. Each criterion must be testable.
   See RE4.md for the test pyramid and evaluation process.

   kepler/EPOCHS.md — start with:
   <!-- RE4:project="[project-name]" -->
   # Epochs
   Named turning points — when the shape of the build changed.
   See RE4.md for the epoch format.

3. Read RE4.md fully. It is your orientation. Follow it.

4. Ask the human what we're building, then begin a loop:
   Alexandria → Q → Gomer → Kepler
```

---

## The Book

See [RE4_BOOK.md](RE4_BOOK.md) for the full text.

