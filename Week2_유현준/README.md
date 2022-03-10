# 원티드(wanted) "프리온보딩 코스_데이터 분석가" 두번째 프로젝트

### File 현황

- [Week2] Jobis_3o3_DB_EDA_v0.1.ipynb : 작업 진행 중(1차)
- [Week2] Jobis_3o3_DB_EDA_v0.3.ipynb : 작업 진행 중(2차)
- [Week2] Jobis_3o3_DB_EDA_v0.7.ipynb : 작업 진행 중(3차)
- [Week2] Jobis_3o3_DB_EDA_v1.0.ipynb : 완성본(v1.0)

<br/>

# 완성본(v1.0) 주요 내용

### 자비스앤빌런즈 "삼쩜삼" 서비스에 대한 고객 Data 분석

<br/>

### 1. Data 구조 파악 및 Feature별 검토
- 총 9개 Feature, 10만개 data로 구성

<img width="646" alt="image" src="https://user-images.githubusercontent.com/76440511/156967131-4728c164-2730-4db9-bdae-1f2507c3c156.png">

### 2. 고객의 결제여부에 영향을 미치는 요인 분석

2-1. 전체 Feature간 상관관계 파악<br/>
2-2. 고객의 결제여부("has_paid")에 따른 특성 비교<br/>
2-3. 결제여부 판단을 위한 "결제비율(%)" 지표 산출 및 그룹별 특성 비교<br/>

<img src="https://user-images.githubusercontent.com/76440511/130347734-d2bc55a7-f7b2-493c-9d78-69ad4b3947b3.png" width="700">

### 3. 고객의 수수료 결제금액의 합을 높이기 위한 방안 검토

**'나이'와 '예상환급액'에 따른 결제비율 특성을 세부적으로 비교/분석**<br/>
&nbsp;&nbsp; => 각 세부그룹별 특성을 종합적으로 비교/분석해 의미를 도출<br/>
&nbsp;&nbsp; => 고객 Segment별 분석 통한 "고객의 수수료 결제금액 총합"을 높이기 위한 방안 검토


<img width="725" alt="image" src="https://user-images.githubusercontent.com/76440511/153356037-fe4561b5-f29e-437a-95d1-25323fb3766f.png">
<img width="725" alt="image" src="https://user-images.githubusercontent.com/76440511/153356217-40de73c8-6592-40cf-abd0-54b75a59f27d.png">
<img src="https://user-images.githubusercontent.com/76440511/130347993-0465231c-14e4-42a7-8809-b40d8c12c4ad.png" width="725">
<img width="725" alt="image" src="https://user-images.githubusercontent.com/76440511/153356358-8f819b6b-65cb-4cd1-9801-b12862e8650e.png">
<img width="725" alt="image" src="https://user-images.githubusercontent.com/76440511/153356407-ad724d9f-6e3c-4407-9fd6-5008838c5b1a.png">
<img width="725" alt="image" src="https://user-images.githubusercontent.com/76440511/153356456-23f21fff-83b4-42bf-b45e-9665565ee89b.png">
<img width="725" alt="image" src="https://user-images.githubusercontent.com/76440511/153356515-f04b5c8f-c4e8-40c5-8a7a-41194acb8a2e.png">


### 4. 결론 : "고객의 수수료 결제금액의 총합"을 높이기 위한 방안(2가지 차원)

#### 1) (총 결제건수를 높이는 차원) 수수료 정책상 20세~29세 고객에게 강하게 나타나는 허들금액 효과 제거
* 현 산출방식 기준 수수료가 1만원 이상으로 조회되는 고객이 20대일 경우, 수수료 상한선 9900원 또는 차등적 할인율 적용
* 기대효과<br>
  (1) 기존에 조회만 하고 수수료가 비싸 결제를 하지 않은 20대 고객의 결제 진행으로 "총 결제건수" 볼륨 증가<br>
  (2) 기존 산출방식 대비 당장은 수수료 금액이 작아지는 측면도 있을 수 있으나 현재 data상 "has_paid"가 True인 건들의 수수료 평균이 약 6209원(첨부자료 1. 참조)인 점을 감안할 때, 9900원 수준의 결제 건 볼륨이 증가한다면 전체 평균금액도 상승하는 효과를 기대 가능<br>
  (3) 또한, 현재 20대인 고객이 향후 30대가 되었을 때 더 큰 수수료 금액을 결제할 수 있으므로 장기적인 고객확보 차원에서도 긍정적임<br>

#### 2) (평균 결제금액을 높이는 차원) 현재 20대에 지나치게 치중된 고객비중을 30대로 확대
* 20대 대비 허들금액 효과가 크지 않고, 높은 수수료 금액의 비중이 큰 30대에 대한 집중 마케팅 전개
* 기대효과<br>
  (1) 현재 20대 대비 3분의 1수준인 30대 고객이 증가할수록 A그룹(1~11그룹)의 결제 비중이 향상될 것임(=> 평균 결제금액 증가)<br>
  &nbsp;&nbsp; ※ A그룹의 평균 수수료는 2.3만원 수준으로, B그룹(6.4천원) 또는 C그룹(1.1천원) 대비 훨씬 높은 수준임(첨부자료 2. 참조)<br>
  (2) 장기적인 관점에서도 30대 고객이 증가하면 연쇄적으로 소득수준이 높은 고연령층 고객의 유입이 전망되며, 이로 인해 고객 증가가 평균 결제금액 상승으로 이어지는 선순환 효과를 기대 가능<br>
