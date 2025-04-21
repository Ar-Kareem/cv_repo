---
layout: page
title: Investigating the Dynamics of the Loss Hessian during training
description: 
    Recently in ML literature, the Hessian of the Loss in Deep Learning is a topic of great interest. In this work, we derive an efficient analytical computation of both the maximum eigenvalue and the trace of the Hessian of the Loss in addition to an analytical and empirical convergence rate of the algorithm. The algorithm is efficiently implemented using nothing but commonly used Machine Learning techniques: the forward pass and backpropagation. Then, we train over 150 models spanning over 10 thousand epochs with different hyperparameters and optimizers and run the algorithm after each epoch to empirically calculate the properties of the hessian during training. We provide empirical results for the relationship between generalizability and the hessian, in addition to several other observations that arise from this data.
img: assets/img/HESS.png
importance: 3
---
