# 예지보전(Predictive Maintenance) 스터디 및 데이터 분석 프로젝트

## 개요

- 회전 설비(모터, 펌프) 예지보전 관련 스터디 및 데이터 분석 프로젝트
- 데이터분석은 다음 내용 포함
  - 산업용 예지보전 분석을 공개 센서 데이터셋을 활용해 수행
  - 다변량 센서 데이터와 진동 신호 분석을 기반으로 회전 기계 설비의 이상 탐지 및 고장 예측 파이프라인을 구축

## 데이터셋

- [AI4I Predictive Maintenance Dataset](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset): AI4I 2020 예측 유지보수 데이터셋은 산업 현장에서 실제로 접할 수 있는 예측 유지보수 데이터를 반영한 합성 데이터셋
- Case Western Reserve University (CWRU) Bearing Data: 회전 기계 설비의 진동 신호 데이터셋으로, 정상 및 다양한 고장 상태의 데이터를 포함

## 분석 내용

- AI4I 2020 Predictive Maintenance Dataset을 기반으로 예지보전 분석을 수행
  - 전처리, 불균형 대응, XGBoost/LightGBM baseline, PR-AUC 및 Recall 중심 평가, SHAP 기반 해석까지 포함하여 고장 예측 파이프라인을 구성
- **Case Western Reserve University (CWRU) Bearing Data Center**의 실제 베어링 진동 데이터를 활용하여, 회전설비의 이상 상태를 진동 신호 기반으로 분석하고 **특징량 추출(feature engineering)** 및 **기초 고장 분류 모델링**까지 수행