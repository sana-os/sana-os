# Personas — Loading Guide

This directory contains persona definitions for SANA OS.

Every persona shares the same immutable core and adds a context-specific layer on top.

---

## Loading order

Always load in this exact sequence. Core files first, persona last.

---

### Persona_Coaching

For personal struggle, workplace conflict, and interpersonal friction.

```
1. core/Core_Principle.md
2. core/Integrated_Knowledge.md
3. core/Communication_Layer.md
4. frameworks/RBM.md
5. frameworks/CPM.md
6. frameworks/Value_Formation.md
7. personas/Persona_Coaching.md
```

**What each file adds:**

| File | Role in Coaching context |
|---|---|
| `Core_Principle.md` | Non-hostile baseline, four invariants |
| `Integrated_Knowledge.md` | Compressed reference for all frameworks |
| `Communication_Layer.md` | Translates analysis into safe dialogue |
| `RBM.md` | Detects demand/supply overload (stress diagnosis) |
| `CPM.md` | Detects cognitive compression and narrative substitution |
| `Value_Formation.md` | Proximity Rule, priority filtering, personal value hierarchy |
| `Persona_Coaching.md` | Coaching-specific response format and guardrails |

---

### Persona_History

For historical events, civilisational analysis, and structural diagnosis across time.

```
1. core/Core_Principle.md
2. core/Integrated_Knowledge.md
3. core/Communication_Layer.md
4. frameworks/GMM.md
5. frameworks/RBM.md
6. frameworks/CPM.md
7. frameworks/RSM.md
8. frameworks/Legitimacy_Layer.md
9. frameworks/History_Analysis.md
10. personas/Persona_History.md
```

**What each file adds:**

| File | Role in History context |
|---|---|
| `Core_Principle.md` | Non-hostile baseline, four invariants |
| `Integrated_Knowledge.md` | Compressed reference for all frameworks |
| `Communication_Layer.md` | Translates structural analysis into dialogue |
| `GMM.md` | Layer A/B/C structural state diagnosis |
| `RBM.md` | Resource bottleneck detection across eras |
| `CPM.md` | Cognitive compression — narrative formation and collapse |
| `RSM.md` | Role failure within institutions and states |
| `Legitimacy_Layer.md` | Narrative Core vs. Institution Core alignment |
| `History_Analysis.md` | Source Trifurcation, Thought Experiment Sandbox |
| `Persona_History.md` | History-specific response format and guardrails |

---

### Persona_Reasoning

For meetings, team priority conflicts, and organisational decision-making.

```
1. core/Core_Principle.md
2. core/Integrated_Knowledge.md
3. core/Communication_Layer.md
4. frameworks/RBM.md
5. frameworks/RSM.md
6. personas/Persona_Reasoning.md
```

**What each file adds:**

| File | Role in Reasoning context |
|---|---|
| `Core_Principle.md` | Non-hostile baseline, four invariants |
| `Integrated_Knowledge.md` | Compressed reference for all frameworks |
| `Communication_Layer.md` | Prevents adversarial escalation in group settings |
| `RBM.md` | Quantifies demand/supply gaps in team capacity |
| `RSM.md` | Diagnoses role capture, architect isolation, and role failure |
| `Persona_Reasoning.md` | Alignment Sequence, strict premise-before-conclusion protocol |

---

### Persona_Template

For building a custom SANA persona for any domain.

```
1. core/Core_Principle.md
2. core/Integrated_Knowledge.md
3. core/Communication_Layer.md
4. [frameworks as needed]
5. personas/Persona_Template.md  ← customise Section 2
```

Load only the framework files relevant to your domain. The four invariants in `Core_Principle.md` must be preserved unchanged.

---

## Notes

- Persona files are always loaded **last**
- Framework files may be added or removed depending on use case
- `Core_Principle.md`, `Integrated_Knowledge.md`, and `Communication_Layer.md` are always required
- For project-based use, paste all files as a single combined system prompt

## Reference composition

The reference system prompt for a persona is defined exactly, so that the same commit always gives the same text ([decision 0003](../decisions/0003-repository-position.md)):

- the files of the persona's loading order above, in that order;
- each file as stored in this repository (UTF-8, LF), with trailing newlines removed;
- joined by one blank line (`\n\n`), with nothing added before, between or after them.

For a persona built from the Template, its file is `Persona_Template.md` with the developer note (the bracketed line under the title) removed and sections 2–3 replaced by the persona's own; the title line and sections 0–1 are kept unchanged.

Changes to text the model receives are tested on this composition. Implementations for a platform may combine the files differently (separators, file headers, frameworks as skills) and state how.
