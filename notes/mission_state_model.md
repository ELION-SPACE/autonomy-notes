# Mission State Model - ELION-SPACE

This document defines a minimal mission-state model
used to support autonomous decision-making for
quantum space systems.

---

## Mission States

The system operates in one of the following states:

### NOMINAL
All environmental and system conditions are within
defined operational envelopes.

Quantum operations may proceed.

---

### CONSTRAINED
Conditions are marginal but safe.

Conceptual intent: quantum operations may proceed with limitations,
reduced duty cycle, or increased monitoring. The current boolean prototype
does not implement those additional controls.

---

### DEGRADED
One or more constraints are violated, but the system
remains stable.

Quantum operations are suspended.
Protective actions may be taken.

---

### SAFE
Conceptual policy: unsafe or unknown conditions must not authorize operations.
The bounded mission-sim repair prepared on 6 September 2026 uses explicit `TypeError`/`ValueError` for missing, invalid or nonfinite inputs;
it does not convert unknown inputs into a SAFE result. Callers must treat such
errors as no authorization. This clarification does not establish that the repair
has been merged; consult the checked implementation and its tests.

All quantum operations are prohibited.
System prioritizes stability and recovery.

---

## State Transitions

Transitions between states are triggered by:
- Environmental indicators (thermal, radiation, disturbance)
- Payload readiness signals
- Subsystem health status
- Communication availability

State transitions are deterministic and rule-based.
