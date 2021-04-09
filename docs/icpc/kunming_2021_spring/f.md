# 2021 ICPC 昆明题解报告



# F. Generating Strings

!!! warning "Constraint"

    Input file: standard input
    
    Output file: standard output
    
    Time limit: 3 seconds
    
    Memory limit: 1024 megabytes



!!! question "Description"


    $\mathrm{Mr}$. Chaos is a high school student. Teachers always ask him to write a lot of compositions, but he isn't interested in it at all. Tired of generating meaningless words by himself, he invented a machine to help him.
    
    His teacher has posted the model article - string $S$, on the blackboard. His machine can generate any lowercase string $T$ of length $n$ at a time. For a fixed string $T,$ the scoring method is simple: for any pair of integers $[l, r]$ such that the substring $T[l, r]$ is a palindrome, the final score will be added by the number that $T[l, r]$ occurs in $S$. Formally, let's define $T[l, r](1 \leq l \leq r \leq n)$ as the string $T_{l} T_{l+1} \ldots T_{r},$ a string is palindromic if it remains the same string when reversing, and the occurrence time of $P$ in $S, \mathrm{OCC}_{S}(P),$ is the number of pairs of $[l, r]$ such that $S[l, r]=P .$ Then, the value of $T,$ namely $\mathrm{V}(T),$ is defined as
    
    $$
    \mathrm{V}(T)=\sum_{1 \leq l \leq r \leq n, T[l, r] \text { is palindromic }} \text { OCC }_{S}(T[l, r])
    $$
    
    For example, given $S=$ bbbaa, when the machine generated a string $T=$ abbaabbaa, one of its palindromic substrings $P$ will be bb. $\mathrm{OCC}_{S}(P)$ is 2 because bb occurs in $S$ twice. Note that there are two bb in this case, and they are considered as different substrings and calculated twice.
    
    As Mr. Chao's best friend, you are asked to tell him the sum of value of all the $T$ that his machine can generate.
    
    You accept this mission without thinking twice. However, it seems that you are getting into trouble, because the teacher makes $m$ revisions on string $S .$ Each time the last character will be deleted or a new character $c$ will be added to the end. So now you have to answer the question for $m+1$ times.
    
    Formally, let $\mathcal{T}$ be the set of all strings of length $n$ that only contain lowercase English letters. You are going to calculate this formula
    
    $$
    \sum_{T \in \mathcal{T}} \mathrm{V}(T)
    $$
    
    at the beginning and after each revision of $S,$ that is, in total $m+1$ times. As the answer may be too large, you only need to output its remainder modulo $10^{9}+7$

# Input:

!!! example ""

    The first line contains one integer $t(1 \leq t \leq 25)-$ the number of test cases. Then $t$ test cases follow. The first line of each test case contains two integers and one string : $n, m, S\left(1 \leq n, m,|S| \leq 5 \times 10^{5}\right)$ the length of the string that machine can generate, the number of revision and the original article $S$. It is guaranteed that $S$ only contain lowercase English letters. Each of the next $m$ lines indicates a revision, in the order that they are made. The format will either be $1 c,$ which means that the character $c$ is added to the end of $S,$ or $2,$ which means that the last character of $S$ is deleted. It is guaranteed that $c$ is a lowercase English letter. It is guaranteed that in a single test file, the sum of $n$, the sum of $m$, and the sum of the length of $S$ among all test cases do not exceed $2 \times 10^{6}$.

# Output:

!!! example ""

    For each test case print $m+ 1$ lines, each containing a single integer. The first line should be the answer of the original $S$, while the next $m$ lines should be the answer after each revision. Note that you only need to print them modulo $109 + 7$.

# standard input


```
3
6 3 aaa
2
1 b
1 a
5 3 aabaaa
2
2
2
6 2 aababa
1 a
1 b
```

# standard output

```
218504832
144861392
216149648
287508208
13924249
11567037
9211852
6924944
430225380
503798516
575088800
```