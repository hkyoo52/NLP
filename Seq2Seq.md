## Sequence to Sequence
* Encoder로 문장을 이해하고 Decoder에서 문장 생성
* SoS : Decoder 처음에 들어가는 토큰
* EoS : Decoder 마지막에 나오는 output

![image](https://user-images.githubusercontent.com/63588046/157810887-d9fdbf0a-4c3b-4891-9d52-2ee24069c793.png)


#### Attention
* 이전 방식은 예전에 학습한거 잘 기억 못함
* vector 1개만 의존하는 것이 아니라 문장 내에 모든 vector 사용
* 각 단어가 encoder에 들어가서 각각의 벡터 생성
* decoder에서 나오는 가중치 값을 각 벡터에 내적해서 각각의 score 생성
* attention score를 가지고 나온 값과 decoder output을 concat해서 최종 결과 단어 생성
* decoder에서 각각 time-step 결과로 전달
* decoder에서 각 단어당 가중치를 얼마나 줄건지 출력
* Teacher forcing :decoder에는 항상 ground truth를 제공한다. (예측값을 넣지 않는다)
* 그러나... teacher forcing을 사용하면 일반화 X
* 그래서 처음에는 teacher forcing을 사용하다가 나중에는 예측값을 decoder에 넣는다.



#### Encoder에서 나온 값과 decoder에서 나온 가중치로 유사도 구하는 방식

* 내적
* general 내적

![image](https://user-images.githubusercontent.com/63588046/157834225-7d7dd687-00da-4abb-a706-41ea82e2547b.png)

#### 행렬 기본 의미
![image](https://user-images.githubusercontent.com/63588046/157835676-eadf708e-768a-4514-9f29-1c0bd1988129.png)



