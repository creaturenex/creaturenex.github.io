---
layout: post
title:  "Day 5 of CodeSmith"
date:   2023-02-10 08:00:00 -0500
categories: codesmith
---

Today we covered
- Algorithms - Time Complexity & Big O Notation
  - What is an algorithm
    - A set of instructions
    - AKA business logic of how data can be created, stored, & change
  - What is Time complexity
    - describes how efficient/effective and algo is
    - more computational steps take longer to complete
  - Big O notation
    - O(1)      - constant key in obj
    - O(n)      - linear   loop though array
    - O(n^2)    - quadratic two sum problem
    - O(log^2)  - binary search tree
    - more
  - Big O generalize ie only the biggest complexity matters

  - Space Complexity
    - how much space in memory this algo/variables take
  - Time Complexity is always more important to solve over Space Complexity

  - Recursion
    - Look at slides for notes
  - Why use recursion
    - Imperative - following steps to generate result
    - Declarative - you really only care about the end result
  - Recursion allow us to write declarative code
  - Types of Recursion
    - Linear Recursion
      - think going down then back up to return answer
    - Tail Call Recursion
      - answer is generated in last recursion
    - Mutual Recursion
      - two function call each other within themselves
    - Tree Recursion
      - splitting function based in inputs or branch decision

  - JSON Javascript Object Notation
    - storing data in string format
    - serializer    - string to object
    - deserializer  - object to string
  - Other languages use JSON and have their own parser
  - Includes
    - string
    - boolean
    - number
    - null
    - objects - these objects never contain functions
    - arrays
  - String must be in double quotes
  - JSON.stringify(jsonObject)
  - JSON.parse(jsonString)
  - Solving the parse is a large problem that will tackle
    - What data are we parsing?
    - Parse primitive data
    - Perform recursion on composite data, to get inner elements
