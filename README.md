# Asteroid Machine Learning Project

## 기계학습 프로젝트 소행성 데이터

1. pha(잠재적 위험이 있는 소행성) Y/N 이진분류
2. orbit class(궤도 등급) 다중 클래스 분류
3. Diameter 회귀


- 데이터 출처 : https://ssd.jpl.nasa.gov/sbdb_query.cgi#x
- 21개의 특성만 가져와서 사용했다.
- 'name', 'neo', 'pha', 'H', 'diameter', 'albedo', 'rot_per', 'spec_B','e', 'a', 'q', 'i', 'om', 'w', 'ma', 'ad', 'n', 'tp', 'per', 'moid', 'class'


## 결과

### 1. PHA Classification
| 앙상블 모델(RandomForest, XGBoost)가 가장 좋은 성능을 보여줌.

| 앙상블, 서포트 벡터, 다층 퍼셉트론, 로지스틱 비교

| StandardScaler로 스케일링 함.(앙상블 제외)


### 2. Orbit Class Classification
| 서포트 벡터, 다층 퍼셉트론, 로지스틱은 SMOTE로 오버샘플링 한 결과가 더 좋음

| 앙상블은 오버샘플링 하지 않고도 다중 클래스를 잘 분류했음

| StandardScaler 사용

### 3. Diameter Regression
| 소행성의 직경을 구함

| 앙상블, 서포트벡터, 다층 퍼셉트론, 릿지, keras 딥러닝 비교

| 랜덤 포레스트, MLP, keras 모델의 MSE가 가장 낮게 나왔는데 KFold 검증을 통해서 이상치의 영향을 찾았음


