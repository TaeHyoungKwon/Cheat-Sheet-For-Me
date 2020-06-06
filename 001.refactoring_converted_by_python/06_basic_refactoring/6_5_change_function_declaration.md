# 6.5 함수 선언 바꾸기(Change Function Declaration)

```python
# Before
def some_function():
	base_price = order.base_price
    return base_price > 1000
```



```python
# After
def some_function():
    return order.base_price > 1000
```



## 배경

### 연결부에서 가장 중요한 것

1. 함수의 이름
   1. 함수의 이름이 좋으면 함수의 구현 코드를 살펴볼 필요 없이 호출문만 보고도 무슨일을 하는지 파악할 수 있다.
   2. 하지만 좋은 이름을 떠올리기란 쉽지 않다.



### 언제 사용 될까?

1. 잘못된 함수를 발견하면 더 나은 이름이 떠오르는 즉시 바꾸라는 명령으로 받아들인다