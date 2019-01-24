---
layout: post
title:  "Data Structure - Tree"
author: "JayLee"
---

# Basic of Tree
Below is what I learned from following lecture  
[Basic Data Structures: Arrays and Linked Lists][lecture] by Neil Rhodes

## Concept of Tree
**Trees** is a widely used data structure simulates a hierarchical tree structure, with a root value and subtrees of children with a parent node, represented as a set of linked nodes.

## Procedures Operating on Trees
Height(tree)
```
if tree = nil:
  return 0;
return 1 + MAX(Height(tree.left), Height(tree.right))
```
Size(tree)
```
if tree = nil:
  return 0;
return 1 + Size(tree.left) + Size(tree.right)
```

## Summary

# Trees in Java

# Practice

[lecture]: https://www.coursera.org/lecture/data-structures/arrays-OsBSF
