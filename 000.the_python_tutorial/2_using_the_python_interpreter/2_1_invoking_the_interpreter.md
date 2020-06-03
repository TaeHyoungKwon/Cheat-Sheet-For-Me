# 2. Using the Python Interpreter

## 2.1 Invling the Interpreter

1. 파이썬은 `/usr/local/bin/python3.8`  에 설치되어있다.
2. 인터프리터는 Unit Shell과 비슷 하게 동작한다.



### 2.1.1. Argument Passing

1. 스크립트 이름과 추가 인수는 문자열 목록으로 바뀌어서 sys 모듈의 argv 변수에 할당된다.

### 2.1.2 Interactinve Mode

```python
>>> the_world_is_flat = True
>>> if the_world_is_flat:
...     print("Be careful not to fall off!")
...
Be careful not to fall off!
```

