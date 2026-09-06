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
  Conceptually permitted with limitations. The implemented boolean gate permits
  them but does not enforce scheduling, duty-cycle or monitoring limits.

- DEGRADED  
  Quantum operations prohibited.  
  Support and protective actions only.

- SAFE  
  All non-protective actions prohibited.

---

## Rationale

Explicit action gating makes the permission rule auditable. Reducing accidental
payload damage and enabling safe future integration are objectives, not validated
capabilities. [The current gate](https://github.com/ELION-SPACE/mission-sim/blob/main/src/action_gating.py)
only returns a boolean for quantum operations; support/protective categories and
execution are conceptual.

Autonomy decides *whether* an action is allowed,
not *how* it is executed.
