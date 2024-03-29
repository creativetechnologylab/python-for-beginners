# Collections

![](pictures/warehouse.jpg)

If variables are boxes for holding data, then Python's _collection_ data types are like warehouses that can hold many boxes. These warehouses have the following key properties:

- They can be _ordered_ or _unordered_.
- They can be _changeable_ or _unchangeable_.

When a collection is ordered this means that the data type will remember the order in which elements were added to it, and preserve this order. On the other hand, an unordered collection will not maintain the order in which elements are added to it.

A _changeable_ collection is a collection that can be modified. This means elements can be added to or removed from it after it has been created. An _unchangeable_ collection is one that cannot be modified after its creation.

## Lists

Lists are an _ordered_ and _changeable_ data type. Here is an example of a basic list containing three strings:

```pycon
>>> my_list = ["string-1", "string-2", "string-3"]
>>> print(my_list)
['string-1', 'string-2', 'string-3']
```

Lists are defined by writing square brackets. Any elements in the list would then be placed inside the brackets, and separated by a comma. But elements are actually optional, and it's fine to create an empty list to start with.

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

Note that `remove()` takes away only the _first occurrence_ of an item.

```pycon
>>> my_list
['string-1', 'string-2', 'string-3']
>>> my_list.append("string-2") # adding the same item again
>>> my_list
['string-1', 'string-2', 'string-3', 'string-2']
>>> my_list.remove("string-2")
>>> my_list
['string-1', 'string-3', 'string-2']
```

The `insert()` command also allows adding an item to a list at a particular index.

```pycon
>>> my_list = ["string-1", "string-2", "string-3"]
>>> my_list.insert(2, "hello")
>>> my_list
['string-1', 'string-2', 'hello', 'string-3']
```

`pop()` can be used to remove an item at a particular index.

```pycon
>>> my_list
['string-1', 'string-2', 'hello', 'string-3']
>>> my_list.pop(2)
'hello'
>>> my_list
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

`clear()` allows us to remove everything from a list.

```pycon
>>> my_list
['string-1', 'lists are changeable', 'string-3']
>>> my_list.clear()
>>> my_list
[]
```

## Tuples

Tuples are an _ordered_ and _unchangeable_ data type. Tuples are created by using round brackets.

```pycon
>>> my_tuple = ("hello-1", "hello-2", "hello-3")
>>> my_tuple
('hello-1', 'hello-2', 'hello-3')
```

Like in the case of lists, we can use indexing to access a particular item from a Tuple.

```pycon
>>> my_tuple
('hello-1', 'hello-2', 'hello-3')
>>> my_tuple[2]
'hello-3'
```

Because Tuples are unchangeable, we cannot add or remove items from them, or change the data at a given index.

```pycon
>>> my_tuple[0] = "tuples are not changeable"
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'tuple' object does not support item assignment
```

We can use the `+` operator like with we did with Lists, but that is because we're actually creating a new Tuple rather than changing an existing one.

```pycon
>>> my_tuple + (1,)
('hello-1', 'hello-2', 'hello-3', 1)
```

## Dictionaries

Dictionaries are an _ordered_ (since Python 3.7) and _changeable_ data type. Dictionaries are comprised of key-value pairs that _map_ one piece of data to another.

<!---
An image would be nice here.
-->

To create a dictionary we use curly brackets. Then any key-value pairs are placed inside these curly brackets, and separated my commas. A colon is used to define a key-value pair.

```pycon
>>> capitals = {"United Kingdom": "London", "Azerbaijan": "Baku", "Norway": "Oslo"}
>>> capitals
{'United Kingdom': 'London', 'Azerbaijan': 'Baku', 'Norway': 'Oslo'}
```

Here we use square brackets to access an item in our Dictionary, but instead we provide a _key_ rather than an _index_.

```pycon
>>> capitals["Norway"]
'Oslo'
```

Adding information to a dictionary is then as simple as _assigning_ a value to a particular key.

```pycon
>>> capitals["Peru"] = "Lima"
>>> capitals
{'United Kingdom': 'London', 'Azerbaijan': 'Baku', 'Norway': 'Oslo', 'Peru': 'Lima'}
```

The `del` keyword can be used to remove data from our dictionary.

```
>>> del capitals["United Kingdom"]
>>> capitals
{'Azerbaijan': 'Baku', 'Norway': 'Oslo', 'Peru': 'Lima'}
```

We can also change the value for an existing key.

```pycon
>>> capitals["Norway"] = "Cairo"
>>> capitals
{'Azerbaijan': 'Baku', 'Norway': 'Cairo', 'Peru': 'Lima'}
```

Now let's change that back to the right value, and add Egypt to the Dictionary.

```pycon
>>> capitals["Norway"] = "Oslo"
>>> capitals["Egypt"] = "Cairo"
>>> capitals
{'Azerbaijan': 'Baku', 'Norway': 'Oslo', 'Peru': 'Lima', 'Egypt': 'Cairo'}
```

Trying to access data that does not exist in the Dictionary leads to a **KeyError**.

```pycon
>>> capitals
{'Azerbaijan': 'Baku', 'Norway': 'Oslo', 'Peru': 'Lima', 'Egypt': 'Cairo'}
>>> capitals["South Korea"]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 'South Korea'
```

Dictionary keys have to be unique. Attempting to have two bits of data with the same key will simply result in one value overwriting the other.

## Sets

Sets are an _unordered_ and _changeable_ data type. They are a special type of Collection that prevent repeating elements. Sets are also defined using curly brackets.

```pycon
>>> my_set = {1, 2, 3}
>>> my_set
{1, 2, 3}
```

However, an empty pair of curly brackets makes Python create a Dictionary.

```pycon
>>> my_set
{1, 2, 3}
>>> type(my_set) # check the type of our set
<class 'set'>
>>> not_a_set = {} # this is not a set
>>> type(not_a_set) # type tells us this is actually an empty dictionary
<class 'dict'>
```

If we want to create an empty set we have to use the `set()` command instead.

```pycon
>>> actually_a_set = set() # create an empty set the proper way
>>> type(actually_a_set) # type tells us this is a set
<class 'set'>
```

We can try to add a repeating item to our Set and Python won't give an Error, but it will simply refuse to add that item.

```pycon
>>> my_set
{1, 2, 3}
>>> my_set.add(2)
>>> my_set
{1, 2, 3}
```

A similar thing applies to creating Sets.

```pycon
>>> my_set = {1, 2, 3, 3} # create a set with a duplicate 3
>>> my_set
{1, 2, 3}
```

## Strings

Strings aren't a type of collection, but can still behave like them. For example, we can use indexing to get a particular character from a string.

```pycon
>>> my_string = "hello"
>>> my_string[3]
'l'
```

Strings are also _unchangeable_.

```pycon
>>> my_string[3] = "!"
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment
```

## Slicing

Slicing allows us to pick segments from a List or String. Let's say we wanted to get just the first three characters from a String or the first three elements from a list. Slicing makes it much simpler to do this.

```pycon
>>> my_string = "hello"
>>> my_string[:3]
'hel'
```

```pycon
>>> my_list = [1, 2, 3, 4, 5]
>>> my_list[:3]
[1, 2, 3]
```

By indexing at -1, we can pick out the _last_ item.

```pycon
>>> my_string
'hello'
>>> my_string[-1]
'o'
```

```pycon
>>> my_list
[1, 2, 3, 4, 5]
>>> my_list[-1]
5
```

You can read more about slicing [here](https://www.freecodecamp.org/news/slicing-and-indexing-in-python/).

## Other Stuff

### `len()`

It is possible to check for the length of a collection using `len()`.

#### Lists

```pycon
>>> len(["a", "b", "c"])
3
>>> len([]) # empty list
0
```

#### Tuples
```pycon
>>> len(("item-1", "item-2", "item-3"))
3
>>> len(()) # empty tuple
0
```

#### Dictionaries
```pycon
>>> len({'United Kingdom': 'London', 'Azerbaijan': 'Baku', 'Norway': 'Oslo'})
3
>>> len({}) # empty dictionary
0
```

In the case of Dictionaries, `len()` counts the number of key-value pairs.

#### Sets
```pycon
>>> len({1, 2, 3})
3
>>> len(set()) # empty set
0
```

We can also observe that adding an item that already exists in a set does not cause its length to change.

```pycon
>>> simple_set = {1, 2, 3}
>>> len(simple_set)
3
>>> simple_set.add(2)
>>> len(simple_set)
3
```

#### Strings

`len()` also lets us see the length of a string.

```pycon
>>> len("cat")
3
>>> len("")
0
```

### `in`

The `in` keyword in Python allows us to see if something is a member of a collection.

#### Lists

```pycon
>>> my_list = ["a", "b", "c"]
>>> "a" in my_list
True
>>> "z" in my_list
False
```

#### Tuples
```pycon
>>> my_tuple = ("a", "b", "c")
>>> "a" in my_tuple
True
>>> "z" in my_tuple
False
```

#### Dictionaries

In the case of Dictionaries, `in` checks for the presence of a key.

```pycon
>>> capitals = {'United Kingdom': 'London', 'Azerbaijan': 'Baku', 'Norway': 'Oslo'}
>>> "United Kingdom" in capitals
True
>>> "Singapore" in capitals
False
```

We cannot do the same thing with values. Checking if "Oslo" is `in` our `capitals` Dictionary gives back `False`.

```pycon
>>> "Oslo" in capitals
False
```

However, we could extract the _values_ from our Dictionary and check if "Oslo" is one of them.

```pycon
>>> capitals.values()
dict_values(['London', 'Baku', 'Oslo'])
>>> "Oslo" in capitals.values()
True
```

Likewise, a similar command exists for extracting the keys from a Dictionary.

```pycon
>>> countries = capitals.keys()
>>> countries
dict_keys(['United Kingdom', 'Azerbaijan', 'Norway'])
```

#### Sets
```pycon
>>> my_set = {1, 2, 3}
>>> 1 in my_set
True
>>> 100 in my_set
False
```

#### Strings

For strings, `in` lets us see if one string contains another.

```pycon
>>> college = "london college of communication"
>>> "london" in college
True
>>> "llege of" in college
True
>>> "utah" in college
False
```

We would say that "london" and "llege of" are _substrings_ of "london college of communication".

## Summary

- Collections in Python are like warehouses for our variable-boxes.
- Lists are ordered, changeable sequences defined with `[ ]`.
- Lists support indexing, slicing, appending, removing, and concatenating.
- Tuples are ordered and unchangeable sequences defined with `( )`. Tuples also support indexing.
- Dictionaries are ordered and  changeable key-value pairs defined with `{ }`.
- Dictionary values are accessed by keys, and dictionaries support adding, removing, and updating items.
- Sets are unordered, changeable collections with unique elements defined with `{ }`.
- Sets prevent duplicates and support adding and removing.
- Strings aren't strictly a Collection but kind of act like one. They are an unchangeable sequences of characters, and support indexing and slicing.
- Slicing allows selecting a range of elements.
- `len()`: Returns the length of a collection.
- `in`: Checks membership in a collection, including substring presence for strings.
---
[Prev](basic-data-types.md) | [List of Contents](README.md) | [Next](loops.md)