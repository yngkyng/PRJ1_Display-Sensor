# Display-Sensor
2023-02-20~ 2023-02-24
시각화 (Part1,Part2)
PPT적용

결론 도출
Part 1:

사용연식, 에러횟수, 교체횟수, 고장횟수간 에러횟수와 고장횟수 사이에는 각각 약한 상관관계가 존재함(상관계수 0.47,0.48)

요인들(전압,회전,압력,진동)의 이상치가 고장과 연관성이 있는지 확인해봤을때, 고장은 압력과 진동 이상치와 상관성 존재
(상관계수 0.6, 0.5)


기계 부품의 고장, 일반적, 종합 교체주기를 확인해봤을때
고장의 교체주기 = (1: 124.04일), (2: 136.96일), (3: 92.89일), (4: 117.81일)
정기적 교체주기 = (1: 68.17일), (2: 55.12일), (3: 75.642일), (4: 66.16일)
고장난 주기 124일, 정기교체주기 68일, 평균 교체주기 94일

고장나기 전에 미리 바꾸는 목적으로 정기교체가 이루어지는건데, 지금은 고장 주기에 비해 지나치게 빨리 정기교체가 이루어진다.

- 가설 설정
부품1만 놓고 본다면, 평균 교체주기인 94일 정도로만 정기교체시기를 늦춰도,
약 한달 가량의 시간을 더 사용할 수 있음.

이로 인해 부품 소모비와 교체를 위해 사용하지 못하는 시간 절약이 가능함.
정기적인 교체주기와 종합 교체주기를 확인했을때 부품 2번이 종합적인 교체주기보다 평균 2일정도 교체를 더 일찍하는것을 확인할수있으며 부품 3번이 고장에의해 교체되는 주기가 다른 부품들에비해 빠른것으로 나타납니다.

- 모델 종류별 고장률 찾기
모델 1번과 모델 2 가 고장률이 높은것으로 나타나며 기계 교체시 모델3 또는 모델 4로 교체하는것이 긍정적으로 나타난다.


<데이터2>

### 1. 제품 유형 별로 볼 때, H(4.6%)와 M(22.9%)은 상대적으로 실패 비율이 낮고, L(72.5%)은 실패 비율이 높다.

### 2. 고장 원인 분석 
 
#### 2-1 고장 원인 : 열 방산
기온과의 상관계수가 가장 높으며,
기온이 27.65도 이상, 공정온도 36.25도 이상, 회전속도 1379 rpm 이하, 회전력 41.6Nm 이상의 조건에서 기계 고장이 일어나는 것으로 보인다.

#### 2-2 고장 원인 : 과부하
공구 마모 시간과의 상관계수가 가장 높으며,
회전속도 1515 rpm 이하, 회전력 46.3Nm 이상, 공구 마모 시간 172min 이상의 조건에서 기계 고장이 일어나는 것으로 보인다.

### 2-3 고장 원인 : 동력 이상
회전속도와 가장 높은 상관관계를 가지며,
회전속도 1479 rpm 이하 또는 2153 rpm 이상, 회전력 15.3Nm 이하 또는 58.5Nm 이상의 조건에서 기계 고장이 일어나는 것으로 보인다 

### 2-4 고장 원인 : 무작위
 
#### 상관관계 : 공정온도, 회전속도와 상관관계를 가지며   
랜덤 고장원인은 평균적으로 기온 27.8도, 공정온도 37.2도, 회전속도 1,474 RPM, Torque 52 Nm, 공구마모 시간 136분 에 발생하였다.
랜덤 고장 발생 시 공구마모의 시간의 Type 별 평균 시간은 H타입 52분, M타입 107분, L타입 147분 이며
  고장 미발생의 경우 H타입 124분, M타입 119분, L타입 144분 으로 H타입이 평균 72분 정도 빨리 고장 발생되었음을 알 수 있다.     

### 3. 종합해 봤을 때, 고장을 막기 위해서는
#### 3-1. 기온은 27.65도, 공정 온도는 36.25도를 넘기지 않는 환경에서,
#### 3-2. 회전속도는 1515~2153rpm 수준으로, 회전력은 15.3~46.3Nm 수준으로 유지하고,
#### 3-3. 공구 마모 시간은 172min을 넘기지 않도록 하는 것이 방안이 될 수 있겠다.

### 4. 기타 
#### 평균값 데이터 
기온은 '열 방산'이 있을 때 평균값이 더 높았다.
공정온도의 평균값은 별다른 차이를 보이지 않았다.
회전 속도의 평균값은 '열 방산', '과부하' 때에는 낮은 수치를, '동력 이상' 대에는 높은 수치를 보였다.
회전력의 평균값은 모든 고장 원인에서 높은 수치를 보였다.
공구 마모 시간의 평균값은 '과부하'가 일어날 때 높은 수치를 보였다.

#### 공구 마모 시간 분석
- 공구 마모 시간은 0에서 200 언저리까지 증가하다가 기계 고장이 일어난 후 교체되는 형태를 보인다.
- 공구 마모 고장은 공구 마모 시간 평균 216.37min에 일어났고, 총 46회이다.
- 공구 교체는 공구 마모 시간 평균 215.66min에 이뤄졌고, 총 119회 했다.
- 공구 교체 시기를 데이터에서 제외하면 공구 마모 고장 횟수가 0회로 줄어든다.

고장 원인간 변수들 상이점 및 특이 분포   
#### 기온 : 열방산이 과부하, 동력이상과 상이하게 기온 높음
#### 공정온도 : 열방산 분포는 중앙값과 3분위에 몰렸으며 과부하, 동력이상과 상이하게 공정온도가 높음  
#### 회전속도 : 동력이상이 열방산, 과부하 와 상이하게 분포 범위가 넓음  
            <동력이상> 1763(평균), 1200(min),  1312(¼), 1386 (median), 2563(¾), 2886 (max)  
             <과부하>  1350(평균), 1181(min), 1313(¼), 1360 (median),  1382(¾), 1515 (max)  
              <정상>   1540(평균), 1168(min), 1429(¼), 1507 (median), 1615(¾), 2695 (max)
          -> 회전속도는 생산과정에서 1168 rpm~ 2695 rpm까지 광범위하게 발생했으나, 
             동력이상은 정상의 평균 속도 1540 보다 평균값이  223.7 큰 1763 이며 정상 3분위수 1615보다 948 큰 바, 
             회전속도 중앙값 1386 부터 3분위 수 2563 까지 넓은 범위에서 고장이 발생함을 알수있음                
#### 회전력 : 회전속도와 마찬가지로 동력이상이 열방산, 과부하 와 상이하게 범위가 넓음  
            <동력이상> 48(평균),  3(min), 12(¼), 63(median), 68(3/4),76 (max) 
             <과부하>  58(평균), 46(min), 53(¼), 57 (median), 61(3/4), 75 (max)  
              <정상>   39(평균), 12(min), 33(¼), 39 (median), 46(3/4), 70 (max)  
           -> 하지만 회전력은 횓전속도와 달리 동력이상 1분위 값 12 부터 중앙값 63까지 아래에 넓게 분포되어 있음
#### 공구마모 시간은 과부하가 동력이상, 열방산과 상이하게 평균 207분 중앙값 207분으로 집중되어 좁게 분포됨  
            <과부하> 207 (평균), 172(min), 197(¼), 207 (median), 216 (¾), 253 (max)
             <정상>  106 (평균),   0(min),  52(¼), 107 (median), 160 (¾), 246 (max)
#             

- 노션 링크(데이터 총 정리)
https://absorbed-stream-8dd.notion.site/637486def24643d8b2bc9f491251c587

- 데이터 폴더
https://drive.google.com/drive/folders/13pYx7XX-hs5gUUGVJjnaIMbGhE_FSZ8O?usp=share_link


데이터 링크
- Machine Predictive Maintenance Classification 기계 예측 유지 보수 분류 C
https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification
- Microsoft Azure Predictive Maintenance -> 
https://www.kaggle.com/datasets/arnabbiswas1/microsoft-azure-predictive-maintenance?select=PdM_telemetry.csv
- Predictive Maintenance Dataset
https://www.kaggle.com/datasets/hiimanshuagarwal/predictive-maintenance-dataset
- Predictive Maintenance Dataset (AI4I 2020) C ->
https://www.kaggle.com/datasets/stephanmatzka/predictive-maintenance-dataset-ai4i-2020
https://www.kaggle.com/datasets/uysalserkan/fault-induction-motor-dataset 


- (데이터 분석 시 참고) 데이터 분석해놓은 블로그
https://medium.com/@Medini_2020/predictive-maintenance-using-machine-learning-3d8b62d5df8e


- 구글ppt 링크
https://docs.google.com/presentation/d/1CUEw3hKR2ayU5mRlvH3K6NZ73LfyuW8bFtEZqRobyPY/edit?usp=sharing

- 구글 PPT 발표용
https://docs.google.com/presentation/d/1yRfBv28OMeRLNcuDb8mNpxJdJiXmJu2tsrm5aVsrRVs/edit#slide=id.g1dd3d26bf8f_0_327

- 테마
https://slidesgo.com/ko/%ED%85%8C%EB%A7%88/%EA%B8%B0%EC%88%A0-%EB%89%B4%EC%8A%A4%EB%A0%88%ED%84%B0#position-1&rs=home-popular
https://www.freepik.com/free-vector/digital-grid-technology-background-vector-white-tone_16252257.htm#query=it%20tech%20background%20image%20white&position=18&from_view=search&track=ais

