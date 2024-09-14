---
layout: default
title: "Wildfire Prevention"
image: "/assets/img/cards/32x32-target-heatmaps.png"
description: "U-Net architecture to efficiently and accuratlety predict wildfire spread."
---
# Wildfire Prevention
This research began as a class project and was published at ICMI 2023. Utilizing satellite imagery, we predict the spread of wildfires over the course of a single day. A PDF of the paper can be found at the following link: <a href="https://dl.acm.org/doi/abs/10.1145/3577190.3614116">ICMI 2023 Paper</a>.

## Abstract
Predicting where wildfires will spread provides invaluable information to firefighters and scientists, which can save lives and homes. However, doing so requires a large amount of multimodal data e.g., accurate weather predictions, real-time satellite data, and environmental descriptors.  In this work, we utilize 12 distinct features from multiple modalities in order to predict where wildfires will spread over the next 24 hours. We created a custom U-Net architecture designed to train as efficiently as possible, while still maximizing accuracy, to facilitate quickly deploying the model when a wildfire is detected. Our custom architecture demonstrates state-of-the-art performance and trains an order of magnitude more quickly than prior work, while using fewer computational resources. We further evaluated our architecture with an ablation study to identify which features were key for prediction and which provided negligible impact on performance. 

## Model
The core of our paper revolved around the idea of real-time predictions that could be deployed by firefighters in the field. With this in mind, we settled on utilizing a lightweight U-Net architecture with attention heads on each of the upward passes. This model was capable of training in 20 minutes when run on six 1080 GPUs and achieved state-of-the-art accuracy.

<img src="/assets/img/icmi/WPN.png" alt="Model Architecture" style="width:50%;"/>

## Findings
Coming soon....