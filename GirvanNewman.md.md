# :mushroom: Girvan Newman Algorithm 

Girvan Newman is a divisive community detection algorithm . In this algorithm we iteratively eleminate the edges that have the hoghest number of shortest paths between nodes passing through it. By doing this the network breaks down into smaller and smaller pieces and these would be the communities.


The idea is to find which edges in a network occur most frequently between other pairs of nodes by finding edge betweenness centrailities. The edges joining communities are then expected to have a high edge betweenness. The underlying community structure of the network will be much more fine-grained once the edges with the highest betweenness are eliminated which means that communities will be much easier to spot.


### Implementation 
The Girvan-Newman algorithm can be divided into four main steps:

1. Calculate the edge betweenness centrality for all the nodes in the graph
2. Remove the edge with the highest betweenness centrality.
3. Calculate the betweenness centrality for every remaining edge.
4. Repeat steps 2–4 until there are no more edges left.
