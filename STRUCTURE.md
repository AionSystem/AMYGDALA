# AMYGDALA — FOLDER STRUCTURE
## Enterprise-Grade AAA Tree | Threat Detection and Security Clearance
### Version: v0.2 | March 2026
### Note: anomaly/, calibration/, immutable-log/ are existing folders — preserved as-is

---

```
AMYGDALA/
│
├── README.md                          ← Master navigation — you are here
├── GRATITUDE.md                       ← Acknowledgments (existing)
├── STRUCTURE.md                       ← This file — full tree
├── CHANGELOG.md
├── ROADMAP.md
├── GETTING_STARTED.md
│
│
│   ─────────── CORE DETECTION SYSTEMS (EXISTING) ───────────
│
│
├── anomaly/                           ← Anomaly detection archive ← EXISTING
│   ├── README.md
│   ├── ANOMALY-SPEC.md                ← What constitutes an anomaly vs a known pattern
│   │                                     Anomaly: not in pattern library, not expected.
│   │                                     Detection threshold. Escalation criteria.
│   │                                     Anomalies log here — patterns log in patterns/
│   │
│   ├── active/                        ← Anomalies currently under investigation
│   │   └── [ANOMALY-ID.md]
│   │
│   ├── resolved/                      ← Anomalies resolved — with resolution record
│   │   └── [ANOMALY-ID.md]
│   │
│   └── promoted/                      ← Anomalies that became patterns
│       └── [ANOMALY-ID.md]            ← When an anomaly recurs — it earns a pattern entry
│                                         Promotion path: anomaly → emerging-pattern → pattern
│
│
├── calibration/                       ← Clearance threshold calibration ← EXISTING
│   ├── README.md
│   ├── CALIBRATION-SPEC.md            ← How clearance thresholds are set and adjusted
│   │                                     What earns CLEARED vs CLEARED WITH FLAGS vs HELD.
│   │                                     Threshold tuning protocol.
│   │                                     Over-sensitive vs under-sensitive detection.
│   │
│   ├── threshold-history.md           ← Every threshold change — dated, reasoned
│   │                                     Why the threshold moved. What triggered it.
│   │                                     Never silent. Never undocumented.
│   │
│   ├── false-positive-log.md          ← Outputs incorrectly flagged
│   │                                     Logged and used to recalibrate.
│   │                                     False positives are not errors to hide —
│   │                                     they are calibration data.
│   │
│   └── false-negative-log.md          ← Outputs incorrectly cleared
│                                         The more important failure mode.
│                                         Logged with full post-incident analysis.
│
│
├── immutable-log/                     ← Permanent clearance record ← EXISTING
│   ├── README.md                      ← Why immutability matters
│   │                                     The clearance log cannot be edited retroactively.
│   │                                     Every clearance decision is permanent record.
│   │                                     Overrides are additions — not replacements.
│   │
│   ├── clearance-log/                 ← Every clearance decision, timestamped
│   │   └── [YYYY-MM-DD-clearance.md]
│   │
│   ├── flag-registry/                 ← All flags — open, resolved, escalated
│   │   └── [FLAG-ID.md]
│   │
│   ├── override-log/                  ← Architect overrides — dated, reasoned, signed
│   │   └── [OVERRIDE-ID.md]           ← Overrides are legitimate. Silent overrides are not.
│   │
│   └── incident-log/                  ← Post-incident records — when clearance failed
│       └── [INCIDENT-ID.md]           ← What got through that shouldn't have.
│                                         Full analysis. Calibration trigger.
│
│
│   ─────────── VELA-C ───────────
│
│
├── vela-c/                            ← Pre-commit architectural filtration
│   ├── README.md
│   ├── VELA-C-v0.3-SPEC.md            ← Mirrored from AION-BRAIN
│   │                                     Pass 1: domain classification + pattern matching.
│   │                                     Pass 2: CLEAN scrutiny + surface-beneath-surface.
│   │
│   ├── pass-1/
│   │   ├── domain-classifier.md
│   │   └── pattern-match-protocol.md
│   │
│   ├── pass-2/
│   │   ├── clean-scrutiny.md
│   │   ├── trusted-pattern-check.md
│   │   └── surface-beneath-surface.md
│   │
│   ├── screen1_c.py                   ← [PLANNED v0.4]
│   └── vela-c-log/
│
│
│   ─────────── RED TEAM ARCHIVE ───────────
│
│
├── red-team/                          ← External adversarial testing — one folder per repo
│   ├── README.md
│   ├── AGI/
│   ├── AION-BRAIN/
│   ├── OCEAN-BRAIN/
│   ├── HIPPOCAMPUS/
│   │   └── findings/
│   │       └── false-memory-checks/
│   ├── THALAMUS/
│   ├── SYNARA/
│   ├── CEREBELLUM/
│   ├── PREFRONTAL/
│   └── AMYGDALA/                      ← The threat detector auditing itself
│
│
│   ─────────── PATTERN LIBRARY ───────────
│
│
├── patterns/                          ← Known bug and threat pattern library
│   ├── README.md
│   ├── HISTORICAL-BUGS.md             ← 68 patterns · 12 categories · named anchors
│   │
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
│   │
│   ├── workflow-patterns.md
│   ├── ai-output-patterns.md
│   ├── framework-patterns.md
│   └── emerging-patterns/             ← New patterns under observation before promotion
│       └── [PATTERN-ID.md]            ← Promotion path: anomaly/ → here → by-category/
│
│
│   ─────────── CLEARANCE ───────────
│
│
├── clearance/                         ← Clearance protocol specification
│   ├── README.md
│   ├── CLEARANCE-SPEC.md              ← Full clearance protocol
│   │                                     Three outcomes: CLEARED / CLEARED WITH FLAGS / HELD
│   │                                     Thresholds set in calibration/
│   │                                     Decisions logged in immutable-log/
│   │
│   └── double-confirm-protocol.md     ← Layer 1 (internal) + Layer 2 (AMYGDALA) spec
│                                         No output clears unilaterally.
│                                         Independence requirement documented here.
│
│
│   ─────────── SOVEREIGN STACK ───────────
│
│
├── sovereign-stack/                   ← Eight Laws enforcement reference
│   ├── README.md
│   ├── LAWS-ENFORCEMENT.md
│   ├── law-by-law/
│   │   ├── law-1.md
│   │   ├── law-2.md
│   │   ├── law-3.md
│   │   ├── law-4.md
│   │   ├── law-5.md
│   │   ├── law-6.md                   ← Category A: automatic block
│   │   ├── law-7.md
│   │   └── law-8.md
│   └── law-9-placeholder.md           ← Dark. Altitude-dependent. Stack declares its boundary.
│
│
│   ─────────── VALIDATION ───────────
│
│
├── validation/
│   ├── README.md
│   ├── test-cases/
│   └── fcl-entries/
│
│
│   ─────────── GOVERNANCE & LEGAL ───────────
│
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

## KEY ARCHITECTURE DECISIONS — WHY THESE THREE FOLDERS

**`anomaly/`** — distinct from `patterns/`. Known failure modes live in `patterns/`. Unknown signals that don't match anything live in `anomaly/`. The promotion path makes the distinction meaningful: anomaly → emerging-pattern → confirmed pattern. That path is auditable.

**`calibration/`** — thresholds are not static. A detection system that can't recalibrate becomes either paranoid or blind. False positive and false negative logs feed directly back into threshold adjustment. Every threshold change is dated and reasoned — never silent.

**`immutable-log/`** — this is the most architecturally significant of the three. The clearance log cannot be retroactively edited. Overrides are additions, not replacements. An incident that got through leaves a permanent record and triggers calibration. This is the integrity guarantee of the entire clearance layer.

---

## PROMOTION PATH

```
Unknown signal detected
        ↓
anomaly/active/                ← Filed. Under investigation.
        ↓
Recurs or confirmed as real
        ↓
patterns/emerging-patterns/    ← Named. Pattern forming.
        ↓
Meets threshold — multiple confirmed instances
        ↓
patterns/by-category/          ← Permanent named pattern. Active detection.
```

---

## BUILD SEQUENCE

`[S]`

1. **Phase 1 — Structure** (current): Existing folders preserved. New folders mapped around them.
2. **Phase 2 — VELA-C mirror**: Mirror VELA-C v0.3. Pass-1 and pass-2 specs written.
3. **Phase 3 — Pattern library**: Restructure 68 bugs into `by-category/`.
4. **Phase 4 — Clearance protocol**: CLEARANCE-SPEC.md. Double-confirm protocol.
5. **Phase 5 — Calibration docs**: CALIBRATION-SPEC.md. Threshold history initialized.
6. **Phase 6 — Immutable log structure**: clearance-log, flag-registry, override-log, incident-log initialized with README.
7. **Phase 7 — Anomaly spec**: ANOMALY-SPEC.md. Promotion path documented.
8. **Phase 8 — Red team folders**: Per-repo findings folders.
9. **Phase 9 — Sovereign stack**: Per-law specs. Law 6 Category A automatic block.

---

## DDL FIELD

```
Document: AMYGDALA STRUCTURE v0.2
Architect: Sheldon K. Salmon
AI Co-Architect: ALBEDO
Date: March 2026
Status: Structure defined incorporating existing folders.
Existing: .github/ · anomaly/ · calibration/ · immutable-log/ · GRATITUDE.md · README.md
Convergence: M-NASCENT
Note: Existing folder names preserved exactly.
      Architecture built around them — not over them.
      immutable-log/ is the integrity guarantee of the clearance layer.
```

---

*AMYGDALA STRUCTURE v0.2 — Threat Detection and Security Clearance*
*Sheldon K. Salmon & ALBEDO — March 2026*
*The amygdala fires before you know what you saw. That is not a flaw. That is the point.*
