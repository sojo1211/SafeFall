
<img width="509" height="705" alt="image" src="https://github.com/user-attachments/assets/932dc04a-ae5e-4378-ba03-8680907c2d46" />
<img width="274" height="387" alt="image" src="https://github.com/user-attachments/assets/83289ab3-65fb-4815-975b-794e9d0116ee" />

✅ “논문 인용” 포함 버전 (발표에서 바로 사용 가능)

저희 팀은 먼저, 공개된 연구 논문과 데이터셋을 인용하여
“낙상사고가 데이터로 사전에 예측 가능한 사고인가?”를 검증하는 것부터 시작했습니다.

공개 데이터셋 Elderly Fall Prediction and Detection과 선행 연구 분석을 통해,
센서 데이터만으로도 낙상 위험 패턴을 충분히 포착할 수 있다는 근거를 확보했고,
이 검증이 바로 “세이프폴 인텔리전스” 기획의 출발점이 되었습니다.

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

3. 고용노동부에 따르면 2022년 기준 재해유형별 사망원인 1위가 낙상사고이며 전체의 약 41.6%를 차지하고 있습니다.

4. 또한 요양시설, 의료시설 등 일상 환경에서 65세 이상의 낙상사고의 비율이 2020년에서 2024년동안 3.2배 증가했습니다.

5. 이러한 낙상사고는 사람의 부주의, 사후대응 등 예방 부재로 인한 구조적 문제를 드러내고 있었습니다.
-----
문제 및 해결 방안


<img width="594" height="455" alt="image" src="https://github.com/user-attachments/assets/9aa20ef9-2e1b-4d23-ac76-1327a6866ab0" />
<img width="609" height="438" alt="image" src="https://github.com/user-attachments/assets/b20aa9b3-679c-47b9-963c-eee28d9f9c8c" />
<img width="633" height="446" alt="image" src="https://github.com/user-attachments/assets/52450f40-7e74-49d9-ae00-acaf27c32dfb" />

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

15. 기존 스마트워치는 이미 성능좋은 IMU와 HRV, spo2 센서를 가지고 있습니다. 
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

21. 이제 시장 기회로 넘어가겠습니다.
현재 산업안전, 실버케어, 헬스, 공공스마트복지가 모두 포함된
국내 웨어러블 시장은 2024년 기준
약 1.7조 원 규모입니다.

22. 해당 시장은 연평균 15~22%의 높은 성장추세를 보입니다.
정부의 중대재해처벌법 시행, 고령화 가속, 지자체 스마트복지 확대, 디지털 헬스 규제 완화 등이 이러한 시장의 성장을 촉진하는 것으로 판단됩니다.

23. 따라서 저희는 전체시장을 산업안전, 실버케어, 웰니스, 공공복지 전체의 시장으로 잡았으며
유효시장으로 산업안전, 요양 복지 분야를 선정하였습니다.
초기목표 시장으로는 b2b, b2g 시장의 진입장벽이 높음을 인지하여 1퍼센트 수준으로 산정하였습니다.

24. 다음은 경쟁사 분석입니다.
스마트워치는 일반 소비자 중심, 산업 안전밴드는 낙상 후 보고 중심, 실버케어 밴드는 사후 건강 확인 중심이라는 한계가 있습니다.
해외의 낙상 솔루션도 / 대부분 스포츠 중심의 / 단일 IMU 기반이기 때문에 /
산업,요양환경에는 적합하지 않습니다.
저희 솔루션은 IMU외에도 세개 이상의 다중센서 기반 엣지 예측으로
기존 솔루션 대비 / 정확도와 적합성을 크게 높였습니다.

25. 국내 타깃은 산업안전 분야, 요양·복지분야, 웰니스분야, 공공조달 시장이고 
구매 의사결정 구조는 보시는 바와 같이 계층적이기 때문에,
저희는 조달형 B2G 판매,
PoC 계약형 패키지 모델,
SaaS 구독형 서비스 등으로 시장 진입을 계획하고 있습니다.

 
26. 비즈니스 모델은
HW 판매, 월 단가 기반 SaaS 구독, 데이터제휴의 3축 수익모델로 도입이후에도 장기적인 반복 매출과 고마진 성장을 목표로 합니다.

27. 총 개발·실증에 필요한 비용은 약 8.5억 원이며,
PoC단계 – MVP개발단계 – Pilot단계 3단계를 거칩니다.
이는 각 1.3억, 3.5억, 3.7억의 소요를 생각하며 
지속적인 개발 역량을 확보하고, 안정적인 서비스 운영 기반을 마련하는 것을 목표로 합니다.

28. 자금조달은 정부지원금 2단계 과제 반영하고
지자체 실증 연계 및 민간 투자(Seed),  초기 고객 선계약 기반 실증비 매칭을 조합한 구조로 안정적인 자금 흐름을 확보합니다.
---
기대효과


<img width="708" height="515" alt="image" src="https://github.com/user-attachments/assets/79ffc046-63e4-48b2-bed8-954cd0a17699" />
<img width="709" height="508" alt="image" src="https://github.com/user-attachments/assets/4f61a93a-8971-43ac-ad96-090f35204e0a" />

29. 이에 따라 다중 바이오 신호 기반의 낙상 ‘예측’ 기술을 통해 단기부터 장기위험을 모두판단하고, 축적데이터로 성능이 계속 발전하는 확장형 AI플랫폼을 구축한다는 기술적 효과와

30. 고령자·건설현장 낙상을 사전에 예측해 부상·비용·관리부담을 줄이고,
지역사회·산업현장 안전체계를 강화하는 사회적 효과를 가질 것으로 기대됩니다.

---
팀소개 


<img width="719" height="523" alt="image" src="https://github.com/user-attachments/assets/3a163713-0e6a-4c91-9c3c-19df41e67226" />
<img width="648" height="437" alt="image" src="https://github.com/user-attachments/assets/a29ae082-2618-4b33-bd11-9e1227298c86" />


