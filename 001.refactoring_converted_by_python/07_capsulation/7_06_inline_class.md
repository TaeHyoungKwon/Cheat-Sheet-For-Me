# 7.6 클래스 인라인하기(Inline Class)

```python
# Before

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



```python
# After

class Person:
    def get_office_area_code():
        return self.office_area_code
    
    def office_number():
        return self._office_number
```







## 배경

* 제 역할을 못해서 그대로 두면 안되는 클래스는 인라인 해버리자
* 두 클래스의 기능을 지금과 다르게 배운하고 시픙ㄹ 때도 클래스를 인라인 한다.
    * 클래스를 인라인 해서 하나로 합친 다음 새로운 클래스를 추출하는 게 쉬울 수도 있기 때문