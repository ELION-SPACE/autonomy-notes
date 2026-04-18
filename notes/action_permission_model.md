# Action Permission Model - ELION-SPACE

Mission autonomy must not only evaluate system state,
but also explicitly control which actions are permitted.

In quantum space systems, prohibiting actions is often
more important than executing them.

---

## Action Categories

For Phase 0.2, actions are abstracted into categories:

- Quantum operations (computation, communication, sensing)
- Support operations (calibration, synchronization)
- Protective actions (safe mode transitions)
- Deferred actions (postponed until conditions improve)

ELION-SPACE autonomy governs permission, not execution.

---

## Permission Logic

Action permission is derived from the current mission state:

- NOMINAL  
  Quantum operations permitted.

- CONSTRAINED  
  Quantum operations permitted with limitations.

- DEGRADED  
  Quantum operations prohibited.  
  Support and protective actions only.

- SAFE  
  All non-protective actions prohibited.

---

## Rationale

Explicit action gating:
- Prevents accidental payload damage
- Makes autonomy behavior auditable
- Allows safe integration with future control systems

Autonomy decides *whether* an action is allowed,
not *how* it is executed.
