# Capstone Project: Classification of Histopatholgy Breast Images

## Problem

Invasive Ductal Carcinoma (IDC) is the most common subtype of breast cancer. In order to predict patient outcome, histopathologists determine IDC's agressiveness grade by analyzing whole slide histopathology images. The purpose of the histopathologist is to identify regions indicating the presence of cancerous tissue. This task is time consumming and prone to human error, then it would be helpful to develop an automized classifier capable of discriminating cancerous tissue from non-cancerous tissue in an image.
The classifier developed in this project uses CNN networks and reaches an accuracy of 84.97%.

## Instructions
### Data set
This project uses clasified breast histopatology images downloaded from this [Kaggle link](https://www.kaggle.com/paultimothymooney/breast-histopathology-images/data).
The images are 50x50 pixels color images in RGB format.

### Working environment
To run the project create a new environment in your local machine using the files in the [requirements](https://github.com/pdagger/Springboard_Data_Science/tree/master/Capstone_Project_2/requirements) folder:

```
conda env create -f requirements/histo.yaml
```  
Alternatively the environment can be created like this:

- __Linux__ or __Mac__: 
  
```
conda create --name histo python=3
source activate histo
pip install -r requirements/requirements.txt
```
  
- __Windows__: 
  
```
conda create --name histo python=3
activate histo
pip install -r requirements/requirements.txt
