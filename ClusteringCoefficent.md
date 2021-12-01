# :snowflake: Clustering Coefficient  

Clustering coefficient is a measure of the degree to which nodes in a graph tend to cluster together. The goal of Clustering coefficient algorithm  is to measure how tightly a group is clustered vs how tightly it could be clustered. 

There are 2 types of clustering coefficients
- Local CLustering Coefficient
- Global Clustering coefficient


### Local Clustering Coefficient 
Local Clustering Coefficient is defined as the  

```
pairs of a node's friends who are friends / pairs of node's friends
```

Here friends refers to the nodes that are connected.

Another way of defining this same thing is :

Multiplying the number of triangles passing through the node by two and then diving that by the maximum number
of relationships in the group. Its given by the formula

<b> CC(u)= 2R(u)/k<sub>u</sub>k<sub>u-1</sub> </b>


Here: 
where:
- u is a node.
- R(u) is the number of relationships through the neighbors of u (this can be obtained by using the number of triangles passing through u)
- k(u) is the degree of u.

![Local Clustering ](/AAD_proj_png/LocalClustering.jpg "Text to show on mouseover")

For the above graph let us see how to calculate the local clustering 

Method 1 :
pairs of a node's friends who are friends  - We can see that out of all the friends of u there are only 2 pairs of nodes who are friends
pairs of node's friends - The number of pairs of nodes friends that were possible is if each of the node was friends with every other node , then the number of pairs that would be possible were  f(f-1)/2 where f is the number of friends of u and in this case f =5.

=> Local Clistering Coefficient =  2/5(5-1)/2 = 1/5




### Global Clustering Coefficient 

We have measured how a node is clustered is a graph , but what if now we want to measure how much the graph itself is clustered. This is where measure is called Global Clustering coefficient.

There are 2 ways to measure Global Clustering Coefficient
- Avergage clustering coefficient 
- Transititvity

- Avergage clustering coefficient 
One of the obivious ways to find the degree of clustering of the grpah is to calculate the avgerage of all the local clustering coeffcients of the nodes in the graph.

- Transitivity

It is given by the formula = 3 x number of closed triads /number of open triads

Before moving to the formula first let us understand what a triad is. A triangle is simply 3 nodes connected by 3 edges, while a triad is 3 nodes connected by 2 edges. We can see that a triangle consists of 3 different triads (when one edge is removed).


We have 2 ways of getting global clustering coefficients but are these 2 similar if not how are they different? 

We can see that both of these methods try to measure the tendency to form triangles but transitivity weighs nodes with larger degree higher but average takes every node to be equal.

### Why should we care about clustering coeffiecients?
- A clustering coefficient is a measure of the degree to which nodes in a graph tend to cluster together. Evidence suggests
that in most real-world networks, and in particular social networks, nodes tend to create tightly knit groups characterized
by a relatively high density of ties this likelihood tends to be greater than the average probability of a tie randomly established between two nodes.
- Empirically vertices with higher degree having a lower local clustering coefficient on average.
- Local clustering can be used as a probe for the existence of  so-called structural holes in a network, which are missing links
  between neighbors of a person.
- Structural holes can be bad when are interested in efficient spread of information or other traffic around a network because
they reduce the number of alternative routes information can take through the network.
- Structural holes can be good thing for the central vertex whose friends lack connections because they give the node power over
information flow between those friends.
- The local clustering coefficient measures how influential a node is in
this sense, taking lower values the more structural holes there
are in the network around the node.
