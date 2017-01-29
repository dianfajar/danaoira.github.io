---
layout: post
title: "Python Functional Programming"
categories:
  - Learning
tags:
  - Functional Programming
  - Python 3
  - Coding
---

The following post replicates and adds notes to the tutorial from [source](http://www.bogotobogo.com/python/python_fncs_map_filter_reduce.php).


**Functional programming** is all about **expressions**. We may say that the Functional programming is an **expression oriented programming**.

Expression oriented functions of Python provides are:

```python
map(aFunction, aSequence)
filter(aFunction, aSequence)
reduce(aFunction, aSequence)
lambda
list comprehension
```
([source](http://www.bogotobogo.com/python/python_fncs_map_filter_reduce.php))

# map()

**Example 1**

```python
items = [1, 2, 3, 4, 5]
squared = []
for x in items:
    squared.append(x ** 2)

squared
[1, 4, 9, 16, 25]
def sqr(x):
    return x ** 2

list(map(sqr, items))
[1, 4, 9, 16, 25]
list(map((lambda x: x ** 2), items))
[1, 4, 9, 16, 25]```

**Example 2**

```python
def square(x):
    return x**2

def cube(x):
    return x**3

f = [square, cube]
for r in range(5);
    value = map(lambda x: x(r), f)
    print((value))

# output
<map object at 0x0000023E622C73C8>
<map object at 0x0000023E622C7908>
<map object at 0x0000023E622C73C8>
<map object at 0x0000023E622C7908>
<map object at 0x0000023E622C73C8>
```

**Error:** Seems test code was written in Python 2.x, so printing a map result returns object instead.

**Fix**: In Python 3.x, use `list()` around the map data to print out values.

> In Python 3+, many processes that iterate over iterables return iterators themselves. In most cases, this ends up saving memory, and should make things go faster. ([source](http://stackoverflow.com/questions/1303347/getting-a-map-to-return-a-list-in-python-3-x))

```python
...

for r in range(5):
     val = map(lambda x: x(r), f)
     print(list(val))

# output
[0, 0]
[1, 1]
[4, 8]
[9, 27]
```

**Example 3**
```python
def mymap(aFunc, aSeq):
    result = []
    for x in aSeq: result.append(aFunc(x))
    return result

list(map(sqr, [1, 2, 3]))
[1, 4, 9]
mymap(sqr, [1, 2, 3])
[1, 4, 9]
```

**Example 4**
```python
list(map(sqr, [1, 2, 3]))
[1, 4, 9]
mymap(sqr, [1, 2, 3])
[1, 4, 9]
pow(3,5)
243
pow(2, 10)
1024
pow(3, 11)
177147
pow(4, 12)
16777216
list(map(pow, [2, 3, 4], [10, 11, 12]))
[1024, 177147, 16777216]
```

**Example 5**
```python
m = [1, 2, 3]
n = [1, 4, 9]

new_tuple = map(None, m, n)

print(new_tuple)
<map object at 0x000002768D8185C0>

print(list(new_tuple))

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'NoneType' object is not callable
```

**Error:** Trackback error. Code above works in Python 2.x

**Fix:** Import `itertools` library.

```python
from itertools import zip_longest
for i, j in zip_longest(m, n):
    print(i, j)

# output
1 1
2 4
3 9
```

* `zip_longest()` iterates and aggregates values `m` and `n`

# filter() and reduce()

* `filter` : Gets elements in sequence that return `True`
* `reduce` : Reduces list to single value based on a function

**Example 6**

Using filter to print negative values.

```python
>>> list(filter((lambda x: x < 0), range(-5, 5)))
[-5, -4, -3, -2, -1]
```

`for()` loop equivalence:

```python
>>> result = []
>>> for x in range(-5, 5):
...     if x < 0:
...             result.append(x)
...
>>> result
[-5, -4, -3, -2, -1]
```
