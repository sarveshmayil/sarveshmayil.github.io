---
title: "Autonomous Robotic Arm"
excerpt: "Developing autonomous capabilities for a 5-DOF robotic arm.<br/><img src='/images/botlab/mbot.jpg' width='500'>"
collection: projects
---

This group project involved developing autonomous capabilities for a 5-DOF robotic arm from the ground up given base hardware and a skeleton software system to accomplish several tasks in sorting and stacking colored blocks. This included a wide range of tasks ranging from integrating forward/inverse kinematics to a full perception system capable of identfying block poses.

The robotic arm is a ReactorX 200 Robot Arm with 5 DOF and is equipped with 7 Dynamixel servo motors. It also has a gripper attached at the end for picking up blocks.

The functionality of the robotic arm can be broken down into control and perception stacks.

### Control

The control portion of the arm handles three main tasks: forward kinematics, inverse kinematics, and path planning.

Forward kinematics allows the system to have knowledge of the end effector's position in 3D space based only on the knowledge of the joint angles, which we accomplish this through the use of screw vectors. An evaluation of the forward kinematics accuracy showed that generally the pose estimate was most accurate near the arm's base and higher further away from the base due to small errors being compounded through the individual joints.

Inverse kinematics is crucial to determining the joint angles that will result in a provided position and orientation of the end effector. This complex problem is solved by first simplifying the problem from 3D to 2D by evaluating the arm in a 2D plane characterized by the arm's rotation about the base. The problem is then decomposed into a 3-link arm with 3 unknown joint angles to solve for as shown in the figure below.

<img src="/images/armlab/Armlab-ik.png" width=300>

Path planning for the robotic arm falls under two categories of block pickup and block placement. For block pickup, we perform a series of motions that mitigate error in the end effector position. The system tests for a range of different pickup angles with higher priority for picking up the block from directly above, which is most accurate. Block placement follows a similar order of operations and finds the safest and most accurate series of motions in order to place the block at the intended position.

### Perception




The full report for the control portion of this work can be found [here](https://sarveshmayil.github.io/files/armlab_control_report.pdf)
