
Premise: **Deeper** Neural networks are more difficult to train. 
What the paper presents: A Learning framework (Residual) to ease the training of networks that are substantially deeper. 

Explicitly reformulate the layers as learning residual functions with reference to the layer inputs instead of learning unreferenced functions. 

This framework works really well on Really deep neural networks , 152 layers, 8x deeper than VGG. with lower error rates. 

![[Resnet.png]]

### The Need for ResNet

We add additional layers to a deep neural network to train complex features that get us improved accuracy and performance. 

But it has been found that there is a threshold for depth with traditional convolutional neural networks. 

### Convolutional Neural Networks - The basics. [[Convolutions.]]
Convolutional neural networks learn directly from images and comprise of multiple layers. These are primarily used for image classification and segmentation. Primarily used for image analyses tasks. 

each layer detects maps and detects something different. 

- Train CNNs from scratch - Accurate but Difficult. 
- Transfer Learning - Use knowledge from one problem to solve a different problem ( Sort of like fine tuning.)
- Pretrained CNN to extract features. 

Three of the most common layers are **convolution**, **activation or ReLU** and **Pooling**

Convolution : Puts the input images through a set of convolutional filters, each of which activates certain features from the images. Convolutional Filters go over the whole image convolutionally and pick up the most activated pixels. 


#### Key Concepts; 
1. Local receptive fields
	 - Only a small region of input neurons are connected to neurons in the hidden layer, as in contrast to traditional neural networks, where each input neuron is connected to neurons in the hidden layer. You can use convolutions to implement local receptive fields. 
2. Shared weights and biases
	- has weights and biases like typical neural networks. 
	- However in the case of CNNs, all weights and biases are the same for a given layer. 
	- All given neurons are detecting the same feature. 
1. Activation and Pooling
	- Activation step applies a transformation to the output of a neuron (ReLU)
	- Pooling reduces the dimesionality of the feature map, by condensing the output of small regions into a single value. This helps simplify the layers and makes training easier. 



Let's look at a sample script: 

