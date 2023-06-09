# Facial Expression Recognizer using Fully Convolutional Network
## Introduction
Facial expression recognition is a challenging task in the field of computer vision. A Fully Convolutional Network (FCN) is a type of neural network that has proven to be effective in image classification tasks. In this project, we aim to build a facial expression recognizer using an FCN.

## Architecture
The FCN architecture consists of convolutional layers that extract features from the input image and final convolutional layer that classify the image based on these features. There are no fully connected layers and the entire network is composed of convolutional layers.

## Dataset
The data used is “Facial Expressions Training Data” from https://www.kaggle.com/datasets/noamsegal/affectnet-training-data, consisting of face images labeled by facial expressions extracted from the original AffectNet dataset. As a preprocessing step to train my model, I resized cropped face images to 66x88 pixels; the aspect ratio of 3:4 allows to show more pixels of the face and less of the background. Additionally, I trained the model using the following facial expressions only: anger, disgust, fear, happy, neutral, sad, and surprise.

## Required Packages
- tqdm: for progress bar
- matplotlib: for plotting
- torch, torchvision (PyTorch): for deep learning
- torchsummary: for model summary in PyTorch
- tensorboard: to log PyTorch model metrics for visualization 
- scikit-learn: to provide various metric functions
- facenet_pytorch: for face detections
- opencv-python: for image processing


## Install
#### Using Nvidia GPU (Cuda 11.8)
```
pip3 install tqdm matplotlib scikit-learn opencv-python torch tensorboard torchsummary torchvision --extra-index-url https://download.pytorch.org/whl/cu118 facenet_pytorch
```

### Using CPU Only: 
### Although, you can use CPU Only, it would take longer time to train
```
pip3 install tqdm matplotlib scikit-learn opencv-python torch tensorboard torchsummary torchvision facenet_pytorch
```
or simply
```
pip3 install -r requirements.txt
```

## Directory Structure
Place all the files in same directory as the following:
```
├─── dataset/
├─── demo/
├─── demo.ipynb
├─── FacialExpressionsRecognizer.py
└─── fcn-facial-expressions.pt
```

This directory contains scripts used to pre-process the dataset
```
├─── utils/
```

## Running Demo
To run the demo, please run the following Jupyter Notebook: demo.ipynb

### recognition on individual face images
![image](https://user-images.githubusercontent.com/2038150/235329728-cc577851-70f5-4a4a-afca-261b62c23f6f.png)

### detect multiple faces and recognize their facial expressions
![image](https://user-images.githubusercontent.com/2038150/235329734-20b08330-6cb6-429e-b57e-2f8e12463e5a.png)


