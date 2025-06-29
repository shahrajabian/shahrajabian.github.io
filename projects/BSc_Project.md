layout: page
title: BSc Project
description: Quadrotor Autopilot 
img: assets/img/BSc_P_front.png
importance: 1
category: Academic
related_publications: true
---
**Design and Implementation of Autopilot for Automatic Takeoff and Landing of a Quadrotor using the MBD Approach

Given the increasing importance of unmanned aerial vehicles in recent decades, studies to model and control these aerial vehicles have taken on a growing trend. One of the most important challenges facing the unmanned aerial vehicle industry is the issues related to the guidance, navigation and automatic control system (autopilot), especially in the take-off and landing phase. In this research, based on the model-based design process, an autopilot system for a quadrotor is designed and practically implemented. At first, quadrotor modeling is done using Newton-Euler equations and the quadrotor nonlinear model is simulated in Simulink environment. Afterwards, flight management and trajectory generation algorithms in the take off, waypoint following and landing pahse are designed and implemented in the Simulink environment. Then, to control the quadrotor and track the  generated trajectory by the guidance system, the multi-loop cascade PID controller is designed. After the design phase of the guidance and control systems, the the performance of the designed controller is evaluated by simulations of the model in the loop in the Simulink environment. Then, in the rapid control prototyping phase of the controller, in order to check the performance of the designed controller on the real system and observe the uncertain effects of the model, the vehicle is placed in the loop with three degrees of freedom and the gains of the controller are tuned. Next, with automatic code generation, the performance of the generated C++ code is verified in the software in the loop simulation, and finally, the code is implemented on the Pixhawk flight controller board and evaluated in the hardware in the loop simulation. At the end, after verification of the code on the hardware, the design validation is done by performing a real-world automaic takeoff and landing test. 

**Contributions:
* Modeling of quadrotor dynamics, Brushless DC motors and wind effects
* Implemented flight management and waypoint following algorithms
* Designed and implemented flight management, waypoint following and control algorithms for the quadrotor
* Implemented custom automatic flight control algorithms on the Pixhawk using Simulink
* Performed Software-in-the-Loop (SIL) simulation, Hardware-in-the-Loop (HIL) simulation and flight tests for verification of custom-designed autopilot using Simulink and the Pixhawk

The result is shown below:
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/BSc_P_Pos.png" title="Position and Velocity" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/BSc_P_Att.png" title="Attitude and Angular Rates" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Quadrotor states in takeoff, waypoint following and landing.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/BSc_P_3D.png" title="Quadrotor Path" class="img-fluid rounded z-depth-1" %}
<div class="caption">
    Quadrotor path in 2D up view and 3d view.
</div>

