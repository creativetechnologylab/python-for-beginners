# Collections

![](pictures/warehouse.jpg)

If variables are boxes for holding data, then Python's _collection_ data types are like warehouses that can hold many boxes. These warehouses have the following key properties:

- They can be _ordered_ or _unordered_.
- They can be _changebale_ or _unchangeable_.

When a collection is ordered this means that the data type will remember the order in which elements were added to it, and preserve this order. On the other hand, an unordered collection will not maintain the order in which elements are added to it.

A _changebale_ collection is a collection that can be modified. This means elements can be added to or removed from it after it has been created. An _unchangeable_ collection is one that cannot be modified after its creation.

## Lists

Lists are an ordered and changeable collection data type. Here is an example of a basic list containing three strings:

```pycon
>>> my_list = ["string-1", "string-2", "string-3"]
>>> print(my_list)
['string-1', 'string-2', 'string-3']
```

Lists are defined by writing square brackets. Any elements in the list would then be placed inside the brackets, and seperated by a comma. But elements are actually optional, and it's fine to create an empty list to start with.

```pycon
>>> my_empty_list = []
>>> print(my_empty_list)
[]
```

When we access a particular item within our list, this is known as _indexing_. To do this, we must place some square brackets at the end of the list and provide a number that corresponds with the location of the item we wish to retrieve. Python uses zero-based indexing and so the item at index 0 would be the first element in the list, the item at index 1 would be the second element in our list, and so-on. An example is given below.

```pycon
>>> my_list = ["string-1", "string-2", "string-3"]
>>> print(my_list)
['string-1', 'string-2', 'string-3']
>>> my_list[0]
'string-1'
```

If we attempt to access an item in our list that doesn't exist, we get an **IndexError**. If a list contains three items then Python doesn't know what to do when we ask for element four.

```pycon
>>> my_list[3]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
```

Because lists are _changeable_, we're allowed to add / remove elements from our list. The `append()` command allows us to add an item to the end of the list, while the `remove()` command allows us to take something away from a list. 

```pycon
>>> my_list.append("string-4")
>>> print(my_list)
['string-1', 'string-2', 'string-3', 'string-4']
>>> my_list.remove("string-4")
>>> print(my_list)
['string-1', 'string-2', 'string-3']
```

We're also allowed to use the `+` operator to combine lists.

```pycon
>>> my_list + ["string-4"]
['string-1', 'string-2', 'string-3', 'string-4']
```

As lists are _changeable_, we may also take the data at a particular index in our list and replace it with something else.

```pycon
>>> my_list
['string-1', 'string-2', 'string-3']
>>> my_list[1] = "lists are changeable"
>>> my_list
['string-1', 'lists are changeable', 'string-3']
```

## Tuples
## Dictionaries
## Sets
## Comprehensions
## Summary
---
[Prev](basic-data-types.md) | [List of Contents](README.md) | [Next](loops.md)