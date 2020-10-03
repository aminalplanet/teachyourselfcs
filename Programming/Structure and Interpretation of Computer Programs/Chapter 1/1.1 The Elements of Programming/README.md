# 1.1 The Elements of Programming

There are three mechanisms that a powerful programming language needs in order to form complex ideas out of simple ones:

- **primitive expressions**: represent the simplest entities in the language
- **means of combination**: ways of building compound elements from simpler ones
- **means of abstraction**: ways of naming compound elements so they can be manipulated as units

We will deal with two kinds of elements:

- **data**: "stuff" to manipulate
- **procedures**: sets of rules for manipulating data

For now we will focus on rules for building procedures, and use only simple data.



## 1.1.1 Expressions

Here is a primitive expression that represents a number:

    486

And here is an expression that represents a primitive procedure:

    +

A _combination_ is a compound expression formed by delimiting a list of expressions within parenthesis in order to denote procedure application. The list is arranged in _prefix notation_, meaning that the left-most element is the operator and the remaining elements operands. For example:

    (+ 137 349)

Prefix notation allows for _nesting_ of combinations, that is, using combinations as elements in combinations:

    (+ (* 3 5) (- 10 6))

So we see that it is trivial to build complex expressions out of simple ones.