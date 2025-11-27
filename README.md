# Elderly_Fall_Prediction 연구 인용

<img width="509" height="705" alt="image" src="https://github.com/user-attachments/assets/932dc04a-ae5e-4378-ba03-8680907c2d46" />
<img width="274" height="387" alt="image" src="https://github.com/user-attachments/assets/83289ab3-65fb-4815-975b-794e9d0116ee" />


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

문제인식 
고용노동부에 따르면 2022년 기준 재해유형별 사망원인 1위가 낙상사고이며 전체의 약 41.6%를 차지하고 있습니다.
또한 요양시설, 의료시설 등 일상 환경에서 65세 이상의 낙상사고의 비율이 2020년에서 2024년동안 3.2배 증가했습니
<img width="468" height="192" alt="image" src="https://github.com/user-attachments/assets/2c37bc4f-e766-47f7-9938-f57ab9176322" />

