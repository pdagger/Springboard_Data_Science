# Project 1 Proposal: 

## Problem:
When entering the job market for the first time or when transitioning to a new career path it is difficult to asses what the base salary for a given position should be. This problem is enhanced when we move to a new area or a different country given that salaries do not only depend on the field we have been trained but are also affected by the location where we are going to work. In order to help not only applicants but also employers it will be helpful to develop a model predicting the base salary a future employee should expect based on the data collected from US work visa applications.

## Possible Clients:
* Professionnals looking to migrate to the US or inside the US.
* Recruiters and HR departments.

## Data:
Initially the curated data will be obtained directly from [Kaggle.com](https://www.kaggle.com/nsharan/h-1b-visa). This data contains the position, company, location in the US and salary pertaining to H-1B visa applications, which is a category for high-skilled workers. However if time permits it, additional data will be obtained directly from the [United States Department of Labor](https://www.foreignlaborcert.doleta.gov/performancedata.cfm) in order to include data and job positions pertaining to non high-skilled workers.

## Approach:
We want to predict an expected salary based on historical data, then this will be a supervised problem that is going to be solved through regression. The location, job title and company are going to be used as predictors in trying to assertain what the salary should be. To train the model, the data is going to be divided in two: training data and validation data.

## Deliverables:
* Code for:
  * Data cleaning if performed.
  * Data analysis and regression.
* Written report.
* Presentation.


