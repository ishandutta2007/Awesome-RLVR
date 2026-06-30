# Interactive Theorem Provers (Formal Math RLVR)

Using formal verification engines to check mathematical statements and proofs step-by-step.

## How it Works
1. The model outputs proofs in a formal language (e.g. Lean 4, Isabelle, Coq).
2. The theorem prover checks every step for logical validity.
3. Rewards are only given for complete, verified proofs.

## Mermaid Flow Diagram
```mermaid
flowchart TD
    Model[Theorem Prover Agent] -->|Formal Proof Code| ITP[Lean 4 / Coq Compiler]
    ITP -->|Verification Check| Kernel[Proof Assistant Kernel]
    Kernel -->|Unbroken Proof Loop| Reward[1.0 Reward]
    Kernel -->|Syntax / Logic Error| Fail[0.0 Reward]
```

[Back to README](../README.md)
