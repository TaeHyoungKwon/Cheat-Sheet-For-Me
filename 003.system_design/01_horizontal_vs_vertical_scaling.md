# Horizontal vs Vertical Scaling



* horizontal과 vertical scaling은 scalability와 관련된 개념들이다.
* horizontal은  흔히 아는 scaling-out, vertical은 scaling-in을 뜻한다.
* 쉽게 설명 하면, horizontal은 컴퓨터를 더 사는거고, vertical은 컴퓨터 성능을 높이는 것



## Horizontal vs Vertical

### Horizontal

1. 로드 밸런스가 필요함
2. Resilient
3. network calls(RPC) - 상대적으로 느림
4. data incosistency
5. 사용자가 컴퓨터를 추가할 수 있음

### Vertical

1. 로드 밸런스가 필요 없음
2. Single point of failure
3. Inter process communication - 상대적으로 빠름
4. data cosistency
5. Hartware limit

