# 6.1 함수 인라인하기 (Inline Function)

```python
# Before
def get_rating(driver):
    return 2 if more_than_five_late_deliveries(driver) else 1

def more_than_five_late_deliveries(driver):
    return 2 if driver.number_of_late_deliveries > 5 else 1
```



```python
# After
def get_rating(driver):
    return 2 if driver.number_of_late_deliveries else 1
```



## 배경

### 언제 적용하면 될까?

1. 함수 본문이 이름만큼 명확할 때 인라인을 하자. 
2. 간접 호출을 너무 과하게 쓰는 것도 흔한 인라인 대상
3. 단순히 위임하기만 하는 함수들이 너무 많아서 위임관계가 복잡히 얽혀 있으며 인라인 한다.