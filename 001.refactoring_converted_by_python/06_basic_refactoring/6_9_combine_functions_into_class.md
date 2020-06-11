# 6.9 여러 함수를 클래스로 묶기(Combine Functions into Class)

```python
# Before


def base(reading):
    pass


def taxable_charge(reading):
    pass


def calculate_base_charge(reading):
    pass
```



```python
# After

class Reading:
    def __init__(self):
        pass
    
    def base(self, reading):
	    pass

	def taxable_charge(self, reading):
    	pass

	def calculate_base_charge(self, reading):
    	pass
```



## 배경

* 공통 데이터를 중심으로 긴밀하게 엮여 작동하는 함수 무리를 발견하면 클래스 하나로 묶고 싶어 진다.
* 중첩함수로 묶어도 되는데, 이때는 테스트 하기 힘들 수 있다.
