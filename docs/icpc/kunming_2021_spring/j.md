# 2021 ICPC 昆明题解报告



# J. Mr. Main and Windmills

!!! warning "Constraint"

    Input file: standard input
    
    Output file: standard output
    
    Time limit: 1 second
    
    Memory limit: 256 megabytes



!!! question "Description"


    Mr. Main took a train from city s to city t and passed a plain full of windmills. The train ran in a straight line. A windmill is a machine used for wind power generation. Its fan blades rotate when the wind blows.
    From his perspective, colorful windmills lined up on the horizon from left to right.
    As the train was running, the order of windmills from his perspective was constantly changing: a windmill was originally on the left/right of another, and then changed to its right/left;
    Given the coordinates of the windmills, please find the coordinate of him when he just observed the h-th windmill exchanged order with other windmills for the k-th times. It is guaranteed that any three of the points given, the cities and the windmills, were not collinear, and that all of the windmills were on the same side of the line that the train ran along.
    ![image-20210409164407218](https://gitee.com/Dicarbene/pic/raw/master/image-20210409164407218.png)
    As shown in the picture, in Mr. Mian’s perspective, B was initially to the left of A, and later to the right of A.
    

# Input:

!!! example ""

    The first line of input contains two integers $n$ and $m$, where $n(1 \leq n \leq 1000)$ is number of windmills, and $m\left(1 \leq m \leq 10^{4}\right)$ is number of queries.
    
    The second line contains four integers $x_{s}, y_{s}, x_{t}$ and $y_{t}\left(-10^{6} \leq x_{s}, y_{s}, x_{t}, y_{t} \leq 10^{6}\right)$, which are the coordinates of the starting city $s$ and destination city $t$. The next $n$ lines describe the windmills, the $i$ -th of which contains two integers $x_{i}, y_{i}\left(-10^{6} \leq x_{i}, y_{i} \leq 10^{6}\right)$, which are the coordinates of the $i$ -th windmill.
    
    The next $m$ lines describe the queries, the $i$ -th of which contains two integers, $h_{i}$ and $k_{i}$ $\left(1 \leq h_{i} \leq n, 1 \leq k_{i} \leq 10^{6}\right)$, denoting a query for the coordinates when observing the $k_{i}$ -th pass of the $h_{i}$ -th windmill.

# Output:

!!! example ""

    Output $m$ lines, each containing two real numbers $x_{i}, y_{i}$, representing the coordinates when the $h_{i}$ -th windmill is observed to exchange order with other windmills for $k$ times; if it does not exist, output -1 . Your answer is considered correct if its absolute or relative error with the standard answer is less than $10^{-5}$

# standard input


```
4 2
0 0 5 0
1 3
2 4
4 1
4 5
1 2
3 2
```

# standard output

```
-1
4.6666666667 0.0000000000
```