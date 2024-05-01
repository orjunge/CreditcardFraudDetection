# CreditcardFraudDetection
신용카드 이상 거래 탐지를 위해 모델링을 진행했고, Recall 점수를 기준으로 최종 모델은 RandomForest로 선정했습니다.  
Recall을 우선적인 지표로 선정한 이유는 이상 거래를 얼마나 잘 이상 거래로 분류할 수 있는지를 나타내는 지표이기 때문입니다.  
이는 실무에서 고비용위험부담을 줄여줄 수 있는 척도라고 생각하여 첫 째로는 Recall, 그 다음은 F1-Score를 기준으로 선정했습니다.

### 프로젝트 기간
- 2024.03.22 ~ 2024.04.28

## 파일 설명
- 0_EDA.ipynb : 데이터탐색을 하며 전처리할 방향을 정했던 파일입니다.
- 1_Model-RandomForest.ipynb : Recall 점수를 기준으로 F1-score, Accuracy, Precision을 고루 평가하여 최종 선정된 모델 입니다.
- 2_Model-LGBM.ipynb : LGBM 모델링에서 유의한 파라미터를 발표에서 공유했기에 코드를 올렸습니다.

# Motivation
신용카드 이상 거래 데이터는 1. 신속한 이상(사기) 거래 탐지 2. 이상 거래의 후속 거래 탐지 및 분석을 위해 필요합니다.  
이상 거래가 발생할 경우, 카드사는 고객과 신뢰를 쌓을 수 있기 때문에 고객에게 적절한 조치를 취하고, 후속 거래를 추적하여 재발 방지를 위해 힘써야 합니다.  
때문에 이번 프로젝트에서는 이상 거래를 얼마나 잘 이상 거래로 탐지할 수 있을지 (2번)에 주목하였고, 이상 거래를 이상 거래로 잘 예측한 Recall과 F1-Score을 올리는 것을 목표로 모델링을 진행했습니다.

# 과정 및 결론
머신러닝의 RandomForest, LGBM, XGBoost와 딥러닝의 AutoEncoder, AutoEncoder로 차원 축소 후 RandomForest로 모델링을 시도했으며, GridSearchCV 및 임계값 조정 등의 과정을 거쳐 최종적으로 0.7에서 0.97까지 Recall 점수가 확인된 RandomForest모델로 선정했습니다.

