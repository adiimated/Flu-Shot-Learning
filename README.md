# Flu-Shot-Learning

## Background and Challenge

Public health measures, particularly vaccination, play a pivotal role in combating infectious diseases. Vaccination not only confers immunity to individuals but also contributes to the broader "herd immunity," essential for reducing disease spread within communities.

This project is inspired by the response to the H1N1 influenza pandemic, also known as "swine flu," which emerged in the spring of 2009. The pandemic highlighted the global challenge of responding to infectious disease outbreaks, with the H1N1 virus causing an estimated 151,000 to 575,000 deaths worldwide in its first year alone.

By October 2009, a vaccine against the H1N1 flu virus was made available to the public. The United States' National 2009 H1N1 Flu Survey, conducted in late 2009 and early 2010, forms the basis of our dataset. This phone survey collected data on whether respondents received the H1N1 and seasonal flu vaccines, alongside questions about their demographics, opinions on vaccine efficacy and illness risks, and behaviors related to transmission mitigation.

Understanding the relationships between these characteristics and vaccination behavior can provide invaluable insights for future public health initiatives. As the world faces new health challenges, including the development of vaccines for emerging diseases like COVID-19, lessons learned from past pandemics remain highly relevant.

## Objective

The primary goal of this challenge is to predict individuals' H1N1 and seasonal flu vaccination status based on information shared about their backgrounds, opinions, and health behaviors. By leveraging machine learning models to analyze the survey data, we aim to uncover patterns and factors that influence vaccination decisions. These insights could guide public health strategies to enhance vaccine uptake and manage disease spread effectively.

## Data Source

The dataset for this challenge comes from DrivenData's "Flu Shot Learning" practice competition, which revisits the public health response to the H1N1 pandemic using data from the National 2009 H1N1 Flu Survey. More details about the competition and dataset can be found here: https://www.drivendata.org/competitions/66/flu-shot-learning/

## Survey Insights: 

### Correlation Matrix

### Understanding Data: General Metrics

#### Seasonal Flu and H1N1 Vaccination Rates

* Vaccinated: 21.2% of the respondents have been vaccinated against H1N1.
* Not Vaccinated: 78.8% of the respondents have not been vaccinated against H1N1.

### Levels of Concern and Knowledge about H1N1

### Doctor Recommendations on Vaccinations and Its Influence

### Opinions on Vaccine Effectiveness

### Socioeconomic Factors
### H1N1 Vaccination Dependency on Socioeconomic Factors

1. Age Group
2. Employment Status
3. Education level
4. Income Level

### Seasonal Vaccination Dependency on Socioeconomic Factors

1. Age Group
2. Employment Status
3. Education level
4. Income Level

## Version 1.0 - Base Model

In the base model version (V1.0), we have streamlined our dataset by eliminating all rows containing missing values to ensure clean and straightforward data for analysis. This initial approach aims to establish a baseline understanding of the dataset and model performance without the complexities introduced by missing data imputation strategies. This reduced the dataset from 26707 to 6437 rows.

With a preprocessed and well-understood dataset, we proceeded to select various machine learning models for evaluation. The selection criteria were based on each model's ability to handle binary classification tasks, as well as their distinct methodological advantages. The models included Logistic Regression, Random Forest, Gradient Boosting, SVM, and XGBoost. Each model was trained on the dataset, utilizing a split of 80% training data and 20% testing data to validate performance.

### Model Evaluation

The performance of each model was meticulously evaluated based on accuracy and ROC AUC scores on the test dataset. These metrics were chosen for their ability to quantify the models' effectiveness in classification tasks and their capability to distinguish between the binary outcomes of vaccine uptake.

H1N1 Vaccine Prediction Model Performance:

| Model              | Accuracy | ROC AUC |
|--------------------|----------|---------|
| Logistic Regression| 0.8315   | 0.8773  |
| RandomForest       | 0.8354   | 0.8625  |
| GradientBoosting   | 0.8331   | 0.8727  |
| SVM                | 0.8300   | 0.8752  |
| XGBoost            | 0.8152   | 0.8656  |

Seasonal Flu Vaccine Prediction Model Performance:

| Model              | Accuracy | ROC AUC |
|--------------------|----------|---------|
| Logistic Regression| 0.7935   | 0.8840  |
| RandomForest       | 0.8075   | 0.8752  |
| GradientBoosting   | 0.7981   | 0.8824  |
| SVM                | 0.7966   | 0.8839  |
| XGBoost            | 0.8059   | 0.8737  |


## Version 1.1 - Feature Focused Modeling

In this iteration of our project, we concentrated our analysis on features with the highest correlation with our target variables: `h1n1_vaccine` and `seasonal_vaccine`. Through exploratory data analysis, we identified several key features that significantly influence vaccination decisions:

- `doctor_recc_h1n1`
- `doctor_recc_seasonal`
- `opinion_seas_vacc_effective`
- `opinion_seas_risk`

This focused approach enables a deeper understanding of the factors driving vaccine uptake and improves our models' predictive performance.

### Model Performance

Evaluating the accuracy of various models provided insight into the effectiveness of our feature-focused approach. Below are the accuracy scores for models predicting H1N1 and Seasonal Flu vaccine uptake.

H1N1 Vaccine Prediction Model Performance:

| Model                | Accuracy |
|----------------------|----------|
| Logistic Regression  | 0.8117   |
| Support Vector Machine | 0.8106 |
| Gradient Boosting    | 0.8071   |
| Random Forest        | 0.8061   |

Seasonal Flu Vaccine Prediction Model Performance:

| Model                | Accuracy |
|----------------------|----------|
| Gradient Boosting    | 0.7552   |
| Random Forest        | 0.7541   |
| Support Vector Machine | 0.7460 |
| Logistic Regression  | 0.7460   |


## Iterative Improvement

Acknowledging the base model as our project's foundational step, we outlined plans for future iterations. These plans encompass exploring advanced imputation techniques for missing data, integrating more complex models, and enhancing our feature engineering efforts to refine our predictive capabilities.

## Contributors
Sarthak Mishra and Pratiksha Naik
