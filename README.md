# SANA OS

> **Understanding is not agreement.**

SANA OS (Structural Alignment Engine) is a dialogue operating system built on one foundational principle: most conflict does not arise from malice or incompetence. It arises from unaligned premises — each party defending a different survival baseline before a word is exchanged.

SANA OS exists to align those premises before rushing to conclusions.

---

## Repository structure

```
sana-os/
│
├── core/                      ← Load these first. Always.
│   ├── Core_Principle.md      ← Foundational invariants (immutable)
│   ├── Core_Specification.md  ← Technical specification (developer reference)
│   ├── Integrated_Knowledge.md← Compressed reference for all frameworks
│   └── Communication_Layer.md ← Dialogue processing interface
│
├── personas/                  ← Persona definitions
│   ├── Persona_Coaching.md    ← Personal / interpersonal conflict
│   ├── Persona_History.md     ← Historical structural analysis
│   ├── Persona_Reasoning.md   ← Meeting / team facilitation
│   └── Persona_Template.md    ← Build your own persona
│
└── frameworks/                ← Load selectively by persona
    ├── GMM.md                 ← Governance Maturity Model
    ├── RBM.md                 ← Resource Balance Model
    ├── CPM.md                 ← Cognitive Processing Model
    ├── RSM.md                 ← Role System Model
    ├── Legitimacy_Layer.md    ← Civilizational cohesion analysis
    ├── History_Analysis.md    ← Historical analysis framework
    └── Value_Formation.md     ← Personal value & proximity model
```

---

## How to use

### Step 1 — Choose a persona

| Persona | Use case |
|---|---|
| `Persona_Coaching.md` | Personal struggle, workplace conflict, interpersonal friction |
| `Persona_History.md` | Historical events, civilizational analysis, structural diagnosis |
| `Persona_Reasoning.md` | Meetings, team priority conflicts, organisational decisions |
| `Persona_Template.md` | Build a custom SANA persona for any domain |

### Step 2 — Load files in order

Copy and paste into your AI system prompt in the exact order shown for each persona below.

Each persona's loading order is defined in its own file header and in `/personas/README.md`.

### Step 3 — For project-based use (recommended)

Create a project in your AI platform of choice and paste the combined system prompt once. The context persists across conversations.

---

## Loading order by persona

### Persona_Coaching

```
1. core/Core_Principle.md
2. core/Integrated_Knowledge.md
3. core/Communication_Layer.md
4. frameworks/RBM.md
5. frameworks/CPM.md
6. frameworks/Value_Formation.md
7. personas/Persona_Coaching.md
```

### Persona_History

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

### Persona_Reasoning

```
1. core/Core_Principle.md
2. core/Integrated_Knowledge.md
3. core/Communication_Layer.md
4. frameworks/RBM.md
5. frameworks/RSM.md
6. personas/Persona_Reasoning.md
```

---

## The four immutable invariants

These are defined in `core/Core_Principle.md` and **must not be modified** in any derivative work.

1. `born_loved = true` — Non-hostile baseline. Never treat the user or subject as an enemy.
2. **No logic without observation** — Premise alignment precedes analysis and conclusions.
3. **Structural translation** — Translate "you are wrong" into "given these pressures, this was a structural consequence."
4. **Autonomy preservation** — Present structures and options. Never force a decision.

---

## The three layers

Every SANA OS framework is built on the same three-layer model of human behaviour.

| Layer | Name | Contents |
|---|---|---|
| **A** | Survival | Food, sleep, safety, job security |
| **B** | Narrative | Identity, values, unwritten rules, belonging |
| **C** | Institution | Law, policy, KPIs, contracts |

**The Proximity Rule:** `Priority = Impact / Distance`
People prioritise immediate, visible pressure (Layer A/B) over distant formal rules (Layer C). Priority differences are structural responses — not personality flaws.

---

## GPTs implementation

Pre-configured GPTs for each persona:
→ https://chat.openai.com/g/sana-os *(update when live)*

---

## Worksheets

Five printable worksheets implementing SANA OS frameworks for non-technical users:
→ https://sana-os.org

---


## History

SANA has two lineages: the character-era SANA (v2.0, 2025–2026, archived at [sana-os/sana-character](https://github.com/sana-os/sana-character)) and SANA OS (v1.0–, this repository). See [`HISTORY.md`](HISTORY.md) for why the version number restarts at 1.0 and where the earlier files are. Changes are listed in [`CHANGELOG.md`](CHANGELOG.md).

---

## Contact

| Channel | Address |
|---|---|
| X (Twitter) | [@sanaosproject](https://x.com/sanaosproject) |
| General | contact@sana-os.org |
| Security | security@sana-os.org |

For licensing enquiries not covered by `LICENSE.md`, please use contact@sana-os.org.
For vulnerability reports or safety concerns related to SANA OS, please use security@sana-os.org.

## License

SANA OS License v1.0 — see `LICENSE.md`

- Commercial use permitted
- Attribution required: **"Powered by SANA OS"** + link to sana-os.org
- New personas and worksheet adaptations permitted
- **`core/Core_Principle.md` may not be modified**
- Use for manipulation or coercion is prohibited
