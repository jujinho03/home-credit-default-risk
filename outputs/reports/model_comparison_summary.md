# Five-Model Holdout Summary

- 검증 데이터: 61,503건
- 최고 ROC-AUC: Logistic Regression, 0.7504
- PR-AUC 기준선: 0.0807
- 클래스 불균형 대응: balanced class weight 또는 동일 사전확률

RBF SVM은 계산 제약으로 층화 5만 건에서 학습했으므로 전체 학습 데이터를 사용한 네 모델과 직접 동등 비교하지 않습니다.
클래스 가중치를 사용한 확률 출력은 절대 부도확률보다 상대적 위험 점수로 해석합니다.
