# Store Sales-Time Series Forecasting

### [Linear Regression with Time Series]

[https://www.kaggle.com/code/zeynepperr/exercise-linear-regression-with-time-series](https://www.kaggle.com/code/zeynepperr/exercise-linear-regression-with-time-series)

### Data

### **train.csv**

- id
- date
- store_nbr identifies the store at which the products are sold.
- family identifies the type of product sold.
    - Beauty / Books / Bread&Bakery / Dairy etc.
- sales gives the total sales for a product family at a particular store at a given date.
- onpromotion gives the total number of items in a product family that were being promoted at a store at a given date.

### test.csv

- id
- date
- store_nbr
- family
- onpromotion

### **sample_submission.csv**

- id
- sales

### Code Review

1. 환경 설정 및 데이터 로드
- Library: pandas, matplotlib, seaborn, sklearn etc.
1. 시계열 데이터 시각화
- 전반적인 데이터 흐름 파악하기 위해 시각화
- 데이터에 일정한 상승/하강 추세 있는지, 혹은 특정 주기마다 반복되는 패턴 있는지를 시각적으로 확인
1. 시간 관련 feature 생성
- 선형 회귀는 기본적으로 시간을 변수로 인식하지 못하기 때문에 모델이 학습할 수 있는 특성 만들어야 함
- Step 특성: 데이터에 순서를 나타내는 변수를 만들어 시간에 따른 선형적인 변화 학습
- Lag 특성: 이전 시점의 값을 현재 시점의 예측을 위한 변수로 사용하여 자기상관성 반영
1. 추세 모델링
- 생성한 시간 관련 특성 사용하여 LinearRegression 모델 학습
- 이 단계에서 데이터의 전반적인 방향성 파악 집중
1. 예측 및 결과 시각화
- 모델 사용하여 미래 시점에 대한 예측값 계산
- 실제 데이터와 모델이 예측한 추세선 함께 그려 모델이 데이터 흐름 얼마나 잘 포착했는지 평가
1. 모델 평가
- MAE
- RMSE

### 차별점 및 배울점

- 시계열의 인덱스를 그대로 쓰는 것이 아니라 모델이 이해할 수 있는 Time-step 변수로 치환
    - 정수형 시퀀스로 변환하여 모델이 “시간이 흐름에 따라 값이 증가/감소한다”는 추세 학습 가능
- Lag features를 통한 자기 상관성 활용
    - 어제의 값이 오늘의 값에 영향을 미친다는 가정을 코드로 구현
- Trend & Noise 분리 이해
    - 딥러닝 모델 쓰기 전, 경향성을 선형 모델로 먼저 잡아내는 baseline 모델 구축 중요
- 시계열 데이터에서 plot을 통해 추세선을 겹쳐 그리는 방식은 모델의 성능을 직관적으로 설득
