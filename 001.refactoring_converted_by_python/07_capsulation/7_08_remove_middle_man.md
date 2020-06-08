# 7.8 중개자 제거하기(Remove Middle Man)

```python
# Before
manager = person.manager

class Person:
    def get_manager(self):
        return self.department.manager
```



```python
# After
manager = person.department.manager
```



## 배경

* 클라이언트가 위임 객체의 또 다른 기능을 사용하고 싶을 때마다 서버에 위임 메서드를 추가해야하는데, 이렇게 기능을 추가하다 보면 단순히 전달만 하는 위임 메소드들이 점점 성가셔 지고, 서버 클래스는 그저 중개자 역할로 전락하여, 차라리 클라잉너특 ㅏ위임 객체를 직접 호출하는게 나을 수 있다.