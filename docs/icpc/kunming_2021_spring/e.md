# 2021 ICPC 昆明题解报告



#  E. Counting Binary Trees

!!! warning "Constraint"

    Input file: standard input
    
    Output file: standard output
    
    Time limit: 3 seconds
    
    Memory limit: 256 megabytes



!!! question "Description"


    You are given an array of positive integers $k_{1}, k_{2}, \ldots k_{m}$.
    A binary tree is special if all of these conditions are satisfied:
    
    - 1. A positive integer is written on every node of the tree.
    - 2. Every non-leaf node has both left child and right child, and the number written on it is equal to the product of numbers written on left child and right child. Here, we define a leaf as a node with no children, and a non-leaf node is a node that is not a leaf.
    - 3. The number written on any leaf is a multiple of at least one $k_{i}$. For two integers $x, y$, we consider $x$ to be a multiple of $y$ if there exists some integer $z$ such that $x=y z$
    Two binary trees are different if one of these conditions is satisfied :
    
    - 1. The numbers written on their root are different.
    - 2. Their left subtrees are different or their right subtrees are different.
    Note that the definition above is recursive.
    For a given $n,$ you need to find the number of special binary trees whose number written on the root is not greater than $n .$ Since the answer can be quite large, output it modulo $998244353$.


# Input:

!!! example ""

    The first line contains a single integer $T(1 \leq T \leq 10)-$ the number of test cases. Then $T$ test cases follow.
    
    The first line of each test case contains two integers $n, m\left(2 \leq n \leq 10^{9}, 1 \leq m \leq 4\right)$. The second line of each test case contains $m$ integers $k_{1}, k_{2}, \ldots, k_{m}\left(2 \leq k_{i} \leq 100\right)$.


# Output:
!!! example ""

    For each test case, print a single integer: the number of special binary trees whose number written on theroot is not greater than $n$. Remember that you only need to print it modulo $998244353$.

# standard input


```
2
6 2
2 3
100 2
6 9
```

# standard output

```
7
28
```

# Note

???+ Note

     In the first test case, you can find:
     
    - 1 special binary tree whose root is 2;
    - 1 special binary tree whose root is 3;
    - 2 special binary trees whose root is 4;
    - 3 special binary trees whose root is 6.
    
    So the answer is 1 + 1 + 2 + 3 = 7. Here is an illustration for the 7 trees.
    ![20210409153214.png](https://gitee.com/Dicarbene/pic/raw/master/img/20210409153214.png)
