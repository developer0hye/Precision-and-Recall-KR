# Precision-and-Recall

본 게시글은 인식, 분류, 검출, 검색 등의 작업 성능 평가시 사용되는 척도인 **Precision(정밀도)** 과 **Recall(재현율)** 에 대한 이해를 돕고자 작성되었습니다.

우선 **Precision** 과 **Recall** 을 설명하기에 앞서 우리가 해결해야할 문제를 정의하고 문제를 해결하기 위한 방법에 대한 성능 평가 척도로 **Precision** 과 **Recall** 을 사용함을 가정하겠습니다.

## 문제: 틀린 그림 찾기

우리가 해결해야할 문제를 **틀린 그림 찾기** 라고 정의하도록 하겠습니다.

**틀린 그림 찾기** 란 2 개의 유사한 그림을 비교해서 서로 다른 부분을 찾는 문제입니다.

(심심하시면 한 번 틀린 부분을 찾아보시길 바랍니다. 정답은 아래에 있습니다.)

<img src="./figures/sponge.jpg" width="50%">

정답은 총 3 개 (소스, 모자, 접시)로 우측 그림에서 검은색 원으로 강조된 부분입니다.

<img src="./figures/answer.png" width="50%">

이제 우리가 **틀린 그림 찾기** 문제에 대한 해결 방법으로 A 방법과 B 방법을 개발했다고 가정하겠습니다.

아래의 그림은 A 방법 및 B 방법을 이용했을 때의 결과를 정답과 비교한 그림입니다. 

보라색 원으로 강조된 부분은 각 방법이 서로 다른 부분(정답)이라고 판단하여 찾아낸 부분입니다.

![results](./figures/results.png)

결과를 비교해보면은 A 방법은 모자와 접시는 잘 찾아냈지만 소스는 찾아내지 못했습니다. 

그리고 B 방법은 모자, 접시, 소스를 모두 잘 찾아냈지만 뒤집개를 잘못 판단하였습니다. 
