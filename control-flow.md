# Control Flow and Conditional Statements

## `if`

If-statements are used to execute a block of code on when a particular condition has been met.

```python
my_bool = True
if my_bool:
    print("The condition is True.")
```

Output:
```
The condition is True.
```

We may put mathematical expressions in place of booleans, as these will _evaluate_ to True or False.

```python
num = 16
if num > 10:
    print(str(num) + " is greater than 10.")
```
Output:
```
16 is greater than 10.
```

Try running the code below:
```python
if False:
    print("What will happen now?")
```

Output:
```
```

This time nothing happens, because our boolean is False.

Like in the case of loops, we have to _indent_ a block of code to let Python know that this code should only be run the condition in our if-statement is True.

```python
if False:
    print("This won't be printed.")
print("This will be printed because it's outside our if-statement.")
```

Output:
```
This will be printed because it's outside our if-statement.
```

Further information on using mathematical operators in Python can be found [here](https://www.w3schools.com/python/python_conditions.asp).

## `if...else`

An if-else statement allows us to run different code depending on whether or not a condition is True or False. This means that at least one of the blocks of code in or if-else statement will be run no matter what.

```python
if False:
    print("This won't be run.")
else:
    print("This will be run, because our if-condition is False.")
```

Output
```
This will be run, because our if-condition is False.
```

On the flip side, when our first condition is True, the code in the else-block is skipped.

```python
if True:
    print("This will be run, because our if-condition is True.")
else:
    print("This won't be run, because our if-condition is True.")
```

Output
```
This will be run, because our if-condition is True.
```

if-else statements allow us to account for both the True and False conditions for a boolean.

## `elif`

The `elif` keyword allows us to check if multiple conditions are True. If our first condition is False, we can move to check if another set of conditions are True by using `elif`. Consider the example below:

```python
age = 25

if age < 13:
    print("You are a child")
elif age < 20:
    print("You are a teenager")
elif age < 30:
    print("You are in your twenties (Vicenarian)")
elif age < 40:
    print("You are in your thirties (Tricenarian)")
elif age < 50:
    print("You are in your forties")
elif age < 60:
    print("You are in your fifties")
else:
    print("You are a senior citizen")
```

Output:
```
You are in your twenties (Vicenarian)
```

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

The continue keyword allows us to "skip" a specific iteration of a loop and move on to the next iteration without executing the remaining code within that code block.

```python
animals = ["dog", "cat", "bird", "pig", "elephant"]

for animal in animals:
    if animal == "pig":
        continue
    print(animal)

```
Output:
```
dog
cat
bird
elephant
```
## Summary
---
[Prev](loops.md) | [List of Contents](README.md) | [Next](functions.md)
