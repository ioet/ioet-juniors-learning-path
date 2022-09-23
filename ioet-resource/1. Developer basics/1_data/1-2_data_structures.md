# Which Python Data Structure Should You Use?
Python is an object-oriented programming (OOP) language. Classes and objects are used to structure and modularize code to be reusable and easy to modify. OOP requires the use of data structures to organize and store data in a way that can be efficiently accessed.

Python has primitive (or basic) data structures such as floats, integers, strings, and Booleans. Python also has non-primitive data structures such as lists, tuples, dictionaries, and sets. Non-primitive data structures store a collection of values in various formats rather than a single value. Some can hold data structures within the data structure, creating depth and complexity in data storage capabilities.
![img](https://miro.medium.com/max/2400/1*2JFd94q0vzsEcr-LB-220g.png)

### What is mutability?
Mutability means that the data in the data structure can be modified (added, deleted, or changed) after creation. Mutability is an important factor to consider when choosing your data structure. If you know that you won’t need to change the internal state, consider using an immutable object to ensure that it is thread-safe and that nothing can overwrite your data.
### Lists
To represent a sequence of items indexed by their integer position, one data structure you can use is a list. Lists contain zero or more elements and can contain elements of different types (even objects!). This makes lists powerful because they allow you to create deep and complex data structures.
Lists are mutable, meaning that you can add, delete, or change elements in a flexible manner. Another sequential data structure is a tuple; the difference between these two is that tuples are immutable.
Because lists have a sequential element: if you only want to keep track of unique values and don’t care about the order, use a Python set.
Create lists using `[]` or `list()`. Typecast using `list()`.
### Tuples
Tuples are also a sequenced data structure, just like lists. However, tuples are immutable; you cannot add, delete, or change items after a tuple is created. Tuples differ from lists by having many fewer functions because they can’t be modified after being defined. Tuples contain zero or more elements and can contain elements of different, immutable types.
Advantages to tuples over lists:
- Tuples use less space
- Immutability prevents changing tuple items by mistake
- Tuples can be used as dictionary keys
- Function arguments are passed as tuples
  
Create tuples using `()` or a comma-separated list of elements with no surrounding brackets or braces. Typecast using `tuple()`.
### Dictionaries
Instead of using an offset, dictionaries use keys to associate with each value. This means that order is not tracked and should not matter if you plan to use a dictionary. Dictionary keys are immutable and unique, however, dictionaries are mutable; the key-value elements can be added, deleted, or changed. In short, dictionaries are very similar to hashmaps.
Create dictionaries using `{}`. Typecast using `dict()`.
### Sets
A set is like a dictionary with only the keys, not the values. This means that sets are unique and not sequential (stored unordered). Sets are also mutable. Sets contain zero or more elements and can contain elements of different, immutable types.
Essentially, sets are used when you want to know if something exists and nothing else about it. If it matters to track value order or store multiple of the same value, consider using a space-friendly tuple instead.
Create sets using `set()`. Typecast using `set()`.

Ref: [Data Structures](https://towardsdatascience.com/which-python-data-structure-should-you-use-fa1edd82946c)