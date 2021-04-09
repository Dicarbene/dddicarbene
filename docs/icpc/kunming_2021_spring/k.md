# 2021 ICPC 昆明题解报告



# K. Parallel Sort

!!! warning "Constraint"

    Input file: standard input
    
    Output file: standard output
    
    Time limit: 1 second
    
    Memory limit: 256 megabytes



!!! question "Description"


    As a master of parallel computing, schwer is recently considering about the method to achieve quick sorting on parallel computers. He needs your help!
    
    Given a permutation $\left(p_{1}, \cdots, p_{n}\right),$ you need to sort the permutation with minimum number of rounds. In a single round, one can take many pairs of integers $\left(x_{1}, y_{1}\right), \cdots,\left(x_{k}, y_{k}\right)$ as long as the values of $x_{1}, y_{1}, \cdots, x_{k}, y_{k}$ are pairwise distinct. Then with the help of $k$ CPUs, for each $i \in[1, k],$ the value of $p_{x_{i}}$ and $p_{y_{i}}$ will be switched immediately. Note that a permutation $\left(p_{1}, \cdots, p_{n}\right)$ is sorted if for every integer $i \in[1, n], p_{i}=i$ holds.
    Take some examples. Assume that $n=4 .$ For $p=(1,2,3,4),$ the minimum number of round is 0 as it is already sorted. For $p=(4,3,2,1),$ the answer is $1,$ as you can swap the indices (1,4) and (2,3) simultaneously.

# Input:

!!! example ""

    The first line of input contains a single integer $n\left(1 \leq n \leq 10^{5}\right)$, indicating the length of the permutation.
    The second line contains $n$ integers $p_{1}, \ldots, p_{n}\left(1 \leq p_{i} \leq n\right),$ the given permutation. It is guaranteed that these integers form a permutation, that is, for every integer $i \in[1, n]$ there exists an unique integer $j \in[1, n]$ such that $p_{j}=i$

# Output:

!!! example ""

    The first line of output should contain a single integer $m$, the minimum number of rounds to get the permutation sorted. Then print $m$ line to show one possible solution.
    
    The $i$ -th of the next $m$ lines should describe the $i$ -th round of your solution, beginning with a single integer $k$, and followed by $2 k$ integers $x_{1}, y_{1} ; \cdots ; x_{k}, y_{k}$. The constraints that $1 \leq x_{i}, y_{i} \leq n$ and the $2 k$ integers are pairwise distinct must be held.

=== "1"

    # standard input



    ```
    4
    1 2 3 4
    ```
    
    # standard output
    
    ```
    0
    ```
=== "2"

    # standard input



    ```
    4
    4 3 2 1
    ```
    
    # standard output
    
    ```
    1
    2 1 4 2 3
    ```