# :spider_web: Dijkstra's Algorithm 

Dijkstra's Algorithm is a Single Source Shortest path algorithm for graphs with non-negative edge weights.

### Time Comlexity
O(E*log(V))

For dijkstra's algorithm we use only non-negative edges . Due to this property dijkstra's can act in a greedy manner ,by choosing next most promissing node . This done becuse we ensure that one we find a shortest path to a node we find another shortest path by taking a path with negative edge weight.

## Implementation

- We maitain an array called dist which maintains the distance to every node. In the starting all the values are infinity and the distance to the starting node is taken as 0.
- We maintain a priority queue of key value pair ie node , distance and by sorting the distance we can find which node to visit next

- At the start we insert (s,0) into the priority queue where s is the starting node and now we loop while till the time priority queue is not empty and we pull out the next most promising pair.

- We now iterate over all edges going outward from the node we are currently at and we relax each edge appending a new key-value pair to the PQ for every relaxation.

## Code 
```
for (int i = 1; i <= n; i++)
{
 distance[i] = INF;
}

distance[x] = 0;
q.push({0,x});
while (!q.empty()) 
{
 int a = q.top().second; q.pop();
 if (processed[a]) 
 continue;
 processed[a] = true;
 for (auto u : adj[a])
 {
  int b = u.first, w = u.second;
  if (distance[a]+w < distance[b]) 
  {
  distance[b] = distance[a]+w;
  q.push({-distance[b],b});
  }
 }
}
```





