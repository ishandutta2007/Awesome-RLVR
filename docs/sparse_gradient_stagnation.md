# The Sparse Gradient Stagnation Wall

Sparse gradients occur when binary rewards (0 or 1) result in almost all failures at the start of training, leaving the model with no optimization direction.

## How it Works
1. Bootstrapping with SFT (Supervised Fine-Tuning) initialization.
2. Training on high-quality pre-verified solutions ensures the base model can achieve a baseline success rate.
3. Enables RL optimization to proceed without flat plateaus.

## Mermaid Flow Diagram
```mermaid
flowchart TD
    Base[Base Model] -->|Poor Quality| ZeroReward[99.9% Zero Rewards - Stagnation]
    Base -->|1. SFT Bootstrapping| TrainedSFT[SFT Model]
    TrainedSFT -->|Some Successes| RL[RL Loop with Sparse Rewards]
    RL -->|Successful Gradients| Optimized[Aligned Reasoning Model]
```

[Back to README](../README.md)
