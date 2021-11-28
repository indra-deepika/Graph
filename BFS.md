# :seedling: Breadth First Search 

Breeadth First Search is a graph traversal algoithm 

## How does it work ?
First we saerch some arbitarary node in agraph , from that node we explore its neighboring nodes first and then we move on to next level of neighbours an so on.

# Places we can use it in
- To find the shortest paths in a graph 
## Time Complexity 
O(V+E)

## Implementation

We follow the following implementation to find the breadth first search of a graph.

We start from an arbitrary node and mark it as visited now we visit all the adjacent vertices , mark them as visited and insert them into a queue. Now when it is left with no unvisited nodes we dequeue the vertex and we repeat this until the queue is empty.

Let us see this with a help of an example 



<!-- pic -->
1. Let us initialise the queue 
<!-- pic -->
2. Let us take the starting node as S and mark it as visited.

- Queue
 
| | |
|--|--|

<!-- pic -->
3. Now let's visit the unvisited adjacent node from S, mark it as visited and enqueue it . In this example there are 3 adjacent nodes for the vertex S so we enqueue them one by one 

- Queue 

| C | B | A |
|---|---|---|

4. Now since S has no other unvisited adjacent vertex , we start following the same procedure for A as we did for S and we dequeue it . Since D is A's unvisited neighbour we enqueue it.

- Queue

| D | C | B |
|---|---|---|

5. Now since all the unvisited adjacent vertices of A are completed so we now perform the same procedure for B . But we can see that has no unvisited adjacent neighbours so we dequeue it , same applie for C and D so we deque them one by one and now the queue is empty and we have traversed the whole graph.

Code:

```
void bfsTraversal(int b)
{
    //Declare a queue to store all the nodes connected to b
    queue<int> q;

    //Insert b to queue
    q.push(b);


    // v is array which keeps track of all the nodes we visited
    //mark b as visited 
    v[b] = true;

    
    while (!q.empty())
    {
        int a = q.front();
        q.pop(); //delete the first element form queue

        for (auto j = g[a].begin(); j != g[a].end(); j++)
        {
            if (!v[*j])
            {
                v[*j] = true;
                q.push(*j);
            }
        }

    }
}

for (i = 0; i < n; i++)
    {
        //if the node i is unvisited
        if (!v[i])
        {
            bfsTraversal(i);
        }
    }


```
 
