#  Parallel Computation of Longest Path Problem in a Grid


### Problem Statement

```
   Find a longest path between any two given vertices in a Grid
```

### Input

![Input](https://user-images.githubusercontent.com/84730469/233823447-8db7fc14-b504-4174-a95e-c37a6b71b604.png)

### Output

![Output](https://user-images.githubusercontent.com/84730469/233823446-a502e9a3-a0d7-486b-83e8-db82d2dbb8df.png)


### Analysis and Comparison

***
Serial Alogrithm:
* Works by exploring all possible paths from the source to the destination. 
* At each step, the algorithm can move in any of the four directions (up, down, left, or right) as long as the next cell is within the boundaries of the matrix, has a value of 1, and has not been visited before.  
* The algorithm explores all possible paths, we visit each cell multiple times. Therefore, the worst-case time complexity of the serial algorithm is **O(4^(MN))**, where M and N are the dimensions of the matrix.

Parallel Algorithm:
* Divides the search space into smaller subspaces that can be explored independently by different threads. 
* Each thread works on a separate subproblem, and the results are combined using a critical section to obtain the final result. 
* The number of threads used by the program is determined by the OpenMP runtime system and depends on the number of available processors and other factors. 
* Assuming that the parallel algorithm uses P threads to explore the search space, the time complexity can be reduced to **O(4^(MN/P))**.


