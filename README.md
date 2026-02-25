# 학습자 수료 예측 (Learner Completion Prediction)

이 프로젝트는 BDAI 학회원 데이터를 기반으로 학습자의 **수료 여부(0/1)** 를 예측합니다.  
전처리 → 학습 → 평가 → 추론(제출 파일 생성)까지의 **End-to-End 파이프라인**을 제공합니다.

## 주요 특징
- **End-to-End 파이프라인**: 전처리 → 학습 → 평가 → 추론(제출 파일 생성)
- **F1 최적화**: 검증 셋에서 threshold(임계값) 튜닝 지원
- **모델 확장 용이**: (기본) CatBoost / (옵션) LightGBM 구조로 확장 가능
- **설정 기반 제어**: `config.yaml` 하나로 경로/파라미터/threshold 관리

## 프로젝트 구조
src/                 # 전처리/학습/평가/추론 코드
data/                # (로컬) 원본 데이터 위치
artifacts/           # 모델/로그/제출파일 등 산출물
config.yaml          # 실행 설정
requirements.txt     # 패키지 목록
README.md
