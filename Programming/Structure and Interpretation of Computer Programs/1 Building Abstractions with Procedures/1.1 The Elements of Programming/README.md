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

```scheme
486
```

And here is an expression that represents a primitive procedure:

```scheme
+
```

A _combination_ is a compound expression formed by delimiting a list of expressions within parenthesis in order to denote procedure application. The list is arranged in _prefix notation_, meaning that the left-most element is the operator and the remaining elements operands. For example:

```scheme
(+ 137 349)
```

Prefix notation allows for _nesting_ of combinations, that is, using combinations as elements in combinations:

```scheme
(+ (* 3 5) (- 10 6))
```

So we see that it is trivial to build complex expressions out of simple ones.

## 1.1.2 Naming and the Environment

As stated above, we need a means of abstraction. This is done by naming _variables_ whose _values_ are computational objects. We can do this with `define`:

```scheme
(define size 2)
```

This causes the interpreter to associate the value `2` with the name `size`. It follows that we can do this with more complex expressions:

```scheme
(define pi 3.14159)
(define radius 10)
(define circumference (* 2 pi radius))
```

Note that in order for these name-value associations to be defined and retrieved, the interpreter must keep a memory of them. This is referred to as the _environment_.

## 1.1.3 Evaluating Combinations

The interpreter follows a procedure for evaluating a combination:

1. Evaluate operand subexpressions

2. Apply the procedure of the operator subexpression to values of the evaluated operand subexpressions

Notice that the first step in evaluating calls for an evaluation. This is the procedure calling itself, which is referred to as _recursion_. Recursion allows us to break break down a complex combination into its primitive expressions (numbers, operators, names whose values are determined by the environment).

Notice also that this evaluation procedure does not apply to `define`, which is a definition rather than a combination. `define` is an example of a _special form_; each special form has its own evaluation procedure. The different expressions and their various evaluation rules make up the _syntax_ of a programming language.
