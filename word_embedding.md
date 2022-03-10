## Word Embedding
* 단어를 벡터로 표현
* 비슷한 의미를 가진 단어가 유사한 곳에 위치하게 만듬 (cat하고 kitty는 가까운 거리) (긍정적인 의미는 가까운 위치)

#### Word2Vec
* 한 문장에 단어 주변에 있는 단어들은 유사하다고 여김
* cat이라는 단어의 벡터는 총 문장에서 cat이라는 단어가 들어간 문장의 모든 단어의 수를 세서 가장 많이 위차한 곳 주변에 cat의 vector를 위치시킴


* I study math -> (I, study), (study, I), (study, math), (math, study)

![image](https://user-images.githubusercontent.com/63588046/157636881-2ebfe235-e9ae-4c07-a21e-9c05efd44567.png)


