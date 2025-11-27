
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

3.고용노동부에 따르면 2022년 기준 재해유형별 사망원인 1위가 낙상사고이며 전체의 약 41.6%를 차지하고 있습니다.

4.또한 요양시설, 의료시설 등 일상 환경에서 65세 이상의 낙상사고의 비율이 2020년에서 2024년동안 3.2배 증가했습니다.

-----
문제 및 해결 방안


<img width="594" height="455" alt="image" src="https://github.com/user-attachments/assets/9aa20ef9-2e1b-4d23-ac76-1327a6866ab0" />
<img width="609" height="438" alt="image" src="https://github.com/user-attachments/assets/b20aa9b3-679c-47b9-963c-eee28d9f9c8c" />
<img width="633" height="446" alt="image" src="https://github.com/user-attachments/assets/52450f40-7e74-49d9-ae00-acaf27c32dfb" />


5. 이러한 낙상사고는 사람의 부주의, 사후대응 등 예방 부재로 인한 구조적 문제를 드러내고 있었습니다.

6. 그러나 현행 안전체계는 낙상사고가 일어난 후에 이를 감지하여 후속 조치를 가능하게 하는 ‘사후 대응’에6 머물러 있습니다.

7. 저희 팀은 기존과 달리 사고 위험을 사전에 알림으로써 낙상을 예방하는 플랫폼을 구축하고자 합니다.

8. 웨어러블 기기를 통해 데이터를 수집·분석하고, 즉각적인 사용자 경고와 관리자 자동 알림 전송까지 가능한 실시간 낙상 예측 플랫폼, 이것이 바로 세이프폴 인텔리전스입니다

----
기술 전략


<img width="604" height="432" alt="image" src="https://github.com/user-attachments/assets/81be7766-db8f-47e0-b2e1-16fe0147c374" />
<img width="603" height="438" alt="image" src="https://github.com/user-attachments/assets/a4981dc7-e35e-4e3b-ad36-a2ead302a705" />
<img width="619" height="444" alt="image" src="https://github.com/user-attachments/assets/814dc523-048d-4b36-b7b8-b49324858bed" />
<img width="705" height="512" alt="image" src="https://github.com/user-attachments/assets/4116c42d-b594-46ae-8472-a9998dbee827" />
<img width="703" height="497" alt="image" src="https://github.com/user-attachments/assets/296d21c9-ae06-44ee-994f-4cb23434f3d9" />
<img width="693" height="498" alt="image" src="https://github.com/user-attachments/assets/4b907dae-2e4d-4f18-b2ad-b8ee7f1692d6" />
<img width="714" height="498" alt="image" src="https://github.com/user-attachments/assets/b0a123c6-6f7f-4b1c-b5d4-746f620226aa" />
<img width="697" height="507" alt="image" src="https://github.com/user-attachments/assets/cd2a5cbc-13cb-43a9-b3cf-c95d3530e3c6" />
<img width="698" height="507" alt="image" src="https://github.com/user-attachments/assets/c25bfa11-1ffb-4240-adda-44448d337927" />
<img width="741" height="511" alt="image" src="https://github.com/user-attachments/assets/7ce41679-cd75-4517-b38b-fad8a8fee042" />
<img width="718" height="517" alt="image" src="https://github.com/user-attachments/assets/463cdb0b-7cd1-4ae2-9d1d-1768e436681f" />
<img width="698" height="484" alt="image" src="https://github.com/user-attachments/assets/be464780-83fd-4c59-9d70-2277d03a53ba" />
9. 본격적인 기술전략 설명에 앞서 주로 사용될 용어를 정리하고 가겠습니다

10. 데이터 수집의 경우
먼저 가상 실험실에서 초기인원 30명으로 낙상 및 쓰러짐 상황을 수집합니다.
다음으로는 안전통제가 이루어진 세팅 현장에서 이를 반복하고
마지막으로는 실제 현장에서 이를 반복함으로써 
낙상 데이터를 수집합니다.

11. 핵심적인 기술전략은 크게 5가지가 있습니다.
먼저 IMU의 경우 가속도와 자이로 센서를 이용하여 낙상 직전 패턴을 잡는 기능을 합니다.
심박 변이도를 통해서는 실신, 어지러움, 균형 저하를 미리 감지하고,
산소포화도를 통해 저산소, 탈수, 피로 등을 감지합니다.

12. EDA를 통해 교감신경의 활성상태를 감지하고 이를 바탕으로 낙상 위험을 확인하며
EMG를 통해 근육이 수축할 때 발생하는 전기신호의 감지로 낙상 패턴을 파악합니다.

13. 플로우차트는 이렇게 구성이 되어있습니다.

14. 궁극적인 목표를 구현하기에 앞서
한번에 모든 것을 집약하기에는
기술적, 비용적 한계가 존재하기 때문에
단계적 목표 수립을 통해 이를 해소하고자 합니다.
1차 목표는 IMU, 심박 변이도, 산소포화도 만을 이용한 스마트워치기반 온디바이스 AI앱을 개발할 예정입니다.

15. 
기존 스마트워치는 이미 성능좋은 IMU와 HRV, spo2 센서를 가지고 있습니다. 
저희는 이 연속적인 데이터를 각각의 딥러닝 모델로 실시간 분석하여
낙상발생 0.5초에서 1초정도 전에 미리 경고하는 기능을 구현합니다.

이미 상용화된 애플워치와 갤럭시워치를 대상으로 하기에
시장 검증이 빠르고, 하드웨어 비용이 추가되지 않는다는 이점이 있으며, 초기 단계에서 빠르게 제품화가 가능합니다.
 
16. 1차 목표를 이룬 후에는 본격적인 자체 디바이스 개발과 서버운영을 병행합니다.
(1차 결과물에 EDR, EMG가 추가된 버전을) / 서버기반으로 / 고정밀 분석하는 / 멀티모달 모델을 제작하는 것입니다.

17. EDA과 EMG 데이터 역시 각각 적합한 딥러닝 모델로 실시간 분석합니다/
이 두가지가 2차에 추가되는 이유는 현재 상용화된 워치 디바이스에는 이를 감지할 수 있는 센서가 탑재되지 않았기 때문입니다. 

또한 IMU의 경우도 / 워치의 착용위치가 신체의 중앙부가 아니기 때문에 / 정확도가 떨어진다는 단점이 있어 / 조끼와 밴드 등의 사용으로 이를 보완합니다.

18.구현영상
다음은 노인의 균형상태, 생체신호, 주변환경을 측정한 데이터로 노인낙상예측모델을 구현한 깃허브 연구자료입니다.
(구현 영상도 준비했으나, 시간 관계상 시연은 생략하고 핵심 결과만 공유하겠습니다.)

19. 지도학습 피어슨 상관계수에 의하면 압력, 심박수, 산소포화도가 낙상여부와 높은 상관도를 보였고, 혈당변화는 낮은 상관도를 보였습니다. 

20. 이러한 성과지표를 통해 k-민 비지도 모델인데도, 정확도 83퍼, f182퍼로 센서데이터로만으로도 낙상유형을 분리해 예측이 도움이 된다라는 결과가 나왔습니다.

-----
시장 기회


<img width="698" height="519" alt="image" src="https://github.com/user-attachments/assets/72d8a966-71ad-405b-b23d-bc1e9693d66e" />
<img width="724" height="511" alt="image" src="https://github.com/user-attachments/assets/83b8d5c2-cc4a-4482-b05b-e0253ccedc45" />
<img width="710" height="512" alt="image" src="https://github.com/user-attachments/assets/3cdbbcd8-f542-496d-8f49-aba9d6b56196" />
<img width="703" height="509" alt="image" src="https://github.com/user-attachments/assets/31fc1de6-8a5a-4aff-8788-506ef77fde4a" />
<img width="706" height="531" alt="image" src="https://github.com/user-attachments/assets/6459ec70-a419-44e7-96cc-dada976e8ea0" />
<img width="739" height="498" alt="image" src="https://github.com/user-attachments/assets/7d61fe9b-5e98-4c58-8cc4-11e017b7564f" />
<img width="734" height="489" alt="image" src="https://github.com/user-attachments/assets/8bf087b9-4717-4ff2-9689-1c913907879f" />
<img width="728" height="509" alt="image" src="https://github.com/user-attachments/assets/536ab8e7-17dc-472b-9a77-0bb9445460fe" />


