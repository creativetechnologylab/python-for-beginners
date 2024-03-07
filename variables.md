# Variables

Following the steps in the previous section, create a new file and call it variables.py.

## Variable Assignment

We can use code like `print(3 + 2)` to display the result of an operation. However, this value isn't stored anywhere.

Using a **variable** allows us to place information in a box so that it may be used again later.

![](./pictures/variable-box.png)

In the code below, we can obtain the result of a calculation and then use it again later.

```python
my_val = 10 + 2
print(my_val)
```

When a variable is given a value, we call this **variable assignment**. The equals (=) symbol is often refered to as the **assignment operator**.

The **assignment operator** is how we let Python know that we want to take a box with a particular label, and place some information in the box. Then if we ever want to see or use what's inside that box again, we can use the variable's name to access the information another time.

Python, unlike some other languages, isn't especially fussed about knowing in advance what _type_ of information you wish to place inside a box. 

## Variable Resassignment
### Garbage Collection
## Naming Variables
## Name Error

Something we can't do is attempt to access a variable that has never been created. In Python this leads to what is known as a **NameError**.

Run the code below and examine the output:

```python
my_val = 2
print(my_val)

my_other_val = 3
print(my_other_val)

print(this_does_not_exist)
```
## Integers and Floats
## Strings
## Booleans
## Summary
---
[Prev](getting-started.md) | [List of Contents](README.md) | [Next](collections.md)