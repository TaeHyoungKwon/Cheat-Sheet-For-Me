# 7.4 임시 변수를 질의 함수로 바꾸기(Replace Temp with Query)

```python
# Before

base_price = quantity * item_price

if base_price > 1000:
    return base_price * 0.95
else
	return base_price * 0.98
```



```python
# After

def get_base_price(quantity, item_price):
    return quantity * item_price

# ... 

if get_base_price() > 1000:
    return base_price * 0.95
else
	return base_price * 0.98
```



## 배경

* 함수 안에서 어떤 코드의 결괏값을 뒤에서 다시 참조할 목적으로 임시 변수를 쓰기도 한다.
* 임시 변수를 사용하면 값을 계산하는 코드가 반복되는 걸 줄이고, (변수 이름을 통해) 값의 의미를 설명할 수 있어서 유용하다.
* 그런데, 아예 함수로 만들어 사용하는 편이 나을 때가 많다.
* 변수 대신 함수로 만들어두면, 비슷한 계산을 수행하는 다른 함수에서도 사용할 수 있어 코드 중복이 줄어든다.
* 변수는 값을 한 번만 계산하고 그 뒤로는 읽기만 해야한다.
  * 변수에 값을 한번 대입한 뒤 더 복잡한 코드 덩어리에서 여러 차례 다시 대입하는 경우는 모두 질의 함수로 추출해야한다.