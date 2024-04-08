---
layout: post
title:  "Learning Go via TDD - Arrays and Slices"
date:   2024-04-06 08:00:00 -0500
categories: go
---

## Learnings Chapter: Arrays & Slices

Arrays have length and capacity

- big difference compared to JS or Ruby
  - you declare the "capacity" of the array ie how many total elements it can hold
- length
  - how many items currently in the array
- capacity
  - NOTE not understanding this can lead to memory leak!
  - How many items are allocated for the array

Slice is an Array without a declared size

- len()
  - returns length of Array
- make()
  - creates arrays with 1arg being array type, 2nd arg array length
- append()
  - allows you add slices together and return a new slice with a length of both arrays
  - its important because of strong typing in go
