# :honeybee: Degree Centrality 

The first type of centrality that we are going to talk about is the degree centrality :

:bulb: <b>INTERESTING FACT </b> <br>
Degree Centrality was proposed by Linton C. Freeman in his paper "Centrality in Social Networks: Conceptual Clarificarion".

In different types of graphs there are different types of degree centrality ie:
1. In non-directed graph : Degree of node is defined as the nuber of direct connections a node has with the other nodes.
2. In directed graph: Degree of node is divided into
   - In-degree
   - Out-degree

### In-degree
In-degree defined as the number of connections incident on the node 
### Out-degree
Out-degree os defined as the number of connections that exist from this node to other nodes.





![DegreeCentrality ](/AAD_proj_png/DegreeCentrality.jpg "Text to show on mouseover")

If the graph is stored in an adjacency matrix : 
For the above graph the adjacency matrix would be

| | A | B | C | D | E |
|-|---|---|---|---|---|
| A |0  | 4 | 0  | 0 | 0|
| B |0 | 0 | 2 | 1 | 0 |
| C |0 | 0 | 0 | 0 | 8 |
| D |5 | 0 | 0 | 0 | 0 |
| E |0 | 0 | 0 | 10 | 0 |

To find in degree of vertex say B

```
int in_degree=0;
int out_degree=0;

for( int i=0; i<5; i++)
{
    if(martix[1][i] != 0)
    in_degree++;
}

for( int i=0; i<5; i++)
{
    if(martix[i][1] != 0)
    out_degree++;
}

```

Applications of Degree centrality

We use degree centrality to analyse influence by looking at the number of incoming and ougoing relationships of a node or find the popularity of individual nodes.

## Applications of degree centrality

- Identifying the powerful individuals through their relationships say number of connections in social network.

- Is useful while seperating fraudsters from legitimate users of an online auction site.

Fradudsters often participate ion their own auctions to drive up the final price. They frequently bid in auctions hosted by other fradulent sellers, and these people often work in the same collusion group. When users and their transactions are represented as graphs , using the centrality algorithms we can detect fraudsters . When we have a small of known fraudsters we can detect more fraudsters by the fact that strong edges exist between fraudsters.  A study was conducted based on this principle and this was the result "Detecting fraudsters who work in collusion with known fraudsters was our primary goal. We also found that weighted degree centrality is a distinct feature that separates fraudsters and legitimate users. We actively used this fact to detect fraud. To this end, we extended the modified adsorption model by incorporating the weighted degree centrality of nodes. The results, from real world data, show that by integrating the weighted degree centrality to the model can significantly improve accuracy. "



