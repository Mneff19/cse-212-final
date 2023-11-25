# Overview
Queues are a simple data structure that are defined by the order in which elements are added to and removed from the structure. They are similar to stacks in this sense. In a queue, elements are added to the end of the and removed from the beginning. This is known as a `FIFO` structure, or `First In First Out`, as illustrated below:

![Illustration of the FIFO structure showing an element being removed from the beginning and another being added to the end.](./queues-img-1.png)

In Python, these are technically just lists but through a custom class implementation we are able to enforce this FIFO structure.

## Conceptual Example - Call Center
When you're on hold and hear the classic line "your call will be answered in the order it was received," this indicates that your call was added to a queue on the call center's servers. This is one of the most prevalent and well-known examples of a queue in our day to day lives.

# Implementation
Python does not natively support queues. However, it is not difficult to create a custom queue implementation using classes. Since a queue is defined by its FIFO structure, all you need to add is custom functionality to add and remove from the list.

> [!NOTE]
> Since queues are essentially lists with specific add/remove functionality, other functionality such as getting the length of the queue and finding a value at a given position is the same syntax as a list.

This is what the skeleton of the class might look like:
```
class Queue:
    def __init__(self):
        self.queue = new list()

    def add(val):
        # Add the val

    def remove():
        #Remove first val
        return val
```

## Add to queue
Adding to the queue is very straightforward. You will need to setup the base class then add this method:
```
def add(self, val):
    self.queue.append(val)
```
Usage is as easy as `queue.add(val)`.

## Remove from queue
Removing is slightly more complicated than adding, because when we remove the first element we have to shift the rest of the list to reflect this change. Luckily, Python handles this for us. It will look something like this:
```
def remove(self):
    val = self.queue[0]
    del self.queue[0]
    return val
```
Usage is easy like adding - `queue.remove()`. Note that this will return the value at the beginning of the list, making it easy to utilize the value stored there.

# Performance
- Adding - O(1)
Since the element is added to the end and does not affect the position of other elements, it is O(1).
- Removing - O(n)
Since removing the first element does affect the position of the rest of the elements, it is O(n).

# Examples
## Code samples - call center queue

# Common Pitfalls
## Syntax errors (very error-resistant structure)

# Sample Problem
## Restaurant order queue