# Greedy Algorithm

> 최적을 찾기 위해 각 단계에서 로컬 최적의 선택을 하는 휴리스틱 문제 해결 알고리즘

* 눈 앞의 이익 만을 좇는 알고리즘
* 합리적인 시간 내에 최적에 가까운 답을 찾을 수 있다는 점에서 매우 유용한 알고리즘이다.
* Greedy 알고리즘이 잘 작동하는 문제들은 `탐욕 선택 속성` 을 가지는 `최적 부분 구조` 인 문제들이다.
  * 탐욕 선택 속성
    * 앞의 선택이 이후 선택에 영향을 주지 않는 것
  * 최적 부분 구조
    * 문제의 최적 해결 방법이 부분 문제에 대한 최적 해결 방법으로 구성되는 경우
* 예제 문제
  * 다익스트라 알고리즘
  * 허프만 코딩
* 다이나믹 프로그래밍 과의 비교
  * 각 단계마다 로컬 최적해를 찾는 문제로 접근해 문제를 더 작게 줄여나가는 형태