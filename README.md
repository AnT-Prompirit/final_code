# Prompirit final code

[Text Emotion Recognition Model](https://drive.google.com/file/d/1VElYIHTkmBXML0YasoBnzPx0I6mKLpS0/view?usp=drive_link)

![pipeline](https://github.com/AnT-Prompirit/prompirit_final_code/assets/77625287/5b7cc62c-4bdd-4417-b473-af2d2c175a63)

#### (A) Preprocess

1. Recognize Text Emotion
    - 입력된 텍스트에서 사용자의 감정을 인식한다.

2. Remove Stopwords & Append one Key-phrase
    - 자유로운 형식의 텍스트를 프롬프트에 적합한 형태로 편집한 뒤 핵심 어구를 반복해 의미 손실을 막는다.

#### (B) Main Process

3. Prepend Emotion Label & Append 3 Synonyms
    - Text Emotion Recognition 모델로 인식한 감정 레이블을 강조한다.
    - 이를 위해 고안한 여러 방법 중 감정 레이블을 prepend하고, 감정 레이블의 동의어 중 중요도가 높은 3개를 append하여 강조하는 방식을 채택한다.

4. Append Style Modifiers
    - 추출한 감정과 관련된 스타일 키워드를 자동으로 추가한다.
