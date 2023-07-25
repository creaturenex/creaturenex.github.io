---
layout: post
title:  "Day 7 of CodeSmith"
date:   2023-02-13 08:00:00 -0500
categories: codesmith
---

Today we covered
- Web Development
  - DOM Manipulation and jQuery
  - HTML Hyper Text Markup Language
  - CSS Cascading Style Sheet
- DOM Document Object Model
  - Specifications lead by W3C
  - World Wide Web Consortium
  - see image below
  - ![DOM model](/assets/DOMmodel.svg)
- DOM Standards maintained by W3C
  - Core DOM
  - XML  DOM
  - HTML DOM
- HTML DOM
  - HTML elements represented as objects
  - When html page loads, it creates a document model
  - This model is accessible to JavaScript via "document"
  - Because the object is created after load we must wait to execute any Javascript
  - This is done using the eventListener function
    - Many types of event you can listen to
- How to Manipulate DOM?
  - Select!
    - ex `getElementById()` singular
    - `getElementsByTagName()` plural
    - `getElementsByClassName()` plural
    - `querySelector()`
    - `querySelectorAll()`
      - returns all object in an Array like object so please be aware Array methods wont work
  - Do something! ier Change
    - ex `element.innerText`
    - `element.attribute`
    - `element.setAttribute`
    - `element.style.the-css-property-you-wanna-change`
  - Add/Remove
    - document.createElement()
    - document.appendChild(the-parent-element)
      - this is key if you want to see it on the page
      - Id might make this easier
  - Events on the DOM
    - Respond to page state change and user activity using event handler.
    - Use eventListener
    - Does not overwrite an event/element
    - You can add many event listener to one element

  - jQuery
    - older technology that allowed users to DOM via events
  - React
    - Modern tool for user interaction
  - Best practices
    - Keep static information in html
    - dynamic info should be handled in JavaScript

  - Implicit Bias and Microaggression
    - We all have implicit bias do to culture, life experiences etc
    - These might reflect in actions towards bias groups that might not represent who you are.

  - Why am I at CodeSmith and what do I want to get out
    - First and foremost, I am looking to improve my skills, specifically technical communication and become a software engineer
      - having Code/Tech be an everyday part of my life
    - Why? Tech is literally everyone and I am excited to learn more and the future
    - My loves :)
