# 🕸️ Community Detection Algorithm

In all types of networks we see the formation of communitites and indetifying these communitites helps us better undersstand the behaviours of these groups like  preferences of peer groups, estimate resiliency, find nested relationships etc.

The general rule while trying to figure out a community is that the nodes in the community have more relationships within the community that outside of it.

Community detection techniques are useful for social media algorithms to discover people with common interests and keep them tightly connected. Community detection can be used in machine learning to detect groups with similar properties and extract groups for various reasons. For example, this technique can be used to discover manipulative groups inside a social network or a stock market. It also allows further to infer special relationships between the nodes that may not be easily accessible from direct empirical tests and it helps to better understand the properties of dynamic processes taking place in a network.

There are 2 types of Community Detection Algorithms 

- Agglomerative Methods
In agglomerative methods, we start with an empty graph that consists of nodes of the original graph but no edges. Next, the edges are added one-by-one to the graph, starting from stronger to weaker edges. New communities are formed in the consecutive steps of the algorithm.

-  Divisive Methods
Divisive Methods are the opposite of agglomerative method,. We start with the complete graph and take off the edges iteratively. The edge with the highest weight is removed first. After a certain number of steps, we get clusters of densely connected nodes.


We are going to see the basics of community detection:

1. Clustering Coefficients 
2. Strongly Connected Components
