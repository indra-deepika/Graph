# :leaves: PageRank 

Pagerank is one of the most popular centrality algorithms. In all the other centrality algorithms above we only measure the direct influence of the nodes whereas in PageRank we consider the influence of the node , the node's neighbour so on and so forth.

INTRESTING FACT :bulb:
PageRank is named after Larry Page , cofounder of Google , he created it to rank the websites in Googl's search results. It was created by the basic assumption that the page that see a lot of incoming links and the one with more influential incomimg links must be the one that is most credible. Here the importance of a web pages can be taken as the number and quality of web pages that refer to it.


Pagerank can be computed iteratively ie moving from the node to its neighbours and so on or it can be done by randomly traversing the graph and calculating  frequency with whic hit the nodes.

## The PageRank Fomula

Let us assume that there are n pages T1...Tn that refer to a given page , then the PageRank as defined by Google paper goes as follows:

PR(u) = 1-d + d( PR(T1)/C(T1) + ...... + PR(Tn)/C(Tn))

- d is the damping factor which lies between the number 0 and 1  and is generally set to value of 0.85. This damping factor is taken as th probability that the user will continue to click on the link.

- 1-d is the probqability that the user has reached this page directly and not from any of the pages that refer to it.
- C(Tn) is defined as the out degree of the node T.


Let us see with an example how we can get the pageranks in a graph,

![PageRank](/PageRank_ex_.png "Text to show on mouseover")

First let us see this with the simple formula  
<!-- PR(u) =    PR(v)/|out(v)|  check this part  -->
and later using our unerstanding we can modifiy it to the real PageRank algorithm 

In the first iteration let us give each page a rank of 1/5. 

Iteration 1:

PR(1): Page 1 has one incoming link from Page 3 and Page 3 has four outgoing links. 
So the PR(1) = PR(3)/4 = (1/5)/4 = 1/20

PR(2): Page 2 has incoming link from Page 1 and Page 1 has one out going link, one incoming link from 3 and Page 3 has four outgoing links. 
So the PR(2)= PR(1)/1 + PR(3)/4 = 1/5 + (1/5)/4  = 5/20 

Here the PR()'s are from the frevious iteration hence we donot use the PR of the 2nd iteration for page 1.

Similary we get ,

PR(3) = PR(4)/2 = (1/5)/2 = 1/10
PR(4) = PR(3)/4 + PR(5)/1 = 1/20 + 1/5 = 5/20
PR(5) = PR(2)/1 + PR(3)/4 + PR(4)/2 = 1/5 + 1/20 + 1/10 = 7/20

Iteration 2: 

Using the same formulas and using the PR's of the 1st iterations we get the page rank for the 2nd iteration .
ie 

PR(1) = 1/20
PR(2) = 5/20
PR(3) = 1/10
PR(4) = 5/20
PR(5) = 7/20

And we get them to be

PR(1) = 1/40
PR(2) = 3/40
PR(3) = 5/40
PR(4) = 15/40
PR(5) = 16/40

So the final ranks are as following 

|     | Iteration 1| Iteration 1| Iteration 2| Final Rank|
|-----|------------|------------|------------|-----------|
| 1   |  1/5       |     1/20       |     1/40       |    5       |
| 2   |  1/5       |       5/20     |         3/40   |     4      |
| 3   |  1/5       |       1/10     |        5/40    |      3     |
| 4   |  1/5       |          5/20  |        15/40    |      2     |
| 5   |  1/5       |         7/20   |        16/40    |       1    |


Now let us try to understand 2 imporatnat question that arise 
1. Why are we calculating the pageranks multiple times?
2. And when should we stop our iterations?

1. We iterate many times because pageranks can fluctuate and one iteration is not enough to tell us if the page is important.

2. We stop our iteration when the rank values that we get become steady or converge
   - If each page's pagerank from the previous iteration differs from the current iteration by less than or equal to the margin of error which we have set to 0.01.
   - Or if we have iterated 100 times

   Whichever condition comes  first we stop according to that.

## Rank Sink 

A node or group of nodes  without outgoing links can monopolize the PageRank score by refusing to share this is known as the rank sink. Circular references cause an increase in their ranks as the surfer bounces back and forth among the nodes. The pagerank can accumulate and get stuck at sinks.

Our goal is to distribute the rank of sink pages among all pages in the graph. There are two ways we can do this :
- We can add outgoing edges from sinks to all pages
- We can distribute a sink’s pagerank evenly among all pages 

<!-- ### Handle Sinks - Adding Edges Method
1. After you have determined which pages are sinks, add outgoing
edges from each sink to every page in your graph, including the
sinks. (This should be done before the main loop and should only
be done once).
2. Remember to update the sinks' number of outgoing edges. (This
should also be done before the main loop).
3. Within the main body of your loop, after you clone your _current
array of pageranks into your _previous array, be sure to reset
the entirety of _current to be 0.0.

### Handle Sinks - Distribute Rank Method
Pseudocode for handleSinks() - you should call this at the start of every
iteration of the algorithm and set that to be each current page’s rank before
updating it:
1. For each sink, set its updated rank to be the sink’s previous rank divided
by the number of total pages and sum all of the sinks’ updated ranks.
2. For every page in the graph, set the new rank to be the sum of the sinks’
updated ranks. -->