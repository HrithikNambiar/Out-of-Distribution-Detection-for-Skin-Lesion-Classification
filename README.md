# Out-of-Distribution-Detection-for-Skin-Lesion-Classification
Deep Learning (CS F425): Course Project

## Abstract

Deep Neural Network models for skin lesion detection lack supervision from unknown data
and as a result, produce overconfident results on Out-Of-Distribution data. VOS (Virtual
Outlier Synthesis) is a novel framework that detects OOD examples by adaptively synthesizing
virtual outliers that can meaningfully regularize the model’s decision boundary during training.
Specifically, VOS samples virtual outliers from the low-likelihood region of the class conditional
distribution estimated in the feature space. It also introduces a novel unknown-aware training
objective, which contrastively shapes the uncertainty space between the In-Distribution data
and synthesized outlier data. In this work, we study the problems dealing with OOD data
for skin cancer classification and compare the performance of VOS with other State-of-the-art
methods.

## Datasets

  In Distribution Dataset
  * HAM 10000 

  Out-Of-Distribution Datasets
  * Derm Skin
  * Clin Skin
  * BBOX
  * BBOX 70
  * NCT
  * Imagenet

## Deep Learning Architectures for training on ID dataset
  * Resnet50
  * VGG
  * Densenet
  DenseNet attained the best result among the 3 DNN models tested on. 82.98% validation accuracy after training for 8 epochs (due to compute limitations).
  
## Pitfalls of DNN
   ### OOD Data
   Densenet gives high confidence predictions on OOD datasets listed above. This is a major problem in the current DNNs.

## Existing OOD methods
  ### ODIN - "ENHANCING THE RELIABILITY OF OUT-OF-DISTRIBUTION IMAGE DETECTION IN NEURAL NETWORKS"
  Paper: [ODIN](https://arxiv.org/pdf/1706.02690.pdf)
  #### Results
  
## VOS: LEARNING WHAT YOU DON’T KNOW BY VIRTUAL OUTLIER SYNTHESIS
  Paper: [VOS](https://openreview.net/pdf?id=TW7d65uYu5M)
