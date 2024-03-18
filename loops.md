# Loops

Loops can be used for iterating over a sequence, or for repeating a block of code. They are a bit like the programming equivalent of a conveyor belt.

![](pictures/conveyor-belt.jpg)

## For Loops

Loops allows us to repeat a block of code. This can be useful when we want to do something with every element in a Collection (Lists, Tuples, Dictionaries, Sets) as well as Sequences such as Strings.

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

While this "solution" works, it is not maintainable and is far more fiddly. If I were to mistakenly What we want to use instead is a for-loop.

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

Strings can also be looped through in this way:

```python
for char in "hello":
    print(char)
```

Output:
```
h
e
l
l
o
```

### Dictionaries

In the case of Dictionaries, simply looping through them will give us their keys.

```python
capitals = {
    "United States": "Washington, D.C.",
    "United Kingdom": "London",
    "France": "Paris",
    "Germany": "Berlin",
    "Japan": "Tokyo",
    "China": "Beijing",
    "India": "New Delhi",
    "Brazil": "Brasília",
    "Russia": "Moscow",
    "Canada": "Ottawa"
}

for country in capitals:
    print(country)
```

Output:
```
United States
United Kingdom
France
Germany
Japan
China
India
Brazil
Russia
Canada
```

If we want to see both a key and a value, we need to loop through the `items()` of the Dictionary.

```python
capitals = {
    "United States": "Washington, D.C.",
    "United Kingdom": "London",
    "France": "Paris",
    "Germany": "Berlin",
    "Japan": "Tokyo",
    "China": "Beijing",
    "India": "New Delhi",
    "Brazil": "Brasília",
    "Russia": "Moscow",
    "Canada": "Ottawa"
}

for country, capital in capitals.items():
    print(country + ": " + capital)
```

Now we obtain the following output:

```
United States: Washington, D.C.
United Kingdom: London
France: Paris
Germany: Berlin
Japan: Tokyo
China: Beijing
India: New Delhi
Brazil: Brasília
Russia: Moscow
Canada: Ottawa
```

### `range()`

`range()` is a command in Python that gives us a sequence of numbers. By default it will start at zero. We can use this with a for-loop to repeat a block of code a fixed number of times.

```python
for i in range(3):
    print("Hello")
```

Output:
```
Hello
Hello
Hello
```

When we actually ask to see the `i` that is being obtained from `range()` at each _iteration_ in our loop, we can see how the `range()` command is performing its counting.

```python
for i in range(5):
    print(i)
```

Output:

```
0
1
2
3
4
```

When we give range a single number as an input (or parameter), it starts at zero and counts up by one, stopping before it reaches our input value.

### Indentation

Indentation is an important part of our Python code. This is how Python recognises that a certain bit of code belongs to a "block."

Consider the code below:
```python
for i in range(3):
    print("Hello from inside the loop.")
print("Hello from outside the loop.")
```

We have a for-loop that will repeat some code 2 times. Our second line with the `print` statement is indented, meaning that there are some spaces at the beginning of the line. Our third line of code containing the other print statement is not indented. It shares the same _level of indentation_ as our "loop header."

This gives us the following output:
```
Hello from inside the loop.
Hello from inside the loop.
Hello from inside the loop.
Hello from outside the loop.
```

Only our first print statement is "looped" because it's loop's code block.

### IndentationError

When we misuse indentation, we can get what is known as an `IndentationError`.

Take the example of a for-loop that doesn't have an indented block.

```python
for i in range(3):
print("Hello")
```

See what VS Code does when given this code:

![](pictures/missing-indentation.PNG)

We have a red squiggly line beneath our `print`. Placing our mouse over this also causes a message to appear. This lets us know that we are going to get an error from running this code.

Output:
```
  File "<stdin>", line 2
    print("Hello")
    ^
IndentationError: expected an indented block after 'for' statement on line 1
```

We can see that an indented block was expected after the `for`, but that none was found. Now, let's do the opposite and add an indent that has no reason to be there.

```python
print("Hello")
    print("Indented for no reason.")
```

Again, VS Code lets us know that something isn't right here.

![](pictures/unexpected-indent.PNG)

Output:
```
  File "<stdin>", line 1
    print("Indented for no reason.")
IndentationError: unexpected indent
```

Now we have another `IndentationError`, but this one is complaining about the opposite issue. An indent appeared for no reason.

Fixing the code is pretty simple:

```python
for i in range(3):
    print("Hello")
```

Output:
```
Hello
Hello
Hello
```

Now we can fix the other code as well:

```python
print("Hello")
print("Indented for no reason.")
```

Output:
```
Hello
Indented for no reason.
```

## While Loops
## `break` and `continue`
## Comprehensions
## Summary
---
[Prev](collections.md) | [List of Contents](README.md) | [Next](control-flow-and-conditional-statements.md)