# Powerline-Detection

Detection of powerlines in aerial images acquired from an UAV using Convolutional Neural Networks

Condition assessment of power lines is one of the critical components of maintenance. In the current scenario, condition assessment of power lines is carried out manually. Manual inspection is carried out using foot patrol. Inspection of power lines through foot patrol is labour intensive, costly and requires experienced staff. The cost increases linearly with the length of power lines to be inspected.  

Advancements in Drone Technology as a remote sensing platform  and the use of AI in remote sensing applications provides interesting  options for solutions in Power sector. Detection of power lines is one of the interesting applications.  Automated detection of powerlines is a necessary perquisite for advanced systems such as autonomous navigation for inspection of powerlines, Automated inspection of powerlines etc.  In this assignment we build a Deep learning Convolutional Neural Network (CNN) for the detection of Powerlines in Aerial imagery of Powerlines acquired from an Unmanned Aerial Vehicle (UAV)

## Table of Contents
* [General Info](#general-information)
* [Appraoch](#approach)
* [Conclusions](#conclusions)
* [Contact](#contact)

## General Information
The objective of this assignment is to build a Deep Learning model for the detection of power lines.  Python Keras framework with Tensor flow backend is used to realize the model.

## Approach
The following approach is followed:

### Data preparation
The dataset contains the original images and their corresponding ground  truth/annotation images that are annotated with the powerlines. These images are converted into grayscale images and resized to 128 * 128 pixel images. The ground truth image is overlayed over the original image to verify that the ground truth is spatially aligned with the original image.

### Model Building and Training

- An ada[tation of an existing UNET model is built for semantic segmentation.
- Parameters used: Adam optimizer, with ‘binary_crossentropy‘ and Accuracy as the metric.
- Model is trained witha  batch size of 10 for 1000 epochs.
- Performance of detectionis visualized. 

### Experiments Performed

- Optimizer learning rate of the Adam optimizer is changed to 1e-4
- Optimizer is changed to SGD
- The model is trained for 100 epochs, 1000 epochs
- Using threshold values of .4, .5, .7, the results of binary thresholding are observed

## Conclusions
- Limitation: For image analysis, a model requires a large number of images in the order of 1000's to converge, which typically requires GPU hardware. Given the xonstraints that teh assignment is carried out on laptop, the training dataset is limited to 30 images. This is not sufficient to come to any visible conclusion.
- However, it can be noted how the learning rate reduces and eventually ealy stopping is triggered in all the cases when a plateau is obtained in loss value.
- Choosing the right number of epochs, setting appropriate learning rate, choice of optimizer - they all impact the learning by the model.
- For each of the models tried, the loss and accuracy metrics for both the training and validation sets have been identified.

## Contact
Created by [@jenifer2409] - feel free to contact me!
