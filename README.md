# Experiment_with_conditional_DCGAN
Experiment with DCGAN by adding conditional context information

In this project, I have using the code from [DCGAN_example](https://github.com/pytorch/examples/tree/master/dcgan) from the PyTorch tutorial as my base skeleton for the work. Without any changes to the code, the model takes a dataset, and a discrimintor and generator will be trained and stored. 

As for the generator, it generates random pictures similar the the data it is fed. Besides generating only random images, I want to control the content of an iamge based on its class label (Dataset which I used for this project were MNIST hand-written digits and CiFar10). The idea of using conditional GAN is based on [Conditional Generative Adversarial Nets](https://arxiv.org/abs/1411.1784). In addtional to using just a one-hot embedding for the context information, I used also pre-trained GloVe word vectors to embed the context information. 

The results seems reasonable with using one-hot embedding while the 300d word embedding may be too complicated that further experiments need to involve dropout regularization.
