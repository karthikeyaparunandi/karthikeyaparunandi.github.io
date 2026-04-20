---
name: T-PFC — Trajectory-Optimized Perturbation Feedback Control
tools: [Motion Planning, Trajectory Optimization, C++, ROS, Robotics]
image: https://images.unsplash.com/photo-1561144257-e32e8d0c7f53?w=800&q=80
description: A trajectory optimization framework that combines nominal path planning with stochastic perturbation feedback for robust robot motion control.
external_url: https://ieeexplore.ieee.org/abstract/document/8755450
---

# T-PFC — Trajectory-Optimized Perturbation Feedback Control

Published in **IEEE Robotics and Automation Letters** and presented at **IEEE/RSJ IROS 2019, Macau, China**.

## Overview

Robot motion controllers typically handle trajectory generation and disturbance rejection as separate concerns. T-PFC unifies them: it jointly optimizes the nominal reference trajectory and the perturbation feedback gains, so the planned path is inherently shaped around the system's ability to handle uncertainty.

The key insight is that a trajectory that looks optimal in the nominal (deterministic) sense may be brittle under real-world noise, while a slightly suboptimal nominal path may enable a much more robust closed-loop response. T-PFC captures this trade-off explicitly in the optimization objective.

## Method

- Frames the problem as a stochastic optimal control problem over a finite horizon.
- Uses a perturbation feedback (LQR-style) controller layered on top of a nominal trajectory.
- Jointly optimizes both the nominal trajectory and the feedback gains using iterative LQR (iLQR) with covariance propagation.

## Results

- Validated on quadrotor trajectory tracking and robot arm motion tasks.
- Outperforms standard iLQR and MPC baselines in the presence of process noise and model mismatch.

<p class="text-center">
{% include elements/button.html link="https://ieeexplore.ieee.org/abstract/document/8755450" text="IEEE Paper" %}
</p>
