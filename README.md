# Injury Severity Prediction: Decision Tree, Random Forest, Neural Network, and Logistic Regression

Overview
This project aims to predict injury severity resulting from vehicle crashes using various machine learning techniques, including Decision Trees, Random Forests, Neural Networks, and Logistic Regression. The analysis is conducted using the KNIME analytics platform, leveraging the CRISP-DM methodology to extract insights from the National Highway Traffic Safety Administration (NHTSA) dataset.


Objectives
- Predictive Modeling: Develop and compare predictive models to estimate injury severity based on crash data.
- Pattern Recognition: Identify key risk factors contributing to severe injuries, such as driver behavior, vehicle characteristics, and road conditions.
- Safety Insights: Provide actionable insights for NHTSA to enhance road safety and allocate resources effectively.


Business Understanding

The primary goal is to assist the NHTSA in reducing motor vehicle crash impacts by accurately predicting injury severity. This project utilizes the CRSS dataset, a national probability sample of over 6 million police-reported crashes, to model injury outcomes and inform safety interventions.


Data Understanding

The dataset includes over 20 variables related to crash incidents, including driver behavior, vehicle traits, road conditions, and collision dynamics. Careful preprocessing was required to handle missing values, anomalies, and categorical data transformation for effective modeling.


Data Preparation
Data preprocessing involved:

- Categorization: Binning variables like weather, day of the week, manner of collision, and more to simplify analysis.
- Normalization: Standardizing numerical data for consistent model input.
- Transformation: Converting categorical data into numerical categories for compatibility with machine learning algorithms.


Examples of Data Binning:
- Weather Conditions: Aggregated into "favorable", "unfavorable", and "unknown".
- Day of Week: Grouped into weekdays and weekends.
- Manner of Collision: Categorized into front, side, rear, and other impacts.
- Alcohol Involvement: Binned into "yes", "no", and "unknown".


Model Building and Testing
A. Decision Tree Model
- Methodology: Used a 10-fold stratified partitioning technique with a random seed of 12345 to maintain class proportionality.
- Evaluation: Assessed using a Scorer tool and ROC curve. The model had lower specificity with an accuracy rate of 0.645.


B. Random Forest Model
- Methodology: Similar settings as the Decision Tree model for comparison.
- Evaluation: Assessed using a Scorer tool and ROC curve.


C. Neural Network (MLP) Model
- Methodology: Preprocessed data through normalization and one-to-many nodes before feeding it into the MLP model.
- Evaluation: Accuracy assessed using ROC Curve and Scorer tools in KNIME.


D. Logistic Regression Model
- Methodology: Data was processed similarly to the Neural Network model and fed into the Logistic Regression learner.
- Evaluation: The Logistic Regression model outperformed others with an accuracy of 0.783.


Testing and Evaluation
The models were compared using a combined ROC curve:

- Best Performing Model: Logistic Regression with 0.783 accuracy.
- Least Performing Model: Decision Tree with 0.645 accuracy.


Key Figures:
- ROC Curve: Combines outputs from all models.
- Random Forest Importance Graph: Highlights important features.


Conclusion
The Logistic Regression model emerged as the most accurate predictor of injury severity among the models tested. This model provides valuable insights into risk factors that can inform safety measures and interventions.
