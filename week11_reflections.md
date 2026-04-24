Final Project Proposal:
Work on Visualization Poster thing,
Have a cylic graph of some sort, and two other **distinct** data structures
- A Queue and a BST are distinct
- Separate chaining hash table 
    - that uses linked lists to resolve are NOT Distinct
- LL Queue isnt distinct
- We are going to be using a google slide to create a presentation/poster on it; canva, anything else just make a poster
- Just have like one slide just like a poster
- assigning last lab
- DO DEMOS ASAP
- 4/22 - DEMO LAB 8/9
- 4/24 - DEMO LAB 11

Lab 13:
use a graph to represent the transit system of a city
going in to try to say what's the shortest path from one landmark to another
mini project: needs to include two distinct data structures besides graph
going to adapating graph theory for transportation
use graph theory to model a simplified a transit network of a fictional city
use the traversal algorithms 
it's a directed graph!!!!!!!!!!!!!
implement a method of BFS and DFS that keeps tracks of landmarks we've visited
edges are the 15 roads
analyze the length of time and how which scenario might be preferred over another....?


Final:
can just add upon midterm project: just add a graph and two other distinct data structues(I think)

Things I learned:
Adjacency Matrix: O(1) access to a specific edge
Adjacency List: No space spent on edges that don't exist

Graph Traversal:
- We need to make use of some implicit data strucutre in order to get out of a graph loop

Graph Traversal Problem:
- Traveling through graphs is inherently more complicated

Breadth-First Search:
- BFS is a fundamental graph traversal algorithm that explores the vertices of graph in layers, starting from a selected source vertex
- It visits all neighbors of the starting vertex, then all their unvisited neighbors, and so on, ensuring that it visits vertices in order of their distance from the starting point, hence the "breadth-first"
- NO Root
- Therefore, we can choose anything as our starting location: we go in a grpah and tackle things in layers
    - layer 0 - starting node
    - layer 1 - whatever is adjacent to layer 0
    - layer 2 - anything that is adjacent to layer 1
    - layer 3 - so on and so forth
This ensures that the vertices are visited from the started point, 4 edges =  4 layers
- guaranteed to find a solution only if a solution exists

Properties of BFS:
- Completeness: BFS is guaranteed to find a solution if one exists
- Optimality: When all edges weights are equal, BFS finds the shortest path to all vertices
    - if each edge is weighted then, the computer doesn't know how to take that into account
- Time Complexity: The time complexity is O(V + E), where V is the number of vertices and E is the number of edges
- Best use for unweighted graphs
- The type of graph we are working with, affects how BFS would perform
- Only really matters in directed or undirected graphs..(something sink)
  - only worry is that it will get stuck in a sink

BFS Data Strucutres:
- In order to conduct search on any graph and avoid infinite cycle loops, we must rely on additional data structures to keep track of what elements we've visited and what elemnts we must visist next
- Boolean array keeps track of visited vertices in both list and matrix representation, true means visited
  - O(1) ~ O(n)
    - depending on how we implement it
- We could use a set
    - adding and removing would be O(1)
    - for dups, we can use memory address (Key ID)
        - memory address is more efficient
- Queue is used to determine which nodes get visited next

BFS Psuedocode:
1. Start by creating an empty set and Queue of vertices to visit, putting the source vertex in the queue and setting it as visited in the array
2. While the Queue is not empty:
   1. Take the front item of the queue and print it
   2. Add all of it **unvisited** adjacent vertices to the back of the queue while also makring them       as visited to avoid adding them again

Depth-First Search:
- DFS is another fundamental algorithm for transversing or searching through a graph
- It explores as far as possible along each branch before backtracking
- This means that in a DFS,
- Uses a callstack, ultimately a stack!

DFS Properties:
- Completeness: DFS will find a solution if one exists, but it may not be the shortest path
- Space Complexity: Since it traverses along a path

- requires less space in the stack
- 

DFS Data Structures:
- Again, much like BFS we need to rely on another data structure

DFS Psuedocode:
1. Create new stack and Boolean array, start at source vertex and add it to stack
2. While the stack is not empty:
     1. Pop a node from the stack to use
     2. If that node has not been visited, mark it as being visited, and print the node
     3. For all non-visited adjacent nodes to the current node, push them onto the stack
  
Weighted Graphs
- a weighted graph is a graph in which each edge is assigned a numerical value or weight
- these weights can represent quantities such as cost, length, or capacity, depending on the context of the problem being represented by the graph
- eadges represented as (u, v, w) triplets
    - u and v represent vertices, w represents weight
 
Applications of Weighted Graphs:
- network routing: in computer networks, weights can represent bandwidth, latency, or other routing metrics
- road maps: in geographic informartion systems (GIS), weights may represent the length of the road, traffic conditions, or travel time
- scheduling: in project management, a weighted graph could repersent tasks to be performed, with weights representing tiime duration or resource usage

Weighted Graph Challenges:
- Working with weighted graphs introduces complexity not present in unweighted graphs
- For example, finding the shortest path is not as straightforward as counting the number edges
- Additionally, negative weights can create scenairos where more complex algorithms are needed

Reward Hacking:
- just algorithmic math, finding the highest reward value
- abuses the algo

Greedy Algorithms:
- a method for solving problems by making a sequence of choices based on **limited information** with the hope it will be optimal
- At each decision point, the algorithm chooses the option that is most beneifical at the moment
- Does not generally guarantee a globally optimal(the best option) solution
    - called globally optimal to be distinguished from local optimal(the best option in our current situation)

Gradient Descent:
- an iterative optimization algorithm used in machine learning to minimize a cost function by updating model parameters (weights and bias) in the opposite direction of the gradient

Example:
- Basic Concept:
    - consider jobs that need to be completed by certain deadlines with given profits
        - goal: Maxmize total profit of completed jobs
- Algorithmic Steps:
  1. selection criterion: choose the job with the highest profit available at the moment
  2. Feasibility Check: Check if this job can be completed before its deadline
  3. Solution Construction: If feasible, include the job in the final solution
  4. Iterative Process: Repeat until no further jobs can bed added without violating the deadline constraint

Greedy Choice:
- the basis of Greedy Algorithms is greedy choice
- in the absence of any further information, picking the local opitmal solution is more likely to lead to a global optimal outcome than any other selection
- Heuristic-based(rule of thumb), we can't speculate about future gains all we know is the gains we're making at the moment

NP hard is when an efficient solution doesn't exist, the optimal solution requires to check/go through every single case

Dijkstra's Algorithm
What is DA?
- Dijkstra's algorithm is a classic algorithm for finding the shortest path from a single source vertex to all other vertices
- only works in weight graph, with non-negative edges
- It was conceived by computer scientist Edsger W. Dijkstra in 1956 and published three years later

Dijkstra's Algorithm Psuedocode
1. Initialization: start by setting the shortest distance to the source vertex as 0 and to all other vertices as infinity. Set the source as the current vertex
2. Relaxation: For the current vertex, consider all of its unvisited neighbors and calculate the tenative distances through the current vertex. Compare the newlt calculated tenative disance to the current assigned value and assign the smaller one
3. Updating: Once we have considered all unvisited neighbors of the current vertex, mark the current vertex as visited. A visited vertex will not be checked again
4. Selection (Greedy choice): select the unvisited vertex with the smallest tenative distance set during the relaxation process, and set it as the new "current vertex"
5. Termination: Repeat steps 2 through 4 until all vertices have been visited

- if you already visit a vertex, you never visit their direction again
