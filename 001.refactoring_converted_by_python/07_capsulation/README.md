# 06 기본적인 리팩토링

## 캡슐화

1. 모듈을 분리하는 중요한 기준
   * 각 모듈이 자신을 제외한 다른 부분에 드러내지 않아야 할 비밀을 얼마나 잠 숨기느냐에 있다.
   * 레코드 캡슐화 하기
   * 컬렉션 캡슐화하기
2. 리팩토링 할 때, 임시 변수가 자주 걸리적 거릴 때,
   * 임시 변수를 질으 ㅣㅎ마수로 바꾸기
3. 클래스는 본래 정보를 숨기는 용도로 설계됨
4. 클래스는 내부 정보 뿐 아니라 클래스 사이의 연결 관계를 숨기는 데도 유용하다.
   * 위임 숨기기
     * 너무 많이 숨기려댜 보면 인터페이스가 비대해질 수 있으니, 중개자 제거하기도 필요
5. 캡슐화 단위는 클래스와 모듈이지만 함수도 구현을 캡슐화 한다.