# :cactus: Depth First Search / DFS 

DFS is a fundamental graph traversal algorithm. 

### How it works?
We start from a node , pick one of its neighbors and traverse as far as we can before bactracking. We do this until we have covered all the nodes of the graph.

###  :bulb: Intersting Fact
DFS was originally invented by French mathematician Charles Pierre Tremaux as a stategy for solving mazes.

 <!-- ////////////////////Insert Pic ///////////////////////////////////////////////////-->

### Implementation

We are assuming that the graph is stored in terms of an adjacency list. To implement the algorithm apart from the adjacency list that represents the graph we will also need an array that keeps track of the nodes that have been visited. 

```
vector<int> adj[N];  // adjacency list
boolean visited[N];  // keep track of nodes visited
```
Initially visited will have all values to be false since none of the nodes are visited yet.
When we arrive at a node s then the corresponding value in the visite array becomes true. It can be implemented in the following way using recursion .

```
void dfs(int s) {
if (visited[s]) return;
visited[s] = true;
// process node s
for (auto u: adj[s]) {
dfs(u); // selecting a neighbour and applying dfs on it 
}
}
```





