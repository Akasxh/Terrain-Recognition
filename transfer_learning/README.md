# EfficientNet for Terrain Classification

This project uses EfficientNet-B0 for terrain classification, achieving high accuracy in distinguishing between different terrain types.

Model Performance:

- Validation Accuracy: 91.93%
- Test Accuracy: 92.40%

### Key Training Parameters:

- **Optimizer**: Adam
- **Learning Rate**: 1e-4 (tuned to optimize the learning of the pre-trained model)
- **Batch Size**: 32
- **Loss Function**: Cross-entropy loss
- **Number of Epochs**: 25
- **Early Stopping**: Implemented based on validation accuracy to prevent overfitting
- **Data Augmentation**: Horizontal flip, random crop, rotation
- **Preprocessing**: Images resized to 224x224 and normalized to align with EfficientNet's input requirements

## EfficientNet: Brief Overview

EfficientNet is a convolutional neural network architecture and scaling method that uniformly scales all dimensions of depth/width/resolution using a compound coefficient. This results in a family of models that achieve state-of-the-art accuracy with much fewer parameters and FLOPs than traditional convolutional networks.

### Key Features:

1. **Compound Scaling**: Balances network depth, width, and resolution for optimal performance.
2. **Mobile Inverted Bottleneck Convolution (MBConv)**: Efficient building block that reduces parameters while maintaining performance.
3. **Squeeze-and-Excitation (SE) blocks**: Improves channel interdependencies at almost no computational cost.

## Architectural Diagram

```
Input Image
    │
    ▼
Stem Conv3x3
    │
    ▼
MBConv1, 3x3
    │
    ▼
MBConv6, 3x3
    │
    ▼
MBConv6, 5x5
    │
    ▼
MBConv6, 3x3
    │
    ▼
MBConv6, 5x5
    │
    ▼
MBConv6, 5x5
    │
    ▼
MBConv6, 3x3
    │
    ▼
Conv1x1 & Pooling
    │
    ▼
Fully Connected
    │
    ▼
Output (5 classes)
```

Each MBConv block includes Squeeze-and-Excitation optimization.

## Model Specifications (EfficientNet-B0)

- **Parameters**: Approximately 4 million
- **Model Size**: Around 15.6 MB
- **Memory Usage**: Around 34.7 MB
- **Inference Speed**:
  - CPU: ~30-60ms per image
  - GPU: ~10-15ms per image
    (Actual speed may vary based on hardware and image size)

## How It Works

1. **Input Processing**: Images are resized to 224x224 and normalized.
2. **Feature Extraction**: The EfficientNet backbone extracts hierarchical features from the input image.
3. **Global Pooling**: Features are pooled to create a fixed-size representation.
4. **Classification**: A fully connected layer maps the features to 5 terrain classes.
5. **Output**: Softmax activation provides class probabilities.

## Training and Optimization

We use a pre-trained EfficientNet-B0 model (trained on ImageNet) and fine-tune it for our terrain classification task. This approach leverages general features learned from a large dataset and adapts them to our specific problem, resulting in faster training and better performance.

### Training Process:

1. **Transfer Learning**: The pre-trained weights are loaded and frozen initially.
2. **Fine-tuning**: After the first few epochs, the top layers are unfrozen, and the model is fine-tuned using a low learning rate.
3. **Batch Normalization Layers**: These layers remain in training mode during fine-tuning to adjust to the new data.

### Evaluation:

- **Accuracy**: Monitored for each epoch using both the validation and test datasets.
- **Confusion Matrix**: Used to visualize the distribution of predictions across the 5 terrain classes.
- **Precision, Recall, F1 Score**: Calculated to evaluate performance across classes with imbalanced representation.
- **Loss**: Monitored during training and validation to ensure optimization.

## Usage

To use a model for terrain classification:

- Update relevant paths in transfer_learning.ipynb
- run transfer_learning.ipynb

To load and use pretrained model

- run load_model.ipynb

To check inference rates of model

- run cal_inference.ipynb
