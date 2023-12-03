# Overview
Sets are another simple data structure, similar to a list except duplicate values are not allowed. In other words, sets contain only unique values. The operations to add, remove, and find elements are different from lists however. Sets are a native structure to Python and are created by using `{}`.

## Conceptual Example - Unqiue Letters in String
Let's say that you wanted to find every unique letter in a given string. Sets would be a perfect solution to this problem, as you could easily add each letter to the set, and if it already existed in the set it would simply not be added again. The result would be a set with all the unique letters in the string.

# Implementation
As mentioned in the overview, sets are a native structure to the Python language. They are created by declaring a variable and setting its value to a set of elements wrapped in curly braces like so:

```
my_empty_set = {}
my_set = {'1', '2', '3', '4', '5'}
```

> [!TIP]
> It is important to remember that sets have different operations than lists!

## Add to set
The built in `add` method is used to add elements to a set:
```
my_set.add('7')
```
This is a straightforward operation where you provide the element to be added and it is then added to the end of the set.

## Remove from set
The built in `remove` method is used to remove elements from a set. 
```
my_set.remove('4')
```
To use this you need to provide the element to be removed, not the index. If the element does not exist, it will throw an error. To avoid this you can use the `discard` moethod instead.

## Check if element in set
Python allows the `element in set` syntax to check if an element is in a set, since the dictionary-style `set.element` syntax is not supported. To continue the examples we've seen so far, it would look like this:
```
if '3' in my_set:
    my_set.remove('3)
```

# Performance
**Adding - O(1)**
Since the element is added to the end and does not affect the position of other elements, it is O(1).

**Removing - O(n)**
Since removing the given element does affect the position of the other elements after it, it is O(n).

# Common Pitfalls
Sets are also very bug-resistant. The only error case that you have to consider is when you try to add an element that already exists in the set - this will throw an error, so you will have to catch it to avoid the program halting.

# Sample Problem
Go back through the examples provided throughout this lesson and track what elements are added/removed from the `my_set` set. What should `my_set` look like if all of the examples operations in this tutorial were applied to it in that order?

This should be your answer:
```
{'1', '2', '5', '7}
```