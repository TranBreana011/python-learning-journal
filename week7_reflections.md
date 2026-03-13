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

Hash Collision: when two items want to be in the same location

Collision Resolution:
- Two major resolution Techniques:
    - Chaining: store multiple key-value pairs at the same index in a linked list or another structure
        - the insertion will become long and it will become o(n) and it will eventually become a linkedlist, the lookup will become slow
    - Open Addressing: probe to find another open spot in the array
        - python dict approach, go find space somewhere else
Linear Probing: just continously checking the next location to see if there's space; linearly traversing through the list, iterating down the list looking for a solution
  - can't stop looking until we find what we are looking for
  - if there is space in the front but we are towards the back, we can use % len(arr) to wrap around to the front to check for space again

Open Addressing Basics:
- open addressing is a collision resolution tehcnique in hash tables where all elements are stored in the array itself
- when a collision occurs, we keep probing to different slots according to a sequence until an empty slot is found
- need two different types of empty values:
    - None - never been used before ever!
    - Deleted - element previously existed here
        - if entry.deleted == True: then that means that there was something here but now isn't
    - if we reach null then we know that whatever we are looking for never existed
    - we need two empty systems because we want to keep O(1)
 
Clustering: where a bunch of similar values wind up colliding in a particular location, creating further risk of collisions
Clustering is a sign of a bad hash function or a bad collision resolution method

Step 1: remove (ant)
Step 2: get (ape)

Lookup and Deletion: 

operation to search and remove will always be closely related
remove is always going to be a little more or a lot more complicated than search

Other probing methods:
Quadratic Probing:
Quadratic Function: still a type of open address, on collision quadratic probing searches for the next available slot using a quadratic function of the form:
Probe(i) = (h(k) + cl * i + c2 * i^2)% m
i = probe number
h(k) = original hash value (start index)
c1 & c2 = auxillary constants (assume 1), basically can remove them
m = table size
- going to wind up jumping
- very first probe = 0
-quadratic probing works better with larger tables
- can still get clusters in quadratic probing but will only happen if they are literal hash space collisions

Double Hashing
- similar set up to Quadratic probe formula, but now based on second hash function
- h(k, i) = (h1(k) + i x h2(k)) % m
h1(k) = original hash value
h2(k) = second hash value
i = probe number
m = table size
- biggest problem with double hashing is that we need to find another hash function

Clusters are going to become a problem the greater the load factor
Consider Load Factor (LF), size /capacity
- the number of items in the hash table divided by the number of buckets
- the closer your array is to getting full, the less efficient your function will be

Open Addressing Pros and Cons:
- Benefits: Memory Efficiency, Cache Efficiency
- Challenges: Load Factor, Complex Deletion, Clustering
    - Load Factor: Performance degrades as the load factor increases. a load factor below 0.7 is usually desirable
    - when ABOVE 0.7, in order to make our hash table more efficient again, we should resize!!!!!!!! simply make the capacity bigger
 
Resize operation = O(n)

In chaining:
Separate Chaining
- we have buckets, continue growing
- we don't have to worry about probing
- we will only get collisions if they hash to the same thing
- but,,, it's entirely possible that everything is clustered into the same spots
    - still have to worry about the load factor
- make sure to pick a good hash space in order to avoid any collisions


