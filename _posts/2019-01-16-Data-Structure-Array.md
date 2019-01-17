---
layout: post
title:  "Data Structure - Array"
author: "JayLee"
---

# Basic of Array
Below is what I learned from following lecture  
[Basic Data Structures: Arrays and Linked Lists][lecture] by Neil Rhodes

## Concept
**Array** is Contiguous area of memory consisting of equal-size elements indexed by contiguous integers.

## What's Special About Arrays
constant-time access  
-> array_addr + elem_size x (i - first_index)

## Two way of arrange array
Q) Assume you have a three-dimensional array laid out in column-major order with the first element at indices (1, 1, 1). What are the indices of the next element in memory?  
A) (2,1,1)  
-> In column-major ordering, the first index changes most rapidly

## Times for Common operations
| | Add | Remove |
|------------| ------------ | -------------|
|Beginning | O(n) | O(n)|
|End | O(1) | O(1)|
|Middle | O(n) | O(n)|

## Summary
- Constant time access to any elements
- Constant time to add/remove at the End
- Linear time to add/remove at an arbitrary location

# Array in Java

# Practice


[lecture]: https://www.coursera.org/lecture/data-structures/arrays-OsBSF
