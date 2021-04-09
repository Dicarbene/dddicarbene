# 2021 ICPC 昆明题解报告



# G. Gift

!!! warning "Constraint"

    Input file: standard input
    
    Output file: standard output
    
    Time limit: 1 second
    
    Memory limit: 256 megabytes



!!! question "Description"


    EQWE is a pastry chef who has $N$ friends. This year (obviously, the year 2021 ), he wants to give each friend a birthday cake made by himself.
    
    If EQWE wants to give the $i$ -th friend a birthday cake made by himself, he need $c_{i}$ days (do NOT need to be contiguous) before his friend's birthday to make it. After that he will get $v_{i}$ favorable impression. Note that it will be OK for him to finish the cake exactly on the birthday, as birthday parties are always held at night.
    
    But EQWE doesn't have much time and he has another plan. There are $M$ special gifts in the shop. EQWE can pay $a_{j}$ yuan to get the $j$ -th special gift and send it to any friend. Note that each gift is unique, which means that he can buy each gift at most once. After that he will get $b_{j}$ favorable impression. EQWE's friends are very polite, so they do NOT want to receive more than one gift (including birthday cakes and special gifts). Note that to gain some favorable impression from a friend, the selected gift must be sent on the exact date of the friend's birthday.
    
    Suppose that it is the first day of the year 2021 now (and he can start making birthday cakes immediately), and EQWE has $W$ yuan. What's the maximum number of favorable impression that EQWE can get in $2021 ?$

# Input:

!!! example ""

    The input file starts with an integer $T(1 \leq T \leq 100)$, denoting the number of test cases. Then $T$ test cases follow.
    
    For each test case, the first line contains three integers $N(1 \leq N \leq 500), M(1 \leq M \leq 15), W\left(1 \leq W \leq 10^{4}\right)$, denoting the number of friends, the number of special gifts, and the amount of money that EQWE has. Each of the following $N$ lines describes a friend, in the format of year $-$ month $-$ day $c_{i} v_{i}$, where year $-$ month $-$ day is the date of the friend's birthday, $c_{i}\left(1 \leq c_{i} \leq 30\right)$ is the day needed to make the birthday cake for the friend, and $v_{i}\left(1 \leq v_{i} \leq 10^{6}\right)$ is the favorable impression that EQWE can get. It is guaranteed that $c_{i}, v_{i}$ are integers. It is also guaranteed that the date given are all valid dates between the year 1990 and 2010 , that is, year is an integer between 1990 and $2010,$ month is an integer between 1 and 12 , and day is a positive integer which do not exceed the number of days in the given month. The next $M$ lines describe the special gifts, the $i$ -th of which contain two inte The $i^{\text {th }}$ line is $a_{i} b_{i}\left(1 \leq a_{i} \leq W, 1 \leq b_{i} \leq 10^{6}\right)$

# Output:

!!! example ""

    For each test case, output a line containing a single integer, denoting the maximum number of favorable impression that $EQWE$ can get.

# standard input


```
1
2 2 100
2000-01-01 10 13
2000-12-31 30 92
99 46
2 2
```

# standard output

```
138
```

# Note

???+ Note

    It is commonly known that a year is divide into 12 months, and for the most of the time the numbers of days in each month are 31,28,31,30,31,30,31,31,30,31,30 and 31. The only exception is that for leap years the second month contains 29 days. Of the time range mentioned in the problem (that is, from 1990 to 2021), the leap years are 1992, 1996, 2000, 2004, 2008, 2012, 2016 and 2020.