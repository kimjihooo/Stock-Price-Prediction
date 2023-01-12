# KOSPI50 일일 종가 예측모형 개발

## 1. 프로젝트 소개
**기간** : 2022.11 - 2022.12

**목적** : 코스피 200 구성종목 가운데 시가총액이 큰 상위 50 개 종목으로 구성된 KOSPI50 의 일일 종가를 예측. 주가의 정확한 가격 예측이 아닌 주가의 상승과 하락을 예측하는 것을 모형의 목표.

## 2. 주요 내용
**데이터** : 코스피50 종목의 2020 년 1 월 1 일부터 2022 년 11 월 30 일까지의 데이터

**모델** : RandomForest, XGBoost, LightGBM, CatBoost

**성능** : 0.67

### (1) 변동기울기
회귀계수의 개념을 사용해 시간의 흐름에 따른 주가의 변동성 반영하는 변수 생성

<img width="600" alt="3" src="https://user-images.githubusercontent.com/97178674/211950249-33a794c6-d53e-43a7-98f9-e95e99ccc2f4.png">


### (2) stacking 메타모형
초모수 조절한 최종 4 가지 예측모형의 예측치를 특성변수의 입력하여 최종예측치를 출력하는 stacking 메타모형을 사용해 성능향상

로지스틱 회귀모형을 메타모형으로 사용

### (3) 변수중요도

<img width="600" alt="1" src="https://user-images.githubusercontent.com/97178674/211950179-cc510a92-2a91-43b2-ade5-36106eb43465.png">

<img width="600" alt="2" src="https://user-images.githubusercontent.com/97178674/211950190-a3d9b565-6448-46ac-9dd3-b4f21619160c.png">



