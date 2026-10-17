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

### Changed — prompt text (no rule is meant to change; effect on interpretation is checked)

- **`Persona_Template.md` §0:** heading "IMMUTABLE CORE (OS Kernel - DO NOT MODIFY)" → "Mandatory Persona Operating Requirements (DO NOT MODIFY)"; "8 structural invariants" → "8 mandatory persona operating requirements". "OS Kernel" and "IMMUTABLE CORE" made the eight look equal to the Core principles (decision 0001). "DO NOT MODIFY" and the strength of the requirement are kept; the eight items are unchanged.
- **`Persona_Coaching.md` §2, `Persona_History.md` §2:** heading "Core Invariants & AI Self-Protection" → "Core Principles Emphasized in This Persona & AI Self-Protection", with two lines stating that the section highlights two principles and that all four in `core/Core_Principle.md` §2 remain mandatory. The heading made two items look like the whole Core. In Coaching, the suffix "(Immutable & Root)" is removed with the old heading: immutability belongs to the four, which the added lines keep mandatory. The two items are unchanged.

### Decided

- **Positions of the 4, 8 and 5 invariants** — [`decisions/0001-invariant-positions.md`](decisions/0001-invariant-positions.md).
  The four in `Core_Principle.md` §2 are the canonical immutable principles; the eight in `Persona_Template.md` are mandatory persona operating requirements; the five in `Core_Specification.md` are design constraints of that version of the engine. The classification is a decision made now and does not reconstruct how the sets came to be. Mapping: [`core/INVARIANTS.md`](core/INVARIANTS.md).
  `Core_Specification.md` §0.3 now says that its five constraints do not replace the four principles. This file is not part of any standard loading order.
- **Time Layer is the name of a concept, not a file.** Defined in `Legitimacy_Layer.md` §7 and `Integrated_Knowledge.md` §3; references to it are kept. `History_Analysis.md` was checked and does not contain it. See [`GLOSSARY.md`](GLOSSARY.md).

No file in any standard loading order was changed for these decisions. The new files (`decisions/`, `core/INVARIANTS.md`, `GLOSSARY.md`) are developer references and are not loaded into prompts.

### Decided, not yet applied

- **The eight are loaded into Coaching and History.** This changes what the model receives and is handled as its own change.
- **Reasoning also receives the eight**, considered separately: it is a special model among the SANA personas. Until then, `Persona_Reasoning.md` still refers to "the 8 structural invariants" without receiving them.

### Open — needs the author's decision

These were found in review and are not changed, because each is a choice rather than a repair.

- **Scope of T7** (`oneshot_deescalation`): when "once" applies — the safety flow of `Communication_Layer.md` §5, or persuasion loops in general (§10) — and that it does not cut off explanations or re-examination the user asks for.
- **Boundary of T8** (`narrative_stabilization`): respect for the user's agency and capacity to absorb, not preservation of the current narrative; facts and safety boundaries are not bent.
- **T4** (`non_adversarial`): being non-adversarial does not mean leaving factual errors uncorrected.
- **External operations (T6 / S3):** doing delegated work vs taking the user's choice away; internal invocation of a framework vs permission for external operations. To be defined as a separate contract.
- **GMM stability condition.** `frameworks/README.md` gives `V ≤ k × A_eff`; `GMM.md` does not contain it.
- **Layer names.** Several names are used for Layers A and B (listed in `GLOSSARY.md`); whether they are synonyms is not decided.
- **Core Principle editions.** English and Latin are both called "Master Edition"; which one is authoritative, and whether the Latin edition is loaded into prompts.
- **Version labels.** `History_Analysis.md` says "Compatible with SANA OS v1.8+"; frameworks carry their own versions (CPM 1.1, RSM 1.3).
- **README GPTs link** is still a placeholder ("update when live").
