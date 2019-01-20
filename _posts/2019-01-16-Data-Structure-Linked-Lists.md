---
layout: post
title:  "Data Structure - Linked List"
author: "JayLee"
---

# Basic of Linked List
Below is what I learned from following lecture  
[Basic Data Structures: Arrays and Linked Lists][lecture] by Neil Rhodes

## Concept of Single Linked List
**Single Linked List** is a linear collection of data elements, whose order is not given by their physical placement in memory. Instead, each element points to the next.

![image][ll]

### List API
- PushFront(Key)  
  1. create node which contains Key  
  2. update 'next pointer'  
  3. update head  
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
- **PopBack** *with tail*  
  It will takes time although we have tail. because after removing last element and change tail. we don't have any pointer. so we should access from first element to last one.  
  -> O(n)
    
## Concept of Doubly Linked List
**Doubly Linked List** is a linked data structure that consists of a set of sequentially linked records called nodes. Each node contains three fields: two link fields (references to the previous and to the next node in the sequence of nodes) and one data field.

### List API
- **PopBack** *with tail*  
  Unlike Single Linked List, It has prev pointer. So there is no need to access from very first.  
  -> O(1)
- PushBack(Key) *with tail*
  -> O(1)
```
node <- new node
node.key <- key; node.next = nil

if tail = nil:
    head <- tail <- node
    node.prev <- nil
else:
    tail.next <- node
    node.prev <- tail
    tail <- node
```
  
## Summary

# Array in Java

# Practice


[lecture]: https://www.coursera.org/lecture/data-structures/arrays-OsBSF
[ll]: https://cdn-images-1.medium.com/max/1600/1*5uUzPIemQ64oWNCSVfHsgQ.png
