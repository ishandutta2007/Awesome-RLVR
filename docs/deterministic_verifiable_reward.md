# Deterministic Verifiable Reward Era (RLVR)

Reinforcement Learning with Verifiable Rewards (RLVR) substitutes neural reward models with deterministic, programmatic verifiers.

## How it Works
1. Model generates answers containing formal statements or code.
2. An absolute verifier (compiler, REPL, or theorem checker) executes and verifies correctness.
3. Policy is optimized directly on binary/fractional verification outcomes.

## Mermaid Flow Diagram
```mermaid
flowchart TD
    Prompt[Prompt] --> Policy[Reasoning LLM]
    Policy --> Reasoning[Reasoning Chain & Answer]
    Reasoning --> Verifier[Programmatic Sandbox / Compiler]
    Verifier -->|Binary Correctness Reward 0/1| RL[RL Optimizer e.g. GRPO]
    RL -->|Update| Policy
```

[Back to README](../README.md)
