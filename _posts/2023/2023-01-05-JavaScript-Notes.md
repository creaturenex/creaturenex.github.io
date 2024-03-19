---
layout: post
title:  "JavaScript Notes 01/05/23"
date:   2023-01-05 12:00:00 -0400
categories: JavaScript
---
I am currently reviewing JavaScript Closure. The cool thing about JavaScript
closures is that the returned function has access to the variables declared in
the outer function but only those variables that are used inside the return
function. In the example below, we can see the return function is actually
accessing two objects. First the index variable declared in the outer function. Secondly, which is being done sneakily, is the names array which was passed in as an argument to the outer function.


Write a function `rollCall` that accepts an array of names and returns a function.
The first time the returned function is invoked, it should log the first name to
the console. The second time it is invoked, it should log the second name to the
console, and so on, until all names have been called. Once all names have been
called, it should log 'Everyone accounted for'.

```JavaScript
function rollCall(names) {
  let index = 0
  let size = names.length - 1

  return function (){
    if (index <= size){
      console.log(names[index])
    } else {
      console.log(`Everyone accounted for`)
    };
    index++
  };
}

const rollCaller = rollCall(['Victoria', 'Juan', 'Ruth'])
rollCaller() // => should log 'Victoria'
rollCaller() // => should log 'Juan'
rollCaller() // => should log 'Ruth'
rollCaller() // => should log 'Everyone accounted for'

// output
'Victoria'
'Juan'
'Ruth'
'Everyone accounted for'
```
