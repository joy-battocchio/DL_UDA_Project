# DL_UDA_Project
Unsupervised domain adaptation solution for deep learning course UNITN AY 2021/22

# DL Project - Unsupervised Domain Adaptation
### Deep subdomain adaptation network
#### Battocchio Joy, Guidolin Davide



Deep learning course, AA 2021/2022

Prof. Elisa Ricci

Unsupervised Domain Adaptation:

It is often the case that after the training phase of a model, its real usage happen in a different domain (target domain) with respect to the one in which it has been trained (source domain).
This may cause a significant drop in the performance of the model.
If some data of the target domain are available, but its ground truth labels are not, it is possibile to improve the performance via the so called *unsupervised domain adaptations*.
There are many examples of different techniques that implement UDA in the literature, here we present ours.

The first model is simply an implementation of the paper: [Deep Subdomain Adaptation Network for Image
Classification](https://arxiv.org/pdf/2106.09388.pdf).

The idea is to use a simple **domain alignment loss**, but instead of compute it globally, use a self-supervised method to compute on each sub-domain.
A sub-domain is composed of all the samples belonging to a specific class, for both domains. Since we can not access the ground truth labels of the target domain, we will use the predictions.
We implemented the loss as described in the paper, but decided to make some changes in the model and the optimizer.

We then improved its performance by adding a **global shift loss** and stibilizing the training through a simple **self-supervised loss**.

Dataset:

In this assignment we train and evaluate our model on a subset of the *Adaptiope* object recognition dataset, using two of its domain (*real world* and *product*) and only 20 out of the 123 classes.


## What is in the repo
- DSAN notebook (official delivery for the project)
- Adversarial feature notebook (not working)

## How to run DSAN notebook
- Download [Adaptiope dataset](https://drive.google.com/file/d/1FmdsvetC0oVyrFJ9ER7fcN-cXPOWx2gq/view)
- Add the zip at your Google Drive, path: gdrive/My Drive/datasets/Adaptiope.zip
- Run cells in order
