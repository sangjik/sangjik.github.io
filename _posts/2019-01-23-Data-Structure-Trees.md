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

### Depth First
InOrderTraversal(tree)
```
if tree = nil:
  return
InOrderTraversal(tree.left)
Print(tree.key)
InOrderTraversal(tree.right)
```

PreOrderTraversal(tree)
```
if tree = nil:
  return
Print(tree.key)
PreOrderTraversal(tree.left)
PreOrderTraversal(tree.right)
```

PostOrderTraversal(tree)
```
if tree = nil:
  return
PostOrderTraversal(tree.left)
PostOrderTraversal(tree.right)
Print(tree.key)
```

### Breath first
LevelTraversal(tree)
```
if tree = nil:
  return
Queue q
q.Enqueue(tree)
while not q.Empty():
  node <- q.Dequeue()
  Print(node)
  if node.left != nil:
    q.Enqueue(node.left)
  if node.right != nil:
    q.Enqueue(node.right)

```

## Summary
- Trees are used for lots of different things
- Trees have a key and children
- Tree walks: DFS and BFS
- When working with a tree, recursive algorithms are common
- In Computer Science, trees grow down

[lecture]: https://www.coursera.org/lecture/data-structures/arrays-OsBSF
