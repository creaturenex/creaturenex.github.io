---
layout: post
title:  "Eloquent Ruby"
date:   2022-11-11 11:00:00 -0500
categories: Ruby Syntactical_Sugar
---

I have been reading [Eloquent Ruby](https://www.amazon.com/Eloquent-Ruby-Addison-Wesley-Professional/dp/0321584104)
by Russ Olsen. Up to Chapter 5 today. I find that its best to do my reading in
the morning as my mind is still fresh and less distracted.

Just some notes I want to capture while reading the book.

One example was to look in the ruby codebase specifically `set.rb`
This involved me reading more about Set vs Array

[Ruby Guides - Set class](https://www.rubyguides.com/2018/08/ruby-set-class/)

[Atomic Object - Set better than Array?](https://spin.atomicobject.com/2012/09/04/when-is-a-set-better-than-an-array-in-ruby/)

Set.class Big Takeaways
- only has unique objects
- cannot! access elements ie Unordered list
- Fast search time using #includes?
  - why? Set compares via `eql?`
  - Array compares via `==`
- Not Core Library, but in Standard Library
  - require"set" in file

So I need to ask myself, when would be the best time to use Set?
