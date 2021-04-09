# 2021 ICPC 昆明题解报告



# B. Chessboard

!!! info "Constraint"

    Input file: standard input
    
    Output file: standard output
    
    Time limit: 2 seconds
    
    Memory limit: 256 megabytes



!!! description ""

    Your are playing a computer game. The game is played on a chessboard of $n$ rows and $m$ columns.
    For each grid on the board, you can choose to put a black piece or a white piece on it, or leave it blank. Denote $(i, j)$ as the grid in the $i$ -th row and the $j$ -column. For each $i \in[1, n], j \in[1, m],$ putting a black piece on $(i, j)$ earns you $s b_{i, j}$ points, while a white piece earns you $s w_{i, j}$ points, and leaving blank do not affect your score. The overall score will be the sum of the points earned by each piece. Note that a grid can contain at most one piece at the same time, that is, you cannot put a white piece and a black one simultaneously. It is guaranteed that $s b_{i, j}, s w_{i, j}$ are all non-negative integers. After you finish placing the pieces, the computer program checks whether the pieces are put in a $beautiful$ way or not. Let's define $b_{i}$ as the number of black pieces in the $i$ -th row, $B_{i}$ as the number of black pieces in the $i$ -th column, $w_{i}$ as the number of white pieces in the $i$ -th row, and $W_{i}$ as the number of white pieces in the $i$ -th column. The pieces are considered $beautiful$ if
    
    - For any $i \in[1, n], b_{i}-w_{i} \in\left[l_{i}, r_{i}\right]$ holds.
    - For any $i \in[1, m], B_{i}-W_{i} \in\left[L_{i}, R_{i}\right]$ holds.
    Tired of high scores, you decide to minimize your score. To simplify the problem, you only need to output the minimum possible score among all beautiful placements of pieces.

## Input
!!! description ""

    The first line of input contains two integers $n, m(2 \leq n, m \leq 50)$, denoting the number of rows and columns of the board.
    
    The next $n$ lines describe the points earned by putting black pieces. The $i$ -th of them contains $m$ integers, the $j$ -th of which denotes $s b_{i, j}\left(0 \leq s b_{i, j} \leq 10^{3}\right)$. The next $n$ lines describe the points earned by putting white pieces. The $i$ -th of them contains $m$ integers, the $j$ -th of which denotes $s w_{i, j}\left(0 \leq s w_{i, j} \leq 10^{3}\right)$. The next $n$ lines describe the constraints on each row, the $i$ -th of which contains two integers $l_{i}, r_{i}\left(-m \leq l_{i} \leq r_{i} \leq m\right),$ whose meaning can be found in the statement above. The next $m$ lines describe the constraints on each column, the $i$ -th of which contains two integers $L_{i}, R_{i}\left(-n \leq L_{i} \leq R_{i} \leq n\right),$ whose meaning can be found in the statement above.
    It is guaranteed that there exists at least one strategy that satisfies all the constraints.

## Output
!!! description ""
    Output a single integer, denoting the minimum score you can get.

## standard input


```
3 3
6 9 0
3 2 7
6 4 6
0 6 5
1 6 9
8 5 7
-3 -1
-3 0
1 3
0 0
1 1
-2 0
```

## standard output

```
9
```

