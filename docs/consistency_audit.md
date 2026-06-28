# 핵심 수치 일관성 검증

README, 분석 보고서와 `outputs/metrics/*.csv`의 핵심 수치를 교차 확인했습니다. 표본 수는 정수, 비율은 소수점 둘째 자리, 모델 지표는 소수점 넷째 자리로 반올림해 문서에 표시합니다.

## 불일치 및 확인 목록

| 파일 | 기존값 | 수정값 | 근거 |
|---|---|---|---|
| `README.md` §2 | 입력 변수 121개 | 원본 전체 122개 → ID·TARGET 제외 120개 → 파생 13개 추가 후 133개 → 원-핫 후 263차원 | 원본 CSV 헤더, `feature_engineering_catalog.csv`, `preprocessing_summary.csv` |
| `docs/findings.md` §3 | 파생변수 13개만 기재 | 120개 → 133개 → 263차원 단계 추가 | `feature_engineering_catalog.csv`, `preprocessing_summary.csv` |
| `docs/findings.md` §4 | PR-AUC 미기재 | 5개 모델 PR-AUC 추가 | `model_holdout_performance.csv` |
| `README.md` §8·`docs/findings.md` §4 | ROC-AUC 0.7504·0.7504·0.7502·0.7495·0.7315 | 변경 없음: 일치 확인 | `model_holdout_performance.csv` |
| `README.md` §8·`docs/findings.md` §4 | PR-AUC 0.2325·0.2324·0.2338·0.2327·0.2067 | README 유지, findings에 동일 값 추가 | `model_holdout_performance.csv` |
| `README.md`·`docs/findings.md` | 상위 10% Lift 3.28배 | 변경 없음: 3.280593을 3.28배로 표시 | `risk_decile_summary.csv`의 10분위 행 |
| `README.md`·`docs/findings.md` | 학습 246,008건 / 검증 61,503건 | 변경 없음: 일치 확인 | `train_validation_split_summary.csv` |
| `README.md`·`docs/findings.md` | 전체·학습·검증 부도율 8.07% | 변경 없음: 8.073%를 8.07%로 표시 | `train_validation_split_summary.csv` |

## 수정 완료 보고

- 모호했던 121개 입력 변수 표현을 네 단계의 변수 차원으로 분리했습니다.
- findings 모델 비교표에 CSV와 동일한 PR-AUC를 추가했습니다.
- Lift는 현재 산출값 3.280593을 기준으로 전 문서에서 3.28배로 통일했습니다.
- 모델 성능, 학습·검증 표본 수와 부도율은 불일치가 없음을 확인했습니다.

변경한 수치는 `model_holdout_performance.csv`, `risk_decile_summary.csv`, `train_validation_split_summary.csv`, `feature_engineering_catalog.csv`, `preprocessing_summary.csv`를 근거로 통일했습니다.
