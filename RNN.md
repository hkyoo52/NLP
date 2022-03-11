## RNN
* h : hidden-state vector
* x : input vector 
* f : RNN function (파라미터 W 내적하는 식)
* y : output vector

![image](https://user-images.githubusercontent.com/63588046/157790564-67e3011e-1825-4882-892e-d9e8148e33c8.png)

#### Ex
![image](https://user-images.githubusercontent.com/63588046/157791105-01e6a001-7963-4927-9a47-8155b493f217.png)

#### Charactoer-level Language Model
![image](https://user-images.githubusercontent.com/63588046/157793913-cd275104-4d1f-4c41-8034-1e7190c01207.png)


#### Backpropagation through time (BPTT) 
![image](https://user-images.githubusercontent.com/63588046/157806040-2b8a3ef8-f733-44e2-8f76-f733c72d6d60.png)

* 모든 길이를 다 학습하면 너무 많은 메모리와 시간 걸림
* trunk : 학습할 데이터 양


#### 단점
* 길이가 길어지면 gradient vanishing/exploding


#### Long Short Term Memory (LSTM)


![image](https://user-images.githubusercontent.com/63588046/157810098-d9ee0594-3cc6-4df5-b08a-e48be84ba3cd.png)







