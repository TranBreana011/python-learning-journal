Things I learned this week:

Greedy Algorithms:
Kruskal's Algorithm:
- Kruskal's algorithm is a greedy algorithm that finds a minimum spanning tree for a connected weighted undirected graph
- This means it finds a subset of the edges that forms a tree that includes every vertex, where the total wieght of all the edges in the tree is minimized
- Our goal is to find a collection of edges that minimizes the total weight
- essentially just tries to minimize the path
- we need this because 

The dumb approach is to go through everything and find the smallest weight
- "hardworking"

Greedy Choice(depends):
- assume you want lowest weights first
- we need smallest valued edge that connects at least one new node
    - avoid cycles!!! it will maximize the weight

Pseudocode:
1. Initialization: Start with an empty Set A that will eventually contain the edges of the minimum spamming tree (MST)
   - fill up the list with edges
2. Sorting Edges (Greedy Step): Sort all the edges of the graph in non-decreasing order by their weights
   - O(n log n)
   - AVOID CYCLES, just adds unnecessary weight without bringing anything new
3. Make Set: For each vertex in the graph, make a disjoint set containg only that vertex. This step is crucial for detecting cycles as the algorithm progresses
   - for every single vertex in the graph
   - ex. {a}, {b}, {c}, {d}
4. Iterate Through Edges: Go through the sorted edges and determine if the edge's vertices belong to different sets:
   - if they are in different sets, adding this edge to A won't form a cycle, and you can safely add it to the MST
   - Union the sets of the two vertices to signify that they are now connected through the MST
       - O(n) operation
   - edge source, dest, weight for e in SortE:
       - is source and dest in the same set? if it's in the same then we need to assume that they're in the same cycle
5. Cycle Detection: the findSet operation provides a way to check if two vertices are in the same set. If they are, adding the edge would create a cycle, which is not allowed in the MST
6. Union: When an edge is added to the MST, the union operation merges the sets of the two vertices, showing that they are now connected

Helper Classes:
- 

Complexity Analysis:





