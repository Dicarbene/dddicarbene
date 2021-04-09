# 2021 ICPC 昆明题解报告



# C. Cities

!!! info "Constraint"

    Input file: standard input
    
    Output file: standard output
    
    Time limit: 4 seconds
    
    Memory limit: 256 megabytes



!!! description ""


    Bob lives in a chaotic country with $n$ cities in a row, numbered from 1 to $n$. These cities are owned by different lords, and the $i$ -th cities currently belongs to the $a_{i}$ -th lord. To simply problems, we assume there are $n$ lords in the country, and they are also numbered from 1 to $n$. Some lords may take control of multiple cities, while some new-born lords have not got any cities yet.
    
    Obviously, the greedy lords are not satisfied with the number of territories they have, so the country is constantly at war. Bob wants to change that, by making all the cities belong to the same lord!
    
    Bob can perform some magical operations to support his grand plan. With the help of each magic, Bob can do the following:
    
    - Choose some cities with consecutive indices such that they belong to the same lord, and assign them to any other lord.
    
    As magics are really tiring, Bob wants to know the minimum number of such operations he needs to use to make all the cities belong to one lord.
    
    The following picture shows an example where $n=6$. Different shapes are used to represent cities belonging to different lords. As shown in the picture, the minimum number of magic operations used is 2.

![image-20210409134223725](E:\图床\image-20210409134223725.png)

## Input:

!!! note ""

    The first line contains two integers $N$ and $K$ $(1≤N≤5×10^5,0≤K≤N)$ 
    
    The second line contains a string of length $N$, denoting the origin prediction. 
    
    It is guaranteed that the string consists of lowercase English letters.


## Output:
!!! note ""

    The first line contains a single integer $t(1 \leq t \leq 160)-$ the number of test cases. The first line of each test case contains an integers $n(1 \leq n \leq 5000)-$ the number of cities in the country. The second line of each test case contains $n$ integers $a_{i}\left(1 \leq a_{i} \leq n\right)-$ the $i$ -th city was originally owned by the $a_{i}$ -th lord. It is guaranteed that currently no Lord will have more than 15 cities, which means no one $a_{i}$ will appear more than 15 times in this line.
    It is guaranteed that the sum of $n$ over all test cases doesn't exceed 6000 .

## standard input


```
2
8
4 3 1 2 1 1 3 3
5
1 2 3 2 1
```

## standard output​

```
3
2
```

