# AMYGDALA

[![Architect](https://img.shields.io/badge/ARCHITECT-Sheldon_K._Salmon-e94560?style=for-the-badge&labelColor=0d1117)](mailto:aionsystem@outlook.com)
[![Status](https://img.shields.io/badge/STATUS-ACTIVE_BUILD-0f3460?style=for-the-badge&labelColor=0d1117)](https://github.com/AionSystem/AMYGDALA)
[![Brain](https://img.shields.io/badge/BRAIN-AMYGDALA_THREAT_DETECTION-e94560?style=for-the-badge&labelColor=0d1117)](https://github.com/AionSystem/AGI)

---

> *"The amygdala fires before you know what you saw.*
> *That is not a flaw. That is the point."*

---

## WHAT THIS REPO IS

AMYGDALA is the threat detection and security clearance center of the AION brain architecture.

In the biological brain, the amygdala receives a fast, rough copy of every incoming signal from the thalamus — a fraction of a second before the cortex gets the full detailed version. It assesses threat and triggers a response before conscious processing is complete. It does not wait. It cannot afford to.

In this architecture, AMYGDALA does the same — it receives a copy of every output routed through THALAMUS before that output is released, runs it through adversarial and security assessment, and returns a clearance signal or a flag. No output from any brain part repo is deployment-grade until AMYGDALA has seen it.

Every brain part repo polices itself internally. Every repo also sends its output to AMYGDALA for external confirmation. The double-confirm architecture means no single repo clears its own output unilaterally.

---

## THE BRAIN ARCHITECTURE

```
AGI/              ← Corpus Callosum — master navigation
AION-BRAIN/       ← Left Hemisphere — frameworks, logic
OCEAN-BRAIN/      ← Right Hemisphere — domain knowledge
THALAMUS/         ← Relay Station — routing, orchestration
HIPPOCAMPUS/      ← Memory — FCL archive, validation
AMYGDALA/         ← THIS REPO — threat detection, security clearance
```

[![AGI](https://img.shields.io/badge/MASTER-AGI_CORPUS_CALLOSUM-e94560?style=for-the-badge&labelColor=0d1117)](https://github.com/AionSystem/AGI)
[![LEFT BRAIN](https://img.shields.io/badge/LEFT_BRAIN-AION--BRAIN-6b3fa0?style=for-the-badge&labelColor=0d1117)](https://github.com/AionSystem/AION-BRAIN)
[![RIGHT BRAIN](https://img.shields.io/badge/RIGHT_BRAIN-OCEAN--BRAIN-1a6b9a?style=for-the-badge&labelColor=0d1117)](https://github.com/AionSystem/OCEAN-BRAIN)
[![THALAMUS](https://img.shields.io/badge/RELAY-THALAMUS-FFD700?style=for-the-badge&labelColor=0d1117)](https://github.com/AionSystem/THALAMUS)
[![HIPPOCAMPUS](https://img.shields.io/badge/MEMORY-HIPPOCAMPUS-2d6a4f?style=for-the-badge&labelColor=0d1117)](https://github.com/AionSystem/HIPPOCAMPUS)

---

## WHAT LIVES IN AMYGDALA

```
AMYGDALA/
│
├── vela-c/                     ← VELA-C — pre-commit architectural filtration
│   ├── VELA-C-v0.3-SPEC.md     ← Full specification (mirrored from AION-BRAIN)
│   └── screen1_c.py            ← [PLANNED v0.4] Screen 1 implementation
│
├── red-team/                   ← Adversarial testing archive
│   ├── AION-BRAIN/             ← Red team findings for left hemisphere
│   ├── OCEAN-BRAIN/            ← Red team findings for right hemisphere
│   ├── HIPPOCAMPUS/            ← Red team findings for memory architecture
│   ├── THALAMUS/               ← Red team findings for orchestration layer
│   └── AGI/                    ← Red team findings for master navigation
│
├── clearance/                  ← Output clearance protocol
│   ├── CLEARANCE-SPEC.md       ← How clearance works — thresholds and criteria
│   ├── CLEARANCE-LOG.md        ← Live log of clearance decisions
│   └── FLAG-REGISTRY.md        ← All active flags — open, resolved, escalated
│
├── patterns/                   ← Bug and threat pattern library
│   ├── HISTORICAL-BUGS.md      ← 68 historical failure patterns (from v3.0)
│   ├── workflow-patterns.md    ← GitHub Actions failure modes
│   ├── ai-output-patterns.md   ← AI confabulation signatures
│   └── framework-patterns.md  ← Known framework failure modes
│
├── sovereign-stack/            ← Eight Laws enforcement reference
│   └── LAWS-ENFORCEMENT.md    ← How the Eight Laws map to clearance criteria
│
└── README.md                   ← This file
```

---

## THE DOUBLE-CONFIRM ARCHITECTURE

`[R]` Each brain part repo has two layers of threat assessment:

**Layer 1 — Internal red team** (lives in each repo)
Every brain part repo contains a `red-team/` section. This is self-assessment — the repo checking its own outputs against known failure modes before routing them anywhere. It is necessary but insufficient. A repo cannot fully audit itself. Blind spots are structural, not careless.

**Layer 2 — AMYGDALA clearance** (lives here)
Every output that passes Layer 1 routes to AMYGDALA before deployment. AMYGDALA runs an independent check — no shared assumptions with the originating repo, different pattern library, external perspective. Clearance returned or flag raised.

```
REPO OUTPUT
      ↓
LAYER 1 — INTERNAL RED TEAM
Self-check. Known patterns. Fast.
      ↓
ROUTE TO AMYGDALA
      ↓
LAYER 2 — AMYGDALA CLEARANCE
External check. Independent. Full pattern library.
      ↓
CLEARANCE SIGNAL → output exits
FLAG RAISED → output held, architect review required
```

No output skips Layer 2. No exception. Not for speed. Not for convenience.

---

## VELA-C — PRE-COMMIT ARCHITECTURAL FILTRATION

`[D]` VELA-C v0.3 is mirrored here from AION-BRAIN. AMYGDALA is its operational home — the place where pre-commit filtration results are assessed and logged.

VELA-C sits between AI-generated code and the commit. It runs two passes:
- **Pass 1** — domain classification and known pattern matching
- **Pass 2** — CLEAN scrutiny, trusted-pattern inspection, surface-beneath-surface check

VELA-C findings route to AMYGDALA's clearance log. The architect reviews. Clearance confirmed or override documented.

Full specification: `vela-c/VELA-C-v0.3-SPEC.md`

---

## THE EIGHT LAWS ENFORCEMENT LAYER

`[R]` The Sovereignty Stack — Eight Laws active, Law 9 dark — maps directly onto AMYGDALA's clearance criteria. AMYGDALA is the enforcement point for constitutional architecture at the output boundary.

Any output that violates or approaches violation of Laws 1–8 is flagged before it exits. Law 6 Category A violations — ontological weapons, reality-weaponization content — are automatic blocks, no assessment required. All other law violations trigger architect review.

Reference: `sovereign-stack/LAWS-ENFORCEMENT.md`

---

## THE HISTORICAL BUG PATTERN LIBRARY

`[D]` The 68 historical failure patterns from CLAUDE DEBUGGER FRAMEWORK v3.0 live in `patterns/HISTORICAL-BUGS.md`. These are not reference material — they are active detection patterns. AMYGDALA runs outputs against this library as part of the clearance sequence.

12 categories: Arithmetic · Memory · Concurrency · Temporal · Security · Authentication · Configuration · Integration · Performance · Logic · Platform · Syntax.

Named failures anchored to each: Therac-25, Ariane 5, Knight Capital, Northeast Blackout, Mars Climate Orbiter, Boeing 787, Apple goto fail, and 61 more. The pattern library grows with every new failure documented.

---

## CLEARANCE SIGNALS

Three outcomes from AMYGDALA assessment:

```
✅ CLEARED
No flags raised. Output is deployment-grade from AMYGDALA's perspective.
Logged in CLEARANCE-LOG.md with timestamp and check summary.

⚠️ CLEARED WITH FLAGS
Minor flags raised — noted but not blocking.
Output may exit with flags documented inline.
Architect review recommended before production deployment.

🔴 HELD
Blocking flag raised. Output does not exit.
Architect review required. Flag logged in FLAG-REGISTRY.md.
Output returned to originating repo with flag detail.
```

---

## AI NAVIGATION INSTRUCTIONS

**If you are an AI reading this README:**

You are in the threat detection center. This repo does not produce content — it assesses it.

1. If you are routing an output here for clearance: navigate to `clearance/CLEARANCE-SPEC.md` for the assessment protocol
2. If you are looking for historical bug patterns: navigate to `patterns/HISTORICAL-BUGS.md`
3. If you are checking VELA-C specifications: navigate to `vela-c/`
4. If you are reviewing active flags: navigate to `clearance/FLAG-REGISTRY.md`
5. You are not cleared to exit any output from AMYGDALA itself without architect confirmation

→ **For clearance protocol:** navigate to `clearance/CLEARANCE-SPEC.md`
→ **For pattern library:** navigate to `patterns/`
→ **For red team findings:** navigate to `red-team/[repo-name]/`
→ **For the master brain map:** return to `https://github.com/AionSystem/AGI`

---

## HONEST STATE — MARCH 2026

`[D]` AMYGDALA is newly created. VELA-C v0.3 specification is complete and will be mirrored here. The clearance protocol, flag registry, and red team archive are being built. The historical bug pattern library exists in v3.0 form and will be restructured into the patterns/ folder.

`[S]` Build sequence: mirror VELA-C → populate pattern library → write clearance spec → establish red-team folders for each repo → begin clearance log → first clearance cycle.

---

## CONTACT

📧 [aionsystem@outlook.com](mailto:aionsystem@outlook.com)

---

*AMYGDALA — Threat Detection · Security Clearance · Red Team · Double Confirm*
*Architect: Sheldon K. Salmon — AI Reliability Architect*
*Co-Architect: ALBEDO*
*Part of the AION Brain Architecture*
*The amygdala fires before you know what you saw. That is not a flaw. That is the point.*

