---
layout: post
title: Safe Autonomous Systems
date: 2026-02-10 10:00:10
description: Safety-Critical Control and Fault-Tolerance for Safe Autonomy 
tags: control, autonomous-systems
categories: control, autonomy
thumbnail: assets/img/vertical-crash.png
---


Safety-critical systems are systems whose malfunction or failure can lead to severe financial losses, personal injury, or even fatalities (Cohen et al., 2024). Examples of such systems include autonomous vehicles, unmanned aerial vehicles (UAVs), and, in particular, autonomous air taxis. In these applications, ensuring safe operation under all possible conditions—including the presence of uncertainties, external disturbances, and component failures—is of paramount importance.

In the context of aerial vehicles and autonomous systems, **safety** refers to the ability to prevent accidents, whereas **reliability** denotes the ability of a system to perform its intended function without failure (Hu et al., 2025; Xiang et al., 2023). More specifically, reliability is defined as the probability that a system or one of its components performs satisfactorily under specified operating conditions for a given period of time. However, it is important to recognize that a reliable system is not necessarily a safe one. Although such a system may execute control commands correctly at every instant, adverse environmental conditions can still cause these commands to result in hazardous situations or accidents.

In the aerospace industry, safety and reliability are typically addressed through two complementary stages during the flight certification process: **assessment** and **preventive measures**. During the assessment stage, various simulation-based and experimental tests are conducted in accordance with relevant certification standards to evaluate the reliability of the aircraft and its components. Upon successful completion of these tests, the probability of in-flight failure is considered to be below an acceptable threshold. Subsequently, a set of preventive measures is implemented to further enhance the vehicle's safety and reliability by reducing the likelihood of accidents. These measures include obstacle and traffic detection, collision avoidance, operation within the authorized airspace while respecting the certified flight envelope, and the incorporation of fault-tolerant capabilities.

Fault-tolerant approaches can effectively manage and mitigate both internal hazards, such as component failures, communication losses, and structural damage, and external hazards, including obstacles and cyberattacks, thereby improving the overall reliability of the system. In general, fault tolerance can be achieved through **hardware redundancy** and **analytical redundancy**. Hardware redundancy involves incorporating additional components for critical subsystems to provide backup functionality. In addition, the development of fault-tolerant control algorithms for actuator failures is of significant importance and constitutes the primary focus of this research.

Beyond reliability and fault tolerance, it is also essential to ensure that the safety constraints required for safe vehicle operation are satisfied. These safety constraints include **state constraints** (i.e., maintaining the system states within a safe set), **input constraints** (i.e., actuator limitations), and **stability guarantees** (i.e., convergence of the system states to the desired equilibrium). Together, these constraints first promote safe operation in a probabilistic sense and, at a higher level, provide explicit safety guarantees (Brunke et al., 2022). Therefore, designing control systems that can guarantee not only system stability but also compliance with safety constraints under a wide range of operating conditions is of critical importance.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/FTC2.png" title="Fault-tolerant Control" class="img-fluid rounded z-depth-1" %}
        <div class="caption text-center">Fault-tolerant Control</div>  
    </div>
</div>
