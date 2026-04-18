# Autonomy Decision Flow (Conceptual)

Autonomy decisions at ELION-SPACE follow a bounded flow:

1. Observe  
   Collect system, payload, and environment state.

2. Evaluate  
   Compare current state against predefined constraints
   and operational envelopes.

3. Decide  
   Select an allowed action or deferment strategy.

4. Act  
   Signal mission mode transitions or payload permissions.

5. Report  
   Log decisions and notify ground operators when appropriate.

This loop operates continuously and deterministically,
supporting explainable and verifiable autonomy behavior.
