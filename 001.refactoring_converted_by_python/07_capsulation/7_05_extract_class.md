# 7.5 클래스 추출하기(Extract Class)

```python
# Before

class Person:
    def get_office_area_code():
        return self.office_area_code
    
    def office_number():
        return self._office_number
```



```python
# After

class Person:
    def get_office_area_code():
        return self.telephone_number.get_area_code()
    
    def office_number():
        return self.telephone_number.get_number()
    
    
class TelephoneNumber:
    def get_area_code():
        return self.area_code
    
    def get_number():
        return self.number
```



## 배경

* 클래스는 반드시 명확하게 추상화하고 소수의 주어진 역할만 처리해야 한다
* 실무에서는 흔히 클래스가 점점 비대해지곤 한다.
* 메서드와 데이터가 너무 많은 클래스는 이해하기 쉽게 적절히 분리하는 것이 좋다.
* 특히 일부 데이터와 메서드를 따로 묶을 수 있다면, 어서 분리하라는 신호
* 함께 변경되는 일이 많거나 서로 의존하는 데이터들도 분리한다.