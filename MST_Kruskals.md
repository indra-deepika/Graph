# :elephant: Minimum Spanning Tree using Kruskal's algorithm

- What is a minmum spanning tree?
A minimum spanning tree (MST) or minimum weight spanning tree is a subset of the edges of a connected, edge-weighted undirected graph that connects all the vertices together, without any cycles and with the minimum possible total edge weight.

- What is Kruskal's Algorithm ?
It is a greedy algorithm in graph theory as in each step it adds the next lowest-weight edge that will not form a cycle to the minimum spanning forest. 

To prove this algorithm first we need toknow the cut property.

- Cut Property:

It staes that : If we take edges X that  are part of a Minimum Spanning Tree of G=(V,E).Pick any subset of nodes S for which X doesn't cross between S and V-S and let e be the lighest edge across this partition then X U {e} is part of some MST.

Proof: The nodes are partitioned into 2 parts ie S and V-S such that no edge of X crosses from the partition. Let us take a new edge e  which is the lightest edge between S and V - S and add it to T. Now we need to prove that this will become an MST . If e is an edge in T it makes no sense because t is already a MST and hence there is nothing to prove. So e must not be a part of T. Since T is spaanning tree it must already have an edge assume e' , so this creates an cycle . Since e is the lightesh edge removing e' and replacing it with e gives us a tree T' . We also can see that T' is connected since e' is a cycle edge and we removing a cycle edge cannot diconnect a graph .Also T and T' have the same number of edges as T so it is also a tree (since any undirected grapgh with V-1 edges is tree). We can see here that the weight of tree T is clearly less than the weight of T' . Which implies that T is not an MST contaradicting our previous statement . Hence , we can say that e must always be present in the MST of the graph.


# Pseudocode For Kruskals Algorithm :

```
procedure kruskal(G, W)
Input: A connected undirected graph G = (V, E) with edge weights we
Output: A minimum spanning tree defined by the edges X
for all u ∈ V :
makeset(u)
X = {}
Sort the edges E by weight
for all edges {u, v} ∈ E, in increasing order of weight:
if find(u) 6= find(v):
add edge {u, v} to X
union(u, v)
```

While performing kruskals algorithm we need to make sure that when we are connecting edges that does not create a cycle we can keep do this in the following way :

- We keep track of all the connected suparts and stores its info in a set , when we want to add an an edge we check wheter the 2 vertices belong to different sets otherwise we will get a cycle. This can be done by using the function find. Here the find fuction tell us the first vertex of the set . 
- If the find of both the vertices are not same now we add an edge between these two sets and combine these 2 sets to make a single set since they are now connected this is done by using the function union. 
- Initially when we start this process each node by itself is a component so we use makeset function to create a singleton set containing just x.
- We need |V| for makeset since we have v vertices and each one is a set , 2|E| find, and |V | − 1 since we need to connect |V|-1 edges
union operations.
- Time complexity of this algorithm will be O(E.(V+logE)) for naive approach of find and union operations.