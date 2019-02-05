---
layout: post
title: Python Cheatsheet
---

#h1 Python Syntax and Common Patterns
Not an exhaustive list, just a few things I find handy to keep in a cheat sheet.

## Variables and Types
* Lists: `["a" , "b", "c"]`
* Tuples: Immutable lists `("a", "b", "c")`
* Dicts: key/value dictionaries/hashtable `{"a": 1, "b":2}`
* Sets: key-only dict `{"a", "b"}`
    * requires property uniqueness 
    * Faster lookup for existence
    * unordered, mutable

## List Methods
```
a.append()
a.reverse()
```

## Dict Methods
```
d.get("i", "default") 
d.update({"j": 5}) # add to dict
d.keys() # iterable of keys
d.values() # iterable of values
d.items() # iterable of both
```

## Loops
* List Comprehension: create new lists in loops
```
original = ["A", "B", "C" ]
converted = [
    i.lower() for i in original
]
```

## Functions
* Lambda functions: one line functions
```
cubed = lambda i: i**3
```
* Variable length arguments
```
do_something(*args, **kwargs)
    for arg in args:
        #iterable of non-keys arguments
    for key, value in kwargs.items():
        # dict of keyed arguments, note items() to allow for iteration
```

## Classes
* constructor
* inheritence 

## Exception Handling
```
try: a.keys()
except Exception as e:
    print("err", e)
```
