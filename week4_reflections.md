What I learned this week:

Ordering Data:
- Selection Sort: has two parts of the list, unsorted and sorted; scan the unsorted portion for the smallest item and swap into the first element of unsorted, growing that part of the list
- Insertion Sort: Maintains unsorted and sorted parts of the list; rather than scanning unsorted section for the smallest and shuffling it forward,

Insertion Sort for sorting cards: for every pos in arr (after first) take pos and while the previous position is larger than post and we are not at the end== swap position back by one
- O(n) is the best 

Fast Sorting Algorithms: In order to efficiently sort large amount of data, we must do better than O(n^2). How to efficiently tackle a big task? DIVIDE AND CONQUER

Quick Sort: A sorting algorithm that repeatedly partitions the input into low and high parts (each part unsorted), and then recursively sorts each of those parts

Pivot - is chosen to divide data into parts lower than it or higher than it
- can be any value, typically middle or last element
- typically be the middle item

Eventually, all elements of the array have been divided into ordered parts

In-Place Quick Sort:
In-Place: Algorithms that do not require us to allocate memory for additional data structures
Can't Create new arrays/no loops through the list

Partition Psuedocode:
- Make last element pivot, and index boundaries
- Keep Track of divide point 'i', start one below low bound
- Loop through from low to high bounds
  -- if current element is less or equal to pivot, increment i and swap arr[i] with arr[curr]
  -- at end of loop i will be in pivot's spot, swap it into place
  -- return pivot location so it can be excluded in recursive calls
- average case: linearithmic O(n log n) because you pick the middle 
- worst case: quadratic O(n^2) because you only go through one at a time

Merge Sort: Split an array in two until you are down to one element arrays, then merge them back up one pair at a time in sorted order
- always split down the middle
- guarantees the most effective divide and conquer but we are going to need extra memory space, space complexity is a problem
1. Split
2. Sort
- it's more efficient
- weaves back in place one at a time
- 
