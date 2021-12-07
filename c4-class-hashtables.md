# Hashtables

## Introduction

A hashtable is a data structure used to store data as key/value pairs.

A hashtable is traditionally created from an array. Each Index of the array is known as a **bucket**; since it can store multiple key/value pairs.

The hashtable uses a **hashing algorithm** that encodes the key to map the value to a specific bucket in the array. In other words, the hash generates the index of the array's bucket in which the value is stored.

![a hashtable](https://miro.medium.com/max/1400/1*tg9ZzmS4SGh8bgmZ3ow2Zg.png)

## Hashing

Basically, a hash code turns a key into an integer. Hash codes:

1. should be deterministic: the output is determined only by the input.
2. the same key should always produce the same output (index).

Each bucket in the array is expected to hold one key/value pair combination. When there is no entry in a specific bucket, it will start null. The hash table starts each bucket empty and overwrites the value once a key generates a hashCode that corresponds with an index. However, the hash map needs to be able to handle two keys resolving to the same index.

## Collisions

A collision occurs when two or more keys hash to the same index in the array. Collisions can be solved in many ways, on of them is chaining the values in the bucket. This can be achieved by changing the initial state of the buckets. Instead of starting them all as null we can initialize a LinkedList in each one. Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list.

![hashtable collision](https://javascriptonthego.files.wordpress.com/2017/04/hashtable1.png?w=640)

Note: Collisions can be avoided using efficient hashCodes. A "perfect hash” will never have any collisions.

## Internal Methods

### Creating the hash -> GetHash()

The `GetHash()` method:

1. accepts a key as a string
2. conducts the hash
3. returns the index of the array where the key/value should be placed

### Storing Values -> Add()

Hash maps use an `Add()` method to add a new key/value pair to a hashtable. The `Add()` method does the following:

1. accepts a key
2. sends the key to the `GetHash()` method to calculate the hash of the key
3. once the hash/index is determined, it goes to that index to check the bucket:
    * if the bucket is empty, add the key/value pair
    * if the bucket is not empty, add the new key/value pair to the data structure within that bucket; usually its a linked list

### Reading Values

Hash maps do this to read value:

1. accept a key
2. calculate the hash of the key
3. use modulus to convert the hash into an array index
4. use the array index to access the short LinkedList representing a bucket
5. search through the bucket looking for a node with a key/value pair that matches the key you were given

### Finding a value -> Find()

The `Find()` method:

1. accepts a key
2. sends the key to the `GetHash()` method to determine the hash of the key
3. once at the index location is found in the array, it iterate through the bucket and see if the key exists and return the value

#### Reading Performance

Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity. This is ideal when quick lookups are required.

### check if a key exists in a hashtable or not -> Contains()

The `Contains()` method:

1. accepts a key
2. sends the key to the `GetHash()` method to determine the hash of the key
3. it checks if that hash exists inside the array and returns a boolean of the result
