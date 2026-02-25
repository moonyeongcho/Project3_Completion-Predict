# 데이콘 제 2회 학습자 수료 예측 AI 경진대회

이 프로젝트는 BDAI 학회의 학회원 데이터를 기반으로 학습자의 **수료 여부(0/1)** 를 예측합니다.  
전처리 → 학습 → 평가 → 추론(제출 파일 생성)까지의 **End-to-End 파이프라인**을 제공합니다.

## 주요 특징
- **파이프라인**: 전처리 → 학습 → 평가 → 추론
- **통계 검정 기반 변수 선택**: competed=0 vs 1 그룹 비교를 통해 유의미한 변수 선별 (p-value 기반) 검증 셋에서 threshold(임계값) 튜닝 지원
- **모델 앙상블(블렌딩)**: CatBoost / XGBoost / RandomForest 확률 평균 블렌딩으로 성능 안정화
- **F1 최적화**: K-Fold 검증 결과(OOF) 기반으로 threshold(임계값) 탐색 및 최적화
- **설정 기반 제어**: `config.yaml`로 경로/파라미터/threshold를 관리

## 프로젝트 구조
- `src/`: 전처리/학습/평가/추론 코드
- `data/`: (로컬) 원본 데이터 위치
- `artifacts/`: 모델/로그/제출파일 등 산출물 
- `config.yaml`: 실행 설정
- `requirements.txt`: 패키지 목록
- `README.md`

## 실행 방법 (Quickstart)

### 1) 환경 설치
```bash
pip install -r requirements.txt
