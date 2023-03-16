# NLI_sentence_classification
🏆[RoBERTa/KoELECTRA] 한국어 문장 분류 경진 대회 

🏆 5위 입상 (Public Score 기준)

<br>

## 💻프로젝트 소개
1. 전제(premise)와 가설(hypothesis)의 관계를 예측하는 task
2. 한국어 문장 관계를 파악할 수 있는 알고리즘 작성
-> premise 문장을 참고해 hypothesis 문장이 참인지(Entailment), 거짓인지(Contradiction), 혹은 참/거짓 여부를 알 수 없는 문장인지(Neutral)를 판별 

- **작업기간** : 2022.01.28 ~ 2022.02.28 
- **투입인원** : 5명
- **스킬 및 사용툴** `python` 

<br>

## 📑분석 내용

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

