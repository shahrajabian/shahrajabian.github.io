---
layout: post
title: Safe Autonomous Systems
date: 2026-02-10 10:00:10
description: Safety-Critical Control and Fault-Tolerance for Safe Autonomy 
tags: control, autonomous-systems
categories: control, autonomy
thumbnail: assets/img/vertical-crash.png
---


Safety-critical systems are systems whose malfunction or failure can lead to severe financial losses, personal injury, or even fatalities. Examples of such systems include autonomous vehicles, unmanned aerial vehicles (UAVs), and, in particular, autonomous air taxis. In these applications, ensuring safe operation under all possible conditions—including the presence of uncertainties, external disturbances, and component failures—is of paramount importance.

In the context of aerial vehicles and autonomous systems, **safety** refers to the ability to prevent accidents, whereas **reliability** denotes the ability of a system to perform its intended function without failure. More specifically, reliability is defined as the probability that a system or one of its components performs satisfactorily under specified operating conditions for a given period of time. However, it is important to recognize that a reliable system is not necessarily a safe one. Although such a system may execute control commands correctly at every instant, adverse environmental conditions can still cause these commands to result in hazardous situations or accidents.

In the aerospace industry, safety and reliability are typically addressed through two complementary stages during the flight certification process: **assessment** and **preventive measures**. During the assessment stage, various simulation-based and experimental tests are conducted in accordance with relevant certification standards to evaluate the reliability of the aircraft and its components. Upon successful completion of these tests, the probability of in-flight failure is considered to be below an acceptable threshold. Subsequently, a set of preventive measures is implemented to further enhance the vehicle's safety and reliability by reducing the likelihood of accidents. These measures include obstacle and traffic detection, collision avoidance, operation within the authorized airspace while respecting the certified flight envelope, and the incorporation of fault-tolerant capabilities.

Fault-tolerant approaches can effectively manage and mitigate both internal hazards, such as component failures, communication losses, and structural damage, and external hazards, including obstacles and cyberattacks, thereby improving the overall reliability of the system. In general, fault tolerance can be achieved through **hardware redundancy** and **analytical redundancy**. Hardware redundancy involves incorporating additional components for critical subsystems to provide backup functionality. In addition, the development of fault-tolerant control algorithms for actuator failures is of significant importance and constitutes the primary focus of this research.

Beyond reliability and fault tolerance, it is also essential to ensure that the safety constraints required for safe vehicle operation are satisfied. These safety constraints include **state constraints** (i.e., maintaining the system states within a safe set), **input constraints** (i.e., actuator limitations), and **stability guarantees** (i.e., convergence of the system states to the desired equilibrium). Together, these constraints first promote safe operation in a probabilistic sense and, at a higher level, provide explicit safety guarantees. Therefore, designing control systems that can guarantee not only system stability but also compliance with safety constraints under a wide range of operating conditions is of critical importance.

**Control Barrier Functions (CBFs)** define a safe set of system states and enforce constraints that prevent the system from leaving this safe set. This approach is typically formulated as a convex optimization problem, most commonly a **Quadratic Programming (QP)** problem, which generally requires significantly less computational effort than the two previously discussed approaches. However, several challenges remain, including robustness to model uncertainties, optimization **infeasibility**, and numerical instability during the solution of the optimization problem.

The need for system resilience against faults has led to the development of **Fault-Tolerant Control (FTC)**. FTC aims to preserve system stability and maintain acceptable performance in the presence of component failures or partial faults. Such control systems are required to autonomously generate appropriate control commands to manage faults, preserve vehicle stability, and successfully complete the mission despite degraded operating conditions.

In general, fault-tolerant control systems are classified into two categories: **Passive Fault-Tolerant Control (PFTC)** and **Active Fault-Tolerant Control (AFTC)**. PFTC relies on robust control designs with a fixed controller structure that is capable of tolerating a predefined class of faults, typically represented as bounded uncertainties. In contrast, AFTC dynamically reconfigures the controller structure or adapts its parameters in response to detected faults. Owing to the time-varying nature of environmental conditions and fault occurrences, AFTC approaches offer greater flexibility and have therefore attracted considerably more attention in practical applications.

Active Fault-Tolerant Control (AFTC) can be broadly classified into two categories. The first category consists of approaches based on **Fault Detection and Diagnosis (FDD)**, which typically rely on a dedicated fault detection and identification module. The second category includes adaptive control approaches that guarantee closed-loop stability without requiring explicit fault detection or identification. Furthermore, for systems equipped with redundant actuators that require control allocation, FDD-based AFTC methods are commonly implemented within a **Dynamic Control Allocation (DCA)** framework. In addition, FDD techniques can generally be categorized into **model-based** and **data-driven** approaches.

Representative model-based FDD methods include **observer-based techniques**, **Kalman filter**-based methods, **Recursive Least Squares (RLS)** parameter estimation, and the **Parity Space Method**. These approaches generally offer faster fault detection and lower computational complexity. However, their performance depends heavily on the availability of accurate system and actuator models. Moreover, an inability to distinguish external disturbances from actual faults may lead to false fault detection, resulting in degraded control performance or even closed-loop instability.

In contrast, **data-driven** FDD approaches are capable of identifying faults without requiring an explicit mathematical model of the system. Representative techniques include statistical methods, **Neural Networks**, **Support Vector Machines (SVMs)**, and frequency-domain analysis. Most data-driven methods are employed to detect fault occurrence and identify fault types through an **offline** training process using historical sensor measurements, such as acceleration, vibration, temperature, current, acoustic signals, and other operational data. Despite their effectiveness, these methods face several challenges, including the lack of rigorous stability guarantees, the difficulty of collecting sufficiently representative datasets, and the challenge of ensuring comprehensive data coverage under diverse operating conditions. Failure to satisfy these requirements can significantly reduce the **generalization** capability of the trained models. In addition to offline learning methods, adaptive neural network approaches with **online** learning capability have also been developed for fault detection and diagnosis. These methods, however, introduce additional challenges, including learning speed, computational burden, network estimation error, data richness, and the requirement for **persistent excitation**.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/FTC2.png" title="Fault-tolerant Control" class="img-fluid rounded z-depth-1" %}
        <div class="caption text-center">Fault-tolerant Control</div>  
    </div>
</div>


Fault Detection and Diagnosis (FDD) encompasses several stages, including **fault detection**, **fault isolation**, **fault identification**, and **fault severity estimation**. Fault detection refers to the process of determining whether a fault has occurred within the system. This is typically accomplished by **monitoring** real-time measurement data and identifying deviations from the system's normal and expected operating behavior.

Once a fault has been detected, **fault isolation** is performed to determine the location of the fault, namely the specific component, subsystem, or actuator in which the fault has occurred. It should be noted that *fault isolation* does not imply physically isolating or disconnecting a faulty component to prevent fault propagation. Rather, it refers to identifying the source or location of the fault. For this reason, the term **fault identification** is sometimes considered more appropriate. Nevertheless, in the FDD literature, the terms *fault isolation* and *fault identification* are often used interchangeably.

Furthermore, some FDD approaches also determine the **fault type** and identify its **root cause**, which can be regarded as an extension of the fault isolation (or identification) process. Collectively, the processes of fault detection and fault isolation constitute the **Fault Detection and Isolation (FDI)** module. The combination of the FDI module and **fault severity estimation** forms the complete **Fault Detection and Diagnosis (FDD)** framework, whose main components are illustrated in the following figure.

<div class="row">
    <div class="col-sm d-flex justify-content-center mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/FDD.png" title="Fault Detection and Diagnosis Block" class="img-fluid rounded z-depth-1" %}
        <div class="caption text-center">Fault Detection and Diagnosis Block</div>  
    </div>
</div>
