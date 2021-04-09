# 2021 ICPC 昆明题解报告



# I. Riichi!!

!!! warning "Constraint"

    Input file: standard input
    
    Output file: standard output
    
    Time limit: 1 second
    
    Memory limit: 256 megabytes



!!! question "Description"


    Yui is a cute girl expert in a kind of Mahjong game. In case you are not familiar with the game, here we briefly introduce its rules.
    Mahjong is played with *tiles*, divided into 34 *kinds*. To simplify the problem, we assume that *there is an infinite number of every kind* (although in real-world game one kind usually contains up to 4 tiles). The 34 kinds of tiles can be further divided into 4 *suites*, named as $bing,\ suo,\ wan,\ and\ zi$. The $bing,\ suo,\ wan$ have 9 kinds for each suite and $zi$ tiles has only 7 kinds.
    Here are the all 34 kinds of tiles used in Mahjong game: Each row refers to a suite of tiles $suo,\ bing,\ wan,\ zi$ in order.
    
    ![image-20210409163954378](https://gitee.com/Dicarbene/pic/raw/master/image-20210409163954378.png)
    
    Minor differences exist in various versions of Mahjong game, and here we only consider some basic rules.
    During the game, each player holds 13 tiles in hand. For each round, one player would draw one tile from the Mahjong table, then discard one tile from one of the 14 tiles owned at the time. A player wins the game if in a round he can create a special combination (defined below) with the 13 tiles in hand and 1 tiles drawn from table or discarded from other player.
    A special combination consists of 14 tiles, which can be divided into four kezi or shunzi, and an additional quetou.
    Here, kezi is a set of 3 identical tiles:
    
    ![image-20210409163848742](https://gitee.com/Dicarbene/pic/raw/master/image-20210409163848742.png)
    
    And shunzi is a set of 3 continuous tiles (please aware that suite zi cannot form shunzi) :
    
    ![image-20210409163826967](https://gitee.com/Dicarbene/pic/raw/master/image-20210409163826967.png)
    
    Finally, quetou is a pair of identical tiles:
    
    ![image-20210409164021263](https://gitee.com/Dicarbene/pic/raw/master/image-20210409164021263.png)
    
    Here are some samples of special combinations:
    
    ![image-20210409163030357](https://gitee.com/Dicarbene/pic/raw/master/image-20210409163030357.png)
    
    The second example might be confusing. Since you can combine your tiles arbitrary, the actual combination is the follows:
    
    ![image-20210409163107101](https://gitee.com/Dicarbene/pic/raw/master/image-20210409163107101.png)
    
    If the player can obtain a special combination by getting some tile, then we call the player is in the Riichi status. In this status one can achieve victory once he/she gets the desired kind of tile!
    For example, the following sets of 13 tiles are in the Riichi status, the tiles after the space indicates the desired tiles to achieve victory.
    
    ![image-20210409163154067](https://gitee.com/Dicarbene/pic/raw/master/image-20210409163154067.png)
    
    Now Yui is playing the Mahjong game. Sometimes she is very close to victory that if she tosses some tile she would reach the riichi status, while sometimes such tiles does not yet exist. And sometimes she has already got a winning hand of 14 tiles!
    To help you improve your Mahjong skills, Yui decides to give you a test. Now it is Yui’s turn and she has 14 tiles in her hand. Please tell her which tile should be discarded in order to reach riichi status, or just tell her that she has already won in this round!

# Input:

!!! example ""

    The input contains multiple tests cases. The first line includes a single integer $T-$ the number of test cases. It is guaranteed that $T \leq 10,000$.
    
    Each of the next $T$ lines indicates a test case. It contains a string $s$ of 28 characters, describing the 14 tiles that Yui currently has. For every $1 \leq i \leq 14$, the $i$ -th tile obtained by Yui is described by the $(2 i-1)$ -th and $2 i$ -th characters in the string: the former is a digit denoting the rank of the tile in its suite and the latter is one of $\mathrm{w}, \mathrm{b}, \mathrm{s}, \mathrm{z},$ which means the suite wan, bing, suo and $\mathrm{z}$ i respectively. It is guaranteed that all the $s$ in the input are valid and legal.

# Output:

!!! example ""

    Output the answer for each test case separately. For each test case, if Yui has already reached the winning status in this round, output Tsumo! in a single line.
    
    Otherwise, output a single integer ans in a single line, the number of choices for discarding tiles to reach riichi status.
    
    Each of the next ans lines should indicate one way to reach the riichi status. It should start with two characters indicating the tile to be discarded. To prove that such way leads to a riichi status, you should print all the tiles that can lead to victory for the status. For clarity, print a space between the first two characters and the rest of the line.
    
    Important: Pay attention to the order when printing the desired tiles, as there is NO special judge. For tiles in different suites, print them in the order wan, bing, suo, zi (that is, always print wan tiles at first, and so on). For tiles in the same suite, print the cards in the ascending order of their digits (that is, the tile with smaller number goes first). Additionally, if there are several tiles available for a riichi status to achieve victory, you should also sort them in the same way. See the Sample Output for details.

# standard input


```
5
1w2w3w4b5b6b7s8s9s1b1b1z2z6z
1w2w3w4b5b6b7s8s9s1b1b2z2z6z
1w2w3w4b5b6b7s8s9s1b1b2z2z2z
1b2b3b4b5b6b2s4s5s5s5s6s7s8s
1b1b1b2b3b4b5b6b7b8b9b9b9b1s
```

# standard output

```
0
1
6z 1b2z
Tsumo!
4
2s 3s4s6s9s
4s 2s
5s 3s
8s 3s
4
2b 1s
5b 1s
8b 1s
1s 1b2b3b4b5b6b7b8b9b
```

???+ Note

    The samples are the tiles below:
    ![image-20210409163431443](https://gitee.com/Dicarbene/pic/raw/master/image-20210409163431443.png)