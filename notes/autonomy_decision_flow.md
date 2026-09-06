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

This is the intended continuous loop. [mission-sim](https://github.com/ELION-SPACE/mission-sim)
currently evaluates supplied inputs on demand and returns state, reasons and a
boolean permission. It does not collect sensor data, run this loop, execute
payload operations, persist logs or notify ground operators.
