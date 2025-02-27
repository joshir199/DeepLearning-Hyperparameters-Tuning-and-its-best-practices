# DeepLearning-Hyperparameters-and-its-best-practices
Understanding various Hyperparameters in-depth using research papers and mentioning its best practices.

This repo provides detailed study about the important hyperparameter used in training process of Deep Learning.
1. Learning Rate
2. Batch Size
3. Choosing proper parameter normalization layer (not exactly a hyperparameter)

************************************************************
# 1. Learning Rate
   
   One of the most important performance optimization for DNNs is to train a deep learning model capable of achieving high test accuracy. It varies between range of 0 and 1.

   Choosing a proper learning rate can be difficult. A too small learning rate may lead to slow convergence, while a too large learning rate can deter convergence and cause the loss function to fluctuate and get stuck in a local minimum or even to diverge.

   Decaying Learning Rates use different forms of decay functions to improve the convergence speed of deep Learning model training by LR annealing. Some of them includes, Step decay, Variable Step decay, Cyclic Decay and Warm-up decay.

![](https://github.com/joshir199/DeepLearning-Hyperparameters-Tuning-and-its-best-practices/blob/main/Learning%20Rate/images/training_with_different_LRs.png)

   Also, LR benchmarking system can be used that provides automated or semi-automated tuning and optimization for finding and selecting a good LR policy when DNN developers or endusers have chosen the dataset and the DNN model for training.


********************************************************
# 2. Batch Size

Batch size hyperparameter is the number of input data used to update the gradients per time. Its number can vary from 1 input data to all the input data of the dataset.

Batch sizes are mostly in the power of 2 with a range of (1, 2, 4, 8, 16, ..., 512, 1024). These batch sizes are divided as small batch size (<= 32) and large bacth size (>= 64).
Both part of batch size has its own limitation and usecases and depends on the other hyperparameters like learning rate.

**********************************************************
# 3. Normalization Layer

There are different forms of Normalization layers which can be used instead of default Batch Normalization.

With the increase in complexity of Deep Learning model, Group Normalization techniques are now getting popular.

Group Normalisation has been proved to be independent of batch size changes while Batch Normalisation is very much dependent on it.

Other factor is use of different set of other hyperparameters like Batch size and learning rate also influence use of specific Normalization method.

Group Normalisation Reference : ![here](https://youtu.be/m3TN9FFmqsI?si=YgVGZRQW7SnYoi3h)

