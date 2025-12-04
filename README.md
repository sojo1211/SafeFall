
<img width="509" height="705" alt="image" src="https://github.com/user-attachments/assets/932dc04a-ae5e-4378-ba03-8680907c2d46" />
<img width="274" height="387" alt="image" src="https://github.com/user-attachments/assets/83289ab3-65fb-4815-975b-794e9d0116ee" />

---

# 📌 **데이터셋 특성 (Dataset Characteristics)**

해당 데이터셋은 총 **2,039개의 샘플**로 구성되어 있으며, **7개의 특징(feature)**을 포함합니다:

1. **Distance (거리)**
2. **Pressure (압력)**
3. **HRV (심박 변이도)**
4. **Sugar level (혈당)**
5. **SpO₂ (산소포화도)**
6. **Accelerometer (가속도계)**
7. **Decision (낙상 여부 레이블)**

`Decision`은 최종 낙상 감지 결과를 나타내는 라벨로, 아래와 같은 값을 가집니다:

* **0:** 낙상 없음 (No Fall detected)
* **1:** 미끄러짐(Slip detected)
* **2:** 확실한 낙상(Definite fall)

---
# 🔧 나의 역할 (My Role): 데이터 라벨링 · 전처리 · 정제**

SafeFall Intelligence 프로젝트에서 저는 다중 센서 데이터를 학습 가능한 형태로 만들기 위해
라벨링, 전처리, 정제, 품질 검증을 수행했습니다.
아래는 제가 맡은 핵심 역할입니다.

**📌 나의 주요 역할 (Key Responsibilities)**

라벨링 기준 설계(Decision Labeling)

Decision 레이블(0: 정상 / 1: 미끄러짐 / 2: 확실한 낙상) 정의

낙상 유형 구분 기준을 구조화하고 일관성 확보

센서 데이터 전처리(Data Preprocessing)

이상치 제거(Outlier Removal)

정규화(Normalization)

Noise 필터링 및 기본 데이터 정제

레이블 정합성 검증(Label Consistency Check)

라벨 오류 탐지 및 수정

중복·모순 레코드 제거

모델 훈련을 방해하는 잘못된 레이블 검수

클래스 불균형 처리(Class Imbalance Handling)

RF, K-Means 학습 전 클래스 비율 분석

데이터 편향을 줄이기 위한 구조적 조정

Feature Engineering(특징 엔지니어링)

특징 선택(Feature Selection)

데이터 분포 확인 및 스케일 조정

모델이 이해할 수 있는 특징 구조로 재가공

데이터 품질 관리(Data Quality Management)

전체 데이터셋의 신뢰성을 점검

안정적인 모델 학습을 위한 고품질 데이터 구축

**📌 핵심 요약 (Summary)**

Decision 라벨 기준을 설계하고 정합성 검증을 수행

이상치 제거·정규화 등 센서 데이터 전처리 수행

클래스 불균형 처리 및 Feature Engineering 수행

다중 센서 데이터를 학습 가능한 구조로 정제하며
모델 성능 향상에 직접 기여

**✨ README 강조 문장**

“다중 센서 데이터를 모델이 학습 가능한 형태로 정제·라벨링하며, 안정적인 낙상 예측 모델 개발의 기반 데이터를 구축했습니다.”
---

# 📌 **연구 질문 (Research Questions)**

### **1. 주요 연구 질문 (Primary Research Question)**

1. **예측 정확도(Prediction Accuracy):**
   제공된 특징들을 활용하여 모델이 고령자의 낙상을 얼마나 정확하게 예측할 수 있는가?

---

### **2. 부가 연구 질문 (Secondary Research Questions)**

2. **특징 중요도(Feature Importance):**
   어떤 특징들이 낙상 예측에 중요한 역할을 하며, 모델의 의사결정에 어떻게 기여하는가?

3. **모델 비교(Model Comparison):**
   랜덤 포레스트(Random Forest)와 K-평균(Kmeans) 모델이 낙상 예측 성능에서 어떻게 비교되는가?

4. **False Positive 분석:**
   고령자 낙상 예측 시스템에서 **오탐(False Positive)**이 발생했을 때 어떤 영향과 위험이 있는가?

5. **실환경 적용 가능성(Real-world Applicability):**
   웨어러블 기반 시스템이 가지는 제약을 고려했을 때, 개발된 모델은 실제 환경에서도 활용 가능한가?

---

# 📌 **모델 설계 (Model Design)**

이 프로젝트는 다음 3가지 유형의 머신러닝 모델을 활용합니다:

* **지도학습 모델: 선형 회귀(Linear Regression)**
* **지도학습 모델: 랜덤 포레스트 분류기(Random Forest Classifier)**
* **비지도 학습 모델: K-평균 군집화(Kmeans Clustering)**

랜덤 포레스트 모델은 라벨이 있는 데이터에 대해 `Decision` 값을 목표(target)로 학습하고,
K-평균 모델은 라벨 없이 데이터의 패턴을 탐색합니다.
선형회귀 역시 라벨 데이터를 기반으로 학습하며,
이 세 모델의 비교 분석을 통해 **고령자 낙상 예측에 어떤 모델이 가장 효과적인지**에 대한 통찰을 얻을 수 있습니다.
---

 “논문 인용” 

저희 팀은 먼저, 공개된 연구 논문과 데이터셋을 인용하여
“낙상사고가 데이터로 사전에 예측 가능한 사고인가?”를 검증하는 것부터 시작했습니다.

공개 데이터셋 Elderly Fall Prediction and Detection과 선행 연구 분석을 통해,
센서 데이터만으로도 낙상 위험 패턴을 충분히 포착할 수 있다는 근거를 확보했고,
이 검증이 바로 “세이프폴 인텔리전스” 기획의 출발점이 되었습니다.



---

# 🛡 SafeFall Intelligence

다중 바이오 신호 기반 낙상 **‘예측’** 플랫폼

---

## 1. 문제 인식 (Problem)

<p align="center">
  <img src="https://github.com/user-attachments/assets/8c205892-e0a6-4cbc-9910-6ff3ac97a537" width="45%" />
  <img src="https://github.com/user-attachments/assets/54a76393-4966-46d2-8c92-96ebec0ebb0a" width="45%" />
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/94bb958b-7315-4d8f-babf-f58966621c79" width="60%" />
</p>

* 고용노동부에 따르면 **2022년 기준 재해 유형별 사망 원인 1위는 ‘떨어짐·추락(낙상)’ 사고**이며, 전체 산업재해 사망자의 약 **41.6%**를 차지합니다.
* 요양시설·의료기관 등 일상 환경에서의 **65세 이상 낙상 사고 비율은 2020년 대비 2024년 약 3.2배 증가**했습니다.
* 이러한 낙상 사고는

  * 개인의 부주의 때문이 아니라,
  * **사전 예측·예방 체계 부재, 사후 중심 대응 구조** 등
    **구조적인 안전 시스템의 한계**를 드러내고 있습니다.

---

## 2. 문제 및 해결 방안 (Approach)

<p align="center">
  <img src="https://github.com/user-attachments/assets/9aa20ef9-2e1b-4d23-ac76-1327a6866ab0" width="32%" />
  <img src="https://github.com/user-attachments/assets/b20aa9b3-679c-47b9-963c-eee28d9f9c8c" width="32%" />
  <img src="https://github.com/user-attachments/assets/52450f40-7e74-49d9-ae00-acaf27c32dfb" width="32%" />
</p>

* 현재 대부분의 낙상 관련 솔루션은
  **“사고가 난 이후”에 넘어졌음을 감지**하고,
  이후 보호자·관리자에게 알려주는 **사후 대응 중심 구조**입니다.
* 하지만 실제로는,

  * 이미 넘어지고 난 뒤의 알림은
    **부상·골절·2차 사고를 막기에는 너무 늦습니다.**
* 그래서 SafeFall Intelligence는

  > **“넘어진 뒤 감지”가 아닌, “넘어지기 직전 예측”을 목표로 하는 플랫폼**입니다.

### 🎯 해결 전략 개요

> 웨어러블 기기를 통해 **다중 바이오 신호(자세·심박·산소포화도·피부전도·근전도 등)**를 수집·분석하고,
> **낙상 직전 위험을 실시간 예측 → 사용자 경고 + 관리자 자동 알림**까지 이어지는
> **실시간 낙상 예측 플랫폼**을 구축하는 것이 핵심입니다.

---

## 3. 기술 전략 (Tech Strategy)

<p align="center">
  <img src="https://github.com/user-attachments/assets/81be7766-db8f-47e0-b2e1-16fe0147c374" width="32%" />
  <img src="https://github.com/user-attachments/assets/a4981dc7-e35e-4e3b-ad36-a2ead302a705" width="32%" />
  <img src="https://github.com/user-attachments/assets/814dc523-048d-4b36-b7b8-b49324858bed" width="32%" />
</p>

### 3-1. 데이터 수집 전략

* **3단계 단계적 수집 구조**

  1. **가상 실험 환경**에서 초기 인원(약 30명)을 대상으로
     다양한 낙상·쓰러짐 상황 데이터를 수집
  2. **안전 통제된 세팅 환경**(실험실, 모의 공사장, 요양시설 시뮬레이션 등)에서 반복 실험
  3. **실제 현장**(요양시설·산업현장)으로 확장하여
     **현실 환경에 가까운 데이터** 축적

---

### 3-2. 핵심 기술 요소 (다중 센서 전략)

<p align="center">
  <img src="https://github.com/user-attachments/assets/4116c42d-b594-46ae-8472-a9998dbee827" width="45%" />
  <img src="https://github.com/user-attachments/assets/296d21c9-ae06-44ee-994f-4cb23434f3d9" width="45%" />
</p>

**1) IMU (가속도 + 자이로 센서)**

* 보행·자세 변화·균형 무너짐 패턴을 감지
* **낙상 직전 급격한 자세 변화 패턴**을 실시간 포착

**2) HRV (심박 변이도)**

* 심박 리듬 변화로 **실신·어지러움·자율신경 불안정**을 사전 감지

**3) SpO₂ (산소포화도)**

* 산소포화도 저하 → **저산소·탈수·피로·컨디션 저하** 상태 탐지

**4) EDA (피부전기활성)**

* 교감신경 활성도를 기반으로 **긴장·스트레스·위험 상황 반응** 파악
* 낙상 가능성이 높은 **불안정 상태** 탐지에 사용

**5) EMG (근전도)**

* 근육 수축 시 발생하는 전기 신호를 분석
* **균형 상실, 미끄러짐, 근피로**와 관련된 패턴 파악

> 👉 이 다섯 가지 신호를 **멀티모달 딥러닝 모델**로 통합해
> **낙상 직전 패턴을 예측하는 구조**를 지향합니다.

---

### 3-3. 단계별 기술 로드맵

<p align="center">
  <img src="https://github.com/user-attachments/assets/4b907dae-2e4d-4f18-b2ad-b8ee7f1692d6" width="45%" />
  <img src="https://github.com/user-attachments/assets/b0a123c6-6f7f-4b1c-b5d4-746f620226aa" width="45%" />
</p>

#### 🔹 1차 목표: 스마트워치 기반 온디바이스 AI

* 사용 센서:

  * **IMU + HRV + SpO₂ (3종)**
* 디바이스:

  * 이미 상용화된 **Apple Watch, Galaxy Watch 등**을 활용
* 기능:

  * **낙상 발생 약 0.5~1초 전에 위험 패턴을 감지**
  * 온디바이스 딥러닝 모델로 **즉각적인 진동·알림 제공**
* 장점:

  * 별도 하드웨어 개발 없이 **빠른 시장 검증 가능**
  * 초기에는 **앱 기반 MVP**로 빠르게 실사용 테스트 가능

#### 🔹 2차 목표: 전용 디바이스 + 서버 기반 멀티모달 모델

* 추가 센서: **EDA + EMG** 센서 탑재
* 폼팩터:

  * 워치의 한계를 보완하기 위해 **조끼·밴드 등 몸 중심부 착용 디바이스** 설계
* 아키텍처:

  * 디바이스 → 서버로 **스트리밍되는 멀티센서 데이터**
  * 서버에서 **고정밀 멀티모달 딥러닝 모델**로 분석
* 목적:

  * 더 높은 정확도로 **산업현장·요양시설 특화 낙상 예측 모델** 구축

---

### 3-4. 구현 사례 및 성과 지표 참고

<p align="center">
  <img src="https://github.com/user-attachments/assets/463cdb0b-7cd1-4ae2-9d1d-1768e436681f" width="45%" />
  <img src="https://github.com/user-attachments/assets/be464780-83fd-4c59-9d70-2277d03a53ba" width="45%" />
</p>

* 노인의 균형상태, 생체신호, 주변환경 데이터를 활용해
  **낙상 예측 모델을 구현한 GitHub 연구 자료**를 분석한 결과,

  * 피어슨 상관계수 기준

    * **압력, 심박수, 산소포화도**가 낙상 여부와 높은 상관성을 보였고
    * 혈당 변화는 낮은 상관성을 보여 제외 가능성이 확인됨
* 비지도 K-Means 기반 모델임에도,

  * **정확도 약 83%**
  * **F1-Score 약 82%**
    의 성능을 보여, **센서 데이터만으로도 낙상 유형 분리 및 예측 가능성**이 충분함을 뒷받침합니다.

---

## 4. 시장 기회 (Market Opportunity)

<p align="center">
  <img src="https://github.com/user-attachments/assets/72d8a966-71ad-405b-b23d-bc1e9693d66e" width="45%" />
  <img src="https://github.com/user-attachments/assets/83b8d5c2-cc4a-4482-b05b-e0253ccedc45" width="45%" />
</p>

* 국내 **웨어러블 시장(산업안전 + 실버케어 + 헬스 + 공공복지)** 규모는
  **2024년 기준 약 1.7조 원**
* 향후 연평균 성장률 **15~22%** 전망
* 성장 촉진 요인:

  * 중대재해처벌법 시행(산업안전 책임 강화)
  * 고령화 가속 → 실버케어 수요 확대
  * 지자체 스마트 복지·돌봄 강화
  * 디지털 헬스 관련 규제 완화

### 🎯 타겟 시장 정의

* **전체 시장(모든 잠재 시장):**

  * 산업안전
  * 실버케어·요양
  * 웰니스
  * 공공 복지/조달

* **유효 시장:**

  * 산업안전
  * 요양·복지 분야

* **초기 목표 시장:**

  * B2B, B2G 특성상 진입 장벽이 높음을 고려하여
  * **1% 수준의 보수적 초기 점유율**로 설정

---

## 5. 경쟁사 및 차별점 (Competition)

<p align="center">
  <img src="https://github.com/user-attachments/assets/3cdbbcd8-f542-496d-8f49-aba9d6b56196" width="45%" />
  <img src="https://github.com/user-attachments/assets/31fc1de6-8a5a-4aff-8788-506ef77fde4a" width="45%" />
</p>

* **스마트워치**

  * 일반 소비자 중심
  * 운동·피트니스 위주 / 낙상은 “감지” 수준에 머무름
* **산업 안전밴드**

  * 낙상 발생 후 **보고 중심(사후 보고)**
  * 사고 이후 대응에 초점
* **실버케어 밴드**

  * 심박/활동량 기반의 **사후 건강 관리 중심**
* **해외 낙상 솔루션**

  * 대부분 **단일 IMU 기반 + 스포츠용**
  * 산업현장·요양시설의 복잡한 환경에는 적합하지 않음

### ✅ SafeFall Intelligence의 차별점

> **IMU + HRV + SpO₂ + EDA + EMG**
> **3개 이상 다중 센서를 엣지/서버 혼합 구조로 활용하는 예측형 솔루션**

* 단순 감지가 아닌 **“낙상 직전 예측”**
* 산업·요양 환경에 맞춘 **고정밀 멀티모달 분석**
* B2B/B2G 도입에 적합한 **플랫폼 구조 + 데이터 연계성**

---

## 6. 비즈니스 모델 & 자금 계획 (Biz Model & Funding)

<p align="center">
  <img src="https://github.com/user-attachments/assets/6459ec70-a419-44e7-96cc-dada976e8ea0" width="45%" />
  <img src="https://github.com/user-attachments/assets/7d61fe9b-5e98-4c58-8cc4-11e017b7564f" width="45%" />
</p>

### 💰 비즈니스 모델 (3축 수익 구조)

1. **HW 판매**

   * 전용 밴드·조끼 등 디바이스 일회성 판매
2. **SaaS 구독**

   * 시설·기업 단위 월 구독 모델 (관리자 대시보드, 알림 시스템 포함)
3. **데이터 제휴**

   * 연구기관·보험사·지자체와의 데이터 연계, 분석 리포트 제공

### 📌 시장 진입 전략

* **조달형 B2G 판매**
* **PoC 계약형 패키지 모델**
* **SaaS 구독형 B2B 서비스**

### 💸 개발·실증 비용 및 단계

* 총 필요 비용: **약 8.5억 원**
* 단계별 구성:

  1. PoC 단계: 약 **1.3억**
  2. MVP 개발 단계: 약 **3.5억**
  3. Pilot 단계(실증·확산): 약 **3.7억**

### 🔄 자금 조달 전략

* 정부지원 과제(2단계 과제 반영)
* 지자체 실증 연계
* 민간 투자(Seed)
* 초기 고객 선계약 기반 실증비 매칭

→ **지속 가능한 개발·운영이 가능한 자금 흐름 구조** 설계

---

## 7. 기대 효과 (Impact)

<p align="center">
  <img src="https://github.com/user-attachments/assets/79ffc046-63e4-48b2-bed8-954cd0a17699" width="45%" />
  <img src="https://github.com/user-attachments/assets/4f61a93a-8971-43ac-ad96-090f35204e0a" width="45%" />
</p>

### 🔧 기술적 기대효과

* 다중 바이오 신호 기반 **낙상 “예측” 기술** 구현
* 단기·장기 위험을 함께 판단할 수 있는 **고도화된 위험도 모델**
* 사용 데이터가 쌓일수록 성능이 계속 향상되는 **확장형 AI 플랫폼** 구축

### 🌍 사회적 기대효과

* 고령자 및 건설·산업현장의 낙상을 **사전에 예측**해

  * 중증 부상·후유증
  * 의료비·산재비·시설 관리 비용
    을 동시에 절감
* 지역사회·산업현장 **안전 체계 강화**
* 초고령사회·산업안전 정책과 맞닿는 **ESG·사회적 가치 창출**

---

## 8. 팀 소개 (Team)

<p align="center">
  <img src="https://github.com/user-attachments/assets/3a163713-0e6a-4c91-9c3c-19df41e67226" width="48%" />
  <img src="https://github.com/user-attachments/assets/a29ae082-2618-4b33-bd11-9e1227298c86" width="48%" />
</p>

* AI·데이터, HCI, 비즈니스 전략, 산업안전, 시니어 케어 등
  다양한 전공과 경험을 가진 팀원들로 구성
* 기술 개발뿐 아니라

  * **현장 실증**
  * **지자체·기관 협력**
  * **ESG 및 공공 가치 반영**
    까지 고려한 **종합형 팀 구성**


📚 내가 배운 점 (What I Learned) — 금융권 관점 정리

SafeFall Intelligence, 보이스피싱 HITL 서비스, 공급망 예측 모델링 등을 개발하면서
저는 “데이터가 잘못되면 실제 사람이 피해를 입는 도메인”이 얼마나 중요한지 직접 경험했습니다.
이 과정은 자연스럽게 금융권 시스템이 왜 가장 높은 신뢰성과 안정성을 요구하는지를 깊이 이해하게 했습니다.

⭐ 1) 데이터 오류가 곧 ‘금전적·생명적 피해’로 연결될 수 있다는 사실

보이스피싱 프로젝트에서는
STT 인식 오류 하나로 위험 탐지가 실패해 실제 피해자가 위험에 노출될 수 있었습니다.

낙상 예측 모델에서는
센서 데이터 지연 0.5초만 발생해도 사고를 막지 못하는 상황을 경험했습니다.

공급망 예측에서는
예측 오차가 조금만 커져도 농가·물류사가 직접적인 금전적 손해를 겪습니다.

이 경험을 통해 금융 데이터도 마찬가지로
한 번의 오류가 부정확한 거래, 잘못된 리스크 평가, 고객 자산 손실 등으로 이어질 수 있음을 깨달았습니다.

→ 결국 “데이터 정확성·신뢰성”이 생명이라는 금융 시스템의 본질을 체감했습니다.

