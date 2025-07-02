---
layout: page
title: Learning AMPC 
description: Learning-based Adaptive MPC of Quadrotor
img: assets/img/ANMPC_frontt.png
importance: 2
category: Academic
related_publications: false
---

**Robust fault-tolerant trajectory tracking of a quadrotor based on learning-based adaptive model predictive control**

In this research, a learning-based adaptive model predictive control (MPC) structure is proposed for fault-tolerant trajectory tracking control of quadrotors in the presence of uncertainties and disturbances. The predictive control method used is acceleration-based, and the predictive model is linearized at each time step around the future trajectory to minimize computational cost in the optimal control problem.

In the proposed approach, a Radial Basis Function (RBF) neural network is used to predict the difference between the actual system behavior and the prediction based on the nominal predictive model. The neural network weights are updated online using the Recursive Least Squares (RLS) method based on system output. The MPC then uses the estimated model to predict future behavior and generate optimal control inputs. Additionally, a disturbance observer is included to account for neural network estimation errors. The proposed control system architecture is shown below:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ANMPC_arc.png" title="The proposed control system architecture" class="img-fluid rounded z-depth-1" %}
<div class="caption">
    The proposed control system architecture.
</div>

The considered uncertainties include ground effect, motor dynamics, and up to 15% parametric uncertainties. Moreover, sinusoidal signals are added to all position and attitude channels as external disturbances. Furthermore, actuator faults are simulated where, after 5 seconds, motor 1’s effectiveness drops to 80%; after 10 seconds, motor 2’s effectiveness drops to 70%; after 15 seconds, motor 3’s effectiveness drops to 90%; and after 20 seconds, motor 4’s effectiveness drops to 90%, representing severe loss-of-effectiveness faults.
The controller's performance, evaluated by Mean Absolute Error (MAE) in trajectory tracking under these varying conditions, is shown below and demonstrates acceptable robustness.

<div class="row">
    <div class="col-sm d-flex justify-content-center mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ANMPC_MAE.png" title="MAE" class="img-fluid rounded z-depth-1"  width="300" %}
</div>

The simulation results is shown below:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ANMPC_result.png" title="Tracking performance" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ANMPC_front.png" title="3D path" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
