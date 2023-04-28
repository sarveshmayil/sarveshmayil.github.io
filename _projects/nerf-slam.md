---
title: "NeRF-SLAM"
excerpt: "Visual SLAM using neural radiance fields<br/><img src='/images/nerf-slam/nerf-slam-kitchen.gif' width='500'>"
collection: projects
---

NeRF-SLAM performs monocular visual SLAM and achieves 3D reconstruction of a scene. It achieves this through a combination of dense monocular SLAM, probabilistic volumetric fusion, and real-time hierarchical volumetric neural radiance fields. This scene reconstruction pipeline has shown to be geometrically and photometrically more accurate than other methods.

NeRF-SLAM was developed by Antoni Rosinol, and a public repository of NeRF-SLAM is available. To make development and deployment of NeRF-SLAM much easier, we present a docker environment than allows NeRF-SLAM to work out the box. Additionally, we reproduce the results of NeRF-SLAM on the Replica dataset and perform inference on real-world custom datasets.

The code for this project can be found [here](https://github.com/sarveshmayil/NeRF-SLAM-docker).


Below, we demonstrate NeRF-SLAM performing SLAM and doing 3D reconstruction for one of the Replica datasets. The video is sped up 4x and does not convey real-time performance.

<img src="/images/nerf-slam/room0-building-nerf.gif" />

Some qualitative comparisons for NeRF-SLAM's performance on real-world custom datasets are shown below. On the left is the real image from the video and on the right is a recreated image from the NeRF at approximately the same location.

<p float="left">
  <img src="/images/nerf-slam/kitchen_real_2.jpg" width="500" />
  <img src="/images/nerf-slam/kitchen_nerf_2.jpg" width="500" /> 
</p>

The full report for this work can be found [here](https://sarveshmayil.github.io/files/NeRF-SLAM.pdf)
