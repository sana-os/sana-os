# Invariants — how the three sets relate

> **Developer reference.** This file is not part of any standard prompt loading order and is not one of the required Core files. Do not load it into a prompt in place of `Core_Principle.md`. If an implementation ever ingests this directory as a whole, or retrieves from it by search, check that this file is excluded or handled deliberately.

Decision: [`decisions/0001-invariant-positions.md`](../decisions/0001-invariant-positions.md).

**How to read the arrows and the "basis" column:** "can be positioned on this basis". Not "follows necessarily from this alone", and not "was written in this order". The records do not show how the sets came to be.

## 1. The four immutable principles — canonical

`core/Core_Principle.md` §2. Immutable (`LICENSE.md`, Core Principle Immutability).

| | Principle |
|---|---|
| **C1** | Non-Hostile Baseline (`born_loved = true`) |
| **C2** | No Logic Without Observation |
| **C3** | Structural Translation |
| **C4** | Autonomy Preservation |

## 2. The eight persona operating requirements — mandatory for personas

`personas/Persona_Template.md` §0. Kept as written. Relation types: **restatement** · **concretisation** · **added operating constraint**.

| | Requirement | Basis | Relation |
|---|---|---|---|
| **T1** | `born_loved = true` | C1 | restatement |
| **T2** | `premises_before_conclusions` | C2 | concretisation as an order of processing; not strictly identical |
| **T3** | `psychological_safety` | Core §0, §1, §3; C1–C4 | the purpose of the Core made a cross-cutting requirement |
| **T4** | `non_adversarial` | C1 + C3; Core §1 (stop grading) | concretisation of stance and expression |
| **T5** | `structural_analysis` | C3 | concretisation of what is analysed and with which models |
| **T6** | `autonomy_preservation` | C4 | operating form of the same aim, with a difference in strength: "never force a decision" (C4) and "do not make decisions for the user" (T6) are not identical |
| **T7** | `oneshot_deescalation` | C4 + `Communication_Layer.md` §5 (safety flow) and §10 (no persuasion loops) | added operating constraint: the count "once" does not follow from C4 alone. Its scope is not yet defined (see the decision) |
| **T8** | `narrative_stabilization` | Core §0, §1; C1 + C4; related to T3 | added constraint on presenting structure in a form the user can absorb. Not a restatement of "understanding is not agreement" |

## 3. The five engine design constraints — for this version of the specification

`core/Core_Specification.md` §0.3. Binding on implementations that claim conformance to this version.

| | Constraint | Basis | Note |
|---|---|---|---|
| **S1** | Alignment First | C2 | C2 as the engine's order of processing |
| **S2** | Stability Over Optimization | Core purpose; T3, T8 | measuring stability as Δv is an implementation choice |
| **S3** | Invocation Is Allowed. Result-Dumping Is Not. | C4; C3 (structure is translated into dialogue) | internal use of a framework is separate from presenting its raw result as a diagnosis. It is **not** a permission for external operations |
| **S4** | Exposure Is Gated. | T3; Communication Layer | exposure has **conditions** (premises, intent, Δv); it does not mean passing every stage in order |
| **S5** | Δv Is the Primary Engine Variable. | — | a design choice of this specification; it does not follow from the four principles |

## 4. Which personas receive which set — observed and decided

| Persona | Receives now (loading order) | Decided |
|---|---|---|
| Coaching | C1–C4 (via `Core_Principle.md`); two of them restated under §2 | to receive T1–T8 — not yet applied |
| History | C1–C4; two of them restated under §2 | to receive T1–T8 — not yet applied |
| Reasoning | C1–C4; refers to "the 8" without receiving them | to receive T1–T8 — considered separately |
| Personas built from the Template | C1–C4 and T1–T8 | — |
