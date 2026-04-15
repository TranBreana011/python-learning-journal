Things I learned this week:
The Basis of Sets:
- Graphs are an ADT that is pivotal in comp. sci and are widely used in various fields
- A graph is essentially a collection of nodes (also referred to as vertices) and the connections between them, called edges
- The Vertices and edges define the graph, both in code and visually

Graphs are useful because they can represent any abstract concept
- one of the biggest things that define graphs are their edges

Restrictions in LL and Trees:
- each node can only have one child/preceeded by one other thing
- no branching
- no loops
- The problem of having no limitation is:
    - entirely possibly to get stuck in an infinite loop
- Therefore, we need extra memory
    - to go in and track where we visisted
 
Types of Graphs:
- Graph type is mostly focused on the nature of the graph's edges
- The edges control how the data relates to one another, showcases the relationship
- Nodes store the graph's data, by their nature need to be vaguely defined in ADT
- Edges define how different bits of information relate to one another and changes in those rules can produce very different results
- These rules differentiate graphs from linked lists, trees, etc.

Undirected vs. Directed:
- Edges are Bi-Directional (Undirected)
- Edges are Uni-Directional (Directed) (when a graph has arrows or directions)

Weighted vs. Unweighted:
- Edges have some 'cost' value associated with them (weighted graph)
    - 'cost' = pos/neg
    - dist/time are common ways of treating edges but not the only ways
    - not so simple to say positive or negative
- Each edge is equal in weight (unweighted graph)
    - js because it's unweighted doesn't mean we can't calculate some sort of distance
    - if every edge doesn't have a weight, then the only thing we can base the edges on are the # of edges traveled/traversed
    - weighted by # of edges traversed if no other weight
    - if every edge is equal in weight, we can simplify every edge to one and if we do then it will then be calculated as every edge we traversed

For the RAM, we will need a reference, some address 
- our edge is typically a reference to something else
- now we need to have a weight associated with it

Cyclic vs. Acyclic (Loops)
- There is one path from a vertex to itself
    - that doesn't use same edge twice
- No cycles exist
- Cyclic (directed) graph
- Acylic (directed) graph
- doesn't particularly affect memory

Simple vs. Non-Simple
- no vertex has an edge to itself, no multiple edges between vertices (simple)
    - abstraction
    - if detailed enough, can become useful
- loops allowed, multiple edges allowed (non-simple)
- 

Choosing the right kind of graph can have extremely important effects
- the fundamentals

Graph Representation
- Graphs can be represented (implemented) in a computer's memory in mainly two ways:
    - Adjacency lists
    - Adjacency matrices
- Which implementation you should use depends on your particular use case for the graph

Adjacency Lists
- An adjacency list is a collection of lists or arrays that represent which vertices are adjacent to which other vertices. Here's how it works
- Structure:For each vertex in the graph, we store a list of all the vertices that are connected to it by an edge. This can be done using an array, a linked list, a mpa, or any other collection type

Adjacency Pros and Cons:
Advantages:
- it's space efficient for sparse graphs (graphs with fewer edges)
- it allows for efficient iteration over the edges adjacent to any given vertex
Disadvantages:
- checking for the presence of a specific edge can be slower than with an adjacency matrix, as it may require a linear search through the list
- it can be less efficient for dense graphs (graphs with many edges)

