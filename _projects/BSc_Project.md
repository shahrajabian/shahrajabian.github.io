---
layout: page
title: BSc Project
description: with background image
img: assets/img/BSc_P_front.png
importance: 1
category: Academic
related_publications: true
---

** Abstract
Given the increasing importance of unmanned aerial vehicles in recent decades, studies to model and control these aerial vehicles have taken on a growing trend. One of the most important challenges facing the unmanned aerial vehicle industry is the issues related to the guidance, navigation and automatic control system (autopilot), especially in the take-off and landing phase. In this research, based on the model-based design process, an autopilot system for a quadrotor is designed and practically implemented. At first, quadrotor modeling is done using Newton-Euler equations and the quadrotor nonlinear model is simulated in Simulink environment. Afterwards, flight management and trajectory generation algorithms in the take off, waypoint following and landing pahse are designed and implemented in the Simulink environment. Then, to control the quadrotor and track the  generated trajectory by the guidance system, the multi-loop cascade PID controller is designed. After the design phase of the guidance and control systems, the the performance of the designed controller is evaluated by simulations of the model in the loop in the Simulink environment. Then, in the rapid control prototyping phase of the controller, in order to check the performance of the designed controller on the real system and observe the uncertain effects of the model, the vehicle is placed in the loop with three degrees of freedom and the gains of the controller are tuned. Next, with automatic code generation, the performance of the generated C++ code is verified in the software in the loop simulation, and finally, the code is implemented on the Pixhawk flight controller board and evaluated in the hardware in the loop simulation. At the end, after verification of the code on the hardware, the design validation is done by performing a real-world automaic takeoff and landing test. 

** Contributions:
* Modeling of quadrotor dynamics, Brushless DC motors and wind effects
* Implemented flight management and waypoint following algorithms
* Designed and implemented flight management, waypoint following and control algorithms for the quadrotor
* mplemented custom automatic flight control algorithms on the Pixhawk using Simulink
* Performed Software-in-the-Loop (SIL) simulation, Hardware-in-the-Loop (HIL) simulation and flight tests for verification of custom-designed autopilot using Simulink and the Pixhawk
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
