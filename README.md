# DMA-Net

Official implementation of **"DMA-Net: Degradation-Aware Dual-Branch Network for Joint Remote Sensing Image Deblurring and Super-Resolution"**, submitted to *IEEE Transactions on Geoscience and Remote Sensing*.

## Notice

:warning: **The source code is currently being organized and will be made publicly available in this repository upon acceptance of the paper.**

**注意：所有代码正在整理中，将在论文被接收后于本仓库完整公开。**

## Overview

DMA-Net is a fully differentiable, degradation-aware dual-branch network for joint remote sensing image deblurring and super-resolution, featuring:

- **DDKB**: Differentiable dynamic-kernel block with per-pixel softmax weights over a multi-scale depthwise kernel bank
- **LMAB**: Low-complexity multi-domain attention block integrating a learnable wavelet transform, a resolution-agnostic spectral filter, and a four-direction selective state-space scan
- **TCAF**: Transposed cross-attention fusion module for bidirectional information exchange between branches
- **DAW**: Degradation-adaptive Wiener loss with closed-form supervision of a per-image radial noise-to-signal profile

## Contact

- Zhen Yang: yangzhen19970821@nuaa.edu.cn
- Yin Zhang (Corresponding author): zhangyin1986@nuaa.edu.cn

College of Astronautics, Nanjing University of Aeronautics and Astronautics, Nanjing 211106, China
