## Data Set

감정 레이블: anger, disgust, fear, sadness, contentment, excitement, awe, amusement

- Empathetic Dialogues와 GoEmotions 데이터셋의 감정 레이블을 재분류
  - SenticNet의 지식 그래프, BERT, spaCy, Word2vec의 벡터 임베딩 유사도를 이용해 재분류 진행
  - GoEmotions 데이터셋의 경우 EDA를 위해 사용됨
  - 부정감정 4개와 긍정감정 4개, 총 8가지 감정 레이블로 분류된 utterance가 담긴 데이터 셋
- 각 감정 당 125개 데이터 랜덤 선택 → 총 1,000개의 utterance 데이터


## Evaluation

### Performance Evaluation
![그림4](https://github.com/AnT-Prompirit/prompirit_final_code/assets/77625287/809bb7da-4512-4443-b9f3-7cddd8bf0cc8)
<img width="476" alt="image" src="https://github.com/AnT-Prompirit/prompirit_final_code/assets/77625287/f92d76bf-072e-4f65-bbac-e55a57813d68">


- Data Analysis와 동일한 평가지표를 이용해 분석함

  → Prompirit이 가장 우수한 이미지-감정 일치도 및 정규화 점수를 보임
  
### User Evaluation
![그림5](https://github.com/AnT-Prompirit/prompirit_final_code/assets/77625287/b8c7403e-2d57-4971-9c1a-cbbc6e23c333)
<img width="442" alt="image" src="https://github.com/AnT-Prompirit/prompirit_final_code/assets/77625287/5c10f66a-fcd5-433b-aa93-772fb24accaf">

- 생성된 이미지의 주관적 평가를 위한 온라인 설문조사 실시 (참여자: 총 100명)
- Task: 서로 다른 3가지 프롬프트 엔지니어링 방식을 통해 생성된 4개 이미지를 포함하고 있는 이미지 세트 제공
    - 각 이미지에 대한 IEA, ITA, Aesthetic Score 평가
    - 총 8개 세트에 대한 평가 진행 (각 감정 레이블 당 한 세트)

#### → Prompirit이 입력 텍스트의 문맥을 정확히 반영하면서도 이미지 결과물의 감정 표현력과 심미성을 향상했음을 증명함
