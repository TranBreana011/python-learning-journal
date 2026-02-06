Things I learned this week:

Polymorphism: many forms
function: isintance 
compile time polymorphism obviously python cannot do because it's an intrepreted language

Recursion:
A function that calls itself

Python allows recursion as it can be useful but it also has its own limitations

Used to break down complex probelms and turned into simple subproblems, making solving problems easier

Helps us by forcing us to understand the call stack: a data structure in a computer that mangaes what our computers are able to do. 

Increases **Efficiency**

Any recursive program can be changed to an iterative program

def F1():
  print ("n")
  F1

Iterative Approachs = loops

Recurisve Approach
--> f() --> f()

Void Functions: Divide and Conquer, breaking a problem up into sub problems within itself
- basic design technique, break large task into subtasks

There are two phases: 1. Base Case (The case that would cause it to stop doing the recusion, when the problem is trivial enough to be solved (recusion ends)) 2. Recursive Case (When you break the problem into a smaller version of itself (calls recursion)) 

Stack Overflows:

It's a specific type of error, it occurs when the call stack exceeds its capacity

common pitfall with recursive functions: if they don't have a proper base case or if the base case isn't reached soon enough

the number (and size) of parameters and local variables results in a larger stack frame

To prevent stack overflow:

Ensire a proper base case: always make sure the recursive function has a base case that it will eventually reach

Limit Recursion Depth

Optimization Technique: python doesn't have this because it's interpreted
