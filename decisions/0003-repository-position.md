# 0003 — What this repository is, how its files are combined, and where changes are tested

- **Status:** Decided
- **Date:** 2026-10-23
- **Decided by:** the author (SANA OS Project)
- **Prepared with:** a draft by Claude, after the author raised the question
- **Developer reference.** This file is not part of any standard prompt loading order.

## Context — what the records show

- The README told users to paste the files, in a given order, into a custom GPT, a Gem or a chat project. The section "GPTs implementation" still pointed at a placeholder ("update when live").
- Custom GPTs are being retired by OpenAI, and Gemini's Gems are being replaced by Skills (announced for November 2026). A platform that is going away is no place to keep the reference behaviour of SANA, and no place to compare before and after a change.
- An implementation for another platform already exists outside this repository: `sana-os/sana-hermes` pins a commit of this repository and builds Hermes Agent profiles from it. It adds text of its own (runtime notes, personas written from the Template) and loads frameworks as skills.
- Changes that alter the text a model receives (decision 0001's persona wording, decision 0002's T7 scope) are to be checked before they are merged. Checked inside a platform, the result would mix the effect of the text with the platform's own layers: its hidden instructions, memory, tools, and the compression of long conversations.

## Decision

1. **This repository is the canonical text of SANA OS.** It holds the principles, frameworks and personas, their loading orders, and the invariants. It does not name a platform on which SANA runs.
2. **Reference composition.** For a persona, the reference system prompt is: the files of its loading order in [`personas/README.md`](../personas/README.md), in that order, each as stored in this repository (UTF-8, LF), with trailing newlines removed, joined by one blank line (`\n\n`). Nothing is added before, between or after them. For a persona built from the Template, its file is `Persona_Template.md` with the developer note (the bracketed line under the title) removed and sections 2–3 replaced by the persona's own; the title line and sections 0–1 are kept unchanged.
   *Reason:* the same commit then always gives the same bytes, so two compositions can be compared, and what the model receives is exactly the files and nothing else.
3. **Implementations for a platform are adapters, kept in their own repositories.** An adapter pins a commit of this repository, includes `core/Core_Principle.md` unchanged, and states what it adds or changes, as the licence requires of an adaptation. An adapter may load the files differently from the reference composition (for example, frameworks as skills); it says how.
4. **Changes to text the model receives are tested on the reference composition,** in a minimal harness: the same model, settings and inputs, a fixed number of repetitions, before and after the change, with every transcript and condition recorded. How a change behaves on a platform is checked in that platform's adapter, as a separate step.
5. **A test result describes behaviour under the recorded conditions.** It is not a proof of correctness and does not replace reading the change.

The harness is kept outside this repository (proposed: `sana-os/sana-eval`). It reads the commits to compare from a checkout of this repository, so it does not pin one.

## Alternatives considered

- **Keep GPTs or Gems as the place SANA runs.** Rejected: both are being retired.
- **Make the Hermes adapter the reference.** Rejected: it adds runtime notes, tools, memory and compression, so it cannot isolate the effect of a text change; and the canonical text would then depend on one adapter. It stays the place to check behaviour on Hermes.
- **Test by talking to SANA in a local app that reproduces GPTs.** Kept for exploration by a person, not as the baseline: the app adds instructions and memory of its own, and a conversation is hard to repeat under the same conditions.
- **Join the files with separators or file headers.** Not chosen for the reference: they would add text that is in no file. Adapters may add them and say so.

## Not decided here

| Item | Where it goes |
|---|---|
| Which model or models serve as the reference for testing | decided per test and recorded with the result |
| How many repetitions are enough | set per test (3 to start with, as in the checks prepared for the wording and T7 changes) |
| Whether results are judged by a person, by a reviewer model, or both | the harness only records; judging is a separate role |
| A machine-readable copy of the loading orders | not needed while `personas/README.md` is the single place they are written |
| Adapters for Gemini Skills or for what replaces custom GPTs | each its own repository, when needed |
