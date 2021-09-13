# 원티드(wanted) "프리온보딩 코스_데이터 분석가" 세번째 프로젝트

### File 현황

- [Week3] moduparking_DB_EDA_v0.1.ipynb : 작업 진행 중(1차)
- [Week3] moduparking_DB_EDA_v0.3.ipynb : 작업 진행 중(2차)
- [Week3] moduparking_DB_EDA_v0.5.ipynb : 작업 진행 중(3차)
- [Week3] moduparking_DB_EDA_Modeling_v0.7.ipynb : 작업 진행 중(4차)
- [Week3] moduparking_DB_EDA_Modeling_v1.0.ipynb : 완성본(v1.0)

<br/>

# 완성본(v1.0) 주요 내용

### 모두의주차장 앱 이용자별 향후 이용건수 예측

<br/>

### 1. Data 형태 파악 및 Feature별 검토

### 2. 예측 모델에 활용할 주요 Feature 선별을 위한 분석작업

&nbsp;&nbsp;&nbsp; - 요일 및 날짜에 따른 이용량 변화 분석 : 월별/"GOODS_TYPE"별 기준 복합 적용

<img src="https://user-images.githubusercontent.com/76440511/132984015-c7c5fbdd-d17a-4528-9d13-15ee2a2e7d2e.png" width="700">

<br/>

### 3. 유저별 이용건수 예측 - 단계별 진행
<br/>

#### 3-1. 예측 모델에 활용할 주요 Feature 선별 및 유저별 이용건수 예측(1차)<br/>

<img src="https://user-images.githubusercontent.com/76440511/132992677-75c92918-e941-41ca-971d-d3ce45b55514.png" width="820">

#### &nbsp;&nbsp;&nbsp;=> 유저별 이용건수 1차 예측 결과, MSE는 0.16944 ~ 0.17540 수준, MAE는 0.08399 ~ 0.08621 수준으로 측정됨
#### &nbsp;&nbsp;&nbsp;=> 현재까지 적용한 OneHotEncoding & Scaler 버전을 기반으로, 이후 추가 Feature 적용 등을 통한 예측 모델 고도화 테스트 진행 예정

<img src="https://user-images.githubusercontent.com/76440511/132984793-0250e201-699f-4ad5-a614-0a46b2396379.png" width="900">

<br/>

#### 3-2. Feature 추가, 외부데이터 활용 및 유저별 이용건수 예측(2차)<br/>

<img src="https://user-images.githubusercontent.com/76440511/132992969-9bf77ceb-8a6b-4c03-b0bf-5f55a210df47.png" width="600">

#### &nbsp;&nbsp;&nbsp;=> 유저별 이용건수 2차 예측 결과

<img src="https://user-images.githubusercontent.com/76440511/132993163-f547ce82-cdac-4f85-bda9-5acefa5d4ee7.png" width="820">

#### &nbsp;&nbsp;&nbsp;=> 추가적으로 이용건수 기준의 USER 그룹 지표를 적용한 뒤, 모델 성능 개선 테스트 진행 예정

<br/>

#### 3-3. USER 그룹 지표 추가 및 유저별 이용건수 예측(3차)<br/>

<img src="https://user-images.githubusercontent.com/76440511/133054463-10f2b505-08d1-449c-b468-cf30e56f44fe.png" width="500">

<img src="https://user-images.githubusercontent.com/76440511/133054764-fb1b15f5-cfcd-4c89-8a56-23b2ace7a42a.png" width="280">

##### "USER_GRADE" Feature 적용 후, 예측 수행 및 성능 측정
 - "요일" 및 "GOODS_TYPE" OneHotEncoding
 - Scaling 진행
 - Training data, Test data 준비

<img src="https://user-images.githubusercontent.com/76440511/130348788-8dfe7f94-2ea0-4b48-b7ab-8a15c6be58ca.png" height="300">

<img src="https://user-images.githubusercontent.com/76440511/133056167-4382f22a-8ee7-4a81-b6e6-619c654ae24a.png" width="900">

#### &nbsp;&nbsp;&nbsp;=> 1차, 2차에서 부분적인 성능 개선 효과가 있긴 했지만 제한적이었던 데에 반해, 3차에서는 확실한 성능 개선 효과가 나타나는 것을 확인함
#### &nbsp;&nbsp;&nbsp;=> 더불어, 랜덤포레스트 적용 시 하이퍼 파라미터 튜닝을 통해 추가적인 성능 개선이 나타남을 확인함

### 4. 결론
- 이용자별 이용건수 예측 모델 평가(MSE, MAE) 및 정리
