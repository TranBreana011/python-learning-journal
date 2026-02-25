What I learned this week:

Linked Lists: as a data type

List ADT:
- abstract data type, has yet to be defined, multiple valid ways to implement it
- specific properities:
   - ordered: elements in a list are added in a specific sequence and can be accessed in the same sequence
   - null elements: null elements can be stored as distinct elements in a list (None)
   - duplicate elements: elements are allowed to be duplicates of other elements in a list without being the same element

An array is a contiguous block of data that is segmented into different blocks of the same data type
Python implements a list as a dynamic array, it also has the behavior that it doesn't worry about the data type, allows us to add and remove from the list (can add and remove stuff in the middle where it cannot be done in other languages)

When we have space, it's O(1)

Prepend and Append is ammortized O(1), most of the time it will be O(1)

Linked Lists: constructed using objects, grows and shrinks during run-time, doubly linked list: a variation with pointers in both directions
- objects backbone of such structures
- trees also use objects
- python list: not a linked list, basically a dynamically sized array

Nodes and Linked Lists:
- linked list: simple example of "dynamic data structure", composed of nodes
- each "node" is variable of struct or class type that's dynamically created with new keyword
    - nodes also contain references to other nodes
    - provide "links"
- also applies to memory,
- We need the reference/pointer

Trees: 

