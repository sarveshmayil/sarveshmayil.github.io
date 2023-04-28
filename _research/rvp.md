---
title: "Reshaping Viscoelastic-string Path Planner (RVP)"
excerpt: "A physics-based path planner for autonomous vehicles<br/><img src='/images/rvp/system_diagram.png' width='500'>"
collection: research
---

We present Reshaping Viscoelastic-String Path-Planner (RVP) a path planner that reshapes a desired global plan for a robotic vehicle based on sensor observations of the environment. We model the path to be a viscoelastic string with shape preserving tendencies, approximated by a connected series of springs, masses, and dampers. The resultant path is then reshaped according to the forces emanating from the obstacles until an equilibrium is reached.

The full paper can be found [here](https://arxiv.org/abs/2303.00947)

The reshaped path from RVP remains close in shape to the original path because of anchor points that connect to the discrete masses through springs. The final path is the resultant equilibrium configuration of the Spring-Mass-Damper network. Two key concepts enable RVP (i) Virtual Obstacle Forces that push the Spring-Mass-Damper system away from the original path and (ii) Anchor points in conjunction with the Spring-Mass-Damper network that attempts to retain the path shape. We demonstrate the results in simulation and compare it’s performance with an existing Reshaping Local Planner (RLP) that also takes a global plan and reshapes it according to sensor based observations of the environment.

RVP represents the path as a set of discrete masses connected through a Spring-Mass-Damper system as shown below, where the path points are shown in blue and anchor points in red. The path points x<sub>i</sub> are a discrete representation of the local path and are connected to adjacent path points via a spring and damper while the anchor points x<sub>a,i</sub> are connected to their corresponding path point via a spring.

<img src="/images/rvp/system_diagram.png" width="750" />

Forces emanating from obstacles result in virtual forces acting on these discrete points, pushing them into regions of safety. A visualization of the dynamically reshaped local path at various integration timesteps for a scenario is shown below. The original path is shown in dashed blue and the current state of the local path in solid magenta.

<img src="/images/rvp/breakdown.png" width="750" />

Comparing the performance of RVP against RLP, we see that it is able to avoid all obstacles while maintaining a lower amount of deviation from the original path.

<img src="/images/rvp/comparison.png" width="750" />