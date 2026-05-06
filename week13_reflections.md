Things I learned this week:
- Dynamic Programming:
- Greedy Algorithms (Greedy Choice)
    - Local Optimums/Minimums:
    - expensive to check every single location possible

Intro to Dynamic Programming:
- DP is a method for solving complex problems by breaking them down into simpler subproblems
- It stores the results of these subproblems to **avoid** computing the same results multiple times
- Dynamic Programming solutions are very useful not just in efficiency, but for allowing us to solve problems that we might not have resources to brute force

DP Key Features:
- Optimal Substructure: A problem is said to have optimal substructure if an optimal solution can be constructed from optimal solutions of its subproblems
- Overlapping Subproblems: A problem is said to have overlapping problems if the same subproblems are solved multiple times
- create a list and save the answer so not more overlapping

Fundamental Concepts:
Memoization vs. Tabulation:
  - Memoization: Top-down approach; solve high-level problems first and store the results for subproblems
  - Tabulation: Bottom-up approach; solve all lower-level subproblems first which are then used to build up solutions to larger problems
Benefits of Dynamic Programming:
  - Reduces time complexity by transforming the problem into a series of decisions
  - Improves efficiency by storing intermediate results and reusing them

Use a list to hold all the calls you've already made with its answers to create a faster fib sequence.

Dynamic Programming vs. Greedy Algorithms:
Greedy Algorithms:
- make local optimal decisions
- do not reconsider choices, faster but less flexible, WE WANT TO BE AS FAST AS POSSIBLE without having to look back
- Can fail to find global optimal solution
Dynamic Programming:
- look at previous decisions to make informed choice about current state
- generally used when greedy fails to get optimal solution
- Often has higher time complexity due to exhaustive search

When to Use Dynamic Programming:
Combinatorics: For example, counting the number of ways to traverse a grid
Probability/Statistics: Such as finding the likelihood of outcomes in a complex scenario
Algebra: Like calculating the nth Fibonacci number or the ways to multiply a chain of matrics
Graphs: For instance, finding the shortest path in a weighted graph with Dijkstra's Algorithm (which uses a greedy approach) or the Floyd-Warshall algorithm(which used DP)

Longest Common Subsequence:
Common Dynamic Programming problem: and not uncommon interview question
Problem: Given two sequences, find length of their longest common subsequence, contiguity is not required but order is
Example: Sequences "DHJRET" and "JDGHTF" have the longest common subsequence of "DHT"

Dynamic Programming Solution:
- Initialize a (n + 1) x (m + 1) matrix where mat[i][j] represents the length of the longest common substring ending at position i-1 in string and j-1 in string 2
    - initialize with 0s
 - Loop through entire matrix starting at 1 in both axis
     - if sequence 1 at i - 1 and sequence 2 at j-1 match, set mat[i][j] = mat[i-1][j-1] + 1
     - else, set mat[i][j] = max(mat[i-1][j], mat[i][j-1])
- Final longest substring length in mat[n][m]

Implementation: DIVIDE AND CONQUER
