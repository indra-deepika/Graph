# ⛄ Shortest/Longest Path in DAG

Let use dynamic programming to find out the shortest path in DAG from the source node S to the destination node T.

- To solve this problem what we try to is that we try to find out the minimum distance of each node from the source node . Here this process can be done easily by compting and storing the value of the minimum distance of each node from source S , now when we have to find out the minimum distance for the next bigger problem we use the minimum distance to tht node and add the edge distance between the two nodes.

- To understand this properly let us take an example : Let us say that to get to node D the only ways are through nodes B and C . Let us take the distance between the nodes D and B to be 3 and that between C and D to be 1 . Now calculating the possible distances between source S and D we get  dist(B) + 3 and  dist(C)+1 [this can be done because D can be reached only through B and C and there are no cycles ].  So here we can see that solving subproblem B and C directly give us the answer the larger subproblem D. 

Pseudo code :
```
initialise all dist(.) values to infinity
dist(s)=0
for each v E V\{s}, in linearized order:
  dist(v)=min{dist(u)+l(u,v)} for (u,v) belonging to E
```
Intializing all the distances to infinity and from source node to source node is taken as 0. Taking a node and using the minimum disatnce of the nodes connected to it ,finding the distance from the source node through each connecting node and storing the minimum of those values. 

Similary longest path also can be found out by taking the maximum distance to each node from the source node instead of the minmum distance.
