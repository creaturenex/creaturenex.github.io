---
layout: post
title:  "Day 8 of CodeSmith"
date:   2023-02-14 08:00:00 -0500
categories: codesmith
---

Today we covered
- Snake Game Approach
- DOM Model ie Tree Structure
- Make sure Javascript functionality is differed until page is loaded
- Bind Function
  - specifically in regards to the setTimeout used to invoked in the head move object.
  - setTimeout is like an array function and this refers to the window object

- We were interested in trying to use setInterval check collisions! but it wasn't working because we never cleared the callback queue that move() kept adding recursively

- Remember that when accessing an elements style it returns a string and NOT number!!!!

- We didn't have to pass the apple via argument to head but we could have accessed the apple element in head via query selector!
- Mollie and I presented!
