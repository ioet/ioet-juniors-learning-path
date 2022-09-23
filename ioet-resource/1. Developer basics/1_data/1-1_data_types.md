# Python Data Types
## Built-in Data Types
In programming, data type is an important concept.

Variables can store data of different types, and different types can do different things.

Python has the following data types built-in by default, in these categories:
- Text Type:	`str`
- Numeric Types:	`int`, `float`, `complex`
- Sequence Types:	`list`, `tuple`, `range`
- Mapping Type:	`dict`
- Set Types:	`set`, `frozenset`
- Boolean Type:	`bool`
- Binary Types:	`bytes`, `bytearray`, `memoryview`
### Python Numbers
We can find complex numbers, floating point numbers and integers in the category of Python Numbers. Complex numbers are defined as a complex class, floating point numbers are defined as float and integers are defined as an int in Python. 
````python
    # Python Numbers
    number: int = 1
    number: float = 1.0
    number: complex = 1j
````
### Python List
An ordered sequence of items is called List. It is a very flexible data type in Python. There is no need for the value in the list to be of the same data type. The List is the data type that is highly used data type in Python. List datatype is the most exclusive datatype in Python for containing versatile data. It can easily hold different types of data in Python.  
````python
    a = [5,9.9,’list’] #list dynamic data type
    fruits : list = ['apple', 'banana', 'cherry']
````
### Python Tuple
A Tuple is a sequence of items that are in order, and it is not possible to modify the Tuples. The main difference list and tuples are that tuple is immutable, which means it cannot be altered. Tuples are generally faster than the list data type in Python because it cannot be changed or modified like list datatype.
````python
    a = (5,9.9,’tuple’) #tuple dynamic data type
    fruits : tuple = ('apple', 'banana', 'cherry')
````
### Python Strings
A String is a sequence of Unicode characters. In Python, String is called str. Strings are represented by using Double quotes or single quotes. If the strings are multiple, then it can be denoted by the use of triple quotes “”” or ”’. All the characters between the quotes are items of the string.
````python
    a = “Hello World” #string dynamic data type
    fruits : str = ‘apple’
````
### Python Set
The Collection of Unique items that are not in order is called Set. Braces {} are used to defined set and a comma is used to separate values. One will find that the items are unordered in a set data type.
````python
    a = {1,2,3,4,5} #set dynamic data type
    fruits : set = {‘apple’, ‘banana’, ‘cherry’}
````
### Python Dictionary
Dictionary is a type of python data type in which collections are unordered, and values are in pairs called key-value pairs. This type of data type is useful when there is a high volume of data.
````python
    a = {“key”:”value”} #dictionary dynamic data type
    fruits : dict = {‘apple’: ‘red’, ‘banana’: ‘yellow’, ‘cherry’: ‘red’}
````
### Boolean Type
There can be only two types of value in the Boolean data type of Python, and that is True or False. 
````python
    a = True #boolean dynamic data type
    fruits : bool = False
````

Ref : 
- [W3school](https://www.w3schools.com/python/python_datatypes.asp)
- [Upgrad](https://www.upgrad.com/blog/top-7-data-types-of-python-python-data-types/#1_Python_Numbers)