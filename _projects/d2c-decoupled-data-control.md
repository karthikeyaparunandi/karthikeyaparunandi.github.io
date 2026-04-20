---
name: D2C — Decoupled Data-Based Control
tools: [Reinforcement Learning, Python, Nonlinear Systems, Control Theory]
image: https://images.unsplash.com/photo-1485827404703-89b55fcc595e?w=800&q=80
description: A data-efficient algorithm for learning to control nonlinear dynamical systems by decoupling data collection from controller synthesis.
external_url: https://ieeexplore.ieee.org/abstract/document/9525194
---

# D2C — Decoupled Data-Based Approach for Learning to Control Nonlinear Dynamical Systems

Published in **IEEE Transactions on Automatic Control, 2022**.

## Overview

Most data-driven control methods require large amounts of data because they entangle the processes of learning the system dynamics and designing the controller. D2C breaks this coupling by separating these two phases:

1. **Data collection phase** — A small amount of exploratory data is collected around a nominal trajectory using open-loop perturbations.
2. **Controller synthesis phase** — A local linear model is fit to the data, and a feedback controller is synthesized analytically using this model.

This decoupling leads to significant improvements in sample efficiency while maintaining strong performance guarantees on nonlinear systems.

## Key Results

- Demonstrated on benchmark nonlinear control tasks including pendulum swing-up, cartpole, and quadrotor stabilization.
- Achieves competitive performance with model-free RL baselines using orders of magnitude fewer samples.
- Provides theoretical guarantees on stability and convergence under mild assumptions.

## Related Work

- **D2C 2.0** ([arXiv, 2020](https://arxiv.org/abs/2002.07368)) extends the framework to stochastic nonlinear systems via model-free iLQR.
- **ACC 2025** workshop paper extends the theoretical analysis of feedback structure in RL.

<p class="text-center">
{% include elements/button.html link="https://ieeexplore.ieee.org/abstract/document/9525194" text="IEEE Paper" %}
{% include elements/button.html link="https://arxiv.org/abs/2002.07368" text="arXiv Preprint" %}
</p>
