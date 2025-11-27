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
----
문제인식 
<img width="607" height="441" alt="image" src="https://github.com/user-attachments/assets/8c205892-e0a6-4cbc-9910-6ff3ac97a537" />
<img width="605" height="435" alt="image" src="https://github.com/user-attachments/assets/54a76393-4966-46d2-8c92-96ebec0ebb0a" />
<img width="604" height="446" alt="image" src="https://github.com/user-attachments/assets/94bb958b-7315-4d8f-babf-f58966621c79" />

고용노동부에 따르면 2022년 기준 재해유형별 사망원인 1위가 낙상사고이며 전체의 약 41.6%를 차지하고 있습니다.
또한 요양시설, 의료시설 등 일상 환경에서 65세 이상의 낙상사고의 비율이 2020년에서 2024년동안 3.2배 증가했습니다.

-----
문제 및 해결 방안
<img width="594" height="455" alt="image" src="https://github.com/user-attachments/assets/9aa20ef9-2e1b-4d23-ac76-1327a6866ab0" />
<img width="609" height="438" alt="image" src="https://github.com/user-attachments/assets/b20aa9b3-679c-47b9-963c-eee28d9f9c8c" />
<img width="633" height="446" alt="image" src="https://github.com/user-attachments/assets/52450f40-7e74-49d9-ae00-acaf27c32dfb" />

이러한 낙상사고는 사람의 부주의, 사후대응 등 예방 부재로 인한 구조적 문제를 드러내고 있었습니다.
현행 안전체계는 낙상사고가 일어난 후에 이를 감지하여 후속 조치를 가능합니다.
저희 팀은 기존과 달리 사고 위험 알림을 통해 낙상을 예방하는 플랫폼을 구축하고자 합니다.
8. 웨어러블 기기를 통해 데이터를 수집, 분석하고, 즉각적인 사용자 경고, 관리자에게 자동 알림 전송까지 가능케하는
실시간 낙상 예측 플랫폼이 바로 세이프폴 인텔리전스입니다.

----
기술 전략
<img width="604" height="432" alt="image" src="https://github.com/user-attachments/assets/81be7766-db8f-47e0-b2e1-16fe0147c374" />
<img width="603" height="438" alt="image" src="https://github.com/user-attachments/assets/a4981dc7-e35e-4e3b-ad36-a2ead302a705" />
<img width="619" height="444" alt="image" src="https://github.com/user-attachments/assets/814dc523-048d-4b36-b7b8-b49324858bed" />


