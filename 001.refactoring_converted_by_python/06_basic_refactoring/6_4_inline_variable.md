# 6.4 변수 인라인하기

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

### 언제 쓸까?

1. 변수의 이름이 원래 표현식과 다를바 없을 때,
2. 변수가 주변코드를 리팩토링 하는데 방해가 될 때

