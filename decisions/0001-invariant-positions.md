# 0001 — Positions of the 4, 8 and 5 invariants

- **Status:** Decided
- **Date:** 2026-10-18
- **Decided by:** the author (SANA OS Project)
- **Prepared with:** a draft by Claude, revised after a separate AI review, then decided by the author
- **Developer reference.** This file is not part of any standard prompt loading order.

## Context — what the records show

At commit `96f08c4` ("Full replace — SANA OS v1.0") three sets already existed side by side:

| Set | Where |
|---|---|
| 4 immutable principles | `core/Core_Principle.md` §2 |
| 8 structural invariants | `personas/Persona_Template.md` §0 |
| 5 core design invariants | `core/Core_Specification.md` §0.3 |

Their relation was stated nowhere. `Persona_Reasoning.md` refers to "the 8 structural invariants", but its loading order does not include them. `Persona_Coaching.md` and `Persona_History.md` hold two items under the heading "Core Invariants".

**The records do not show in which order the three sets were written, or whether one was derived from another.** This decision does not reconstruct the original intent. It keeps the existing texts and decides how they are positioned from now on. Not knowing the history is not a reason to leave the specification undecided.

## Decision

1. **The canonical immutable principles are the four in `core/Core_Principle.md` §2.** The Core text is not changed.
2. **The eight in `Persona_Template.md` are kept as mandatory persona operating requirements.** They mix restatements of the four, concrete forms of them, and additional operating constraints. Renaming them does not make them optional.
3. **The five in `Core_Specification.md` are design constraints of that version of the engine specification.** An implementation that claims conformance to the specification keeps them. A different engine design that satisfies the four principles is not ruled out by them; whether it may still be called conformant to an unchanged version of the specification is a separate question.
4. **This classification is a decision made now.** It does not settle how the sets came to be, or any derivation between them at the time they were written.
5. **Changes that alter scope or meaning are recorded separately** from changes to wording and references.

The mapping between the sets is kept in [`core/INVARIANTS.md`](../core/INVARIANTS.md). An arrow there means "can be positioned on this basis", never "follows necessarily from this alone" or "was written in this order".

## Alternatives considered

- **Merge the three into one list.** Rejected: it would rewrite texts that must be kept, and erase the difference between principle, operating requirement and engine design.
- **Treat the eight as equal to the four.** Rejected: `LICENSE.md` names only `core/Core_Principle.md` as the file that may not be modified, and several of the eight add constraints the four do not contain.
- **Treat the eight as optional guidance.** Rejected: the Template already requires them strongly, and nothing observed in use gave a reason to weaken them.
- **Treat the specification as an optional developer note.** Rejected: `core/README.md` says only that it need not be loaded into prompts, not that it binds nothing.

## Precision notes

- `Persona_Template.md` is not, like `Core_Principle.md`, a file that `LICENSE.md` names as unmodifiable. The licence's other conditions — purpose preservation, adaptation marking — still apply to it. Changes to it are not unrestricted.
- Specification item 4 means **exposure has conditions** (premise alignment, intent, Δv), not that it passes through every stage in order.

## Not decided here

These are recorded so that this decision is not read as having settled them.

| Item | Where it goes |
|---|---|
| Headings and introductions of the Template, Coaching and History that present these sets | a separate change that alters prompt text: wording is aligned, no rule is meant to change, and the effect on interpretation is checked |
| Loading the eight into Coaching and History | decided by the author (2026-10-18), not yet applied. It changes what the model receives and is handled as its own change |
| Reasoning | will also receive the eight, but is considered separately: it is a special model among the SANA personas |
| Scope of T7 (one-shot de-escalation): when it applies, and that it does not cut off explanations the user asks for | its own change |
| Boundary of T8: respect for the user's agency and capacity to absorb, not preservation of the current narrative; facts and safety boundaries are not bent | its own change |
| T4: being non-adversarial does not mean leaving factual errors uncorrected | its own change |
| T6 / S3: doing work the user delegated vs taking their choice away; internal invocation of frameworks vs permission for external operations (sending, deleting) | a separate contract for external operations |
