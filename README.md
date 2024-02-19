# Flu-Shot-Learning
Predict H1N1 and Seasonal Flu Vaccines:  Predicting whether people got H1N1 and seasonal flu vaccines using information they shared about their backgrounds, opinions, and health behaviors. 

# Version 1.1

## Overview
This repository contains the first checkpoint for the machine learning project, focusing on the initial dataset exploration, preprocessing, and model building. 

## Dataset
The dataset used for this project contains Flu Shot Learning: Predict H1N1 and Seasonal Flu Vaccines
data. Before preprocessing, the dataset contained missing data which was addressed prior to model building.

## Preprocessing
### Missing Data Handling
Three major missing data columns were identified and removed from the dataset. Additionally, all rows with missing data were removed to ensure data integrity.

## Model Building
Two sets of machine learning models were constructed using different subsets of the dataset:
1. **Set 1**: Utilized a subset of the columns.
   - Gradient Boosting Classifier
   - Random Forest Classifier
   - Support Vector Classifier
   - Logistic Regression Classifier
   
2. **Set 2**: Utilized all columns.
   - Gradient Boosting Classifier
   - Random Forest Classifier
   - Support Vector Classifier
   - Logistic Regression Classifier

## Next Steps
In the next checkpoint, the performance of the models will be evaluated, and further optimizations will be explored to enhance model accuracy and efficiency.

## Usage
To replicate the results or further explore the project, follow these steps:
1. Clone this repository.
2. Install the necessary dependencies.
3. Run the provided Jupyter notebook or Python scripts.