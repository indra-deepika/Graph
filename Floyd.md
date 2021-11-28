# :fallen_leaf: Floyd Warshall

Floyd-Warshall algorithm is an All-Pairs Shortest Path algorithm.

- All-Pairs Shortest Path algorithm - It can find the shortest path between all pairs of nodes

We can approach this by  using dijstras for all the vertices .  But another way to approach this is using dynamic programming - Floyd Warshall 

#### Time complexity
O(V<sup>3</sup>)

## Implementation

To do implement this first we take a matrix with all the edge lengths maapped on it and where there is no edge then that path is taken to be infinity. 

Let us take an example :

Let the edges be <br>
1 -> 2 : length = 3 <br>
2 -> 3 : length = 2 <br>
3 -> 4 : length = 1 <br>
4 -> 1 : length = 2 <br>
1 -> 4 : length = 7 <br>
3 -> 1 : length = 5 <br>
2 -> 1 : length = 8 <br>


now we construct a matrix representing this graph

[0 3  inf  7]<br>
[8 0   2  inf]  = A0 <br>
[5 inf 0   1] <br>
[2 inf inf 0] <br>

Now we construct a matrix such that we take all paths that have an intermediate vertex = 1
Now we modify all thesse values such that we can add the paths having 1 as the the intermediate vertices .

So now we get  A1[2,3] = min{ A0[2,1] + A0[1,3], A0[2,3] } <br>
               A1[2,4] = min{ A0[2,1] + A0[1,4], A0[2,4] } <br>

           this can be done for each matrix value 

we get the matrix A1 = 

[0 3  inf  7] <br>
[8 0   2  15]  <br>
[5 8   0   1] <br>
[2 8  inf  0] <br>

And similary we go on to do this for the vertex 2

here we get A2=

[0 3   5  7] <br>
[8 0   2  15]  <br>
[5 8   0   1] <br>
[2 5   7  0] ............ so on for 3 and 4 also <br>

Pseudocode:
here dist(i,j,k) is the path length from i to j when only the intermediate vertices from 1 to k are considered
```
for i = 1 to n:
for j = 1 to n:
dist(i, j, 0) = ∞
for all (i, j) ∈ E:
dist(i, j, 0) = l(i, j)
for k = 1 to n:
for i = 1 to n:
for j = 1 to n:
dist(i, j, k) = min{dist(i, k, k − 1) + dist(k, j, k − 1), dist(i, j, k − 1)}
```
