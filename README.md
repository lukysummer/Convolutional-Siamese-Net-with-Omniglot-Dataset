# Convolutional Siamese Network with Omniglot Dataset (PyTorch)

This is a code implementation of [this paper](https://www.cs.cmu.edu/~rsalakhu/papers/oneshot1.pdf).

The code was mainly referenced from sources listed at the bottom.

## One-Shot Classification
The purpose was to train **One-Shot Classification** task, where during TESTING stage, given ONE example of a novel class (= a new class, never seen during training),
predicting its class correctly.

Specifically, using Omniglot Dataset, given an image of a novel character (let's call it *main character*) and images of novel characters of which ONE is same as the *main character*, the task is to identify which of the novel characters is the *main character*. 

## Convolutional Siamese Network
* uses the **distance** between the encoding vectors of two images to measure the *Similarity Score* of the two. 
* using this score, it tries to decide if the two images are of the same class or different classes 

## Dataset

Downloadable from [here](https://github.com/brendenlake/omniglot).

I only used:
* /python/images_background.zip (training & validation)
* /python/images_evaluation.zip (one-shot classification testing)

**Important Note** : 

* Input and output of the network is NOT an image and its class
* It is pair of images and the fact that the two are from same class (1.0) or different classes (0.0)
		  
## Results

I reached the best one-shot classification testing accuracy of ~75%. 

*If any of the readers have an idea to improve the accuracy, please suggest one in Issues section.*

## Sources

* https://github.com/fangpin/siamese-pytorch
* https://towardsdatascience.com/building-a-one-shot-learning-network-with-pytorch-d1c3a5fafa4a
* https://github.com/ttchengab/One_Shot_Pytorch
