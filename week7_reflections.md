Things I learned this week:

Hash Tables are dictionaries:
- A data structure that maps keys to values
- providse fast access to data using a key
- operates in constant time, O(1), on average for insertions, lookuos, and deletions
- just arrays with lists renamed
- hashing is going in and convert any data type into an **int value**

Application of Hash Tables:
- databases: store and retrieve data using unique identifiers
- caching: quick access to pre-computed results
- symbol tables: store variable names and values in compilers/interpreters

Dictionaries: 
- have a key and value that are linked together
- two parts: one pair is the key, the other pair is the value
- dict[key] will output its paired value

looping through in order won't be as easy as it looks, can't just set up a for loop 

you are allowed to have the same values in a dictionary but not the same keys
- not allowed to have duplicate keys is the same reason why we cannot have duplicate indices
- the keys are renamed indices!!!!!!!!!!!!!!!!!!

Hashing
- what is hashing?
    - converts a key into a hash code(a number)
    - a hash function generates the hash code from the key
    - the hash code is used as an index in the underlying array where values are stored
- Properities of a Good Hash Function:
    - Deterministic: The same key always produces the same hash
    - Uniform Distribution: Hashes should be evenly spread across the array
    - Efficient: Should be quick to compute, want it to be O(1)
 
Turning an object into an integer so we can turn that INT into an array location
key (any DT) --> hash code --> index

Hash Table ADT
Key Component:
- array: used to store data (often called "buckets")
- hash function: maps keys to indices in the array
- collision resolution: deals with cases where multiple keys map to the same index
    - we will be looking for ways to resolve these collisions
 
Hash Table Operations, for all of these we want them to be o(1) 
- Insertion: Put
    - apply the hash function to the key
    - use the hash code as an index to store the value in the array
- Lookup: Get
    - apply the hash function to the key
    - use the hash code to access the value at the corresponding index
- Deletion: Pop/Remove

- we want the hash number to be so large because the possible of string....makes collision more mathematically improbable
- hashes can be negative numbers, it wants to esssentially just hash everything

Collision Resolution:
- Two major resolution Techniques:
    - Chaining: store multiple key-value pairs at the same index in a linked list or another structure
        - the insertion will become long and it will become o(n) and it will eventually become a linkedlist, the lookup will become slow
    - Open Addressing: probe to find another open spot in the array
        - python dict approach, go find space somewhere else
Linear Probing: just continously checking the next location to see if there's space; linearly traversing through the list, iterating down the list looking for a solution
  - if there is space in the front but we are towards the back, we can use % len(arr) to wrap around to the front to check for space again

Open Addressing Basics:
- open addressing is a collision resolution tehcnique in hash tables where all elements are stored in the array itself
- when a collision occurs, we keep probing to different slots according to a sequence until an empty slot is found
- need two different types of empty values:
    - Null - never been used before
    - Deleted - element previously existed here
    - if we reach null then we know that whatever we are looking for never existed
 
Clustering: where a bunch of similar values wind up colliding in a particular location, creating further risk of collisions
Clustering is a sign of a bad hash function or a bad collision resolution method

Step 1: remove (ant)
Step 2: get (ape)
