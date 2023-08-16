---
layout: page
title: Safety
description: Verifiable Safety for Autonomous Vehicles
img: assets/img/polaris-gem.png
importance: 1
category: av-safety
related_publications: bansal2022verifiable, bansal2022synergistic, bansal2021risk
selected: true
---

<div style="text-align: center;">
  <img src="/assets/img/synergistic-simplex-block.png" alt="Centered Image" style="width: 600px; height: auto;">
</div>
<div class="caption">
    System architecture of Synergistic Simplex
</div>

<div style="text-align: justify;">

<p>
Safety in autonomous vehicles (AV) remains a key challenge.
An inherent limitation of traditional autonomous
driving agents is that the responsibilities of mission (navigation)
and safety (collision avoidance) are diffused throughout
the system. Without the separation between mission-critical
and safety-critical tasks, the optimization goals of the system
become ill-formed. Worse, without separation, the safety problem
becomes intermingled and convoluted.
</p>

<p>
An example of this intermingling are the Deep Neural
Networks (DNN) for object detection in AV.
These solutions couple the tasks of identifying object existence
and class e.g., vehicle or pedestrian. This approach
works incredibly well for mission-critical systems, enabling
a plethora of new applications, including AV. However, in
safety-critical systems where obstacle existence detection is a
necessary requirement, while object classification is not,
this inter-dependency between the two can result in errors from
one task e.g., object classification, to cause critical faults in the
other i.e., obstacle existence detection. Furthermore, the
intermingled complex tasks then require complex solutions.
While DNN has been deployed quite successfully to fulfill
these complex requirements, their inherent limitations for
complete verification and analysis, make
them unsuitable for safety-critical tasks.
<p>

</p>
The impasse caused by the necessity of DNN solutions to
enable AV’s mission capabilities and their unsuitability for
safety-critical tasks can be resolved by decoupling the responsibilities of mission
and safety. The disassociated fulfillment of safety
and mission requirements has been successful in system architectures
like Simplex, leading to systems that work
with high performance in typical cases but provide verifiable
safe behavior in safety-critical conditions. But thus far, such
a separation has not been achieved in AV.
</p>

<p>
Perception of obstacles remains a critical safety concern for AV.
Real-world collisions have shown that the autonomy faults leading to fatal collisions originate from obstacle existence detection. Therefore, we first target such faults, while developing a generalized framework, extensibel to address other fault types.
</p>

<p>
This research aims to create a safety layer for AV, that bears the primary responsibility for maintaining the system's safety and is verifiable for its behavior.
</p>

</div>