## RNN 문제점
* RNN은 과거에 있는 정보는 hidden state를 통해서 전달
* 문장의 길이가 길어질수록 이전 정보는 점점 gradient vanishing/exploding 발생

![image](https://user-images.githubusercontent.com/63588046/158730088-509e748b-069f-4500-9a6f-fbb810616d9f.png)


## transformer
* queries : 내가 분석하고 싶은 벡터 
* keys : queries와 내적 할 벡터
* values : 가중치 적용

* key와 value 벡터들은 서로 개수가 같아야함

![image](https://user-images.githubusercontent.com/63588046/158737207-dc24c495-1c4b-431f-8f45-d3d85de6b431.png)

![image](https://user-images.githubusercontent.com/63588046/158747549-f62bafd6-a2ed-4772-99fa-5aa12492599d.png)

concat -> linear



* transformer는 한번에 계산
* RNN은 h_n을 계산 하려면 h_1, h_2,,,, 다 계산해야함


![image](https://user-images.githubusercontent.com/63588046/158749809-385943fd-33e3-443f-abac-967af4d3152f.png)


## ADD & Norm
* residual block 사용해서 ADD & Norm layer에서 2개 그대로 더함 (dimention 유지)
* Norm같은 경우 batchnorm해서 평균 0, 분산 1로 만들어줌

![image](https://user-images.githubusercontent.com/63588046/158780233-5a303cdf-82a2-45ba-982c-387913c18630.png)

#### layer Normalization
* Batch Norm한 결과를 linear 식에 넣음

![image](https://user-images.githubusercontent.com/63588046/158782256-fb18c5da-ad93-4765-a2a9-2c11d9243935.png)



## Positioning encoding
* 그냥 attention을 하면 "I go home"과 "home go I"는 동일한 결과가 나옴
* 위치에 따라 명확히 비교 가능하는 값을 더함


## decoder
* 문장이 나와야 하는 단어 이전에 정답 레이블을 넣어서 동일하게 score를 만든다.(masked 적용)
* encoder에서 나온 값이 key, value로 들어감
* score 값으로 나온 것을 value로 사용
* 나온 벡터는 이전에 있는 단어와 encoder의 결과 2개를 모두 사용

#### mask
* 이후에 있는 단어는 -무한으로 만듬

