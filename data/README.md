# 데이터 안내

## 1. 데이터 출처

- Kaggle 대회: [Home Credit Default Risk](https://www.kaggle.com/competitions/home-credit-default-risk/data)
- 이 프로젝트에서 사용하는 파일: `application_train.csv`, `application_test.csv`

원본 CSV는 용량과 배포 조건 때문에 GitHub 저장소에 포함하지 않습니다.

## 2. 원본 데이터 배치

Kaggle에서 데이터를 내려받아 압축을 해제한 뒤 다음 위치에 두 파일을 배치합니다.

```text
data/raw/home-credit-default-risk/
├─ application_train.csv
└─ application_test.csv
```

PowerShell에서 아래 명령의 결과가 모두 `True`이면 준비가 완료된 것입니다.

```powershell
Test-Path .\data\raw\home-credit-default-risk\application_train.csv
Test-Path .\data\raw\home-credit-default-risk\application_test.csv
```

현재 모델링에는 `application_train.csv`를 사용합니다. 보조 테이블은 신청 시점 이전 정보인지 충분히 확인하지 못해 이번 분석에 결합하지 않았습니다.

## 3. 폴더 구성

- `raw/`: Git에서 제외한 Kaggle 원본 데이터
- `processed/`: 재생성 가능한 중간 데이터 안내

세부 원본 데이터 준비 방법은 [`raw/README.md`](raw/README.md), 처리 데이터 기준은 [`processed/README.md`](processed/README.md)를 확인합니다.
