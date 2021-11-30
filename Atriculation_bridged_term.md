# :fireworks: Articulation Point
In a graph, a vertex is called an articulation point if removing it and all the edges associated with it results in the increase of the number of connected components in the graph.

![Atriculation Point ](/Atriculation.png "Text to show on mouseover")

If in the above graph, vertex 1 and all the edges associated with it, i.e. the edges 1-0, 1-2 and 1-3 are removed, there will be no path to reach any of the vertices 2, 3 or 4 from the vertices 0 and 5, that means the graph will split into two separate components. One consisting of the vertices 0 and 5 and another one consisting of the vertices 2, 3 and 4 .Likewise removing the vertex 0 will disconnect the vertex 5 from all other vertices. Hence the given graph has two articulation points: 0 and 1.


### Where can be atriculation point be used ?
Articulation Points represents vulnerabilities in a network. 

###  Algorithm for finding atriculation points 

- To check if a point is an atriculation point or not we first calculate the number of connected components when the vertex is present and then calculate it when it is not present is the latter is greater then we can say that that vertex is an atriculation point.


### Implementation
- Iterate over all the vertices and in one iteration applies a Depth First Search to find connected components for bothe cases and compare them.

# Bridges

An edge in a graph between vertices say u and v is called a Bridge, if after removing it, there will be no path left between u and v. It's definition is very similar to that of Articulation Points. Just like them it also represents vulnerabilities in the given network.

![Atriculation Point ](/Atriculation.png "Text to show on mouseover")

For the graph given , if the edge 0-1 is removed, there will be no path left to reach from 0 to 1, similarly if edge 0-5 is removed, there will be no path left that connects 0 and 5. So in this case the edges 0-1 and 0-5 are the Bridges in the given graph.

### Algorithm to find if a vertex if a bridge or not
- To find out if a vertex is a bridge or not we remove an edge, if we find that there is no other path connecting the vertices of that edge then it is a bridge.

