
# Lecture 1
2025-01-22

## Flood-fill
A type of DFS, usually used when we want to search in a grid. 

## Representation of Input

### Bitmap:
To represent 2D-grid, or array of pixel in a image. Consider using a bitmap. That you read each row as a string, 




## Time complexity

### Subset
*$2^{n}$ subsets (or combinations) of n elements.*
Consider N = 3 ${A, B, C}$, total number of subset: $2^3= 8$.
1. Empty subset
2. {A}, {B}, {C}
3. {A,B},{A,C}, {B,C}
4. {A, B, C}
#### Algorithm:
We check that the bit at position j is 1 using the condition, if true we include in the subset, else exclude.

```c++
vector<vector<int>> find_subset(const vector<int>& vec) {
    vector<vector<int>> allsubs;
    int n = vec.size();
    int m = pow(2, n);
    
    for (int mask = 0; mask < m; mask++) {
        vector<int> subs;
        for (int j = 0; j < n; j++) {
            if (mask & (1 << j)) {
                subs.push_back(vec[j]);
            }
        }
        if (mask != 0) {
            allsubs.push_back(subs);
        }
    }
    return allsubs;
}
```
![[subset-demo.png]]


## Debugging
Use LLDB which is included by default with Xcode. 
1. *g++ -g your_program.cpp -o your_program*
2. *lldb ./your_program*
3. run
4. *if it craches use bt - backtrace*

## Gready Algorithm
**Q.** Which kinds of problem often have greedy solution?
- Scheduling problems, some graph algorithm.

**Q.** How do we design a greedy algorithm?
- Intuition and trial and error.
- What is fast.

## Dynamic Programming
**Q.** When might dynamic programming be useful?
- There are subproblems.
- Subproblems have have an ordering "small" to "large".
**Q.** How to draw dynamic programming diagram?
- Table - start filling it out from base case.
- Find recurrence relations. 
### Sources:
**Ex.**
https://www.cs.mun.ca/~kol/courses/2711-w08/dynprog-2711.pdf
### Ex. w solutions
https://home.csulb.edu/~tebert/teaching/lectures/528/dp/dp.pdf

## Graphs

### Flood-fill

### BFS (Breadth first search)

### MST Kruskal's algorithm

```pseudo

```



### Dijkstras 
``` pseudo

```
