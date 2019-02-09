---
layout: post
title:  "Data Structure - Stack"
author: "JayLee"
---

# Basic of Stack
Below is what I learned from following lecture  
[Basic Data Structures: Arrays and Linked Lists][lecture] by Neil Rhodes

## Concept of Stack
**Stack** is an abstract data type that serves as a collection of elements, with two principal operations:

- push: which adds an element to the collection
- pop: which removes the most recently added element that was not yet removed.

![image][LIFO]
Last In First Out

## Solving Balanced Brackets using Stack
```
Stack stack
for char in str:
  if char in ['(', '[']:
    stack.Push(char)
  else:
    if stack.Empty(); return False
    top <- stack.Pop()
    if (top = '[' and char != ']') or (top = '(' and char != ')'):
    return False
return stack.Empty()
```

## Problem of Stack implemented by Array
- possibility of wasting memory
- memory will limited after define  
-> can resolved by using Linked List

## Summary
- Each stack operation is O(1): Push, Pop, Top, Empty
- Stacks are occasionally known as LIFO queues

[LIFO]: https://images.agoramedia.com/everydayhealth/gcms/The-Health-Benefits-of-Water-722x406.jpg?width=722
[lecture]: https://www.coursera.org/lecture/data-structures/arrays-OsBSF
