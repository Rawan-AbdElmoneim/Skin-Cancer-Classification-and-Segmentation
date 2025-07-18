# Skin Cancer Classification and Segmentation

## Overview
This project implements a multi-task deep learning model for simultaneous skin cancer classification and lesion segmentation using the HAM10000 dataset. The model performs two key tasks:
1. **Classification**: Identifying 7 types of skin lesions (MEL, NV, BCC, AKIEC, BKL, DF, VASC)
2. **Segmentation**: Precisely segmenting the lesion areas in the images

## Dataset
The HAM10000 dataset contains:
- Images of skin lesions
- Corresponding segmentation masks
- Ground truth labels for 7 classes


## Model Architecture
The implementation uses a **multi-task ResNet-18** architecture with:
- **Shared backbone**: Pre-trained ResNet-18 (features extraction)
- **Classification head**: Custom fully-connected layers
- **Segmentation head**: Decoder with transposed convolutions

### Key Features:
- Total parameters: <60 million (meets requirement)
- Weighted loss function to handle class imbalance
- Batch normalization and dropout for regularization
- Multi-task learning (shared feature extraction)

## Evaluation Metrics
### Classification:
- Overall accuracy
- Confusion matrix
- Per-class precision, recall, and F1 score

### Segmentation:
- Dice coefficient
- Intersection over Union (IoU)


## Results
The model achieves:
- Classification accuracy on test set
- Mean Dice coefficient for segmentation
- Mean IoU for segmentation

