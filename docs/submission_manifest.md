# 제출 파일 목록

## 저장소에 포함하는 파일

| 구분 | 포함 내용 |
|---|---|
| 실행 설정 | `config.yaml`, `requirements.txt` |
| 데이터 안내 | `data/README.md`, `data/raw/README.md`, `data/processed/README.md` |
| 분석 코드 | `notebooks/`의 노트북 3개 |
| 결과 그래프 | `outputs/figures/` |
| 결과표 | `outputs/metrics/` |
| 요약 보고서 | `outputs/reports/`, `docs/` |
| 프로젝트 설명 | `README.md` |

## 저장소에서 제외하는 파일

| 제외 항목 | 이유 |
|---|---|
| Kaggle 원본 CSV | 대용량 및 배포 조건 |
| 모델 `.pkl` 파일 | 대용량이며 노트북으로 재생성 가능 |
| `.venv/` | 개인 PC의 가상환경 |
| `private/` | 지원 회사와 면접 준비용 개인 메모 |

## 제출 전 확인

1. README의 내부 링크와 이미지가 열리는지 확인합니다.
2. 노트북 3개에 실행 오류가 없는지 확인합니다.
3. 원본 CSV, 모델 파일, 개인 메모가 Git 대상에 포함되지 않았는지 확인합니다.
4. 결과표의 핵심 수치가 README와 일치하는지 확인합니다.
5. 저장소 공개 후 다른 환경에서 설치·실행 안내를 따라갈 수 있는지 확인합니다.
