# pstage_02_tabular_classification
- 기간 : 2021.04.12~2021.04.23
- 대회 내용 : 2년간의 구매 내역으로 마지막 월에 300을 초과하여 구매할 유저를 예측(AUC : 0.8599 최종 20등) 
- 수행 요약 : EDA, 12월에 근접한 구매내역이 있는 우량 유저들을 target으로 핵심 피처 생성, pytorch, matplotlib, seaborn, mlflow이용

### notebook환경으로 진행
- Boosting_Model : use LGBM, XGBoost, CatBoost for train, inference
- EDAnEnsemble : data EDA, feature making,Ensemble
- tabnet : use tabular NN model(tabnet) for train, inference                                                         
### Important Technic
- Stratified KFold
- label threshold control (payment predict for )
- hard voting 
- delete outlier (based on LGBM Feature Importance method)  
### Important Feature
- user's last order time
![fi](https://user-images.githubusercontent.com/52443401/126287361-7b134160-7516-453e-9ebc-b783ab9ab905.png)

### Ensemble figure
![image](https://user-images.githubusercontent.com/52443401/122660653-f4bd4180-d1bd-11eb-90dc-a059609af60a.png)

모델간의 label 분포 개수의 차이가 클 때 앙상블의 재료로 사용했습니다.
