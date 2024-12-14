README: Problematic Internet Usage Prediction

Project Overview

The objective of this project is to predict the severity of problematic internet usage (SII) among children and adolescents using data related to demographics and physical activity. Based on the dataset, a series of models were developed to identify the most important predictors of problematic internet behavior and to evaluate the relationship between various physical and demographic features and the SII severity index. The target variable, SII, is categorized into four levels:

0: None

1: Mild

2: Moderate

3: Severe

Dataset Information

The dataset is divided into two parts:
Demographic Data: Stored in a CSV file with 3960 instances and 82 features. This dataset includes both numerical and categorical features such as sex, age, weight, height, and BMI.
Physical Activity Data: Stored in a Parquet file with 996 instances and 13 numerical features, collected via accelerometer devices worn by participants.

Feature Distribution

Target Variable (SII): The distribution is imbalanced:
None: 58.3%
Mild: 27.6%
Moderate: 13.8%
Severe: 1.2%
Age: The distribution is unimodal, with a peak at 10-12 years and a gradual decline as age increases.
Sex: Imbalanced distribution with 62.7% males and 33.3% females.
Physical Features (BIA): Most are non-normal and skewed, with significant outliers and low variance.
PCIAT Features: Represent responses to questions about internet habits. Their distribution is bimodal and strongly correlated with SII.


Correlation Insights

SII and PCIAT Features: Strongest correlation (0.37 to 0.90).
SII and Physical Features: Moderate correlation (-0.04 to 0.31).
SII and BIA Features: Correlation ranges from -0.01 to 0.41.
SII and FCG Features: Weak to moderate correlation (-0.2 to 0.35).

Implementation of Models
Five distinct models were implemented to explore the relationship between SII and other features:

First Model
This model identifies key features by computing a correlation matrix and excluding features with correlations below a certain threshold.
Steps:
Encode categorical data using OneHotEncoder.
Merge encoded categorical and numerical features.
Compute correlation with SII and discard features with correlation below ±0.3.
Remove NaN or infinite values.
Train multiple models and record results.

Second Model
The second model merges Parquet and CSV files to create a single dataset.
Steps:
Merge demographic and physical activity data.
Drop columns with >60% missing values and irrelevant columns (e.g., season-related features).
Handle null values and outliers.
Train and evaluate models.

Third Model
This model is similar to the second but includes scaled features and retains outliers.
Differences:
Scale data using StandardScaler.
Train models without removing outliers.

Fourth Model
Focuses on dimensionality reduction using PCA.
Steps:
Use PCA to reduce dimensionality to 2 components.
Train models using the reduced dataset.
Maintain satisfactory accuracy scores.

Fifth Model
Combines PCA and manual feature selection to further reduce dimensions.
Steps:
Reduce accelerometer data to 3 key features using PCA.
Merge reduced data with the demographic dataset.
Impute missing values and encode features via pipelines.
Train, predict, and evaluate models.

Key Findings

Gender Influence: Boys are more likely to have problematic internet usage than girls.
Age Factor: Adolescents aged 10-19 have the highest risk of intense problematic usage.
Daily Computer Usage: Increased hours of computer use correlate with higher SII levels.
Physical Features: Most physical features show positive trends with increasing SII, except for diastolic blood pressure and heart rate, which remain unaffected or decrease.
PCIAT Features: Strongly correlated with SII; responses to internet habit questions provide valuable predictive power.

Suggestions for Next Steps
Address Imbalanced Data: Consider techniques like oversampling (e.g., SMOTE) or undersampling to address the severe imbalance in the target variable.
Model Optimization: Fine-tune hyperparameters for more accurate models.
Feature Engineering: Create interaction terms between physical and PCIAT features to explore combined effects.
Extend Demographic Insights: Investigate the role of additional demographic factors like socioeconomic status or educational background.



