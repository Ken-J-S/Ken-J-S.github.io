---
layout: page
title: IK manifold flows
description: Solve inverse kinematics leveraging generative manifold flows and latent nullspace projections
img: assets/img/IK_M_Flow.png
importance: 8
category: work
related_publications: false
---

> :dart: **Goal**: Learn a generative model, that predictes the closest joint states given a current seed configuration and a target pose.

> :bulb: **Idea**: Leverage [manifold flows](https://proceedings.neurips.cc/paper/2020/file/051928341be67dcba03f0e04104d9047-Paper.pdf) (Normalizing flows + zero padding) to learn a latent nullspace state given target pose and project current joint state into it

<div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/Latent_Projection_Flow.png" title="Overview" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    Schematic representation of the projection into the nullspace and (b) generation of a target configuration (a).
</div>

First, the given seed configuration $$\mathbf{q}$$ (current joint state) is projected on a latent nullspace state $$\mathbf{z}$$ conditioned on target pose $$\mathbf{x}$$ using a manifold flow $$f(\mathbf{q} | \mathbf{x})$$. This flow is designed via conditioned Affine Coupling Layer. From this latent nullspace state we can generate a target configuration in null space using the inverted manifold flow $$f^{-1}$$ and zero padding.

<div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/overview_nullspace_projection.png" title="Schematic relation" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    Schematic relation of the manifold flow model.
</div>

:test_tube: **Experiments**: Generate target joint state given seed configurations

The model is trained with $$125000$$ sampled joint states from an 3 DOF robot arm. For testing $$100$$ seed configurations and one target position (not in training set) are sampled from the robot simulator. Then the target configuration is predicted. For reference the IK solution using Levenberg-Marquardt (LM) algorithm is calculated. The resulting target pose has currently a position error of approx. $$1\text{cm}$$.

<div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/experiment_nullspace_projection.png" title="experiment_nullspace_projection" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    Predicted target configuration (orange) and calculated IK solution (green).
</div>

Experiments on a 7 DOF robot will follow soon.
