# 🔥 Calories-Burned-Prediction-ML
OZ AI BootCamp 03 mini project

> **신체 지표 및 운동 데이터를 활용한 고정밀 칼로리 소모량 예측 머신러닝 모델 개발**

본 프로젝트는 개인의 신체 정보(성별, 나이, 체중 등)와 운동 정보(심박수, 체온, 운동 시간)를 바탕으로 실시간 칼로리 소모량을 예측하는 모델을 구축하는 것을 목표로 합니다. 데이터 전처리부터 모델 최적화, 해석까지의 전체 머신러닝 파이프라인을 구현했습니다.

---

## 🎯 프로젝트 목표 (Project Objectives)
- **정밀한 소모량 예측:** 다양한 신체 지표를 기반으로 오차를 최소화한 칼로리 예측 모델 구축
- **모델 최적화:** Optuna를 활용한 하이퍼파라미터 튜닝으로 모델 성능 극대화
- **앙상블 기법 적용:** CatBoost와 Gradient Boosting의 결합을 통해 모델의 일반화 성능 향상
- **모델 해석성 확보:** SHAP Value 분석을 통해 칼로리 소모에 기여하는 핵심 변수 규명

## 🛠 기술 스택 (Tech Stack)

### **Machine Learning & Analysis**
- ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
- ![Scikit-Learn](https://img.shields.io/badge/scikitlearn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
- ![CatBoost](https://img.shields.io/badge/CatBoost-FF4B4B?style=for-the-badge&logo=PyTorch&logoColor=white)
- ![Optuna](https://img.shields.io/badge/Optuna-4E94CE?style=for-the-badge&logo=python&logoColor=white)

---

## 📊 핵심 프로세스 및 성과 (Key Process & Results)

### 1. 데이터 전처리 및 EDA
- **특성 공학(Feature Engineering):** 체질량지수(BMI), 체표면적(BSA) 등 신규 피처 생성을 통한 모델 성능 개선.
- **이상치 처리:** Box-Cox 변환 및 Clipping 기법을 적용하여 데이터 왜곡 최소화.

### 2. 하이퍼파라미터 최적화
- **Optuna 활용:** 베이지안 최적화(TPE)를 사용하여 모델의 핵심 파라미터 자동 튜닝.
- **10-Fold Cross-Validation:** 데이터 누수(Data Leakage)를 방지하고 신뢰도 높은 평가 지표 산출.

### 3. 주요 인사이트 (SHAP Analysis)
> "심박수와 운동 시간이 칼로리 소모량 결정의 핵심 변수임을 수치적으로 증명했습니다."

* **심박수(Heart Rate):** 칼로리 소모와 가장 강력한 양(+)의 상관관계를 보임.
* **운동 시간(Duration):** 소모량 예측에 있어 두 번째로 중요한 기여도를 차지함.
* **성별 가중치:** 동일 조건 하에서 성별에 따른 대사율 차이가 모델 가중치에 유의미하게 반영됨.

---

## 📈 모델 결과 시각화 (Visualization)
*(이곳에 코드 결과물 중 'SHAP Summary Plot'이나 'Actual vs Predicted' 산점도 이미지를 캡처해서 넣어주세요)* `![SHAP Plot](./docs/shap_summary.png)`

---

## 📂 프로젝트 자산 (Project Assets)
- [📄 최종 발표 자료 (PDF)](./Calorie_Prediction_Presentation.pdf)
- [📓 모델링 및 분석 코드 (.ipynb)](./머리어깨8조_예측모델미니프로젝트_제출_260223.ipynb)

---

## 📚 연구 및 이론 근거 (Technical Reference)
- *Prediction of energy expenditure from heart rate monitoring during submaximal exercise (Journal of Sports Sciences, 2026)*
- *Revised Harris-Benedict Equation: New Human Resting Metabolic Rate Equation (Metabolites, 2023)*
