# Basic Data Types

## Integers and Floats

In Python there are two core numeric types that you typically deal with. `int` is the type for whole-numbers or integers, while `float` is the type for numbers with a decimal point.

```python
two_int = 2
two_float = 2.0
```
### type()

The `type()` command in Python shows us the type of some data.

```pycon
>>> type(2)
<class 'int'>
>>> type(3.2)
<class 'float'>
```

The meaning of `class` is something that will be explained a bit later...

### Division Operator

The division operator `/` will always return a float. This is true when it is applied to `float` and `int`.

```pycon
>>> 1 / 2
0.5
>>> 4 / 2
2.0
>>> 15 / 3.0
5.0
```
### Floor Division Operator

The floor division operator `//` can be used to obtain an `int` result from division if two integers are given as inputs.

```pycon
>>> 15.0 // 3
5.0
>>> 15 // 3
5
```
### Converting Between Float and Integer

Floats can be converted to integers with the `int()` function. This will round down.

```pycon
>>> int(3.5)
3
>>> int(3.0)
3
>>> int(3.9)
3
```
Likewise, there is a `float()` command that can convert an `int` to a `float`.

```pycon
>>> float(3)
3.0
>>> float(1)
1.0
```

There are also a couple of other ways we can convert an `int` to a `float`.

```pycon
>>> 5 + 0.0
5.0
>>> 10 * 1.0
10.0
```

## Strings

The `string` type can hold text information. We can use either double or single quotation marks to create them.

```pycon
>>> "hello"
'hello'
>>> 'hello'
'hello'
```

In both cases, their `type()` will still be `string`.

```pycon
>>> type("hello")
<class 'str'>
>>> type('hello')
<class 'str'>
```

The `+` operator allows us to combine or _concatenate_ strings. But sometimes you need to remember to add a space!

```pycon
>>> "hello" + "world"
'helloworld'
```
Instead we could do one of the following:

```pycon
>>> "hello " + "world"
'hello world'
>>> "hello" + " world"
'hello world'
>>> "hello" + " " + "world"
'hello world'
```

## Booleans
## Summary
---
[Prev](variables.md) | [List of Contents](README.md) | [Next](collections.md)