# MLCapstone
ML Capstone Project: Stanford Dogs Image Recognition

Model Architecture & Training
We used a pre-trained ResNet-50 from the Transformers library, fine-tuned on the Stanford Dogs dataset. The model consists of convolutional layers, global average pooling, and a classification head modified for 120 dog breeds.
Due to Mixup and CutMix augmentation blending images from multiple classes (e.g., 60% Corgi + 40% Golden Retriever), we used Soft Target Cross Entropy loss during training to handle fractional labels. Standard Cross Entropy was used for validation and testing.
Data Augmentation
Training used aggressive augmentation to prevent overfitting:

RandAugment: Random sequences of rotation, shearing, and color jittering
Random Erasing: 25% probability to occlude image regions
Mixup & CutMix: Blending multiple images and labels
Random translations and crops

Validation and test sets used only resizing and normalization.

## Training

**Note:** This model was trained on Kaggle's GPU infrastructure. 
Training takes approximately 4 hours on a GPU and is not recommended 
for local execution without GPU access.

To reproduce:
1. Upload to Kaggle or Google Colab
2. Enable GPU runtime
3. Run the training script
