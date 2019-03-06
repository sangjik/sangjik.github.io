---
layout: post
title:  "Priority Queues"
author: "JayLee"
---

# Priority Queues
Below is what I learned from following lecture  
[Basic Data Structures][lecture] by Neil Rhodes

## Introduction
A queue is an abstract data type supporting the following main operations
- PushBack(e) adds an element to the back of the queue
- PushFront() extracts an element from the front of the queue

A priority queue is a generalization of a queue where each element is assigned a priority and elements come out in order by priority

## Additional operations
- Remove
- GetMax
- ChangePriority..

## Algorithms that use Priority Queues
- Dijsktra's algorithm
- Prim's algorithm
- Huffman's algorithm
- Heap sort

## Summary
Unsorted array/list or Sorted array/list will takes either O(1) or O(n) to operate insert and extract max.  
Binary heap is recommended data structure as all operation will become O(log n)

[lecture]: https://www.coursera.org/lecture/data-structures/arrays-OsBSF
