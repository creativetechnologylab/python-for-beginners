# Functions

Functions are small, reusable chunks of code that allow us to repeat a specific task. You can think of functions as being a bit like the programming equivalent of a recipe in which we have ingredients (our function inputs), a set of steps for preparing the food (a function _body_), and a finished dish (our program output).

The "ingredients" that are function needs are its _parameters_. Later, we will see that some functions do not actually take inputs or give back outputs, but that does not prevent them from being useful in certain situations.

## Function Definition
### Function Header

The first component of our function is the function _header_. This is the first line of our function in which we give it its name and decide what inputs it will take. We can create a basic function that will simply print "Hello World" when executed.

```python
def greet():
    print("Hello")
```

In Python the `def` keyword is used to start the function definition. This is then followed by the function name, which is what we will need to use when we execute a function.

Notice that the code within our function is in an indented block, as we saw previously with loops.

### Calling a Function

Once we have a function ready, we can use it by _calling_ the function. To do this, you use the function name, followed by brackets. We can see this with our `greet()` function:

```python
def greet():
    print("Hello")

greet()
```
Output:
```
Hello
```

Functions are reusable, so we can _call_ the function multiple times:

```python
greet()
greet()
greet()
```
Output:
```
Hello
Hello
Hello
```

### Parameters

At the moment, the `greet()` function has no inputs. This means that it will always give the same result when it's run. We can modify our function, so that it takes a _parameter_ when called. This will, in turn, allows us to vary its behavior with each execution.

```python
def greet(name):
    print("Hello, " + name)
```

In the above example, we have created a parameter called `name`. This parameter is then combined with the string "Hello, " to create a greeting. Now we can try running the function again:

```python
greet()
```

Output:
```
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: greet() missing 1 required positional argument: 'name'
```

The problem here is that the function now _expects_ a value for `name` to be given. To do this, we have to give a value inside the brackets:

```python
greet("Bob")
```

Output:
```
Hello, Bob
```

Now we can use different values to cause the function to behave differently each time its executed:

```python
greet("George and Jeanie")
greet("Charlotte")
greet("Renie")
greet("Uncle Geoff")
greet("Cousin Julie")
```

Output:
```
Hello, George and Jeanie
Hello, Charlotte
Hello, Renie
Hello, Uncle Geoff
Hello, Cousin Julie
```

## `return`
## Built-in Functions
## Summary
---
[Prev](control-flow.md) | [List of Contents](README.md) | [Next](libraries.md)