# 6.3 변수 추출하기(Extract Variable)

```python
# Before

def some_function():
    return order.quantity * order.item_price - max(0, order.quantity - 500) * ....
```



```python
# After

def some_function():
	base_price = order.quantity * order.item_price
	const quantity_discount = ....
	...
	return base_price - quantity_discount + shipping
```



## 배경

### 언제 적용하면 될까?

1. 표현식이 너무 복잡해서 이해하기 어려울 때, -> 이를 통해 코드의 목적을 훨씬 명확히 드러낸다.



### 변수 추출을 고려한다는 것

1. 표현식에 이름을 붙이고 싶다는 뜻
2. 이름을 붙이기로 했다면 그 이름이 들어가 문맥도 살펴야한다.
   1. 현재 함수 안에서만 의미가 있다면 변수로 추출
   2. 함수를 벗어난 넓은 문맥에서 까지 의미가 된다면, 넓은 범위에서 통용되는 이름을 생각해야한다.
      1. 함수로 추출해야한다.