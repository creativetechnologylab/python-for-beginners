# Loops

Loops can be used for iterating over a sequence, or for repeating a block of code. They are a bit like the programming equivalent of a conveyor belt.

![](pictures/conveyor-belt.jpg)

## For Loops

For loops allows us to repeat a block of code. This can be useful when we want to do something with every element in a Collection (Lists, Tuples, Dictionaries, Sets as well as Sequences such as Strings.

Let's say we have a list of strings that contain a mix of uppercase and lowercase characters.

```python
mixed_strings = ["Hello", "wOrlD", "PyThOn", "ProGRamming", "Is", "FuN"]
```

What if we want to print the strings in all lowercase? We can use the `.lower()` command to convert a string to lowercase, but we need to run this on _every_ string in our List. Here is the not-so-fun way of doing it.

```python
print(mixed_strings[0].lower())
print(mixed_strings[1].lower())
print(mixed_strings[2].lower())
print(mixed_strings[3].lower())
print(mixed_strings[4].lower())
print(mixed_strings[5].lower())
```

While this "solution" works, it is not maintainable and is far more fiddly. If I were to mistakently What we want to use instead is a for-loop.

```python
mixed_strings = ["Hello", "wOrlD", "PyThOn", "ProGRamming", "Is", "FuN"]

for mixed_string in mixed_strings:
    print(mixed_string.lower())
```

This gives the following output:

```
hello
world
python
programming
is
fun
```

### `range()`

## While Loops
## `break` and `continue`
## Comprehensions
## Summary
---
[Prev](collections.md) | [List of Contents](README.md) | [Next](control-flow-and-conditional-statements.md)