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

Quantum operations may proceed with limitations,
reduced duty cycle, or increased monitoring.

---

### DEGRADED
One or more constraints are violated, but the system
remains stable.

Quantum operations are suspended.
Protective actions may be taken.

---

### SAFE
Conditions are unsafe or unknown.

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
