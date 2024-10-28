# Terrain Recognition using Transfer Learning

This project is focused on classifying images into five terrain classes: **Coast**, **Forest**, **Glacier**, **Mountain**, and **Desert**. We used transfer learning with **ConvNeXT Tiny** and **MobileNetV2** architectures to leverage pre-trained models for effective terrain classification. This README provides an overview of the models, transformation parameters, accuracy results, and detailed model parameters.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset and Classes](#dataset-and-classes)
3. [Model Architecture](#model-architecture)
4. [Image Preprocessing and Transforms](#image-preprocessing-and-transforms)
5. [Model Parameters and Sizes](#model-parameters-and-sizes)
6. [Results and Evaluation](#results-and-evaluation)
7. [Conclusion](#conclusion)

---

## Project Overview

The primary goal of this project is to perform accurate terrain classification using transfer learning. Two models—**ConvNeXT Tiny** and **MobileNetV2**—were chosen for their balance of accuracy and efficiency, and each model was fine-tuned to classify images into five terrain types.

## Dataset and Classes

The dataset consists of images belonging to the following classes:

1. **Coast**
2. **Forest**
3. **Glacier**
4. **Mountain**
5. **Desert**

Each image is preprocessed and transformed to ensure compatibility with the models and maximize classification accuracy.

---

## Model Architecture

### 1. ConvNeXT Tiny

ConvNeXT Tiny is a convolutional model inspired by the Swin Transformer, optimized for image classification tasks. It provides high accuracy with minimal computational cost.

**Model Summary:**
- **Architecture**: ConvNeXT Tiny
- **Number of Parameters**: *27,823,973*
- **Input Image Size**: 224x224
- **Layer Configuration**: Standard ConvNeXT Tiny layers
- **Pre-trained Weights**: ImageNet

### 2. MobileNetV2

MobileNetV2 is a lightweight model designed for efficient use on mobile devices while maintaining high accuracy for tasks like image classification.

**Model Summary:**
- **Architecture**: MobileNetV2
- **Number of Parameters**: *2,230,277*
- **Input Image Size**: 224x224
- **Layer Configuration**: Standard MobileNetV2 layers
- **Pre-trained Weights**: ImageNet

---

## Image Preprocessing and Transforms

For each model, specific image transformations were applied to prepare the images for the classification task.

### ConvNeXT Tiny Transforms
```python
test_transforms = transforms.Compose([
    transforms.Resize((224,224 )),
    transforms.ToTensor(),
    transforms.Normalize(mean=[0.485, 0.456, 0.406], std=[0.229, 0.224, 0.225])
])
```

### MobileNetV2 Transforms
```python
test_transforms = transforms.Compose([
    transforms.Resize((224, 224)),
    transforms.ToTensor(),
    transforms.Normalize(mean=[0.485, 0.456, 0.406], std=[0.229, 0.224, 0.225])
])

```

Both models use the same normalization parameters, consistent with ImageNet pre-trained weights.

---

## Model Parameters and Sizes

Here is a comparison of the parameters and model sizes:

| Model          | Number of Parameters | Model Size (MB) |
|----------------|----------------------|------------------|
| ConvNeXT Tiny  | 27.8 million            | *106 MB*  |
| MobileNetV2    | 2.2 million            | *9.71 MB*  |
* Size may vary
---

## Results and Evaluation

### ConvNeXT Tiny
- **Accuracy**: *92.11%*
- **Loss**: *.2168*

**Confusion Matrix**  
![Confusion Matrix for ConvNeXT](https://github.com/Shreyansh-G/Terrain-Recognition/blob/main/transfer_learning/images/confconnet.jpg?raw=true)

**Model Architecture**  
![ConvNeXT Architecture](https://github.com/Shreyansh-G/Terrain-Recognition/blob/main/transfer_learning/images/convnextarch.jpg?raw=true)

**Model Accuracy Curve** 
![ConvNext Accuracy](https://github.com/Shreyansh-G/Terrain-Recognition/blob/main/transfer_learning/images/convnextaccu.jpg?raw=true)

---

### MobileNetV2
- **Accuracy**: *91.33%*
- **Loss**: *.2798*

**Confusion Matrix**  
![MobileNetV2 Confusion Matrix](https://github.com/Shreyansh-G/Terrain-Recognition/blob/main/transfer_learning/images/confnet.jpg?raw=true)

**Model Architecture**  
![MobileNetV2 Architecture](https://github.com/Shreyansh-G/Terrain-Recognition/blob/main/transfer_learning/images/mobilenetarch.png?raw=true)

**Model Accuracy Curve** 
![MobileNetV2 Accuracy](https://github.com/Shreyansh-G/Terrain-Recognition/blob/main/transfer_learning/images/mobilenetacc.jpg?raw=true)

---

## Conclusion

This project demonstrates the effective use of transfer learning for terrain classification. While **ConvNeXT Tiny** offered higher accuracy, **MobileNetV2** showed competitive results with a lighter model size, making it suitable for mobile applications. Both models effectively classified the terrains, with each model offering unique advantages depending on the deployment context.

---

## How to Run

1. Clone the repository.
   ```bash
   git clone https://github.com/Akasxh/terrain-recognition.git
   cd terrain-recognition
   ```

2. Run the notebooks
3. Enjoy the predictions

Feel free to explore, contribute, and leave feedback!

---
