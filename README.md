# Terrain-Recognition

### Overview
This project uses a Convolutional Neural Network (CNN) to classify terrain types based on input images. The model achieves an accuracy of 74% on a test dataset, demonstrating its capability to recognize various terrains.

#### drive for train,test data and pre-trained model : https://drive.google.com/drive/folders/1hbL1m39TF8ABe0oCj5XYDbHXY-gPIjcQ?usp=sharing

#### Table of Contents

-[Project Description](#project-description)

-[Dataset](#dataset)

-[Model Architecture](#model-architecture)

-[Results](#results)

-[Usage](#usage)

-[Dependencies](#dependencies)

-[Acknowledgments](#acknowledgments)

### Project Description

Terrain recognition is essential in various applications, such as autonomous vehicles, robotics, and environmental monitoring. In this project, we used a CNN to classify images into five terrain categories: Coast, Desert, Forest, Glacier, and Mountain. The model was trained on a labeled dataset and evaluated on a test dataset.

### Dataset

We used a custom dataset consisting of images of different terrains. The dataset was divided into a training set and a test set. The training set was used to train the model, while the test set was used to evaluate its performance.

#### Dataset Statistics:

 Total Images: 11000

 Training Images: 10000

 Test Images: 1000

 Classes: 5 (Coast, Desert, Forest, Glacier, Mountain)

### Model Architecture

The CNN model used for terrain recognition consists of the following layers:

 Convolutional Layer 1

 Max-Pooling Layer 1

 Convolutional Layer 2

 Max-Pooling Layer 2

 Flattening Layer

 Fully Connected Layer ('relu')

 Output Layer ('softmax')

The model architecture was chosen based on experimentation and fine-tuning. The model was trained using the training dataset and optimized for accuracy.

#### Results

The trained model achieved an accuracy of 74% on the test dataset, demonstrating its ability to recognize different terrains. Here are some sample predictions:

  Coast: 80% accuracy

  Desert: 70% accuracy

  Forest: 85% accuracy

  Glacier: 65% accuracy

  Mountain: 78% accuracy

The model's performance can be further improved with additional data and fine-tuning.

#### Usage

 To use the trained model for terrain recognition, follow these steps:

 Install the required dependencies (see Dependencies).

 Load the pre-trained model using a Python script.

 Provide an image to the script, and it will predict the terrain type.

 For detailed usage instructions, refer to the project's source code and documentation.

It is recommended to do this in google collab as access to images,files and models are easier as such.

#### Dependencies

 Python 3.x

 TensorFlow (deep learning framework)

 Jupyter Notebook (for running and experimenting with the code) or use google collab

 Numpy (for data manipulation)

You can install the required Python packages using pip:

"pip install tensorflow numpy  jupyter"

### Acknowledgments

This project was developed by Team "LearnX" as part of SIH: Deep learning for terrain recognition.

#### TEAM: LearnX

TEAM LEAD: S AKASH

MEMBER 1:Vihaan Agrawal

MEMBER 2:Ruchi Chand Thakur

MEMBER 3:Manas Gupta

MEMBER 4:Tanmay Singh

MEMBER 5:Harshith Patnaik
