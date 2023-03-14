# NLI_sentence_classification
[RoBERTa/KoELECTRA] 한국어 문장 분류 경진 대회 5위

## 자연어 처리 프로젝트
#### 한국어 문장 관계 분류 경진대회(DACON)
- 전제(premise)와 가설(hypothesis)의 관계를 예측하는 task

#### 주요 과정
1. 전처리  
  - 정규표현식을 통한 특수문자 전처리  
  - **Papago의 번역을 이용해 한국어 > 영어 > 한국어로 변환하여 augmentation**
2. 모델링
  - **KLUE-roberta, Koelectra**의 사전학습 모델 사용
  - Automodel을 이용해 모델 생성 > 사전학습 적용
3. 앙상블
  - 5-fold로 나누어 다양한 방법으로 앙상블 적용
  - 데이터 augmentation 여부로 나누어 5-fold 학습 각각 진행
  - 최종적으로 8개 모델 앙상블

#### 최종 결과
20
Public score 기준 최종 5위 기록
