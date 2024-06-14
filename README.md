# Prompirit's Final Pipeline Code

## 실행 방법
**Pipeline_DEMO.ipynb : 최종 데모 코드**
- "example_data.csv" 파일 속 프롬프트가 Prompirit의 pipeline을 거쳐 엔지니어링되는 과정

- 데모코드 안 "0ver2_SOTA_ED_model_comp_0.8973.pt"는 아래 링크로 다운받을 수 있음.

    [Text Emotion Recognition Model](https://drive.google.com/file/d/1VElYIHTkmBXML0YasoBnzPx0I6mKLpS0/view?usp=drive_link) : pretrained model 다운받기
- RAG 데이터베이스 연결을 위한 "styleDB" 폴더는 "styleDB.zip" 을 압축해제 하여 사용

## Pipeline

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
      
<img width="1731" alt="KakaoTalk_20240614_231354646" src="https://github.com/AnT-Prompirit/prompirit_final_code/assets/77625287/ee585012-6cad-41c6-8f69-73b236dbe5fd">

이후 진행된 Evaluation 과정을 통해 위와 같은 Prompirit의 파이프라인을 통해 생성된 이미지는 감정 표현력, 맥락 일치도, 시각적 만족도 측면에서 기존의 다른 프롬프트 엔지니어링 방식으로 생성된 이미지에 비해 가장 선호되는 것으로 나타났다. 
