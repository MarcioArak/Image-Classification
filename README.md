# Image-Classification
This is an image classification model with Deep Learning using tensorflow. The project takes training data of images that are categorized by folders and later predicts which category the image belongs to. For this example I will be using sport balls because they are similar in shape and can vary in appearance to see if the machine can detect the differance.

## Overview
This notebook is my first Deep Learning experience following this [tutorial](https://www.youtube.com/watch?v=jztwpsIzEGc). The purpose of this project is to learn more about AI and Machine Learning by writing down all the steps it takes to make and test a model, while also taking notes of my machine learning experience.

Thed model classifies objects of 5 categories at about 80-90% accuracy testing images that would be consider edge cases. The project shows how to evaluate the model using k-fold cross validation in addition to plotting performance and statistics.

## Data
Data is stored in a folder called 'data' where training and testing data is separated by their corresponding folders. Each dataset for the training images contains around 1000+ pictures but only uploaded 50 images each for this repository. This project also shows how to augment data to create for training images if your dataset is not sufficient.

# Notes

The data was collected from various search engines, and stored in a file called 'data' where we will separate the images in folders with their corresponding label. We start by setting up our GPU for usage and installing all dependencies. We remove any images that do not have an image extension and resizing all images to a consistent size. Data is preprocessed by scaling it down to make it easier to iterate and then split into training, validation and testing batches. We use a Sequential model and feed it the training batches. The model was successful when identifying two categories using the sigmoid activation function, but when adding more datasets the model's accuracy dropped to about 30%. I gave it more training cycles to see if the model just needed more training but it did not increase in accuracy.

Upon further reviewed I noticed that the pictures I was testing were going in as BGR because of OpenCV, when I had trained my data with RBG. After converting the testing data to RGB the model's classification increased to about 60-70%. When I tried using VGG16 model that had won awards for images classification the accuracy surprisingly dropped to about 30%. Leading me to believe that the model is too big for my datasets since it's only about 250 images per category and the model was made to classify 1000s of categories filled with 1000s of pictures. The recommended amount of images is 1000 per category so after downloading more images and cleaning them up manually my model's accuracy increased to about 80%.
