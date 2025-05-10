# Xception_V1 - Terrain Classifier

This model uses the Xception architecture from Keras applications to classify terrain types. It achieves improved accuracy compared to earlier CNNs.

## Architecture
- Base model: Xception (pretrained on ImageNet)
- Added:
  - GlobalAveragePooling
  - Dense(1024, relu)
  - Dense(num_classes, softmax)

## Performance
- Accuracy: 92.8% on test set
- Included metrics: Precision, Recall, F1-Score, Confusion Matrix

## Notes
- Training done on resized images (150x150)
- EarlyStopping and ReduceLROnPlateau used
- Dataset same as original repo
