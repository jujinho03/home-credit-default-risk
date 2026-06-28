# 분석 산출물 안내

노트북 실행 결과는 역할에 따라 네 폴더에 저장합니다.

## figures

README와 분석 보고서에서 사용하는 그래프입니다.

- `model_roc_curves.png`: 모델별 ROC 곡선
- `model_precision_recall_curves.png`: 모델별 Precision-Recall 곡선
- `cross_validation_roc_auc.png`: 교차검증 ROC-AUC 비교
- `logistic_standardized_effects.png`: 로지스틱 표준화 효과 크기
- `logistic_permutation_importance.png`: 검증 데이터 순열 중요도
- `logistic_threshold_metrics.png`: 임계값별 Recall·Precision·F1
- `risk_decile_default_rate.png`: 위험 10분위별 실제 부도율

그 밖의 파일은 데이터 품질과 탐색적 분석 결과를 보여줍니다.

## metrics

검수 결과와 모델 평가값을 CSV로 저장합니다.

- `data_quality_checks.csv`: 중복, 결측, 무한값 점검
- `model_holdout_performance.csv`: 모델별 검증 성능과 학습시간
- `cross_validation_summary.csv`: 5겹 교차검증 요약
- `threshold_scenarios.csv`: 세 가지 임계값 시나리오
- `risk_decile_summary.csv`: 위험구간별 부도율과 Lift

## models

실행 중 생성되는 전처리기와 모델 파일이 저장됩니다. `.pkl` 파일은 크기가 크고 노트북으로 다시 만들 수 있으므로 Git에서 제외합니다.

## reports

각 분석 단계에서 자동 생성한 간단한 Markdown 요약입니다. 전체 해석은 [`../docs/findings.md`](../docs/findings.md)를 기준으로 봅니다.
