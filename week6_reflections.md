Things I learned this week:

Stacks and Queues:

Stacks: List ADT(abstract data type) + one more requirement, a list but can only access in a certain way either from array or from linked lists
- Stack Data strcuture: retrieves data in reverse order of how stored, LIFO - Last-in/First-out, Think of like "hole in ground"
- Used for many tasks: track function calls, memory management
- Our Use: use linked lists to implement stacks

Call Stack: keeps track of what functions were called and what order; used to recall every single function = add from the top and remove from the top going down, used to keep track of where we are and where we go next

Stacks can be used in other areas as well 

To add to a stack: Pushing
To remove from a stack and return the value: Popping

Back Stack: 
Foward Stack:

IsEmpty(): returns true if stack has no elements in it and false otherwise
Peek(): returns the top element without removing it from list as in Pop() - return without removing 

Efficiency Comparison
push() = O(1) amortized for ARRAYSTACK, 

Space Efficiency:
O(M) because we have to copy the entire array if we have more elements than the space already allocated. Essentially wasting space.

Overhead: when LLS
Generally speaking, LLS are more efficiency and we care more about runtime efficiency than space efficiency. Space is cheap (Moore's law) it increases exponentially anyway and time is money. PRIORITIZE TIME NOT SPACE.

Queues: List ADT + one more requirement
- Another common data strcuture: handles data in first-in/first-out manner (FIFO)/first come first serve, items inserted to the end of list, items removed from front
- Representation of typical "line" forming : like bank teller lines, movie theatre lines, etc.

Queue Operations: 
Push: Enqueue(queue, x)
Pop: Dequeue(queue)

For LinkedLists:
- the tail must be the enqueue location
- the head must be the dequeue location

For doubly linked lists:
- it doesn't matter

Queue Applications:
- in computer networks, queues manage packet sequencing between devices
- **operating systems** employ queues for task scheduling and CPU access prioritization
- web servers use queues to handle incoming requests with available resources
- print queues organize the printing order of documents
- queues are integral to algorithm like breadth-first search in graph theory

System of Priority: Priority Queues

Why not treat everything equally?
- importance
    - pre-requisite, time-sensitive, cost/reward, resources

Optimization Processes: 
- continuous processes, go in and execute processes every second

Priority Queues:
- self.priority = priority

- two systems: low and high priority
- if one is low, everything else is high, vice versa
- it's like flipping a greater than or less than symbol

Priority Queue Operations:
- enqeueue(data, priority) - O(n)
- dequeue() - removes data at the top of the list and return it - O(1)
- peek() - removes data at the top of the list and does not return it - O(1)


Tree: A data structure, similar to a linked list, every item can be followed by more than onee item(many branches)
- the top of the tree == root aka the max value or the largest number
- traversals 

Binary Tree: 
- is ordered
- can have null values but still need to have multiple bracnhes and every item can be followed by at most 2 other items
- 

List: ordered, null values, duplicates, every item can be followed by at most 1 other item (no branches)

Heaps are natural Priority Queues
O(log n) when we have to replace the root
Peek stays O(1)

A Max Heap is a tree based on a binary tree where it has a max of two branches: 
- head == parent
- the branches == children
- every parent is >= children
- In the worst case scenario, it would be O(log n)

A Min Heap is flipping the sign so:
- every parents <= children

Binary Search: O(log n)
- every level you go through, you go through twice as much

Representing Heaps with Arrays:
- complete trees are difficult to insert into
- so, represent Heaps as an array insantly
- can jump from child to child
- can traverse forward and backward
- or integer division
- makes it very easy to swap indicies
- import heapq: now have access to a python library of heaps and with that we can do things like heapify to pass things into, to print things in sorted order (not everytime), heappop, heappeek
- 
