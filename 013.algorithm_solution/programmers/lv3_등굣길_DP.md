# 등굣길



## 문제 설명

* 최단거리를 구하는 문제이다.
* 초, 중딩 때 풀었던 최단거리 문제와 똑같다.
* 이 문제는 DP로 접근



## 문제 풀이





#### Step

1. Board 그리기
2. DP로 계산하기
3. 결과 값 리턴하기

### 이 문제에서 배울 점

1. Board 그리기
   * 예를들어서, 가로 3칸 세로 4칸을 board 를 그리기 위해서, 일부러 1칸씩 여유분을 만들어서 그려준다.
2. DP로 계산하기
   * 그림을 그려서 내가 계산하고자 하는 값을 어떻게 프로그래밍 수식으로 옮길 수 있는지에 대한 고민 필요



### Usefule Snippets

```python
def get_board_with_puddles(m, n):
    board = [[0] * (m + 1) for _ in range(n + 1)]
    board[1][1] = 1
    return board
```



```python
def calc_shortest_path(m, n, puddles, board):
    def set_board_value():
        if [j, i] in puddles:
            board[i][j] = 0
        else:
            board[i][j] = board[i - 1][j] + board[i][j - 1]

    for i in range(1, n + 1):
        for j in range(1, m + 1):
            if i == 1 and j == 1:
                continue
            set_board_value()

    return board
```







