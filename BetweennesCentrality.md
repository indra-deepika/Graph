## :hibiscus: Betweeness Centrality    

The third type of centrality that we are going to discuss is the Betweennes Centrality


Between Centrality focuses on the concept that sometimes the most important part in the system is not the one with the highest power or status but it's the middleman that connects groups or the brokers who control most of the flow of the information.

Betweennes Centrality detects the amount of influence that a node has over the flow of information or resources in the graph and is used in finding out which nodes act as the bridges from one group in the graph to another.

Pivitol node - A node is considered as a pivotal node for 2 other nodes if present in every shortest path between these nodes. We can see how pivitol nodes are essential to a graph without them the paths we need to take would be longer and it would be costlier.

The betweenness centrality is given by 

B(u) = ∑ <sub> s ≠ u ≠ t </sub> p(u)/p

here

- u is a node
- p is the total number of shortests paths that exist between the nodes s and t 
- p(u) is the number of shortest paths between nodes s and t that pass through node u

## Betweenness Centrality Applications

Betweenness Centrality applies to a wide range of problems in real-world networks.
We use it to find bottlenecks, control points, and vulnerabilities.

Example use cases include:

- Identifying influencers in various organizations. Powerful individuals are not
necessarily in management positions, but can be found in brokerage positions
using Betweenness Centrality. Removal of such influencers can seriously destabi
lize the organization. This might be considered a welcome disruption by law
enforcement if the organization is criminal, or could be a disaster if a business
loses key staff it underestimated. More details are found in “Brokerage Qualifica‐
tions in Ringing Operations”, by C. Morselli and J. Roy.

-  Uncovering key transfer points in networks such as electrical grids. Counterin‐
tuitively, removal of specific bridges can actually improve overall robustness by
“islanding” disturbances. Research details are included in “Robustness of the
European Power Grids Under Intentional Attack”, by R. Solé, et al.

- Helping microbloggers spread their reach on Twitter, with a recommendation
engine for targeting influencers. This approach is described in a paper by S. Wu
et al., “Making Recommendations in a Microblog to Improve the Impact of a
Focal User”.
   



