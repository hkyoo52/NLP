## NLP 종류

* Low-level parsing
  * tokenization : 단어를 token이라고 여기고 token단위로 나누는 과정
  * stemming : 어미를 없애고 의미 유지

* Word and phrase level
  * NER : 문장의 품사 파악

* Sentence level
  * Sentiment analysis : 문장의 감정 파악

* Multi-sentence and paragraph level
  * 문장들이 양립할 수 있는 건지 파악
  * 질문의 정답이 무엇인지 파악

#### Text mining
* 데이터에서 정보 추출
* 문서들을 grouping 함
* 데이터 분석해서 사회과학에 사용


## NLP 역사
* RNN family(RNN, LSTM, GRU): 단어가 순차적으로 되어있음 -> 순서대로 넣고 output 구함
* transformer : self-attention으로 순서를 대체시킴
  * 자가지도학습 : 입력중 일부 문장을 가렸을 때 앞 뒤 문맥을 보고 그 단어를 맞추는 것

## Bag of Words
* 각 단어를 one-hot vector로 표현
* Bag of Words : 각 단어들의 one-hot vector를 모두 더한 값


## NaiveBayes 분류
* 서류의 내용을 분류할때 c=class, d=서류

![image](https://user-images.githubusercontent.com/63588046/157574000-78e78329-efb3-400b-b8a0-a668db8337ac.png)

![image](https://user-images.githubusercontent.com/63588046/157574105-eda1edce-3ecc-4c0a-93c5-8ed1e3aa7273.png)










