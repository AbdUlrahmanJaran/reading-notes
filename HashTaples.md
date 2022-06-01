# Hash Taples
Hashtables are a data structure that utilize key value pairs. This means every ``Node`` or ``Bucket`` has both a key, and a value.

The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a ``hash``. A ``hash`` is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an `O(1)` time complexity. This is ideal when quick lookups are required.

## Terminology:
**Hash** - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
**Buckets** - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
**Collisions** - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

### Used For
- Hold unique values
- Dictionary
- Library

### Internal Methods
1. ``Add()``

2. ``Find()``

3. ``Contains()``

4. ``GetHash()``

### Collision resolution techniques
#### 1. Separate chaining (open hashing)
Separate chaining is one of the most commonly used collision resolution techniques. It is usually implemented using linked lists. In separate chaining, each element of the hash table is a linked list. To store an element in the hash table you must insert it into a specific linked list.

#### 2. Linear probing (open addressing or closed hashing)
In open addressing, instead of in linked lists, all entry records are stored in the array itself. When a new entry has to be inserted, the hash index of the hashed value is computed and then the array is examined (starting with the hashed index).

#### 3. Quadratic Probing
Quadratic probing is similar to linear probing and the only difference is the interval between successive probes or entry slots. Here, when the slot at a hashed index for an entry record is already occupied, you must start traversing until you find an unoccupied slot. The interval between slots is computed by adding the successive value of an arbitrary polynomial in the original hashed index.

#### 4. Double hashing
Double hashing is similar to linear probing and the only difference is the interval between successive probes. Here, the interval between probes is computed by using two hash functions.

### Applications
1. Associative arrays
2. Database indexing
3. Caches
4. Sets
5. Transposition table

#### Ref: [Terminology](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html), [Collision resolution techniques](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/) and [Applications](https://en.wikipedia.org/wiki/Hash_table).