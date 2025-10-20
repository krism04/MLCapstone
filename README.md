# MLCapstone
ML Capstone Project: Stanford Dogs Image Recognition

This project implements a Convolutional Neural Network (CNN) to recognize and classify images of dogs across 120 different breeds. We trained our model on a dataset of 20,000 labeled dog images, which were divided into training, validation, and testing sets. Each dataset was handled using PyTorch data loaders with a batch size of 32 and randomized shuffling for robust training.

Data can be found at: http://vision.stanford.edu/aditya86/ImageNetDogs/ or https://www.kaggle.com/datasets/jessicali9530/stanford-dogs-dataset

The CNN architecture consists of four convolutional blocks, each containing:
  * Convolutional layers for feature extraction
  * Batch Normalization to normalize pixel values (scaled from [0, 255] to [0, 1])
  * Max Pooling (2×2) to reduce spatial dimensions
  * Dropout (p=0.1) to prevent overfitting

The output from each block feeds into the next, followed by an adaptive pooling layer that averages each feature map. Model weights and biases are updated and saved after each epoch to track learning progress.
This repository demonstrates the end-to-end process of dataset handling, CNN design, and training for image classification.
