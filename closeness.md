# :shamrock: Closeness Centrality 
The second type of centrality that we are going to discuss is the Closeness Centrality.

Closeness Centrality is a way of detecting nodes that are able to spread information efficiently through a subgraph.Closeness centrality of a node is measured as its average farness with respect to all other nodes. The nodes that are closeset to other node have the highest closeness centrality.

Centrality algorithm calculates the closeness centrality by taking the sum of the distances to other nodes(shortest distance) and the resulting sum is inverted.

C(u) = 1/ ∑ d(u,v) where v goes from 1 to n-1

Here u is the node whose closeness centrality we are calculating
n is the number of nodes in the graph
d(u,v) is the shortest distance between the nodes u and v

For getting normalised score to compare nodes of different graph we use the inverse of average length of the shortest path rather than the sum of shortest path.
So, the normalised closeness centrality is given by


C<sub>norm</sub>(u)= n-1/ ∑ <sub>v=1</sub> <sup> v=n-1</sup> d(u,v) 


## Closeness Centrality Variation: Wasserman and Faust

We modify the above problem to find the ratio of fraction of nodes in the group that are reachable to the average distance from the reachable nodes.


C<sub>WF</sub>(u)= (n-1/N-1)*(n-1/ ∑ <sub>v=1</sub> <sup> v=n-1</sup> d(u,v) )

here:
- u is a node.
- N is the total node count.
- n is the number of nodes in the same component as u.
- d(u,v) is the shortest-path distance between another node v and u.

## Closeness Centrality Application 


We apply Closeness Centrality when you need to know which nodes disperse things
the fastest. Using weighted relationships can be especially helpful in evaluating interaction speeds in communication and behavioral analyses.

Case studies:

- Uncovering individuals in very favorable positions to control and acquire vital
information and resources within an organization. One such study is “Mapping
Networks of Terrorist Cells”, by V. E. Krebs.

-  As a heuristic for estimating arrival time in telecommunications and package
delivery, where content flows through the shortest paths to a predefined target. It
is also used to shed light on propagation through all shortest paths simultane‐
ously, such as infections spreading through a local community. Find more details
in “Centrality and Network Flow”, by S. P. Borgatti.

- Evaluating the importance of words in a document, based on a graph-based key‐
phrase extraction process. This process is described by F. Boudin in “A Compari‐
son of Centrality Measures for Graph-Based Keyphrase Extraction”.
