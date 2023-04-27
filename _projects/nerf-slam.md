---
title: "NeRF-SLAM"
excerpt: "Visual SLAM using neural radiance fields<br/><img src='/images/500x300.png'>"
collection: projects
---

NeRF-SLAM performs monocular visual SLAM and achieves 3D reconstruction of a scene. It achieves this through a combination of dense monocular SLAM, probabilistic volumetric fusion, and real-time hierarchical volumetric neural radiance fields. This scene reconstruction pipeline has shown to be geometrically and photometrically more accurate than other methods.

NeRF-SLAM was developed by Antoni Rosinol, and a public repository of NeRF-SLAM is available. To make development and deployment of NeRF-SLAM much easier, we present a docker environment than allows NeRF-SLAM to work out the box. Additionally, we reproduce the results of NeRF-SLAM on the Replica dataset and perform inference on real-world custom datasets.

The code for this project can be found [here](https://github.com/sarveshmayil/NeRF-SLAM-docker).
