# 2021 ICPC 昆明题解报告



# A. AC

!!! warning "Constraint"

    Input file: standard input
    
    Output file: standard output
    
    Time limit: 1 second
    
    Memory limit: 256 megabytes



!!! question "Description"


    Crystal's fortune predict system is successfully developed!
    
    The predict system is a distributed system consists of $N$ computers. When it receives a predict request, each computer will generate one lowercase letter as its output. The final fortune predict result is determined by the concentration of all $N$ outputs.
    
    Tired of getting bad predictions like awful: millions of bugs $awful:\ millions\ of\ bugs$, Ben decides to hack into the predict system and modify the predict result. He has already got the access permission of every computer in the predict system, so he can modify their output to any letter arbitrarily. 
    
    As Ben is going to take part in ICPC Asia Regional Kunming Site 2077, he wants predictions like suitable for writing $suitable\ for\ writing\ codes$ or will $get\ accepted\ for\ every\ problem$ . He has found that the more times the substring $ac$  occurs in the concentration of all $N$ outputs, the luckier he will get in the contest. But as the contest is coming soon, he only has time to modify at most $K$ outputs of the computers in the predict system.
    
    As Ben is busy hacking into the system, could you tell him how to get the most $ac$ substrings after his modification?

# Input:

!!! example ""

    The first line contains two integers $N$ and $K$ $(1≤N≤5×10^5,0≤K≤N)$ 
    
    The second line contains a string of length $N$, denoting the origin prediction. 
    
    It is guaranteed that the string consists of lowercase English letters.

# Output:

!!! example ""

    Output two lines. The first line contains a single integer, denotes the maximum number of $ac$ substring Bob can get, after his modification. The second line contains the final modified predict string. If there are multiple ways that results in the maximum number of $ac$ substring, print any.

# standard input


```
9 2
arakbacca
```

# standard output

```
3
acacbacca
```