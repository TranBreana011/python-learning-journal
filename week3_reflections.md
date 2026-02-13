Week 3:

Algorithm Runtime Complexity:

1. Space/Storage, space can grow exponentially

2. Time

3. Cost (API)

Constant Time Operations O(1)
- math, = (assignment), comparison, [] = index for arrays
- python doesn't have fixed size intgers

  Growth of Functions and Complexity
  - as the size of input data increases, the behavior of algorithms change

Upper bound = worst case scenario
Lower bound = best case scenario

Murphy's Law - We care more about upper bounds/worst case scenarios because there's nothing to fix about best case scenarios

Upper bounds may take more time and space

Big O Notation
- provides a standardized way to describe the upper bound/worst case runtime complexity of an algorithm

Our goal is to see how functions will scale with size, allowing us to analyze algorithms independent of the hardware or implementation

Big O Time Complexitiy: 

O(1) (KING) - Constant Time Complexity: The algorithm's run 
- Addition is considered O(1) only if the data types are fixed sizes
- Always try to use it

O(n) - Linear
- It's fine but approaches danger with bigger data sets, look for alternatives if any
- gets more expensive

O(log n) - Logrithamic 
- Is the most efficient, even more time saving with each input
- The time saving gets bigger and bigger
- As n increases, the savings of time increases

Linear Search = O(n)
Binary Search = O(log n)

Order of use:
1. First try O(1)
2. Second try O(log n)
3. Third try O(n)
4. Fourth try O(n^2)

O(n^2) 
for i in range(ourN):              <--- n
  for j in range(ourN):            <--- n 
    print (i * j, " ")
  print ()

O(n log n) - Linearithmic Time Complexity: OFten seen in efficient sorting algorithms like Merge Sort and Quick Sort, these algorithms exhibity intermediate growth rates between linear and logarithmic 

O(n^2), O(n^3),... - Polynomial Time Complexity: common in algorithms with nested loops. INEFFICIENT for large data sets

O(2^n), O(n!) - Exponential and Factorial Time Complexity: becomes impractical for all but the smallest inputs. Recursive algorithms with poor base cases may fall into this category

Depending on what we value, we might want to use a worse time complexity aglorithm than a faster one, because less cost. Make sure to check all efficiency types!!!!!!!

Simplification in Big O
- Big O notation simplifies to dominate term, often discarding constants and lower order terms
- Is done because as input size grows, they become negligible compared to dominate term

Sorting Algorithms














