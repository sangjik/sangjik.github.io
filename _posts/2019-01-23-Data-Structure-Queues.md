---
layout: post
title:  "Data Structure - Queues"
author: "JayLee"
---

# Basic of Queues
Below is what I learned from following lecture  
[Basic Data Structures: Arrays and Linked Lists][lecture] by Neil Rhodes

## Concept of Queues
**Queue** is an abstract data type with the following operations
- Enqueue(Key): add key to collection
- Key Dequeue(): removes and returns least recently-added key

![image][FIFO]
First In First Out

## Queue Implemented with Linked List
- Enqueue: use List.PushBack
- Dequeue: use List.TopFront and List.PopFront
- Empty: use List.Empty

## Queue Implemented with Array
- use Circular Array  
-> define read and write index

## Summary
- Queues can be implemented with either a linked list (with tail pointer) or an array
- Each queue operation is O(1): Enqueue, Dequeue, Empty(Array have limited index)

# Queues in Java

# Practice

[FIFO]: http://image14.hanatour.com/uploads/2013/03/0321.jpg
[lecture]: https://www.coursera.org/lecture/data-structures/arrays-OsBSF
