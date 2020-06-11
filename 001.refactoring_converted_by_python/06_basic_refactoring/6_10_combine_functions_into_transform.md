# 6.10 여러 함수를 변환 함수로 묶기(Combine functions into Transform)

```python
# Before

reading = {'customer': 'ivan', 'quantity': 10, 'month': 5, 'year': 2017}

def update_customer(reading):
    pass


def taxable_charge(reading):
    pass
```



```python
# After

reading = {'customer': 'ivan', 'quantity': 10, 'month': 5, 'year': 2017} 

def enrich_reading(origin_reading):
    reading = dict(origin_reading)
    reading['customer'] =  'kwon'
    reading['quantity'] = 10
    return reading
    
    
    
```



## 배경

* 원본 데이터를 입력 받아서 필요한 정볼르 모두 도출한 뒤, 각각을 출력 데이터의 필드에 넣어 반환한다.
* 도출 로직이 중복된느 것을 피하기 위해서
