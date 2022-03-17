## Gready search
* 문장을 생성하는 도중에 문장을 잘못 생성했다는 것을 알았다.
* 근데 되돌아 가기 어려움
* 총 V^t만큼 탐색 필요 (V : 단어의 수, t : step 수)

![image](https://user-images.githubusercontent.com/63588046/158717874-c2424918-807c-458f-bf93-6f6c7cc7e21c.png)


## Beam search
* 모든 경우를 다 따지지는 X
* 가능한 최적의 경우를 다 따짐

![image](https://user-images.githubusercontent.com/63588046/158718564-1bf19431-803b-441f-8fcb-4330a0c16cef.png)

* k 개를 선택함. 그 다음 예측 경우의 수는 k^2임
* k^2 경우의 수 중 가장 확률이 높은 k개 선택
* 위 과정 반복

* 총 단어 개수만큼 score에서 나눔
* 단어 수가 길어질수록 score 점수 낮아야함
* 너무 score가 커지는 거를 방지하기

![image](https://user-images.githubusercontent.com/63588046/158719444-e407b794-5bc7-4a95-92e7-12476b8d8d85.png)


## BLEU score

#### 이전 방식
* 고정된 위치에서 score 점수 계산하면 안된다. (ground truth : I love you, pred : oh i love you는 둘다 좋은데 고정된 위치로 따지면 score이 0이 됨)

* precision, recall -> F-score 사용


![image](https://user-images.githubusercontent.com/63588046/158719970-e0295861-045d-48e4-806f-0c67176dd2d7.png)

#### 문제점
* 문장 순서가 막 섞여 있어도 100% 정확도가 발생한다.

#### BLEU score
* N-gram : 





