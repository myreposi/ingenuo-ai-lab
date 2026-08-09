
# 01-Foundations: Deep Learning (DL)

## 1. What is Deep Learning?
Deep Learning is a specialized subset of Machine Learning that relies on artificial neural networks with multiple layers (hence "deep") to model complex, non-linear relationships in data. Unlike traditional Machine Learning, which often requires manual feature engineering, Deep Learning architectures can automatically discover representation features directly from raw inputs like text, images, and audio.

## 2. Core Architectural Components

### A. Artificial Neural Networks (ANN)
The baseline architecture modeled after biological brains. 
* **Input Layer**: Receives the raw features or dataset dimensions.
* **Hidden Layers**: Interconnected node layers that perform mathematical transformations to extract abstract patterns.
* **Output Layer**: Yields the final model prediction or classification array.

### B. Computational Neurons (Perceptrons)
The fundamental computational unit of a network layer.
* **Weights & Biases**: Parameters adjusted during training to control signal strength and shift activation scales.
* **Activation Functions**: Mathematical operations that introduce non-linearity, allowing networks to learn complex boundaries.
  * *Examples*: ReLU (Rectified Linear Unit), Sigmoid, Tanh.

## 3. Training & Optimization Mechanics
* **Forward Propagation**: Passing input data through the network layers to calculate an output prediction.
* **Loss Function**: A mathematical function quantifying the exact distance between the prediction and the true target value.
* **Backpropagation**: An algorithm calculating gradients of the loss function relative to all network weights using the mathematical chain rule.
* **Optimizers**: Algorithms that iteratively update network weights to minimize the loss value.
  * *Examples*: Stochastic Gradient Descent (SGD), Adam (Adaptive Moment Estimation).

## 4. Specialized Deep Architectures
* **Convolutional Neural Networks (CNNs)**: Designed to process grid-structured data like images by using convolutional filters to preserve spatial hierarchies.
* **Recurrent Neural Networks (RNNs)**: Built with internal feedback loops to process sequential data like time-series or text, though heavily bottlenecked by memory degradation over long sequences.
* **Transformers**: The modern industry standard that replaces recurrence with attention mechanisms to process sequences in parallel (the direct pathway to modern LLMs).
  
