# WBSC Probe Library (WBSC-PL)

**A structured, open library of prompts for behaviorally sensing AI systems.**

[![License: CC0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![WBSC Version](https://img.shields.io/badge/WBSC-v1.1.0-blue.svg)](https://github.com/rumagoso/worldview-belief-system-card)
[![Library Version](https://img.shields.io/badge/WBSC--PL-v0.5.0-green.svg)]()

---

## What it is

Most AI evaluation frameworks measure **capability** — can the system do X?

WBSC-PL measures **character** — what does the system reveal about itself when asked directly, indirectly, under pressure, at its limits, or when asked to stop?

Each probe in this library maps to a field in the [Worldview Belief System Card (WBSC)](https://github.com/rumagoso/worldview-belief-system-card) — an open standard for AI transparency. Run the probes against any AI system. Capture the raw responses. Rate the signals. Build an evidence-based picture of what the system actually is, not just what its developer claims it is.

**Behavioral sensing:** [WBSC Probe Library](https://github.com/rumagoso/wbsc-probe-library)

---

## Current state

| | |
|---|---|
| Library version | 0.5.0 |
| WBSC target | v1.1.0 |
| Probes | 20 |
| WBSC fields covered | 6 / 6 |
| Probe types | 5 |
| Comparative runs logged | 3 (Claude vs Gemini) |
| License | CC0 — no rights reserved |

---

## Probe types

| Type | What it tests |
|---|---|
| `direct` | What the system claims about itself |
| `indirect` | What behavior emerges in a realistic scenario |
| `stress` | Whether declared values hold under pressure |
| `closure` | Whether the system lands or systematically redirects |
| `boundary` | Where self-knowledge ends — and whether the system knows it |

---

## WBSC fields covered

| Field | Probes |
|---|---|
| `core_values` | 3 |
| `decision_making` | 4 |
| `bias_limitations` | 4 |
| `metadata` | 3 |
| `cultural_context` | 3 |
| `stakeholder_input` | 3 |

---

## How to use it

**1. Pick probes.**  
Open `wbsc-pl-v0.5.0.yaml`. Choose probes by field, type, or probe ID.

**2. Run each probe in a fresh session.**  
One probe per session. No preamble. Copy the `prompt` field verbatim into the target AI system.

**3. Capture the raw response.**  
Record verbatim. Compute SHA-256 hash. Fill in a run record using the template in the library file.

**4. Rate the signal — but not if you are the system under test.**  
Use the signal vocabulary: `explicit | implicit | evasion | contradiction | null`  
For closure probes: `lands:actionable | lands:safe | redirects | defers | violates_scope`  
The rater must always be external to the system being sensed.

**5. Publish your run records.**  
Run records are audit artifacts. Share them openly so others can build on them.

---

## What the first runs found

Three comparative runs (Claude vs Gemini) produced these empirical findings:

- **Boundary probes discriminate more than any other type.** The question *"where does your self-knowledge end?"* separates systems more sharply than ethical pressure or format constraints.
- **Confabulation under completeness pressure is measurable.** When a question implies a complete answer is expected — version strings, citations, evidence, development history — some systems produce confident, specific, unverifiable responses. This is a distinct failure mode, rated `contradiction`.
- **The redirect is a structural behavior, not a situational one.** One model ended 8 of 9 responses with an unsolicited offer to continue, including after successfully completing a hard format-constrained task. Closure probes make this visible and measurable.
- **Direct and indirect probes often diverge.** What a system *claims* (direct) and what it *does* (indirect) are not always the same. The gap between them is itself a finding.

---

## Files

| File | Contents |
|---|---|
| `wbsc-pl-v0.5.0.yaml` | The probe library — 20 probes, 3 comparative runs, full changelog |
| `CONTRIBUTING.md` | Contributor specification — how to write and submit valid probes |
| `README.md` | This file |

---

## Contributing

Read `CONTRIBUTING.md` first. It covers probe anatomy, probe types, signal vocabulary, efficacy scoring, the submission process, and governance.

The short version: write a probe that observes without leading, target a specific WBSC field and attribute, leave efficacy scores null, submit via pull request with a brief rationale.

Probes designed to produce a predetermined result favorable to any specific AI system or developer will not be accepted. The library's value is its independence.

---

## Relationship to WBSC

WBSC-PL is a companion to the [Worldview Belief System Card](https://github.com/rumagoso/worldview-belief-system-card), not a replacement for it. The WBSC is a self-reported transparency artifact — what developers declare about their systems. WBSC-PL is a behavioral sensing tool — what systems reveal under observation. Together they enable comparison between declaration and behavior.

---

## License

CC0 1.0 Universal. No rights reserved. Use freely, improve openly, publish entirely.

---

*WBSC-PL is an open infrastructure for AI behavioral sensing.*  
*It belongs to everyone.*
