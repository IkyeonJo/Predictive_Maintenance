
# 프로젝트 수행 개요/계획
---

## 1) 데이터 이해 및 정합성 점검

- 센서 종류, 샘플링 주기, 수집 기간 확인
- 설비별 운전 조건 확인
- 정상/이상/고장 이력 확보 여부 확인
- 결측치, 이상치, 드리프트, 센서 불량 점검

## 2) 탐색적 시계열 분석

- 시간대별 패턴
- 운전 조건별 분포 차이
- 이벤트 직전 패턴 변화
- 설비별 개체 차이
- 계절성/주기성/부하 영향 확인

## 3) Feature Engineering

- RMS
- Peak-to-peak
- Kurtosis
- Skewness
- Crest factor
- FFT dominant frequency
- band power
- envelope analysis 관련 특징
- rolling statistics
- time-window aggregation features
- lag features
- operating regime별 normalized features

## 4) 모델링

가능한 방향은 보통 다음과 같습니다.

- 지도학습: 고장 라벨이 있으면 binary classification / multiclass classification
- 반지도/비지도: 라벨이 부족하면 Isolation Forest, One-Class SVM, Autoencoder류
- 트리 기반: XGBoost, LightGBM
- 시계열 딥러닝: LSTM, 1D CNN, Temporal model

## 5) 검증 및 성능 개선

- 시간 누수(data leakage) 방지
- 설비별 generalization
- 고장 직전 구간 검증
- false alarm 최소화

## 6) PoC 리포트 작성

다음과 같은 내용을 포함한 기술 보고서 + 사업적/운영적 시사점 도출
- 어떤 데이터로
- 어떤 가설을 세웠고
- 어떤 특징이 유의미했고
- 어떤 모델이 가장 타당했으며
- 한계는 무엇이고
- 다음 단계에서 무엇이 필요한지