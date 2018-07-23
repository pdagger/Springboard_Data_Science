# Project 2 Milestone Report: 

## Problem:
The most common breast cancer subtype is the Invasive Ductal Carcinoma (IDC). In order to predict patient outcome, histopatologists determine IDC's grade agressiveness by analyzing whole slide images. The purpose of the histopatologist is to identify regions indicating the presence of cancerous tissue. This task being time consumming and prone to human error, it would be helpful to develop an automized classifier capable of discriminating cancerous tissue from non-cancerous tissue in a same slide.

## Possible Clients:
* Hospitals.
* Histopathology laboratories.
* Medical centers

## Data:
The curated data is obtained directly from [Kaggle.com](https://www.kaggle.com/paultimothymooney/breast-histopathology-images/data). The data contains only whole slides images divided by patient. Each whole slide image is segmented in patches of 50x50 pixels. Each of the patches corresponds either to an IDC region or a cancer free region. Each image patch class is contained in its file name. The presence of IDC is indicated by a 1 while 0 corresponds to an IDC free area.

## Data Wrangling:
The data corresponds to histopathology slides from patients presenting IDC. There is a total of 279 patients. Each slide contains cancerous and non-cancerous regions. Each image slide has been previously segemented in separated images of 50x50 pixels. The small size of these regions allows to classify them as being only IDC images or healthy tissue images.

As mentioned before, the class type for each 50x50 pixel image is indicated in its file name. The file name consists of three parts: a four digit number identifying the patient, a set of (x, y) coordinates corresponding to the region position in the whole slide, and finally the category class. The class can be eithert 0 or 1. 0 represents health tissue or absence of cancer while 1 correponds to regions were IDC was found.

The images come from a clean data set, so they don't need to be preprocessed. However, a quick review of the number of samples for each class shows that the classes are unbalanced. There are 196,454 images labeled as 0 and 78,768 images labeled as 1. This represents a ration of around 2.5 to 1 between both classes that is important to take into account when developing the models. 

Finally, to avoid any possible errors when loading the data and traning training the classification model, only files corressponding to 50x50 pixels images size are considered.

## Approach:
The purpose of the project being to classify images using two possible labels, this is by defibition a supervised binary classification problem. In recent years convolutional neural networks (CNN) have been proven to be very efficient in recognizing and classifying images. So, in this project the goal is to develop or use an existing CNN architecture in order to identify IDC images. To train the CNN model, the data is divided in two: 90% as training set and 10% validation set.

Given that the classes are unbalanced, the 'stratify' option from scikit-learn's 'train_test_split' method is used. This ensures that the 2.5 to 1 ratio between the classes is preserved in the training and validation sets.

To assess the fitness of the developped model, it is important to know how many labels in the validation set are predicted correctly. So, the metric of choice to evaluate the model is the accuracy. The accuracy calculates the number of correct predicted labels to the total number of labels. To explain this with an equation let's define first the following terms:

TP: true positives, it represents the images correctly identified as 1, meaning IDC baing part of an IDC region.

FP: false postives, it denotes the images of healthy tissue incorrectly indetified as 1.

TN: true negatives, it refers to the healthy tissue images correctly identified as 0.

FN: false negatives, it defines IDC region images identified as 0 or being healthy.

With theses definitions at hand, the accuracy is defined as:

![Accuracy](https://latex.codecogs.com/gif.latex?Accuracy&space;=&space;\frac{TP&space;&plus;&space;TN}{TP&space;&plus;&space;TN&space;&plus;&space;FP&space;&plus;&space;FN})

In addition to the accuracy, given that classes are unbalanced, a metric of interest is the F<sub>1</sub> score:

![F_1](https://latex.codecogs.com/gif.latex?F_1&space;=&space;\frac{2}{\frac{1}{Precision}&space;&plus;&space;\frac{1}{Recall}}&space;=&space;2\frac{Precision.Recall}{Precision&space;&plus;&space;Recall})

Having determined how to split the data and the evaluation metrics, now it is important to define a benchmark model to assess the developed models. Given that the classes are unbalanced and that the negative classes dominates the positive classes, a model predicting that all the images correspond to a label of 0 is a good starting model.

# Initial Findings
