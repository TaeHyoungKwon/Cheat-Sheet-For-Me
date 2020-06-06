# 6.6 변수 캡슐화하기(Encapsulate Variable)

```python
# Before
default_owner = {'first_name': '마틴', 'last_name': '파울러'}
```



```python
# After
default_owner = {'first_name': '마틴', 'last_name': '파울러'}


def default_owner():
    return default_owner_data


def set_default_owner(arg):
    return default_owner_data = arg
```



## 배경

### 언제 사용할까?

1. 접근 할 수 있는 범위가 넓은 데이터를 옮길 때는 먼저 그 데이터로의 접근을 독점하는 함수를 만드는 식으로 캡슐화하는 것이 가장 좋은 방법일 때가 많다.



### 데이터 캡슐화가 도움을 주는 경우

1. 데이터를 변경하고 사용하는 코드를 감시할 수있는 확실한 통로가 되어 줌
2. 변수를 참조하는 코드를 추가하거나 변경할 때마다 최대한 캡슐화 한다.



### 불변데이터

1. 불변 데이터는 가변 데이터보다 캡슐화할 이유가 적다 이유는 데이터가 변경될 일이 없엇 ㅓ갱신 전 검증 같은 추가 로직이 자리할 공간을 마련할 필요가 없기 때문이다.





