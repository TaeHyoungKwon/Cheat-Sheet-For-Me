# 7.2 컬렉션 캡슐화하기(Encapsulate Collection)

```python
# Before
class Person:
    def get_courses(self):
        return self.courses
    
    def set_courses(list_):
        self.courses = list_
```



```python
# After
class Person:
    def get_courses(self):
        return self.courses[:]
    
    def add_courses(course):
        ...
        
    def remove_courses(cource):
        ...
```



## 배경

* 모든 팀원이 원본 모듈 밖에서는 컬렉션을 수정하지 안흔 습관을 갖고 있다면, add(), remove() 같은 메서드를 제공하는 것만으로도 충분할 수 있다.
* 컬렉션 게터가 원본 컬렉션을 반환하지 않게 만들어서 클라이언트가 실수로 컬렉션을 바꿀 가능성을 차단하는게 낫다
* 내부 컬렉션을 직접 수정하지 못하게 막는 방법
  1. 절대로 컬렉션 값을 반환하지 않게 함
     1. 컬렉션에 접근하려면, 컬렉션이 소속된 클래스의 적절한 메서드를 반드시 거치게 하는 것
  2. 컬렉션을 읽기전용으로 제공할 수있다.
  3. 가장많이 사용하는 방식은 컬렉션 게터를 제공하되 내부 컬렉션의 복제본을 반환하는 것