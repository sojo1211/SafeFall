# Elderly_Fall_Prediction

This project aims to develop and evaluate predictive models for detecting falls among the elderly using sensor data from a wearable device called 'cStick.' The dataset, named ["Elderly Fall Prediction and Detection"](https://www.kaggle.com/datasets/laavanya/elderly-fall-prediction-and-detection/data), is sourced from Kaggle and comprises information collected from elderly participants wearing the 'cStick' device. This wearable not only detects falls but also predicts the likelihood of a fall incident. The 'cStick' monitors the surroundings, issues warnings to the user, and updates the location and surroundings based on the detected falls. The overall fall decision (prediction, warning, or detection) is determined with an impressive accuracy of around 95%.

## Dataset Characteristics

The dataset consists of 2039 instances, each with 7 features:

1. **Distance**
2. **Pressure**
3. **HRV (Heart Rate Variability)**
4. **Sugar level**
5. **SpO2 (Oxygen Saturation)**
6. **Accelerometer**
7. **Decision**

The 'Decision' feature serves as the label, representing the outcome of the fall detection, with the following values and meanings:

- 0: 'No Fall detected'
- 1: 'Slip detected'
- 2: 'Definite fall'

## Research Questions

The primary research question:

1. **Prediction Accuracy:** How well can the models predict falls among the elderly based on the provided features?

This project will also address the following secondary research questions:

2. **Feature Importance:** Which features play a crucial role in predicting falls, and how do they contribute to the models' decision-making process?

3. **Model Comparison:** How do the Random Forest Classifier and Kmeans Clustering models compare in terms of predictive performance for fall detection?

4. **False Positive Analysis:** What are the implications and potential consequences of false-positive predictions in an elderly fall detection system?

5. **Real-world Applicability:** How suitable are the developed models for real-world deployment, considering the practical constraints and challenges associated with wearable devices?

## Model Design

The project will employ three types of models:

- **Supervised Model: Linear Regression**
- **Supervised Model: Random Forest Classifier**
- **Unsupervised Model: Kmeans Clustering**

The Random Forest Classifier will be trained on labeled data, leveraging Decision as the target variable, while the Kmeans Clustering algorithm will explore patterns and relationships within the dataset without using labeled information. The linear regression model will also be trained on labeled data. The comparative analysis of these models will provide insights into their effectiveness for the specific task of elderly fall prediction.
