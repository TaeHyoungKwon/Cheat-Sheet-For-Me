# 7.7 위임 숨기기(Hide Delegate)

```python
# Before

manager = person.department.manager
```



```python
# After

manager = person.manager

class Person:
    def get_manager(self):
        return self.department.manager
```



## 배경

* 캡슐화는 모듈들이 시스템의 다른 부분에 대해 알아야 할 내용을 줄여준다.

* 캡슐화가 잘되어 있다면 무언가를 변경해야할 때 함꼐 고려해야 할 모듈 수가 적어져서 코드를 변경하기 쉬워진다.

* 객체 지향을 처음 배울 때는 캡슐화란 필드를 숨기는 것이라 배우는데, 경험이 쌓이면서 캡슐화의 역할이 그보다 많다는 사실을 깨닫게 된다.

    