# Hybrid Soft-Hard Reward Systems

Combining neural reward models (soft) and deterministic verifiers (hard) to optimize policies.

## How it Works
1. Soft reward models grade stylistic qualities (e.g. comment quality, readability).
2. Hard verifiers check functional correctness (compilation, correctness).
3. Combined reward optimizes both functional validity and styling.

## Mermaid Flow Diagram
```mermaid
flowchart TD
    Model[LLM Policy] --> Output[Code / Response]
    Output --> SoftRM[Neural Reward Model: Style, Readability]
    Output --> HardVerifier[Deterministic Sandbox: Functionality]
    SoftRM --> CombinedReward[Combined Weighted Reward]
    HardVerifier --> CombinedReward
    CombinedReward --> Optimize[RL Step]
```

[Back to README](../README.md)
