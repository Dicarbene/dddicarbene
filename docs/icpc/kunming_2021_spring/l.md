# 2021 ICPC 昆明题解报告



# L. Simone and Graph Coloring

!!! warning "Constraint"

    Input file: standard input
    
    Output file: standard output
    
    Time limit: 2 seconds
    
    Memory limit: 512 megabytes



!!! question "Description"


    Simone, a student of Graph Coloring University, is interested in permutation. Now she is given a
    permutation of length n, and she finds that if she connects each inverse pair, she will get a graph.
    Formally, for the given permutation, if $i < j and a_i > a_j$ , then there will be an undirected edge between node $i$ and node $j$ in the graph.
    Then she wants to color this graph. Please achieve poor Simone’s dream. To simplify the problem, you just need to find a way of coloring the vertices of the graph such that no two adjacent vertices are of the same color and minimize the number of colors used.

# Input:

!!! example ""

    There are multiple test cases. The first line of the input contains an integer $T\left(1 \leq T \leq 10^{6}\right),$ indicating the number of test cases.
    
    For each test case, the first line contains an integer $n\left(1 \leq n \leq 10^{6}\right),$ indicating the length of the permutation.
    The second line contains $n$ integers $a_{1}, a_{2}, \ldots, a_{n},$ indicating the permutation. It is guaranteed that the sum of $n$ over all test cases does not exceed $10^{6}$.

# Output:

!!! example ""

    For each test case, the first line contains an integer $c,$ the chromatic number(the minimal number of colors been used when coloring) of the graph.
    The second line contapins $n$ integers $c_{1}, c_{2}, \ldots, c_{n},$ the color of each node. Notice that $c_{i}$ should satisfy the limit that $1 \leq c_{i} \leq c$
    If there are several answers, it is acceptable to print any of them.

# standard input


```
2
4
1 3 4 2
2
1 2
```

# standard output

```
2
1 1 1 2
1
1 1
```