---
layout: post
title: Today, I successfully defended my bachelor thesis and I graduated from the Amirkabir University of Technology with Summa Cum Laude!
date: 2022-10-22 14:00:00-0400
inline: false
related_posts: false

---

Bachelor's Thesis: Design and Implementation of Autopilot for Automatic Takeoff and Landing of a Quadrotor using the Model-Based Design Approach

---
According to the increasing importance of unmanned aerial vehicles in recent decades, studies to model and control these aerial vehicles have taken on a growing trend. One of the most important challenges facing the unmanned aerial vehicle industry is the issues related to the guidance, navigation and automatic control system (autopilot), especially in the take-off and landing phase. 
{% include figure.html path="assets/img/MBD.png" title="" class="img-fluid rounded z-depth-1" %}
In this research, based on the model-based design process, an autopilot system for a quadrotor is designed and practically implemented. At first, quadrotor modeling is done using Newton-Euler equations and the quadrotor nonlinear model is simulated in the Simulink environment. In the following, flight management and trajectory generation algorithms in the take-off, waypoint following and landing phase are designed and implemented in the Simulink environment. Then, to control the quadrotor and track the generated trajectory by the guidance system, the multi-loop cascade proportional-integral-derivative controller is designed. After the design phase of the guidance and control systems, the verity of the Simulink controller model performance is evaluated by simulations of the model in the loop in the Simulink environment. Then, in the rapid control prototyping phase of the controller, to check the performance of the designed controller on the real system and observe the uncertain effects of the model, the vehicle is placed in the loop with three degrees of freedom and the gains of the controller are tuned. Next, with automatic code generation, the verity of the control code function is checked in the software in the loop simulation, and finally, the code is implemented on the Pixhawk flight controller board and evaluated in the hardware in the loop simulation. In the end, after verification of the code on the hardware, the design validation is done by performing a flight test.
