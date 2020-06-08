# 7.9 알고리즘 교체하기(Substitue Algorithm)

```python
# Before

def found_person(peoples):
    for people in peoples:
        if people == 'DON':
            return 'DON'
		if people == 'John':
            return 'John'
		if people == 'Kent':
            return 'Kent'
    return ''
```



```python
# After

def found_person(peoples):
    candidates = ['Don', 'John', 'Kent']
    return [people if people in peoples else '' for people in candidates]
```



## 배경

* 더 간명한 방법을 찾아내면 복잡한 기존 코드를 간명한 방식으로 고친다.
* 이 작업을 착수하려면 반드시, 메서드를 가능한 잘 게 나눴는지 확인해야한다.
* 알고리즘을 간소화하는 작업부터 해야 교체가 쉬워진다.