<div align="center">

<img width="300px" alt="Graphiti-ts-small" src="https://github.com/shadynasrat/PICaSo/blob/main/docs/PICaSo_files/static/picaso_logo.png">

## PICaSo 2.0: Real–Sim–Real Human Robot Co-Inpainting system on a Shared Physical Canvas

<br />

![UBUNTU](https://img.shields.io/badge/UBUNTU-20.04-orange?style=plastic&logo=ubuntu)
![python](https://img.shields.io/badge/python-3.9-blue?style=plastic&logo=python)
![ROS2](https://img.shields.io/badge/ROS-Noetic-white?style=plastic&logo=ros)

Project Page : [Click Here](https://shadynasrat.github.io/PICaSo/)

<br />

</div>

# Abstract
We present PICaSo 2.0, a humanoid, bi-manual robotic drawing system that performs Co-Inpainting on a shared physical canvas. Unlike one-way Sim→Real or prior “co-painting” approaches that mainly add content, Co-Inpainting is two-way and local: people draw/erase directly on the board; the system captures those on-surface changes, synchronizes a digital line-art state, and then executes mask-guided erase-then-redraw in that exact region within a Real→Sim→Real loop. Execution is embodied bi-manually for role legibility (left erases, right draws). PICaSo 2.0 reuses the line-art–biased inpainting and waypoint pipeline from PICaSo 1.0, with addition camera-feedback loop allowing translating human edits into the inpainting loop. We demonstrate the system in a single-canvas, 10-turn alternation with 10 volunteers (five human on-surface edits interleaved with five robot, mask-conditioned edits), and in two shorter replications (2 human + 2 robot), showing the ability and scalability of the system. To our knowledge, PICaSo 2.0 is the first system to allow human-robot co-inpainting within one closed loop on the same physical canvas. The fine-tuned line-art inpainting model is already public; we will release code, evaluation scripts, and an anonymized dataset from the study.


<br />

<p align="center">
    <img src="/docs/PICaSo_files/preview.gif" width="700px">   
</p>

<br />



# Roadmap

Here’s what we’ve accomplished and what’s coming soon:

- [x] Launched project website
- [ ] Implement inference code with ROS2 integration
- [ ] Publish fine-tuned models

# Overview

Our approach involves editing on a physical canvas and publishing the resulting waypoints to a ROS2 topic. This simplifies the integration with various robotic arms, enabling seamless compatibility and deployment.


# Installation
```
pip install -r requirements

python main.py
```





## bibtex
```
@inproceedings{PICaSo,
  author={Shady Nasrat, Jae-Bong Yi, Minseong Jo, and Seung-joon Yi},
  booktitle={2024 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
  pages={xxxx--xxxx},
  year={2024},
  organization={IEEE}
}
```
