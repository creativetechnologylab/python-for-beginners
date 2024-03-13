# Basic Data Types

## Integers and Floats

In Python there are two core numeric types that you typically deal with. `int` is the type for whole-numbers or integers, while `float` is the type for numbers with a decimal point.

```python
two_int = 2
two_float = 2.0
```
### type()

The `type()` command in Python shows us the type of some data.

```ipython
>>> type(2)
<class 'int'>
>>> type(3.2)
<class 'float'>
```
### Division Operator

The division operator `/` will always return a float. This is true when it is applied to `float` and `int`.

```ipython
>>> 1 / 2
0.5
>>> 4 / 2
2.0
>>> 15 / 3.0
5.0
```
### Floor Division Operator

The floor division operator `//` can be used to obtain an `int` result from division if two integers are given as inputs.

```ipython
>>> 15.0 // 3
5.0
>>> 15 // 3
5
```
### Converting Between Float and Integer

Floats can be converted to integers with the `int()` function. This will round down.

```ipython
>>> int(3.5)
3
>>> int(3.0)
3
>>> int(3.9)
3
```

## Strings
## Booleans
## Summary
---
[Prev](variables.md) | [List of Contents](README.md) | [Next](collections.md)