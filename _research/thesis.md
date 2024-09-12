---
layout: default
title: "Thesis"
image: "/assets/img/cards/TeaserPic.png"
description: "Utilizing MAMBA blocks and Fourier transforms to predict smoke opacity."
---

## Abstract 
Computer vision has traditionally faced difficulties when applied to amorphous objects like smoke, owing to their ever-changing shape, texture, and dependence on background conditions. While recent advancements have enabled simple tasks such as smoke detection and basic classification (black or white), quantitative opacity estimation in line with the assessments made by certified professionals remains unexplored. To address this gap, I introduce the SMOKE+ dataset, which features opacity labels verified by three certified experts. My dataset encompasses five distinct testing days, two data collection sites in different regions, and a total of 13,632 labeled clips. Leveraging this data, we develop a state-of-the-art smoke opacity estimation method that employs a small number of Residual 3D blocks for efficient opacity estimation. Additionally I explore the use of MAMBA blocks in a video based architecture, exploiting their ability to handle spatial and temporal data in a linear fashion. Techniques developed during the SMOKE+ dataset creation were then refined and applied to a new dataset titled CSU101, designed for educational use in Computer Vision. In the future I intend to expand further into synthetic data, incorporating techniques into Unreal Engine or Unity to add accurate opacity labels.