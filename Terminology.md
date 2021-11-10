### Simple Graph 
Pair of vertices can have only one edge betweeen them.
### Multighraph
Vertex pair can have multiple edges between them
### Graph or Pseudograph
Vertex pairs can have multiple edges between them, vertices can loop back to themselves.

## Directed Graph  vs Undirected Graph
A directed graph or digraph is graph where all the edges are directed from one vertex to another. In contrast, a graph where the edges are bidirectional is called an undirected graph.
![Directed vs Undirected ](/Directed_.png "Text to show on mouseover")


## Weighted Graphs vs Unweighted Graphs
In weighted graphs, each edge is assigned a weight. This weight can represent the strength of the connection between two nodes, or a value associated with moving between two nodes. If the edges are not assigned any weights then it is know as an unweighted graph. <br><br>
![Weighted vs Unweighted ](/Weighted_.png "Text to show on mouseover")


## Connected Graphs vs  Disconnected Graphs
If there is a path from any point to any other point in the graph then such a raph is called a connected graph . A graph that is not connected is said to be disconnected.
A subgraph of a graph that is connected within itself but not connected to the rest of the graph  is called a connecting component.
![Connected vs Disconnected ](/Connected_.png "Text to show on mouseover")


## Cyclic Graphs vs Acyclic Graphs
In graph theory cycles are the paths such that it starts and ends at the same node. If a graph has a cycle then it is called a cyclic graph. If there are no cycles present in the graph then it is called a acyclic graph.
![Cyclic vs Acyclic ](/Cyclic_.png "Text to show on mouseover")

## Sparse graph vs Dense Graph 
<p>A dense graph is a graph in which the number of edges is close to the maximal number of edges. The opposite, a graph with only a few edges, is a sparse graph. </p>

<p>The *sparsity* of a graph is based on the number of edges it has compared to the maximum possible number of edges, which would occur if there was a edge between every pair of nodes.</p>

<p>A graph where every node has an edges corresponding to every other node is called a complete graph, or a clique for components.</p>

<p>To measure the actual density of a graph we use the following formula = 2R/N(N-1). Where R is the number of relationships (edges).</p>

![Sparse vs Dense ](/Sparse_.png "Text to show on mouseover")


# Special Graphs 

## Trees
A tree is an undirected graph with no cycles. Equvivalent;y , it is a connected graph with N nodes and N-1 edges.
![Trees ](/Trees.png "Text to show on mouseover")
## Rooted Tree
A rooted tree is a tree with a designated root node where every edge either points away from or towards the root node. When edges point away from the root the graph is called an <b> arborescence (out-tree) </b> and <b>anti-aborescence (in-tree)</b> otherwise.
![Rooted ](/Rooted.png "Text to show on mouseover")

## Directed Acyclic Graph
DAGs are directed graphs with no cycles.
Fact :bulb: 
<p>All out-trees are DAGs but not all DAGs are out-trees</p>

![DAG ](/DAG.png "Text to show on mouseover")

## Bipartite Graph
<p>A bipartite graph is one whose vertices can be split into two independant groups U,V such that every edge connects between U and V. </p> or
<p>The graph is two colourable ie A graph is 2-colorable if we can color each of its vertices with one of two colors, say red and blue, in such a way that no two red vertices are connected by an edge, and no two blue vertices are connected by an edge (a k-colorable graph is defined in a similar way). </p> or <p> There is no odd length cycle. </p>

![Bipartite ](/Bipartite.png "Text to show on mouseover")


## Complete Graphs
<p> A complete graph is one where there is a unique edge pair of nodes. A complete graph with n vertices is denoted as the graph K<sub>n</sub></p>

![Complete](/Complete.png "Text to show on mouseover")

# Representation of graphs

## Adjacency Matrix

<p> A adjacency matrix is a very simple way to represent a graph. The idea is that the cell m[i][j] represents the edge weight of going from node i to node j.</p>

![Adjacency Matrix](/Adj_Matrix.png "Text to show on mouseover")

|PROS     | CONS  |
|-------- |-------|
| Sapce efficient for represening dense graph     |  Requires O(V<sup>2</sup>) space                        |
| Edge weight lookup has a time complexity of O(1)|  Iterating over all the edges take O(V<sup>2</sup>) time|
| Simplest graph representation                   |                                                         |
## Adjacency List
<p>An adjacency list is a collection of unordered lists used to represent a finite graph. Each unordered list within an adjacency list describes the set of neighbors of a particular vertex in the graph.</p>

![Adjacency List](/Adj_List.png "Text to show on mouseover")

|PROS     | CONS  |
|-------- |-------|
| Sapce efficient for represening sparse graph     |  Less space efficient for denser graphs         |
| Iterating over all edges is efficient            |         Edge weight lookup is O(E)              |
|                                                  |    Sligthly more complex type of representation |
## Edge List
<p>An edge list is a way to represnt a graph simply as an unordered list of edges. Assume the notation for any triplet (u,v,w) means : The cost fom node u to node v is w </p>

![Edge List](/Edge_List.png "Text to show on mouseover")
|PROS     | CONS  |
|-------- |-------|
| Sapce efficient for represening sparse graph     |  Less space efficient for denser graphs         |
| Iterating over all edges is efficient            |         Edge weight lookup is O(E)              |
| Very simple struture                             |    Sligthly more complex type of representation |

