---
layout: post
title:  "Dynamic Arrays"
author: "JayLee"
---

# Dynamic Arrays and Amortized Analysis
Below is what I learned from following lecture  
[Basic Data Structures][lecture] by Neil Rhodes

## Idea
How we know max size when allocating an array  
-> store a pointer to a dynamically allocated array, and replace it with a newly-allocated array as needed

## Definition of dynamic array
Abstract data type with the following operations(at a minimum)
- Get(i)
```
if i<0 or i >= size:
  ERROR: index out of range
return arr[i]
```
- Set(i, val)
```
if i<0 or i >= size:
  ERROR: index out of range
arr[i] = val
```
- PushBack
```
if size = capcity:
  allocate new_arr[2*capacity]
  for i from 0 to size-1:
    new_arr[i] <- arr[i]
  free arr
  arr <- new_arr; capcity <- 2*capacity
arr[size] <- val
size <- size+1
```
- Remove(i)
```
if i<0 or i>=size:
  ERROR: index out of range
for j from i to size-2:
  arr[j] <- arr[j+1]
size <- size-1
```
- Size()

### Common implementations
- C++: vector
- Java: ArrayList
- Python: list

## Summary
- Unlike static arrays, dynamic arrays can be resized
- Appending a new element to a dynamic array is often constant tiem, but can take O(n)
- Some space is wasted

[lecture]: https://www.coursera.org/lecture/data-structures/arrays-OsBSF
