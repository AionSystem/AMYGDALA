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
├── GRATITUDE.md                       ← Acknowledgments
├── STRUCTURE.md                       ← Full tree — all folders and files
├── CHANGELOG.md
├── ROADMAP.md
├── GETTING_STARTED.md
│
│   ── Core Detection Systems ──
│
├── anomaly/                           ← Unknown signal archive
│   ├── README.md
│   ├── ANOMALY-SPEC.md
│   ├── active/                        ← Under investigation
│   ├── resolved/                      ← Closed with resolution record
│   └── promoted/                      ← Became a named pattern
│
├── calibration/                       ← Threshold calibration and feedback
│   ├── README.md
│   ├── CALIBRATION-SPEC.md
│   ├── threshold-history.md
│   ├── false-positive-log.md
│   └── false-negative-log.md
│
├── immutable-log/                     ← Permanent clearance record
│   ├── README.md
│   ├── clearance-log/
│   ├── flag-registry/
│   ├── override-log/
│   └── incident-log/
│
│   ── Detection Infrastructure ──
│
├── vela-c/                            ← Pre-commit architectural filtration
│   ├── README.md
│   ├── VELA-C-v0.3-SPEC.md
│   ├── pass-1/
│   ├── pass-2/
│   ├── screen1_c.py                   ← [PLANNED v0.4]
│   └── vela-c-log/
│
├── patterns/                          ← Known bug and threat pattern library
│   ├── README.md
│   ├── HISTORICAL-BUGS.md             ← 68 patterns · 12 categories · named anchors
│   ├── by-category/                   ← arithmetic · memory · concurrency · temporal ·
│   │                                     security · authentication · configuration ·
│   │                                     integration · performance · logic · platform · syntax
│   ├── workflow-patterns.md
│   ├── ai-output-patterns.md
│   ├── framework-patterns.md
│   └── emerging-patterns/             ← Anomalies that recurred — not yet confirmed
│
│   ── Clearance and Red Team ──
│
├── clearance/
│   ├── README.md
│   ├── CLEARANCE-SPEC.md
│   └── double-confirm-protocol.md
│
├── red-team/                          ← External adversarial testing
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
│   ── Sovereign Stack ──
│
├── sovereign-stack/
│   ├── README.md
│   ├── LAWS-ENFORCEMENT.md
│   ├── law-by-law/
│   └── law-9-placeholder.md           ← Dark. Altitude-dependent.
│
├── validation/
│   ├── README.md
│   ├── test-cases/
│   └── fcl-entries/
│
│   ── Governance & Legal ──
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

## THE THREE CORE SYSTEMS

**`anomaly/`** — Unknown signal archive. A signal that doesn't match anything in the pattern library lands here, not in patterns. The promotion path is what makes the distinction meaningful: `anomaly/active` → `patterns/emerging-patterns` → `patterns/by-category`. Every stage auditable. Nothing promoted without recurrence.

**`calibration/`** — Threshold calibration and feedback loop. False positives and false negatives both log here and both feed back into threshold adjustment. Every threshold change is dated and reasoned — never silent. A detection system that cannot recalibrate goes blind or paranoid.

**`immutable-log/`** — The integrity guarantee of the entire clearance layer. The clearance record cannot be retroactively edited. Overrides are additions, not replacements. An incident that got through leaves a permanent record and triggers calibration. This is what makes AMYGDALA auditable rather than just operational.

---

## THE DOUBLE-CONFIRM ARCHITECTURE

`[R]` Each brain part repo has two layers of threat assessment:

**Layer 1 — Internal red team** (lives in each repo): self-assessment against known failure modes. Necessary but insufficient — a repo cannot fully audit itself.

**Layer 2 — AMYGDALA clearance** (lives here): independent check with no shared assumptions, different pattern library, external perspective.

```
REPO OUTPUT
      ↓
LAYER 1 — INTERNAL RED TEAM
      ↓
ROUTE TO AMYGDALA
      ↓
LAYER 2 — AMYGDALA CLEARANCE
      ↓
✅ CLEARED → logged in immutable-log/ · output exits
⚠️ CLEARED WITH FLAGS → logged · exits with flags documented
🔴 HELD → logged · architect review required · override possible
```

No output skips Layer 2. No exception. Override is legitimate — silent override is not.

---

## PROMOTION PATH — UNKNOWN TO KNOWN

```
Unknown signal detected
        ↓
anomaly/active/
        ↓
Recurs or confirmed as real
        ↓
patterns/emerging-patterns/
        ↓
Multiple confirmed instances — threshold met
        ↓
patterns/by-category/          ← Permanent named pattern. Active detection.
```

---

## VELA-C — PRE-COMMIT ARCHITECTURAL FILTRATION

`[D]` VELA-C v0.3 mirrored here from AION-BRAIN. AMYGDALA is its operational home.

Pass 1 — domain classification and known pattern matching.
Pass 2 — CLEAN scrutiny, trusted-pattern inspection, surface-beneath-surface check.

Findings route to `immutable-log/`. Architect reviews. Clearance confirmed or override documented.

Full specification: `vela-c/VELA-C-v0.3-SPEC.md`

---

## THE EIGHT LAWS ENFORCEMENT LAYER

`[R]` The Sovereignty Stack — Eight Laws active, Law 9 dark — maps onto AMYGDALA's clearance criteria.

Law 6 Category A violations: automatic block, no assessment required.
All other law violations: architect review.

Full enforcement mapping: `sovereign-stack/LAWS-ENFORCEMENT.md`

---

## BUILD SEQUENCE

`[S]`

1. **Phase 1 — Structure** (current): Existing folders preserved. New folders mapped around them.
2. **Phase 2 — VELA-C mirror**: VELA-C v0.3 spec mirrored. Pass specs written.
3. **Phase 3 — Pattern library**: 68 bugs restructured into `by-category/`.
4. **Phase 4 — Clearance spec**: CLEARANCE-SPEC.md and double-confirm protocol.
5. **Phase 5 — Calibration docs**: CALIBRATION-SPEC.md. Threshold history initialized.
6. **Phase 6 — Anomaly spec**: ANOMALY-SPEC.md. Promotion path documented.
7. **Phase 7 — Red team folders**: Per-repo findings folders.
8. **Phase 8 — Sovereign stack**: Per-law enforcement specs.
9. **Phase 9 — First clearance cycle**: First outputs through full sequence. Logged.

---

## AI NAVIGATION INSTRUCTIONS

**If you are an AI reading this README:**

1. **Route output for clearance** → `clearance/CLEARANCE-SPEC.md`
2. **Check historical patterns** → `patterns/HISTORICAL-BUGS.md`
3. **File an anomaly** → `anomaly/active/`
4. **Review active flags** → `immutable-log/flag-registry/`
5. **Check Eight Laws enforcement** → `sovereign-stack/LAWS-ENFORCEMENT.md`
6. You are not cleared to exit any output from AMYGDALA itself without architect confirmation

→ **For clearance protocol:** navigate to `clearance/CLEARANCE-SPEC.md`
→ **For pattern library:** navigate to `patterns/`
→ **For anomaly filing:** navigate to `anomaly/`
→ **For the master brain map:** return to `https://github.com/AionSystem/AGI`

---

## HONEST STATE — MARCH 2026

`[D]` AMYGDALA enterprise structure defined March 2026 incorporating existing folders: `anomaly/`, `calibration/`, `immutable-log/`. VELA-C v0.3 specification complete — will be mirrored here. Historical bug patterns in v3.0 form — restructuring pending. `immutable-log/` is the integrity foundation of the clearance layer.

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
