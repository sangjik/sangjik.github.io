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

- AddBefore(node, key) *with tail*
  -> O(1)
  
```
node2 <- new node
node2.key <- key
node2.next <- node
node2.prev <- node.prev

node.prev <- node2
if node2.prev != nil:
    node2.prev.next <- node2
if head = node:
    head <- node2
```

## Single Linked List vs Double Linked List
|                      | no tail | no tail | with tail |
|----------------------|---------|---------|-----------|
|                      | Single  | Double  |           |
| PushFront(Key)       | O(1)    | -       |           |
| TopFront()           | O(1)    | -       |           |
| PopFront()           | O(1)    | -       |           |
| PushBack(Key)        | O(n)    | -       | O(1)      |
| TopBack()            | O(n)    | -       | O(1)      |
| PopBack()            | O(n)    | O(1)    |           |
| Find(Key)            | O(n)    | -       |           |
| Erase(Key)           | O(n)    | -       |           |
| Empty()              | O(1)    | -       |           |
| AddBefore(Node, Key) | O(n)    | O(1)    |           |
| AddAfter(Node, Key)  | O(1)    |         |           |

## Summary
- Contant time to insert at or remove fron the front  
If you handle first element, Linked List is better than array, because in case of array If we remove first element, we should change all element's position
- With tail and Doubly Linked, constant time to insert at or remove from the back
- **O(n)** time to find arbitrary element
- List elements need not be contiguous  
Separated allocated locations of memory
- With Doubly Linked List, constatnt time to insert between nodes or remove a node

# Linked List in Java

# Practice


[lecture]: https://www.coursera.org/lecture/data-structures/arrays-OsBSF
[ll]: https://cdn-images-1.medium.com/max/1600/1*5uUzPIemQ64oWNCSVfHsgQ.png
