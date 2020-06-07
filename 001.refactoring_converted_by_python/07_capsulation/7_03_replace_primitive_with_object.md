# 7.3 기본형을 객체로 바꾸기(Replace Primitive with Object)

```python
# Before

DELIVERED = 'delivered'
READY = 'ready'
DELIVERING = 'delivering'
```



```python
# After

class DeliveryStatus(enum):
    Delivered = 'delivered'
    READY = 'ready'
    DELIVERING = 'delivering'
    
    @classmethod
    def is_registered(cls, status):
        return status in cls.__members__
```



## 배경

* 개발 초기에 단순한 정보를 숫자나 문자열 같은 간단한 데이터 항목으로 표현할 때가 많다.
* 단순 출력 이상의 기능이 필요해 지는 순간 그 데이터를 표현하는 전용 클래스를 정의하는 편