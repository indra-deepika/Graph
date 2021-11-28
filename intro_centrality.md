# :herb:  Centrality
While analysing a graph Centrality is a very important concept in identifying the importantant nodes (how "central" the node is to the graph). The importance can be of various types  and ech metric defines importance of a node from different perspectives.

Centrality algorithms are used to understand the roles of paticular nodes in a graph and the impact that they have on that network. They help us in understanding what the important nodes are and help us better understand groupo dynamics such as credibility , accesibility , the speed at which things spread and bridges between the groups. 

## Degree Centrality 

The first type of centrality that we are going to talk about is the degree centrality :

:bulb: <b>INTERESTING FACT <b> <br>
Degree Centrality was proposed by Linton C. Freeman in his paper "Centrality in Social Networks: Conceptual Clarificarion".

In different types of graphs there are different types of degree centrality ie:
- In non-directed graph : Degree of node is defined as the nuber of direct connections a node has with the other nodes.
- In directed graph: Degree of node is divided into
1. In-degree
2. Out-degree

### In-degree
In-degree defined as the number of connections incident on the node 
### Out-degree
Out-degree os defined as the number of connections that exist from this node to other nodes.

## Closeness Centrality

The second type of centrality that we are going to discuss is the Closeness Centrality.

Closeness Centrality is a way of detecting nodes that are able to spread information efficiently through a subgraph.


##  Betweeness Centrality    

The third type of centrality that we are going to discuss is the Betweennes Centrality


Between Centrality focuses on the concept that sometimes the most important part in the system is not the one with the highest power or status but it's the middleman that connects groups or the brokers who control most of the flow of the information.

Betweennes Centrality detects the amount of influence that a node has over the flow of information or resources in the graph and is used in finding out which nodes act as the bridges from one group in the graph to another.

## PageRank 

The last type of centrality that we are going to discuss is the PageRank.

Pagerank is one of the most popular centrality algorithms. In all the other centrality algorithms above we only measure the direct influence of the nodes whereas in PageRank we consider the influence of the node , the node's neighbour so on and so forth.
