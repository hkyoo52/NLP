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










