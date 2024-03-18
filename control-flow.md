# Control Flow and Conditional Statements

## `if`
## `if...else`
## `elif`
## `break` and `continue`

`break` and `continue` are two words that allow us to alter the flow of loops.

### `break`

`break` terminates a loop immediately. Take the example below:

```python
animals = ["dog", "cat", "bird", "pig", "elephant"]

for animal in animals:
    if animal == "pig":
        break
    print(animal)
```
Output:
```
dog
cat
bird
```

Because the loop was "broken" upon reaching the element "pig", we only see the first three items printed. 

### `continue`

The `continue` keyword allows us to "skip" a 

```python
animals = ["dog", "cat", "bird", "pig", "elephant"]

for animal in animals:
    if animal == "pig":
        continue
    print(animal)

```

## Summary
---
[Prev](loops.md) | [List of Contents](README.md) | [Next](functions.md)
