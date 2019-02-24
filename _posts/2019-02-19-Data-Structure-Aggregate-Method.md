---
layout: post
title:  "Amortized Analysis: Aggregate Method"
author: "JayLee"
---

# Dynamic Arrays and Amortized Analysis
Below is what I learned from following lecture  
[Basic Data Structures][lecture] by Neil Rhodes

## Definition
Amortized cost: Given a sequence of n operations, the amortized cost is:  
Cost(n operations) / n

### In case of dynamic array
Regarding PushBack(), still worst case is O(n)  
But amortized cost will be O(1)

## Banker's Method
Dynamic array: n calls to PushBack  
Charge 3 for each insertion. 1 coin is the raw cost for insertion.
- Resize needed: To pay for moving the elements, use the coin that's present on each element that needs to move
- Place one coin on the newly-inserted element, and one coin capacity/2 elements prior

## Alternatives to Doubling the Array Size
- Calculate amortized cost of an operation in the context of a sequence of operations
- Three ways to do analysis:
  - Aggregate method
  - Banker's method
  - Physicist's method
- Nothing changes in the code: runtime analysis only

[lecture]: https://www.coursera.org/lecture/data-structures/arrays-OsBSF
