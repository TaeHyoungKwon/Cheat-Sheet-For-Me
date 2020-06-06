# 6.1 함수 추출하기 (Extract Function)

```python
# Before
def print_owing(invoice):
    print_banner()
    outstanding = calculate_outstanding()
    
    # 세부 사항 출력
    print(f'고객명: {invoice.customer}')
    print(f'채무액: {outstanding}')
```



```python
# After
def print_owing(invoice):
    
    def print_detail(outstanding):
        print(f'고객명': {invoice.customer})
        print(f'채무액': {outstanding})
        
    print_banner()
    outstanding = calculate_outstanding()
    print_details(outstanding)
    
    
```



## 배경

### 코드를 언제 묶어야 하나?

1. 길이
2. 재사용성
3. 목적과 구현을 분리하는 방식

### 함수를 짧게 만들면 성능이 느려지나?

 요즘은 그럴일이 없다. 함수가 짧으면 캐싱하기가 더 쉽게 때문에 컴파일러가 최적화하는 데 더 유리할 떄가 많다.

### 짧은 함수의 이점을 취하려면?

 이름을 잘지어야 한다. 해당 코드 덩어리를 추출한 함수의 이름을 지을 때 주석을 참고하자.