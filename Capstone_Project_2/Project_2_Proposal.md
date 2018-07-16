# Project 2 Proposal: 

## Problem:
The most common breast cancer subtype is the Invasive Ductal Carcinoma (IDC). In order to predict patient outcome, histopatologists determine IDC's grade agressiveness by analyzing whole slide images. The purpose of the histopatologist is to identify regions indicating the presence of cancerous tissue. This task being time consumming and prone to human error, it would be helpful to develop an automized classifier capable of discriminating cancerous tissue from non-cancerous tissue in a same slide.

## Possible Clients:
* Hospitals.
* Histopathology laboratories.
* Medical centers

## Data:
The curated data is obtained directly from [Kaggle.com](https://www.kaggle.com/paultimothymooney/breast-histopathology-images/data). The data contains only whole slides images divided by patient. Each whole slide image is segmented in patches of 50 by 50 pixels. Each of the patches corresponds either to an IDC region or a cancer free region. Each image patch class is contained in its file name. The presence of IDC is indicated by a 1 while 0 corresponds to an IDC free area. 

## Approach:
The purpose of the project being to classify images among two labels, this is a supervised binary classification problem. In recent years convolutional neural networks (CNN) have been proven to be very efficient in recognizing and classifying images. So, in this project we are going to develop or use an existing CNN architecture in order to identify IDC images. To train the CNN model, the data is going to be divided in two: training data and validation data.

## Deliverables:
* Code for:
  * Image classification.
* Written report.
