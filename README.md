# 고속도로 교통사고 예측 프로젝트

> 고속도로 사고 데이터를 분석하여 사고 위험도를 예측하는 머신러닝 모델 개발 프로젝트입니다.<br>
> [발표자료 보기: 고속도로 사고 예측 (PDF)](./고속도로%20사고%20예측.pdf)
---

## 프로젝트 개요

고속도로 사고의 높은 치사율과 기후 변화에 따른 위험 증가에 대응하기 위해, 과거 사고 데이터를 기반으로 사고 위험도를 예측하고 고위험 조건을 사전에 식별하는 것이 목표입니다.

---

## 데이터 개요

- **출처**: TASS 교통사고 분석 시스템
- **기간**: 2020년 ~ 2022년
- **대상**: 주요 고속국도 (경부, 남해, 중앙 등 9개 도로)
- **종속변수**: 사고 위험도 (ARI 지수 기반 상/중/하)
- **파생 변수**: 시간대, 계절, 요일, 지역, 주야간 여부 등
- **전처리**:
  - 널값 및 이상치 처리
  - 파생 변수 생성
  - 카이제곱 검정으로 유의미 변수 선정

---

## 적용 모델

1. **Random Forest**
2. **Support Vector Machine (SVM)**
3. **AdaBoost**
4. **XGBoost**

---

## 모델 성능 비교

| 모델명         | 정확도 (Accuracy) | F1-score |
|----------------|-------------------|----------|
| Random Forest  | 0.940             | 0.928    |
| SVM            | 0.920             | 0.897    |
| AdaBoost       | 0.925             | 0.892    |
| XGBoost        | 0.929             | 0.923    |

> Random Forest가 가장 뛰어난 성능을 보였습니다.

---

## 주요 인사이트

- **가을**, **맑음**, **건조한 노면**에서 사고 위험도(중/상)가 가장 높게 나타남
- 가해자는 대부분 **상해 없음**, 피해자는 **중상** 발생 비율이 높음
- **노면 상태 '건조'**가 전체의 88.2% → 데이터 편향 존재

---

## 한계점

- 운전자 숙련도, 차량 상태 등 비정형 변수 미포함
- 회귀 분석 시 종속변수의 정규성 부족으로 R²값 낮음
- 일부 변수의 **데이터 불균형**이 모델 성능 저하 요인

---

## 기술 스택

<div align="left">

<img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=Python&logoColor=white"/>
<img src="https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white"/>
<img src="https://img.shields.io/badge/Numpy-013243?style=flat&logo=numpy&logoColor=white"/>
<img src="https://img.shields.io/badge/Matplotlib-11557C?style=flat&logo=matplotlib&logoColor=white"/>
<img src="https://img.shields.io/badge/Seaborn-16A085?style=flat&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white"/>
<img src="https://img.shields.io/badge/XGBoost-EC6610?style=flat&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=Jupyter&logoColor=white"/>

</div>

---

## 팀원

- 정다훈, 강하빈, 김세령, 김지훈, 조민서

---

## 참고 링크

- [TASS 교통사고 분석 시스템](https://www.taas.koroad.or.kr/)

