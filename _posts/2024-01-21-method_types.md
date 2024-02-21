---
layout: post
title:  "Difference between helpers and utils"
date:   2024-01-21 08:00:00 -0500
categories: tip
---

Sometimes I have trouble remembering which methods go were, in the context of an express app this comment was helpful

[What's the differences between helpers and utils?](https://github.com/erikras/react-redux-universal-hot-example/issues/808)

`/utils` is a place where you can place small snippets you can use throughout the application. Small functions to build bigger things with.

`/helpers` is more of a place where you store code architectural snippets in my view. Things essential for bootstrapping components and developer ergonomics.

|   |Helper Functions/Classes   |Utility Functions/Classes   |
|---|---|---|
|Purpose   |Provide support or aid to other parts of the program   |Perform common or generic operations that are not tied to any specific part of the program   |
|Scope   |Typically used within a specific module or part of the program   |Can be used throughout the program or in multiple programs   |
|Dependencies   |Often depend on other parts of the program or external libraries   |Usually independent of other parts of the program   |
|Examples   |Form validation functions, data formatting classes   |String manipulation functions, math libraries   |
