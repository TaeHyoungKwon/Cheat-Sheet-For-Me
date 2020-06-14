# Load balancing

* 로드밸런스가 하는 역할은 간단하다.
  * 요청을 받고, 요청을 n개의 서버 중 하나로 보내준다.
  * consistent hashing
    * request ID 값을 기반으로 hash function을 이용해서, 어디로 전달할지 결정하는데,
    * 웹서버의 숫자가 수시로 변경되는 상황에서는 이로인해 hash function의 결과 값이 바뀌게 되고, 해당 서버에서 사용되는 로컬 캐시를 다시 엎어야 하는 성능 상 비효율이 발생할 수 있는데,
    * 이 방법을 해결하기 위해 고안된 알고리즘
    * [관련 포스팅](http://sarghis.com/blog/726/)

