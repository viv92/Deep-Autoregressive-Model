# Deep-Autoregressive-Models

## Description
In this project, we explore deep autoregressive models for density estimation such as Neural Autoregressive Density Estimator (NADE) and Masked Autoregressive Density Estimation (MADE). Our hypothesis is that deep autoregressive models such as MADE generate richer samples than those generated by mixture models such as GMM. We verify the hypothesis by training a MADE model and a GMM on 3 different datasets (MNIST, Atari frames and Anime faces) and comparing the samples generated. 

The final presentation can be found [here](Project_presentation.pdf) (relative link).

## Models explored
### 1. Neural Autoregressive Density Estimator (NADE):

<img src="imgs/nade_pgm.png" alt="nade_pgm" width="200"/>

NADE is a Bayesian Network model for density estimation having an "autoregressive property" in which the full joint probability of all random variables is given as:

<img src="imgs/nade_pdf.png" alt="nade_pdf" width="200"/>

All of the conditional distributions are modelled by a neural network:

<img src="imgs/nade_net.png" alt="nade_net" width="300"/>

<img src="imgs/nade_neteq.png" alt="nade_neteq" width="300"/>

Our implementation code for NADE with all the conducted experiments can be found in the NADE [subfolder](NADE).


### 2. Masked Autoregressive Density Estimation (MADE):

<img src="imgs/made_net.png" alt="made_net" width="500"/>

MADE is a deep, generative autoencoder capable of learning hierarchies of distributed representations from data. Its an extension of NADE where all conditional distributions are learnt using a masked variational autoencoder. The masks are generated such that they sustain the autoregressive property of the model by dropping out suitable connections. Our implementation code for MADE with all the conducted experiments can be found in the pytorch-MADE [subfolder](pytorch-MADE).

### 3. GMM (as baseline)

## Results



