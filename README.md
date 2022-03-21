# blocking-hate-speech
욕설 뿐만 아니라 상대를 비난하는 코멘트를 감지하고 방지하는 모델 개발.  



## 📌 Dataset
- 데이터 출처 : [Korean HateSpeech Dataset](https://github.com/kocohub/korean-hate-speech)
- 데이터 : 연예 뉴스 댓글과 비방(Hate/Offensive) 여부  



## 📌 프로젝트 목적 

<p align="center"><img src="https://user-images.githubusercontent.com/30399933/155271578-f0b2bd43-885c-4449-9fab-6d2a4f17b2e6.png"></p>
<p align="center"><출처: 2018년 사이버폭력 실태조사 (방통위, 한국정보화진흥원></p>

- 사이버 명예훼손 및 모욕 사건의 수는 증가 하고 있지만 법적 처벌을 받을 확률은 적어지고 있습니다.
- 악성 댓글로 인한 피해 사례가 끊이질 않고 있습니다. 네이버 연예 뉴스 댓글 기능은 폐지 되었지만, 개인 SNS로 몰려가 댓글 테러를 하는 사이버 폭력이 만연합니다.
- 지정된 욕설을 감지하여 악플이라고 판단하는 현 시스템 만으로는 부족합니다. 
- 자연어 처리 기술을 이용하여 욕설이 포함되어 있지 않아도, 문맥상 비방/비난 어조의 댓글을 감지하고 방지하는 시스템이 필요합니다.  
  
  
  
  
## 📌 Pre-trained Model
- BERT multilingual base model
- kykim/bert-kor-base

  

## 📌 모델 학습 결과
  
||Accuracy|Val_accuracy|F1_Score|
|:---:|:---:|:---:|:---:|
|bert-base-multilingual-cased|0.952|0.711|0.750|
|kykim/bert-kor-base|0.984|0.804|0.839|
  
kykim/bert-kor-base을 파인 튜닝한 모델의 성능 조금 더 높은 것을 확인하였다. kykim/bert-kor-base의 성능을 자세히 보면 다음과 같다.
  
<p align="center"><img width="670" src="https://user-images.githubusercontent.com/30399933/155516720-e47353a6-95b2-4f42-936d-8df67bcb4f7d.png"></p>


- 라벨 1은 비방/비난 댓글, 라벨 0은 비방 아닌 댓글 의미입니다.
<p align="center"><img width="670" src="https://user-images.githubusercontent.com/30399933/155525918-017a8c0b-57e5-4a18-8fb4-66fa1be8b254.png"></p>

- 웹에서 구현하기
![web_example](https://user-images.githubusercontent.com/30399933/155274390-73a42204-7dac-4adf-880d-efd76fbe0a10.gif)

