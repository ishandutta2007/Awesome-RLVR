# Process-Verifiable Rewards (PVR)

PVR interleaves programmatic validation checks throughout the entire generation sequence.

## How it Works
1. Model generates intermediate steps.
2. Fast checking subroutines verify each step (e.g., intermediate tool executions, compiler passes).
3. The reward is dynamically generated step-by-step.

## Mermaid Flow Diagram
```mermaid
flowchart TD
    Start[Start Prompt] --> Step1[Step 1]
    Step1 --> Check1[Verify Step 1]
    Check1 -->|Pass| Step2[Step 2]
    Check1 -->|Fail| Penalty[Abort / Penalize]
    Step2 --> Check2[Verify Step 2]
```

[Back to README](../README.md)
