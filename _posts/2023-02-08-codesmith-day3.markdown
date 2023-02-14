---
layout: post
title:  "Day 3 of CodeSmith"
date:   2023-02-08 08:00:00 -0500
categories: codesmith
---

Today we covered
- Data Structures and System Types
  - Dynamic
    - variables don't have a type, assigned at runtime
    - Not compiled, rather interpreted
  - Static
    - variables have a type, assigned at compile tile
  - Why does this matter?
    - By having a more structured program ie typed we can minimize errors and code ie type checking that can cause inefficiencies.
    - Trade off is longer initial setup in static vs ability to execute faster and accept the possibility of having incorrect data type.
  - Strongly
    - No ability to change the type of an data object via type coercion.
  - Weakly
    - Ability to change the type of an data object via type coercion.
    - ie return 1(num) + 'a' = '1a' converts num to string
  - JavaScript is Dynamically Type and Weakly Type

- Covered DataTypes
  - Primitives
  - Composite
    - ES6 introduce
    - Set unique values
    - Map key:value with key being any data type
      - as opposed to object with key being string only

- Stack: Last In, First Out
  - think stack of dishes
- Queue: First In, First Out
  - think a line to a movie
  - enqueue ie add is a constant time complexity O(1)
  - dequeue ie remove is linear time complexity O(n)
- Link List: Collection of Objects
  - Individuals objects are nodes
  - Head - starting point to enter the list
  - Tail - endpoint of list that point to null
  - Different types
    - single
    - double
    - circular
- Hash Table:
  - Key/Value pairs store in specific index in array
  - Hash Function
    - Map to unique numbers as much as possible to prevent collision
    - Which means that each key returns a unique value
    - Map the same key/value to the same index each time
    - Collision
      - When a function return a different key with same value
      - double check above statement
      - Which key do you assign to the value?
        - We need to keep track of these colliding values
        - Use a link list for this
- Binary Search Tree (BST)
  - List that allows for fast and efficient data lookup
  - Nodes point to each other
    - top value is root
    - lesser value to left
    - greater value to the right
    - nodes that to null are leafs
  - Search Traversal - Add picture
    - Breadth
      - travel by level ie left to right, then to next row
    - Depth
      - preOrder
        - parent → left child → right child
      - postOrder
        - left child → right child → parent
      - inOrder
        - left child → parent → right child

- Imposter Syndrome
  - Hit close to home especially as I struggled with the morning practice
  - Shared RJ's advice about Imposter Syndrome :) with the group
- Git and Github
  - information shared was review for me
