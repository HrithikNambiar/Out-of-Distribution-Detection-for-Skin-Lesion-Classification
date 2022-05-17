# Out-of-Distribution-Detection-for-Skin-Lesion-Classification
Deep Learning (CS F425): Course Project

Report: 

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
  * Densenet : DenseNet attained the best result among the 3 DNN models tested on. 82.98% validation accuracy after training for 8 epochs (due to compute limitations).
  
## Pitfalls of DNN
   ### OOD Data
   Densenet gives high confidence predictions on OOD datasets listed above. This is a major problem in the current DNNs.

## Existing OOD methods
  ### ODIN - "ENHANCING THE RELIABILITY OF OUT-OF-DISTRIBUTION IMAGE DETECTION IN NEURAL NETWORKS"
  Paper: [ODIN](https://arxiv.org/pdf/1706.02690.pdf)
  #### Results
  
## VOS: LEARNING WHAT YOU DON’T KNOW BY VIRTUAL OUTLIER SYNTHESIS
  Paper: [VOS](https://openreview.net/pdf?id=TW7d65uYu5M)
  
## Ours (Training using outlier synthesis and using ODIN inference method)

We have used the training strategy proposed by VOS and used the inference method suggested in
ODIN.

## Results

![Result](AAD6B208-2D2E-4A0A-BAF2-C93CB4DCB164.jpeg)

![FPR95](BC24C137-23A7-4A9F-BF68-B98A421BCF26.jpeg)
## Our contributions

* Identifying the problem of OOD data in the current Skin cancer classifiers and attempting to alleviate it using current SOTA OOD detection algotithms.
* Combining the training method proposed in VOS using outlier synthesis with the promising inference methods proposed in ODIN.
* Studying the effects on different OOD datasets.

## Possibilities of future work

* We believe that VOS requires longer epochs of training since virtual outliers can only be efficiently sampled from the low-likelihood regions only after the distribution has been learned sufficiently well. Training using this strategy does seem to improve the results, however, we were unable to train for longer epochs due to the limitations in compute and time.
* Using the OOD prediction branch of VOS and doing inference using it might work well, if we train VOS for longer epochs.

## Contributors:

* Vishwa Shah
* Hrithik Nambiar
* Preeyam Sahu

