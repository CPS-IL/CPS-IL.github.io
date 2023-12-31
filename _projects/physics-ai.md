---
layout: page
title: Safe Physics-AI
description: Physics Model Guided Machine Learning
img: assets/img/physics-ai.jpg
importance: 1
category: Physics Integrated Machine Learning
related_publications:
selected: true
---

<div style="text-align: justify;">

<p>
A physics model is a validated low-dimensional model of causality with critical properties such as provable stability in control applications. DNN is a high-dimensional model of correlations that may capture not only unmodeled dynamics overlooked by the physics model but also spurious corrections in the training samples (overfitting). As a result, while DNN has statistically significant performance improvement, but it may also generate outputs inconsistent with the laws of physics that could lead to catastrophic failures. We propose a solution that combines the best of the physical model and DNN model.
</p>

<p>
Traditionally,  we project a higher dimensional space to a lower dimension space for computational efficiency at the cost of performance. Physics model-based neuron editing turns this conventional projection approach upside down. We project a lower dimensional physics model onto a higher dimensional DNN model by 1) augmenting the input feature vector with physic variables and 2) removing relations permitted by DNN but contradicting the laws of physics. The physics model edited DNN  is constrained by physical laws. We gain control performance at the cost of computing.  To ensure the stability of control despite DNN software failures, we use Simplex architecture to ensure that the states under the control of the edited DNN must remain within the stability envelope of the physical model-based control.
</p>

</div>

##### Work 1: Phy-DRL: Physics-Regulated Deep Reinforcement Learning (DRL) Towards Safety Guarantee

<p>
Phy-DRL = Physics Model-Based Policy + Data-Driven DRL Policy. 
<div style="text-align: center;">
  <img src="/assets/img/physics-ai/phydrl.png" alt="Centered Image" style="width: 500px; height: auto;">
</div>
</p>

== Phy-DRL's Benefits: 
- Best-Trade-Off: Simplify model-based policy to be an analyzable and verifiable linear one, while offering fast and stable training. 
- Performance: Mathematically-provable safety and stability guarantees, with high system performance.  


<p>
Experiment in Cart-Pole System.
<div style="text-align: center;">
  <img src="/assets/img/physics-ai/id.png" alt="Centered Image" style="width: 500px; height: auto;">
</div>
</p>

<p>
Experiment in Quadruped Robot: safe lane tracking, safe velocity regulation, and safe center-gravity management.
<div style="text-align: center;">
  <img src="/assets/img/physics-ai/ph2.png" alt="Centered Image" style="width: 500px; height: auto;">
</div>
</p>

<p>
Demonstration Video: 
<iframe width="560" height="315" src="https://www.youtube.com/embed/BK8k92jahfI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</p>