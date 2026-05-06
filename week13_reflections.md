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
