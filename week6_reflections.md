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
- operating systems employ queues for task scheduling and CPU access prioritization
- web servers use queues to handle incoming requests with available resources
- print queues organize the printing order of documents
- queues are integral to algorithm like breadth-first search in graph theory

System of Priority: Priority Queues
