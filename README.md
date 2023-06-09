# Image-Classification
This is an image classification model with Deep Learning using tensorflow. The project takes training data of images that are categorized by folders and later predicts which category the image belongs to. For this example I will be using sport balls because they are similar in shape and can vary in appearance to see if the machine can detect the difference.

![alt text](https://github.com/MarcioArak/Image-Classification/blob/main/results/image_testing.png)
## Overview
This notebook is my first Deep Learning experience. The purpose of this project is to learn more about AI and Machine Learning by writing down all the steps it takes to make and test a model, while also taking notes of my machine learning experience.  

The model classifies objects of 5 categories at about 80-90% accuracy. This project could be useful in creating an application that identifies sports balls and gives you information on either the object (the ball or any trained object) or the sport that the ball belongs to. 

The project shows how to evaluate the model using k-fold cross validation in addition to plotting performance and statistics. 


![alt text](https://github.com/MarcioArak/Image-Classification/blob/main/results/confusion_matrix.jpg)

## Data
Data is stored in a folder called 'data' where training and testing data is separated by their corresponding folders. Each dataset for the training images contains around 1000+ pictures but only uploaded 50 images each for this repository. This project also shows how to augment data to create for training images if your dataset is not sufficient.


## In progress
Working on using greyscale and edge detecting to increase accuracy
