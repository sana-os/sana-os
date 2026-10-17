# Changelog

All notable changes to SANA OS are recorded here: what changed, why, and the observation that prompted it.
Versions before 1.0 belong to the character-era lineage; see [`HISTORY.md`](HISTORY.md).

## [Unreleased]

### Fixed

- **`personas/Persona_Template.md` — restored stripped characters.**
  Observation: every `\ / : * ? " < > |` was missing from this file only — the set of characters Windows does not allow in file names — producing words such as "victorydefeat" and "$rightarrow$". Only the missing characters were put back, following the label format of `Persona_Reasoning.md` and `Persona_History.md`; no wording was changed. The bold markers and the colons after the invariant names are the least certain part of the reconstruction.
- **`core/Communication_Layer.md`, `frameworks/CPM.md`, `frameworks/Legitimacy_Layer.md` — removed whole-file ```` ```markdown ```` wrappers.**
  Observation: the wrapper turned every diagram block inside-out when rendered, and left an unclosed block in `Communication_Layer.md`. The YAML metadata is now real front matter at the top of each file; the metadata of the embedded *CPM Metadata Spec* is kept as a `yaml` block. No text was changed.
- **`frameworks/Value_Formation.md` — removed `[cite_start]` / `[cite: N]` markers and updated file references.**
  Observation: the markers pointed to line numbers in the author's working files, which are not in this repository. The source files are kept as provenance; *Related Frameworks* now names `History_Analysis.md` and `core/Communication_Layer.md`.
- **`LICENSE.md` — the immutability clause now names `core/Core_Principle.md`.**
  Observation: it named `core/SANA_OS_Core_Principle.md`, which does not exist.
- **`frameworks/RSM.md` — "General Meaning Model" → "Governance Maturity Model".**
  Observation: GMM's own definition file and both READMEs use "Governance Maturity Model".

### Added

- **`.gitattributes`** — LF line endings for text files. Observation: a Windows checkout converted files to CRLF, which changes the hash of the immutable `Core_Principle.md` without changing its text.
- **`HISTORY.md`** — the two lineages of SANA, why the version restarts at 1.0, and where the files removed by the full replacement are.

### Open — needs the author's decision

These were found in the same review and are not changed, because each is a choice rather than a repair.

- **Invariant hierarchy.** `Core_Principle.md` defines 4 invariants, `Persona_Template.md` 8, `Core_Specification.md` 5 design invariants; their relation is not stated. `Persona_Reasoning.md` refers to "the 8 structural invariants" but its loading order does not include the Template.
- **Time Layer.** Referenced by `Integrated_Knowledge.md`, `Communication_Layer.md`, `CPM.md`, `Legitimacy_Layer.md`, `Persona_History.md` and `Persona_Template.md`; no `Time_Layer.md` exists.
- **GMM stability condition.** `frameworks/README.md` gives `V ≤ k × A_eff`; `GMM.md` does not contain it.
- **Layer names.** Layer A appears as Survival / Instinct / Survival · Stability, Layer B as Narrative / Culture / Culture · Stories / Meaning · Cultural Identity. A glossary would state which are synonyms.
- **Core Principle editions.** English and Latin are both called "Master Edition"; which one is authoritative, and whether the Latin edition is loaded into prompts.
- **Version labels.** `History_Analysis.md` says "Compatible with SANA OS v1.8+"; frameworks carry their own versions (CPM 1.1, RSM 1.3).
- **README GPTs link** is still a placeholder ("update when live").
