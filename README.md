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

## V1.0 - Base Model

In the base model version (V1.0), we have streamlined our dataset by eliminating all rows containing missing values to ensure clean and straightforward data for analysis. This initial approach aims to establish a baseline understanding of the dataset and model performance without the complexities introduced by missing data imputation strategies.

With a preprocessed and well-understood dataset, we proceeded to select various machine learning models for evaluation. The selection criteria were based on each model's ability to handle binary classification tasks, as well as their distinct methodological advantages. The models included Logistic Regression, Random Forest, Gradient Boosting, SVM, and XGBoost. Each model was trained on the dataset, utilizing a split of 80% training data and 20% testing data to validate performance.

### Model Evaluation

The performance of each model was meticulously evaluated based on accuracy and ROC AUC scores on the test dataset. These metrics were chosen for their ability to quantify the models' effectiveness in classification tasks and their capability to distinguish between the binary outcomes of vaccine uptake.

| Model              | Accuracy | ROC AUC |
|--------------------|----------|---------|
| Logistic Regression| 0.8315   | 0.8773  |
| Random Forest      | 0.8354   | 0.8625  |
| Gradient Boosting  | 0.8331   | 0.8727  |
| SVM                | 0.8300   | 0.8752  |
| XGBoost            | 0.8152   | 0.8656  |

## Iterative Improvement

Acknowledging the base model as our project's foundational step, we outlined plans for future iterations. These plans encompass exploring advanced imputation techniques for missing data, integrating more complex models, and enhancing our feature engineering efforts to refine our predictive capabilities.

## Contributors
Sarthak Mishra and Pratiksha Naik
