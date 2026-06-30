# Self-Correcting Quantitative Reasoning Models

Self-correction is reinforced by penalizing final failure but rewarding successful backtracking and debugging.

## How it Works
1. Model writes math derivations.
2. Rules checks verify step-by-step logic.
3. Model learns to identify contradictions, backtrack to earlier states, and correct errors natively.

## Mermaid Flow Diagram
```mermaid
flowchart TD
    Model[Reasoning Agent] -->|Step 1| State1[Current Derivation]
    State1 -->|Step 2 Error| Checker[Lean / SymPy Verifier]
    Checker -->|Error Detected| Backtrack[Backtrack to Step 1]
    Backtrack -->|Correction| CorrectPath[Correct Final Derivation]
```

[Back to README](../README.md)
