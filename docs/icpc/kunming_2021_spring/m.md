# 2021 ICPC 昆明题解报告



# M. Stone Game

!!! warning "Constraint"

    Input file: standard input
    
    Output file: standard output
    
    Time limit: 4 seconds
    
    Memory limit: 1024 megabytes



!!! question "Description"


    There are $n$ piles of stones, the $i$ -th of which contains $s_{i}$ stones. The tiles are numbered from 1 to $n$. Rika and Satoko are playing a game on it.
    
    During each round of the game, Rika chooses some piles from all $n$ piles. Let denote the set of all chosen piles as $S$. Satoko then writes a non-negative integer $x .$ If Rika takes some piles from $S$ with the number of stones among all the taken piles equal to $x$, she wins the game, while otherwise (Rika cannot find such piles) Satoko wins the game. Note that each tile can be taken at most once during a round, and it is possible that Rika does not pick up any tile (when $x=0$ ).
    
    There are $Q$ rounds of game in total, and for the $i$ -th round of game Rika will let $S$ be the set of all piles with index between $l_{i}$ and $r_{i} .$ For each round, Satoko wonders the minimum integer $x$ she can write to win the game. As you are a master of programming, it is your turn to solve the problem!

# Input:

!!! example ""

    The first line of input contains two integers $n$ and $Q,$ where $n\left(1 \leq n \leq 10^{6}\right)$ is the number of tiles and $Q\left(1 \leq Q \leq 10^{5}\right)$ is the number of the rounds of the games. The second line contains $n$ integers $s_{1}, \ldots, s_{n}$, the $i$ -th of which, $s_{i}\left(1 \leq s_{i} \leq 10^{9}\right)$, indicates the number of stones in the tile with index $i$.
    
    Satoko wants you to compute the answers immediately after Rika chooses the interval, so she uses the following method to encrypt the input. The $i$ -th of the next $Q$ lines contains two integers $l_{i}^{\prime}, r_{i}^{\prime}\left(1 \leq l_{i}^{\prime}, r_{i}^{\prime} \leq n\right) .$ The chosen index range for the $i$ -th round, $l_{i}, r_{i},$ can be computed by the following formula:
    
    $l_{i}=\min \left\{\left(l_{i}^{\prime}+a n s_{i-1}\right) \bmod n+1,\left(r_{i}^{\prime}+a n s_{i-1}\right) \bmod n+1\right\}$
    
    $r_{i}=\max \left\{\left(l_{i}^{\prime}+a n s_{i-1}\right) \bmod n+1,\left(r_{i}^{\prime}+a n s_{i-1}\right) \bmod n+1\right\}$
    
    where $a n s_{i}$ denotes the answer for the $i$ -th round of the game (and thus $a n s_{i-1}$ is the answer for the previous round). You can assume that $a n s_{0}=0$. It is clear that under the given constraints, $1 \leq l_{i} \leq r_{i} \leq n$ holds.

# Output:

!!! example ""

    Output $Q$ lines, the $i$ -th of which contains a single integer ans $_{i}$, denoting the minimum integer $x$ Satoko can choose to win the $i$ -th round of the game.

# standard input


```
5 5
1 4 2 1 6
1 3
2 1
2 4
1 4
3 4
```

# standard output

```
8
15
4
9
4
```

???+ Note

    In the example above, the actual query intervals are [2,4], [1,5], [3,5], [1,4] and [3,4].