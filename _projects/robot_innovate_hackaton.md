---
layout: page
title: robo.innovate
description: Hackathon 2025
img: assets/img/roi_hackathon_key.png
importance: 1
category: fun
related_publications: false
---

> :dart: **Goal**: Automating vertical farming.

The robo.innovate hackathon 2025 took place at markerspace in Munich from 17.03-20.03. Ten teams, each with different challenges, competed against each other, sponsored by different organizations or companies. We were supported by Franka Robotics, which provided the hardware (robot, Ai Companion and vertical farming tower).

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/robot_innovate_entry.jpg" title="robot.innovate" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/robot_innovate_team.jpg" title="Team" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Entry to the makerspace of the robo.innovate hackathon on the left. My awesome team on the right. 
</div>

We have set ourselves the goal of automating various processes in vertical farming to make it more profitable. In doing so, we enabled the pick and place of fully planted seedlings in the vertical farming tower. Using FastSAM, we were able to recognize the degree of maturity of vegetables and thus harvest mature and fully grown vegetables automatically. By using ArUco markers, we were able to make the pick and place in trays and in the vertical farming tower adaptive.

<div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/leaf_detection.jpg" title="Maturity of vegetables" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    Maturity of vegetables and harvest readiness detection using FastSAM.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/place_salat_in_tower.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/place_tomato_tray.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
<div class="caption">
    Exemplary robot skills: (i) On the left, placing a planned lettuce seedling in the farming tower; (ii) On the right, picking and placing a ripe tomato in the tray
</div>

None of this would have been possible without my wonderful and committed team. :heart:
