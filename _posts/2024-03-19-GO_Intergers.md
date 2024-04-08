---
layout: post
title:  "Learning Go via TDD - Integers"
date:   2024-03-19 08:00:00 -0500
categories: go
---

Chris James shared this blog by [Dave Chaney](https://dave.cheney.net/2014/12/01/five-suggestions-for-setting-up-a-go-project) which has some great discussion on GO.

## Learnings Chapter: Integers

- When writing tests we can format the displayed text
  - String: '%q'
  - Integer: '%d'
- Go module are collection of packages ie functions that be called from another module
- package is directory that contains functions and or test
- go.mod is a dependencies management file think package.json or gemfile
- In go you can define Example functions inside of a `_test.go` file, the benefit of this that the example can be tested. If an example ws in a readme and the function where to change we easily forget to update the example.
  - ```go
    func ExampleAdd() {
	  sum := Add(1, 5)
	  fmt.Println(sum)
	  // Output: 6
    }
  - **_Note_** Example functions without **output comments** are compiled but not executed.
- To execute a test run
  - `go test` if package is in root
  - if multiple packages in a module use
    - `go test ./package` add the `-v` flag for more info.
    - cd into package directory and run `go test`
    - from module root run `go test ./...` ie recursively run test on subdirectories
