# Kidney disease classification using VGG16  CNN

## Overview

This project applies a Convolutional Neural Network & VGG16 CNN to classify images from a kidney dataset. The model is trained to detect and differentiate kidney-related conditions through image analysis, providing an efficient approach to medical image classification.

## Project Goals

This project aims to develop an accurate image classification model using a Convolutional Neural Network & VGG16 CNN to assist in detecting kidney-related medical conditions from imaging data.

## Dataset

The CT-KIDNEY-DATASET-Normal-Cyst-Tumor-Stone contains **12,446 records**. These records include fetal health classifications annotated into 4 classes:
- **Normal**
- **Cyst**
- **Tumor**
- **Stone**

## Methodology

### 1. **Data Preprocessing**
- **Rescaling Pixel Values**: All datasets (training, testing, and validation) are processed using ImageDataGenerator, which rescales pixel values from 0-255 to 0-1 by dividing by 255. This normalization helps improve model convergence during training.
- **Image Size Adjustment**: Images are resized to a target size of (180, 180) pixels. This standardization ensures that all input images have consistent dimensions, facilitating batch processing in deep-learning models.
- **Categorical Class Encoding**: The datasets utilize class_mode='categorical', indicating that the target labels are one-hot encoded. This setup is essential for multi-class classification tasks, allowing the model to distribute probability over multiple classes.
- **Data Splitting**: The dataset was split into **80% training**, **10% validation** and **10% testing** sets using the `train_test_split` function from scikit-learn.

### 2. **Machine Learning Models**
We implemented and evaluated the following models:
- **VGG16 CNN**
-  **CNN**


## Results

- The **CNN** model achieved the highest performance with an accuracy of **99.92%**.

| Model                  | Accuracy (%) | Precision (%) | Recall (%) | F1-Score (%) |
|------------------------|--------------|---------------|------------|--------------|
| **VGG16 CNN**          | 99.91        | 99.82         | 99.89      | 99.85        |
| **CNN**                | 99.92        | 99.93         | 99.89      | 99.91        |

