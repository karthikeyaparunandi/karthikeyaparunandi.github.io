---
name: Robust Pose-Graph SLAM with Absolute Orientation Sensing
tools: [SLAM, C++, ROS, Mobile Robotics, Sensor Fusion]
image: https://images.unsplash.com/photo-1518314916381-77a37c2a49ae?w=800&q=80
description: A robust simultaneous localization and mapping approach that fuses absolute orientation sensing with pose-graph SLAM to improve resilience to outliers and loop-closure errors.
external_url: https://ieeexplore.ieee.org/abstract/document/8613891
---

# Robust Pose-Graph SLAM Using Absolute Orientation Sensing

Published in **IEEE Robotics and Automation Letters** and presented at **IEEE ICRA 2019, Montreal, Canada**.

## Overview

Pose-graph SLAM constructs a map of an environment by accumulating relative motion estimates between robot poses. The main failure mode is spurious loop-closure edges—false matches that introduce large inconsistencies into the graph and corrupt the final map.

This work augments the standard pose-graph formulation with absolute orientation measurements from an IMU or compass. Because orientation is measured globally rather than relative to prior poses, these measurements act as anchors that significantly reduce the ambiguity in the graph and improve the system's ability to detect and reject outlier loop closures.

## Method

- Extends standard pose-graph SLAM (g2o / GTSAM style) to incorporate absolute orientation factors.
- Derives the appropriate noise model and information matrix for orientation measurements.
- Uses an M-estimator robust cost function to down-weight outlier edges during graph optimization.

## Results

- Tested on 2D and 3D datasets with varying levels of loop-closure noise.
- Absolute orientation anchoring reduces final map error by up to 40% compared to standard robust SLAM baselines under high outlier rates.

<p class="text-center">
{% include elements/button.html link="https://ieeexplore.ieee.org/abstract/document/8613891" text="IEEE Paper" %}
</p>
