### **Terrain Classification Using CNN**
This project implements a Convolutional Neural Network (CNN) for terrain classification using various optimizers. The aim is to explore the impact of different optimization strategies on model performance. The dataset comprises images representing five different terrain types, and the model was trained using Keras and TensorFlow.


### **Project Overview**
The primary goal of this project is to classify images of terrain into one of five categories. The CNN model leverages multiple convolutional, pooling, and fully connected layers to extract features from the images and make predictions.

###  **Model Architecture**
The architecture used for all versions of the model includes:

- **Input Layer:** 64x64 RGB images.
- **Convolutional Layers:** Three convolutional layers with ReLU activation, consisting of 32, 64, and 128 filters, respectively.
- **Pooling Layers:** MaxPooling layers after each convolution to reduce spatial dimensions.
- **Fully Connected Layers:** Two fully connected layers with 1024 units each, followed by a final dense layer with 5 output units for classification.
- **Batch Normalization:** Applied after each convolution and dense layer to stabilize learning.
- **Dropout:** Introduced between fully connected layers to prevent overfitting.
  

### **Optimizers Tested**
The following optimizers were used to compile the models:


**RMSprop (Terrain_V6)**

**Parameters:** Learning Rate = 0.001
**Results:**

- Final Training Accuracy: 0.7767
- Final Validation Accuracy: 0.8846

![image](https://github.com/user-attachments/assets/bb63b0a7-e1d0-48a4-a313-51853f22e7e3)


**RMSprop (Terrain_V6-Copy 1)**

**Parameters:** Learning Rate = 0.001
**Results:**

- Final Training Accuracy: 0.7842
- Final Validation Accuracy: 0.8077

![{26FCEE34-8C69-42F2-824A-47E1293D3B01}](https://github.com/user-attachments/assets/da242312-28dc-49c9-b8ff-026383e8068f)


**ADAM (Terrain_V4-Copy 1)**

**Results:**

- Final Training Accuracy: 0.7643
- Final Validation Accuracy: 0.8269

![image](https://github.com/user-attachments/assets/4a8741b3-4828-4cd1-8f25-2cbbf7f6adf4)




**SGD with Momentum (Terrain_V5)**

**Parameters:** Learning Rate = 0.01, Momentum = 0.9
**Results:**

- Final Training Accuracy: 0.7583
- Final Validation Accuracy: 0.8077

![{40658373-D866-4690-AD00-47471B936129}](https://github.com/user-attachments/assets/58036ad5-b0f1-43a9-bc00-eb63d80205f8)



**Adagrad (Terrain_V7)**

**Parameters:** Learning Rate = 0.01
**Results:**

- Training Accuracy: 0.7439
- Validation Accuracy: 0.7692

![image](https://github.com/user-attachments/assets/79c9970f-85b9-4c32-b7ca-07802a2c5a7d)


### **Findings and Unique Insights**
**1. SGD with Momentum (Terrain_V5)**
**Observation:**
Steady but slower improvement in accuracy. The model showed a tendency to plateau after a certain number of epochs, indicating a need for better learning rate tuning or decay scheduling.

**2. RMSprop (Terrain_V6)**
**Observation:**
Achieved the best validation accuracy among the optimizers. RMSprop adapts learning rates effectively, particularly useful in non-stationary data scenarios like high-variance image datasets. Its quick convergence enhances both training and validation accuracy, though it may risk overfitting.

**3. Adagrad (Terrain_V7)**
**Observation:**
Moderate performance with an early convergence tendency due to its adaptive learning rate mechanism. While beneficial for sparse data, this optimizer struggled in this task, indicating a plateau in performance.

### Key Learnings

**1. Optimizer Choice Matters:** The optimizer significantly impacts training speed and final accuracy. RMSprop yielded the best results for this dataset due to its adaptive learning capabilities.
**2. Effect of Batch Normalization:** It stabilizes and accelerates training, especially in deeper layers, preventing gradient explosion or vanishing.
**3. Dropout and Overfitting:** Introducing Dropout layers at 20% effectively reduced overfitting. Without it, training accuracy was disproportionately higher than validation accuracy.
**4. Learning Rate Scheduling:** Dynamic scheduling with optimizers like SGD and RMSprop enhanced performance, while Adagrad's built-in adaptation sufficed for convergence.

**Conclusion**
This project underscores the importance of selecting the appropriate optimizer based on the dataset and problem type. RMSprop emerged as the best performer for terrain classification, whereas Adagrad exhibited limited effectiveness. SGD with Momentum may improve with further training epochs or refined learning rate scheduling.
