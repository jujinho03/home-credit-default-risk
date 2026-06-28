# 원본 데이터 준비

원본 CSV는 용량과 배포 조건을 고려해 GitHub 저장소에 포함하지 않습니다.

1. [Kaggle Home Credit Default Risk 데이터 페이지](https://www.kaggle.com/competitions/home-credit-default-risk/data)에서 파일을 내려받습니다. Kaggle 로그인이 필요할 수 있습니다.
2. 압축을 해제합니다.
3. `application_train.csv`와 `application_test.csv`를 아래 폴더에 배치합니다.

```text
data/raw/home-credit-default-risk/
```

현재 모델링은 `application_train.csv`를 사용합니다. 다른 보조 테이블은 원본 데이터에는 존재하지만 현재 모델에는 결합하지 않습니다.

PowerShell에서 다음 명령을 실행하면 두 파일이 올바른 위치에 있는지 확인할 수 있습니다.

```powershell
Test-Path .\data\raw\home-credit-default-risk\application_train.csv
Test-Path .\data\raw\home-credit-default-risk\application_test.csv
```

두 줄이 모두 `True`이면 데이터 준비가 완료된 것입니다.
