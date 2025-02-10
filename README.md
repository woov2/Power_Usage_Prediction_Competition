# 2023 DACON Power Usage Prediction Competition
### 전력사용량 예측 AI 개발

## 1. 배경 & 목적

- 안정적이고 효율적인 에너지 공급을 위해서는 전력 사용량에 대한 정확한 예측이 필요.
- 전력사용량 예측 AI 모델 개발.
- 평가 지표: SMAPE

<br/>

## 2. 주최/주관 & 참가 대상 & 성과

- 주최/주관: 한국에너지공단 / DACON
- 참가 대상: 데이커라 누구나
- 성과: 상위 1%

<br/>

## 3. 대회 기간

- 제출마감: 2023년 08월 28일
- 코드 평가 마감 및 최종순위 발표: 2023년 09월 18일

<br/>

## 4. 내용
- 건물번호를 기준으로 전력소비량의 상위,하위 1%를 이상치로 간주하여 clip
- 건물별, 요일별, 시간별 전력소비량의 평균 및 표준편차 feature 생성
- 공휴일 feature 생성
- 날짜 feature에 대한 sim,cos transformation
- 온도, 습도에 대한 min/max/mean feature 생성
- l1 / l2 loss function Ensemble
- 이전 1달에 대한 전력 소비량을 기준으로 post processing

<br/>

## 5. Process

### ch.1 Feature Engineering

- EDA
- Building/dayofweek/hour based mean, std Feature
- Holiday Feature
- Sin/Cos Transformation
- Various Temp/Humid Feature

---

### ch.2 Preprocessing

- Outlier Processing
- NAN Processing

---

### ch.3 Modeling

- LGBM(L1/L2 Loss Ensemble)
- XGB(L1/L2 Loss Ensemble)

---

### ch.4 Ensemble

- Loss Function
- Seed
- Weighted Ensemble

<br/>

## 6. 참고자료

[데이콘 2023 전력사용 예측 AI 경진대회 사이트](https://dacon.io/competitions/official/236125/overview/description)
