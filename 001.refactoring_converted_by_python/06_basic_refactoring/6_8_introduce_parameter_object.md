# 6.8 매개변수 객체 만들기(Introduce Parameter Object)

```python
# Before
def amount_invoiced(start_date, end_date):
    pass

def amount_received(start_date, end_date):
    pass
    
def amount_overdue(start_date, end_date):
    pass

    
```



```python
# After
date_range = {
    'start_date': '2020-06-01',
    'end_date_date': '2020-06-06',
}


def amount_invoiced(date_range):
    pass

def amount_received(date_range):
    pass
    
def amount_overdue(date_range):
    pass
```



## 배경

* 데이터 항목 여러 개가 이 함수에서 저 함수로 함께 몰려다니는 경우 데이터 구조 하나로 모아준다.
  * 데이터 사이으 ㅣ관계가 명확해진다는 이점을 얻을 수 있다.
  * 매개변수의 수가 줄어든다.

