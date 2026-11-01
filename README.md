# DMA-Net

Official implementation of **"DMA-Net: Degradation-Aware Multi-Domain Adaptive
Network for Joint Remote Sensing Image Deblurring and Super-Resolution"**,
submitted to *Knowledge-Based Systems*.

## Notice

:warning: **The source code is currently being organized and will be made publicly
available in this repository upon acceptance of the paper.**

**注意：所有代码正在整理中，将在论文被接收后于本仓库完整公开。**

## Overview

DMA-Net is a fully differentiable, degradation-aware dual-branch network for joint
remote sensing (RS) image deblurring and super-resolution (SR), embedding
degradation awareness into the representation, interaction and objective levels:

- **DDKB (Differentiable Dynamic-Kernel Block)**: softly mixes a multi-scale
  depthwise kernel bank of sizes {1, 3, 5, 7} with per-pixel softmax weights and a
  learnable temperature, so the effective receptive field adapts continuously to
  the local blur strength
- **LMAB (Low-complexity Multi-domain Attention Block)**: unifies a fully
  differentiable learnable wavelet-like transform, a resolution-agnostic spectral
  filter generated from normalized frequency coordinates, and a four-direction
  selective state-space scan, at near-linear cost in the number of spatial tokens
- **TCAF (Transposed Cross-Attention Fusion)**: exchanges channel-axis context
  bidirectionally between the deblurring and SR branches and fuses the enhanced
  features with per-pixel weights
- **DAW (Degradation-Adaptive Wiener loss)**: a lightweight degradation estimator
  predicts an orientation-dependent noise-to-signal profile for each training
  image, supervised by a closed-form target, so that the frequency-domain
  regularization adapts to the degradation of every sample (training only)

## Results

- On RSSCN7 at ×2, DMA-Net-L attains **29.35 dB PSNR / 0.7565 SSIM** with only
  10.4M parameters and 24.4G FLOPs, surpassing the strongest joint baseline by
  0.87 dB at about one fifth of its parameters
- Restored images raise downstream scene classification to **94.05%** accuracy and
  semantic segmentation to **37.24% mIoU**

## Contact

- Zhen Yang: yangzhen19970821@nuaa.edu.cn
- Yin Zhang (Corresponding author): zhangyin1986@nuaa.edu.cn

College of Astronautics, Nanjing University of Aeronautics and Astronautics,
Nanjing 211106, China
