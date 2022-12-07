# Hashtables
  - Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array
  - Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
  - Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

Why do we use them?
  - Hold unique values
  - Dictionary
  - Library

## Hashing
  - Basically, a hash code turns a key into an integer. It’s very important that hash codes are deterministic: their output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.
 
## Creating a Hash
  - Here is a simplistic hashing algorithm:
  1. Add or multiply all the ASCII values together.
  2. Multiply it by a prime number such as 599.
  3. Use modulo to get the remainder of the result, when divided by the total size of the array.
  4. Insert into the array at that index.


## Methods
  - hash()
     - The hash() method will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.
  - keys()
     - The keys() method returns a collection (array) of unique hash keys.

  - has() 
     - The has() method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the hash() method and check the hashtable if the key exists in the table given the index returned.

  - get()
     - The get() method takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

  - set()
      - send the key to the hash() method.
      - Once you determine the index of where it should be placed, go to that index
      - Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
      - If something does exist, add the new key/value pair to the data structure within that bucket.

