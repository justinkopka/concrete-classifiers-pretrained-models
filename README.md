# concrete-classifiers-pretrained-models
This project is part of the IBM AI Engineering Professional Certificate program. It provides a hands-on opportunity to explore fine-tuning pre-trained convolutional neural networks (CNNs) — specifically, ResNet50 and VGG16 from Keras — for a binary image classification task.

The objective is to classify images of concrete as either cracked or not cracked, using transfer learning techniques.

# Project Overview
Data Preparation:

Each script uses Keras's ImageDataGenerator to download, augment, and prepare the dataset for training, validation, and testing.

Model Architecture:

The pre-trained VGG16 or ResNet50 models are imported without their top classification layers. A new Sequential model is constructed by adding a single dense output layer (binary classification) on top.

Fine-Tuning Approach:

Only the final added layer's parameters are set to be trainable; the base pre-trained layers are frozen to retain learned features.

Models are trained in batches for efficient learning.

Training Details:

Optimizer: Adam

Loss Function: Categorical Cross-Entropy

Metrics: Accuracy

# Results on Test Data

Model	Loss	Accuracy

ResNet50	0.009	99.8%

VGG16	0.011	99.6%

Both models achieve high accuracy on the test set, demonstrating the effectiveness of transfer learning for this task.
