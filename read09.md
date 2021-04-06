# FUNCTIONAL PROGRAMMING

![](https://miro.medium.com/max/2660/1*3wp2A9xFW7LbCKFA_X2-sw.png)

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data — Wikipedia


## Pure functions

Pure function returns the same result if given the same arguments (it is also referred as deterministic),
moreover it does not cause any observable side effects.


Pure function returns the same result if given the same arguments.


**Regarding Reading** Files, If our function reads external files, it’s not a pure function — the file’s contents can change.

**Regarding Random number generation**,
Any function that relies on a random number generator cannot be pure.


Pure Function does not cause any observable side effects

## Pure functions benefits

The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:

* Given a parameter A → expect the function to return value B
* Given a parameter C → expect the function to return value D

## Immutability


When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

pure functions + immutable data = referential transparency


## Higher-order functions

When we talk about higher-order functions, we mean a function that either:
* takes one or more functions as arguments, or
* returns a function as its result

The doubleOperator function we implemented above is a higher-order function because it takes an operator function as an argument and uses it.
You’ve probably already heard about filter, map, and reduce. Let's take a look at these.


## Filter

Given a collection, we want to filter by an attribute. The filter function expects a `true` or `false` value to determine if the element should or should not be included in the result collection. Basically, if the callback expression is `true`, the `filter` function will include the element in the result collection. Otherwise, it will not.


## Map

The map method transforms a collection by applying a function to all of its elements and building a new collection from the returned values.


## Reduce

The idea of reduce is to receive a function and a collection, and return a value created by combining the items.

## Refactoring JavaScript for Performance and Readability

Refactoring means updating the source code without changing the behavior of the application. Refactoring helps you keep your code solid, dry, and easy to maintain.

## When Should You Refactor Your Code?

A great time to refactor your code is when you are working with something that you need to write over and over again. This isn’t the only time that you can refactor your code, however, it’s extremely common to run into things that are repetitive.

## The Basics of Refactoring Your Code

To refactor your code, you can basically go through a fairly simple 3 step process. If you implement this into your coding habits, you will notice fairly quickly that your code will start to look much more professional and tidy. The image below shows the typical 3 step process that you should go through when refactoring your code.

