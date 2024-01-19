---
title: "Low-light Visual SLAM"
excerpt: "A comprehensive comparison of low-light visual SLAM pipelines<br/><img src='/images/LL-slam/kitti.gif' width='500'>"
collection: projects
---

This project presents a comparative study of low-light visual SLAM pipelines, specifically focusing on determining an efficient combination of the state-of-the-art low-light image enhancement algorithms with standard and contemporary Simultaneous Localization and Mapping (SLAM) frameworks by evaluating their performance in challenging low-light conditions. In this study, we investigate the performance of several different low-light SLAM pipelines for dark and/or poorly-lit datasets as opposed to just partially dim-lit datasets like other works in the literature. Our study takes an experimental approach to qualitatively and quantitatively compare the chosen combinations of modules to enhance the feature-based visual SLAM.

The code for this project can be found [here](https://github.com/TwilightSLAM).

We compare the performance of four different image enhancement modules (EnlightenGAN, Bread, Zero-DCE, Dual) along with two SLAM frameworks (ORB-SLAM3, SuperPoint-SLAM) on several datasets (3 KITTI sequences and 2 ETH3D low-light sequences).

A qualitative comparison of the performance of each of the image enhancement modules can be seen below.

<img src="/images/LL-slam/LL-slam-comparison.png" style="display: block; margin: 0 auto" />

After performing SLAM with the entire pipelines, we see best trajectory results for each SLAM framework on the datasets.

<img src="/images/LL-slam/LL-slam-tracking.png" style="display: block; margin: 0 auto" />

We see the real-time performance of the ORB-SLAM3 and SuperPoint-SLAM frameworks on a KITTI sequence below. (ORB-SLAM3 on top and SuperPoint-SLAM below). The green points represent detected features.

<img src="/images/LL-slam/kitti-orb3.gif" width="700" style="display: block; margin: 0 auto" />
<img src="/images/LL-slam/kitti-superpoint.gif" width="700" style="display: block; margin: 0 auto" />

The full report for this work and results can be found [here](https://arxiv.org/abs/2304.11310)
