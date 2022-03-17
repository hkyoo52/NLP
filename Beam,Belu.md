## Gready search
* 문장을 생성하는 도중에 문장을 잘못 생성했다는 것을 알았다.
* 근데 되돌아 가기 어려움
* 총 V^t만큼 탐색 필요 (V : 단어의 수, t : step 수)

![image](https://user-images.githubusercontent.com/63588046/158728143-52b59418-4dbe-4be7-bbbd-7fadd70b22af.png)


## Beam search
* 모든 경우를 다 따지지는 X
* 가능한 최적의 경우를 다 따짐

![image](https://user-images.githubusercontent.com/63588046/158718564-1bf19431-803b-441f-8fcb-4330a0c16cef.png)

* k 개를 선택함. 그 다음 예측 경우의 수는 k^2임
* k^2 경우의 수 중 가장 확률이 높은 k개 선택
* 위 과정 반복

* 총 단어 개수만큼 score에서 나눔
* 예측된 단어의 길이가 짧은 것 방지

![image](https://user-images.githubusercontent.com/63588046/158719444-e407b794-5bc7-4a95-92e7-12476b8d8d85.png)


## BLEU score

#### 이전 방식
* 고정된 위치에서 score 점수 계산하면 안된다. (ground truth : I love you, pred : oh i love you는 둘다 좋은데 고정된 위치로 따지면 score이 0이 됨)

* precision, recall -> F-score 사용


![image](https://user-images.githubusercontent.com/63588046/158719970-e0295861-045d-48e4-806f-0c67176dd2d7.png)

#### 문제점
* 문장 순서가 막 섞여 있어도 100% 정확도가 발생한다.

#### BLEU score
* N-gram : N개의 단어를 하나의 토큰으로 봄    Ex. 4
* 아래 식은 N=4로 두었을때 계산하는 식

![image](https://user-images.githubusercontent.com/63588046/158722291-4e8dc305-7c12-44d1-a2cf-95deac19d9ec.png)

![image](https://user-images.githubusercontent.com/63588046/158728181-e842923a-b9f4-4531-8356-799edf62d996.png)





