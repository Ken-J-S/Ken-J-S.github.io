---
layout: page
title: mu-zero Hyperloop
description: Levitation Control
img: assets/img/Leviosa.png
importance: 1
category: work
related_publications: false
---

> **Goal**: Develop a non-linear levitation control for a 6DOF free-floating hyperloop pod.

Based on an electromagnetic suspension (EMS), the reluctance force is utilized to generate a force that counteracts gravity and makes the vehicle levitate. Complex non-linear electromagnetic system properties must be stabilized.
It is important to get as close as possible to the rail in order to save energy, but the force becomes significantly more non-linear and the control system more complex. In addition, temperatures and irregularities in the surface make static stabilization more difficult.
The idea was first to develop a very accurate physical model. On the basis of this model, the system behaviour can be linearized in the operating range via linear compensation and simple PI-PD controllers can be developed.
In a final step, a distance between the EMS systems and the rail is calculated using a state estimation consisting of a Kalman filter. It is important here that these EMS systems are decoupled via viscoelastic materials.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Leviosa.png" title="Leviosa" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Levitation_run.png" title="Levitation" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/MuZero_ControlConcept.png" title="ControlConcept" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
{% include video.liquid path="assets/video/GA-Opt.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=false %} 
<div class="caption">
    Control parameter optimization with particle swarm optimisation in combination with a Genetic algorithm with tournament selection
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Test-Stand_setup.jpg" title="Levitation" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/lev_1D.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Overall_dem_setup_side.jpg" title="Test setup" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Test stand to analyze the levitation behavior
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/overall_pod.png" title="Hyperloop pod" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Test stand to analyze the levitation behavior
</div>
