# Youtube_sentiment_analysis

## 1. 프로젝트 개요

유튜브 영상을 보기전에, 그 영상의 댓글의 감성을 간단히 확인할 수 있도록 감성분석 모델링을 만드는 것이 목표

![image](https://user-images.githubusercontent.com/87663692/144718466-13c83475-b16b-4ad9-ab7f-449a8fcb88b9.png)

팀원들 대부분이 자연어 처리 분야를 처음 접해보았기에, NLP 스터디를 약 3주간 진행

그 후 유튜브 댓글 크롤링 및 스크랩핑을 진행하고, 데이터셋을 구성하여 전처리를 한 뒤, 모델링을 진행

## 2. Data

Train set: NSMC Training set 100,000개

Test set: 직접 크롤링을 이용하여 총 3505개의 유튜브 댓글 긍정 1, 부정 0으로 labeling한 data 3505개 & NSMC Test set 50,000개

## 3. 전처리

- 한글만 남기기(+특수부호 제거)

- 띄어쓰기(PyKoSpacing)

- 맞춤법검사(Py-hanspell,soynlp)

- 형태소 분석 및 품사 Tagging(Khaii 사용)

- 워드 임베딩 (Skip-gram 사용)

## 4. 모델링

BERT/Bi-LSTM+attention/GRU/CNN+GRU/CNN+LSTM/CNN/LSTM/GRU+relu 총 8개의 모델 사용

## 5. 프로젝트 결과

Accuracy를 기준으로 하였을 때, BERT의 성능이 가장 뛰어남

![image](https://user-images.githubusercontent.com/87663692/144719002-3f47daa8-0ea3-4f07-8e16-265b3a482153.png)

![image](https://user-images.githubusercontent.com/87663692/144719007-bd94a190-3515-49f1-acc0-fb2231ee3791.png)

