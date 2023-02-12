---
layout: post
title:  "Day 6 of CodeSmith"
date:   2023-02-11 08:00:00 -0500
categories: codesmith
---

Today we covered
- Auxiliary Objects
  - What are auxiliary objects?
  - Temporary objects used to solve a problem
- Set Object
  - returns unique elements from invoked object
  - Don't forget to convert back to array
  - let arr = [...new Set(oriArr)]
- Union - function
  - Not an actual object, rather functionality, uses Set object
  - Combines 2 or more arrays and return non duplicated elements
- Map Object
  - Ex used to find element with the highest occurrence
- TwoSums
  - I believe Set was used to if the difference between target and element was saved in Set
  - then check if diff ele is in Arr

- Solutions to Algorithms
  - functionBind() - Binding problem use closure
    - How to reference *this* within a different context
  - Rock, Paper, Scissor - Permutation problem Use Recursion
    - Attach image best to draw out
  - MergeSort
    - if smaller push left
    - if larger push right
