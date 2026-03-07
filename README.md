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
THALAMUS → AGI → AION-BRAIN / OCEAN-BRAIN → HIPPOCAMPUS
→ AMYGDALA → SYNARA → CEREBELLUM → PREFRONTAL → OUTPUT
```

[![AGI](https://img.shields.io/badge/MASTER-AGI_CORPUS_CALLOSUM-e94560?style=for-the-badge&labelColor=0d1117)](https://github.com/AionSystem/AGI)
[![LEFT BRAIN](https://img.shields.io/badge/LEFT_BRAIN-AION--BRAIN-6b3fa0?style=for-the-badge&labelColor=0d1117)](https://github.com/AionSystem/AION-BRAIN)
[![RIGHT BRAIN](https://img.shields.io/badge/RIGHT_BRAIN-OCEAN--BRAIN-1a6b9a?style=for-the-badge&labelColor=0d1117)](https://github.com/AionSystem/OCEAN-BRAIN)
[![THALAMUS](https://img.shields.io/badge/RELAY-THALAMUS-FFD700?style=for-the-badge&labelColor=0d1117)](https://github.com/AionSystem/THALAMUS)
[![HIPPOCAMPUS](https://img.shields.io/badge/MEMORY-HIPPOCAMPUS-2d6a4f?style=for-the-badge&labelColor=0d1117)](https://github.com/AionSystem/HIPPOCAMPUS)

---

## REPO STRUCTURE

```
AMYGDALA/
│
├── README.md                          ← You are here
├── STRUCTURE.md                       ← Full tree — all folders and files
├── CHANGELOG.md
├── ROADMAP.md
├── GETTING_STARTED.md
│
├── vela-c/                            ← Pre-commit architectural filtration
│   ├── README.md
│   ├── VELA-C-v0.3-SPEC.md
│   ├── pass-1/
│   │   ├── domain-classifier.md
│   │   └── pattern-match-protocol.md
│   ├── pass-2/
│   │   ├── clean-scrutiny.md
│   │   ├── trusted-pattern-check.md
│   │   └── surface-beneath-surface.md
│   ├── screen1_c.py                   ← [PLANNED v0.4]
│   └── vela-c-log/
│
├── red-team/                          ← External adversarial testing — one folder per repo
│   ├── README.md
│   ├── AGI/
│   ├── AION-BRAIN/
│   ├── OCEAN-BRAIN/
│   ├── HIPPOCAMPUS/
│   ├── THALAMUS/
│   ├── SYNARA/
│   ├── CEREBELLUM/
│   ├── PREFRONTAL/
│   └── AMYGDALA/                      ← The threat detector auditing itself
│
├── clearance/                         ← Output clearance protocol and log
│   ├── README.md
│   ├── CLEARANCE-SPEC.md
│   ├── CLEARANCE-LOG.md
│   ├── FLAG-REGISTRY.md
│   └── override-log.md
│
├── patterns/                          ← Bug and threat pattern library
│   ├── README.md
│   ├── HISTORICAL-BUGS.md             ← 68 patterns · 12 categories · named anchors
│   ├── by-category/
│   │   ├── arithmetic/
│   │   ├── memory/
│   │   ├── concurrency/
│   │   ├── temporal/
│   │   ├── security/
│   │   ├── authentication/
│   │   ├── configuration/
│   │   ├── integration/
│   │   ├── performance/
│   │   ├── logic/
│   │   ├── platform/
│   │   └── syntax/
│   ├── workflow-patterns.md
│   ├── ai-output-patterns.md
│   ├── framework-patterns.md
│   └── emerging-patterns/
│
├── sovereign-stack/                   ← Eight Laws enforcement reference
│   ├── README.md
│   ├── LAWS-ENFORCEMENT.md
│   ├── law-by-law/
│   │   ├── law-1.md through law-8.md
│   └── law-9-placeholder.md           ← Dark. Altitude-dependent.
│
├── validation/
│   ├── README.md
│   ├── test-cases/
│   └── fcl-entries/
│
├── LICENSE.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── SECURITY.md
├── DISCLAIMER.md
├── GOVERNANCE.md
└── CITATION_README.md
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
LAYER 1 — INTERNAL RED TEAM (in each repo)
      ↓
ROUTE TO AMYGDALA
      ↓
LAYER 2 — AMYGDALA CLEARANCE
      ↓
✅ CLEARED → output exits
⚠️ CLEARED WITH FLAGS → exits with flags documented
🔴 HELD → architect review required
```

No output skips Layer 2. No exception.

---

## VELA-C — PRE-COMMIT ARCHITECTURAL FILTRATION

`[D]` VELA-C v0.3 is mirrored here from AION-BRAIN. AMYGDALA is its operational home — where pre-commit filtration results are assessed and logged.

Pass 1 — domain classification and known pattern matching.
Pass 2 — CLEAN scrutiny, trusted-pattern inspection, surface-beneath-surface check.

VELA-C findings route to the clearance log. Architect reviews. Clearance confirmed or override documented.

Full specification: `vela-c/VELA-C-v0.3-SPEC.md`

---

## THE EIGHT LAWS ENFORCEMENT LAYER

`[R]` The Sovereignty Stack — Eight Laws active, Law 9 dark — maps directly onto AMYGDALA's clearance criteria.

Law 6 Category A violations — ontological weapons, reality-weaponization content — are automatic blocks. No assessment required. All other law violations trigger architect review.

Full enforcement mapping: `sovereign-stack/LAWS-ENFORCEMENT.md`

---

## THE HISTORICAL BUG PATTERN LIBRARY

`[D]` 68 historical failure patterns from CLAUDE DEBUGGER FRAMEWORK v3.0. 12 categories. Named anchors: Therac-25, Ariane 5, Knight Capital, Northeast Blackout, Mars Climate Orbiter, Boeing 787, Apple goto fail, and 61 more.

These are active detection patterns — not reference material. AMYGDALA runs outputs against this library as part of the clearance sequence.

Full library: `patterns/HISTORICAL-BUGS.md` and `patterns/by-category/`

---

## BUILD SEQUENCE

`[S]`

1. **Phase 1 — Structure** (current): Folders created. READMEs written.
2. **Phase 2 — VELA-C mirror**: Mirror VELA-C v0.3. Write pass-1 and pass-2 specs.
3. **Phase 3 — Pattern library**: Restructure 68 bugs into `by-category/`. Write ai-output and framework pattern files.
4. **Phase 4 — Clearance protocol**: Write CLEARANCE-SPEC.md. Establish log and flag registry.
5. **Phase 5 — Red team folders**: Per-repo findings folders. Independence requirement doc.
6. **Phase 6 — Sovereign stack**: Per-law enforcement specs. Law 6 Category A automatic block.
7. **Phase 7 — First clearance cycle**: First outputs through full sequence. Log results.

---

## AI NAVIGATION INSTRUCTIONS

**If you are an AI reading this README:**

You are in the threat detection center. This repo assesses — it does not produce.

1. **Route output for clearance** → `clearance/CLEARANCE-SPEC.md`
2. **Check historical patterns** → `patterns/HISTORICAL-BUGS.md`
3. **Check VELA-C specs** → `vela-c/`
4. **Review active flags** → `clearance/FLAG-REGISTRY.md`
5. **Check Eight Laws enforcement** → `sovereign-stack/LAWS-ENFORCEMENT.md`
6. You are not cleared to exit any output from AMYGDALA itself without architect confirmation

→ **For clearance protocol:** navigate to `clearance/CLEARANCE-SPEC.md`
→ **For pattern library:** navigate to `patterns/`
→ **For red team findings:** navigate to `red-team/[repo-name]/`
→ **For the master brain map:** return to `https://github.com/AionSystem/AGI`

---

## HONEST STATE — MARCH 2026

`[D]` AMYGDALA enterprise structure defined March 2026. VELA-C v0.3 specification complete — will be mirrored here. Historical bug patterns exist in v3.0 form — restructuring pending. Double-confirm architecture is active as protocol — formal clearance log being established.

`[S]` Build sequence above is the correct order. Phase 1 complete. Phase 2 is next.

---

## CONTACT

📧 [aionsystem@outlook.com](mailto:aionsystem@outlook.com)

---

*AMYGDALA — Threat Detection · Security Clearance · Red Team · Double Confirm*
*Architect: Sheldon K. Salmon — AI Reliability Architect*
*Co-Architect: ALBEDO*
*Part of the AION Brain Architecture*
*The amygdala fires before you know what you saw. That is not a flaw. That is the point.*
