---
layout: post
title:  "Data Structure - Linked List"
author: "JayLee"
---

# Basic of Linked List
Below is what I learned from following lecture  
[Basic Data Structures: Arrays and Linked Lists][lecture] by Neil Rhodes

## Concept
**Linked List** is a linear collection of data elements, whose order is not given by their physical placement in memory. Instead, each element points to the next.

![image][ll]

## List API
- PushFront(Key)  
  1. create node which contains Key  
  2. update 'next pointer'  
  3. update head  
  -> O(1)
- PopFront
  1. update head to second elements
  2. removing first elements  
  -> O(1)
- PopBack() *no tail*
  1. find last element   
  -> because we don't know position of last element, we should access from first element to last one  
  -> O(n)  
  2. Add element and change pointer of 'last-1' element  
- PushBack(Key) *with tail*
  1. Add element to last and change current tail's pointer
  2. Update tail to last one  
  -> O(1)
- PopBack *with tail*  
  It will takes time although we have tail. because after removing last element and change tail. we don't have any pointer. so we should access from first element to last one.  
  -> O(n)

## Summary

# Array in Java

# Practice


[lecture]: https://www.coursera.org/lecture/data-structures/arrays-OsBSF
[ll]: https://cdn-images-1.medium.com/max/1600/1*5uUzPIemQ64oWNCSVfHsgQ.png
