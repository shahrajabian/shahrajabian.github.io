---
layout: page
title: MSc Project
description: Safe Intelligent Control of Air Taxis
img: assets/img/MSc_P_front.png
importance: 1
category: Academic
related_publications: false
---
**Fault-Tolerant Adaptive Intelligent Control of an Autonomous Multi-rotor eVTOL Air Taxi**

With increasing urban density, large cities face challenges such as air pollution, traffic congestion, and limited accessibility to various areas. In this context, autonomous electric vertical take-off and landing (eVTOL) air taxis are emerging as an innovative solution for urban transportation. Achieving fully autonomous air taxis requires addressing several flight control challenges, including safety, reliability, and optimal performance in the presence of parametric uncertainties, unmodeled dynamics, external disturbances, and actuator and sensor faults. This study focuses on the control of an air taxi with a multi-rotor configuration and distributed electric propulsion to enable autonomous flight and trajectory tracking despite uncertainties, unmodeled dynamics, external disturbances, and motor failures. The proposed control method employs a Composite Learning-based Adaptive Neural Control with Disturbance Observer (CANCDO) for attitude and altitude control (inner loop) and an ESO-augmented proportional-derivative (PD) controller for position control and trajectory tracking (outer loop). The controller design is based on Lyapunov's theorem, and the neural network weights are updated online to handle uncertainties and reduce tracking errors. The disturbance observer compensates for external disturbances and neural network estimation errors, while a state observer is used to enhance network learning. The dynamic control allocation block is responsible for optimal distributions of the virtual control commands based on the actuator's health. Furthermore, Control Barrier Functions are employed to enforce the safety constraints on the position and velocity of the vehicle. Simulation results in various scenarios demonstrate the effectiveness of the proposed control system in tracking the desired trajectory in different flight conditions and faults. 

**Contributions**:
* Developed a high-fidelity simulation framework incorporating gyroscopic effects, rotor and body aerodynamic effects, ground effect, and wind disturbances to evaluate the proposed methods under realistic urban flight scenarios.
* Proposed a Composite-Learning-Based Adaptive Neural Control with Disturbance Observer (CANCDO) approach considering input constraints for the second-order systems (multirotors) to improve the quality of online uncertainty estimation and capable of robust trajectory tracking under system uncertainties, external disturbances.
* Developed a dynamic control allocation algorithm based on a novel two-stage FDD framework, combining AEKF and OS-ELM approaches to handle simultaneous actuator faults.
* Developed adaptive CBFs as safety filter for enforcing safety constraints on critical states and guaranteeing operation within safe flight envelopes.

* Compensating for the uncertainty caused by the variability of the thrust and drag torque coefficients in the system model and considering them as constant in the control allocation matrix by the proposed CANCDO approach
The overal architecture of the proposed control system is shown below:
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/MSc_control_system_arc.png" title="Control System Architecture" class="img-fluid rounded z-depth-1" %}
<div class="caption">
    The proposed safe intelligent control system architecture for multirotors. 
</div>
The simulation result in the presence of up to 20 percent parameter uncertainties, unmodeled dynamics, wind and gusts, and 6 actuator faults is shown below:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AirTaxi_Path.png" title="Air Taxi Path" class="img-fluid rounded z-depth-1" %}
<div class="caption">
    3D view of Air Taxi path.
</div>

