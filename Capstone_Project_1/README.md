# Capstone Project: Predict Salaries from H-1B Applications

## Problem

When entering the job market after college for the first time or when transitioning to a new career
path it is difficult to assess what the base salary for a given position should be. This is particularly
true for foreign workers when moving to a new area given that salaries do not only depend on the
field of knowledge, but are also dependent on the location where the future employee is going to
work. In order to help not only job applicants but also employers it will be helpful to develop a
model predicting the base salary a future employee should expect based on historical data collected
from US H-1B visa applications.
The data set used to solve this problem contains information on location, job position and
field of knowledge. This information serves as the input to the model. The data set also has
the corresponding prevailing wages and employer salaries, which are continuous target variables.
Therefore, the problem at hand corresponds to a supervised regression problem that can be solved
by linear regression or random forest regression.

## Instructions
### Data set
The data for this project can be downloaded from [here](https://www.foreignlaborcert.doleta.gov/pdf/PerformanceData/2017/H-1B_Disclosure_Data_FY17.xlsx).
### Initial Data Exploration
Data exploration can be found in the file [Data_visualization.ipynb](https://github.com/pdagger/Springboard_Data_Science/blob/master/Capstone_Project_1/data/Data_visualization.ipynb) located in the [data](https://github.com/pdagger/Springboard_Data_Science/blob/master/Capstone_Project_1/data/) folder.
### Data Wrangling:
After download, process the data set using the file [data_wrangling.ipynb](https://github.com/pdagger/Springboard_Data_Science/blob/master/Capstone_Project_1/data/data_wrangling.ipynb) present in the [data](https://github.com/pdagger/Springboard_Data_Science/blob/master/Capstone_Project_1/data/) folder. This creates the clean data set used for the project.
### Working environment
To process the data set and run the project create a new environment in your local machine using the files in the [Requirements](https://github.com/pdagger/Springboard_Data_Science/tree/master/Capstone_Project_1/Requirements) folder:

```
conda env create -f Requirements/h1b.yaml
```  
Alternatively the environment can be created like this:

- __Linux__ or __Mac__: 
  
```
conda create --name h1b python=3
source activate h1b
pip install -r Requirements/requirements.txt
```
  
- __Windows__: 
  
```
conda create --name h1b python=3
activate h1b
pip install -r Requirements/requirements.txt
```

