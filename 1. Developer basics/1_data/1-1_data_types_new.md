<!-- markdownlint-disable MD033 -->

# Data Types

## Authors

- Daniela García @dsgarcia8
- Jefferson Oña @jeffqev

### Topics

- [Integer](#integer)
  - [Long](#long)
  - [Short](#short)
- [Decimal Number](#decimal-numbers)
  - [Single Precision](#single-precision-are-the-32bit-decimals)
  - [Double Precision](#double-precision-are-the-64bit-decimals)
- [String](#string)
- [Character](#character)
- [Boolean](#boolean)
- [Void](#void)
- [Nothing](#nothing)
- [Date](#date)
- [Timestamp](#timestamp)
- [Key Values data types](#key-values-data-types)
  - [Dictionary](#dictionary)
  - [Hash Map and Hash Table](#hash-map-and-hash-table)
  - [Enum](#enum-enumerated)

> A data-type defines the type of value an object can have and what operations
> can be performed on it. Different programming languages support different
> data-types. For example, C supports char, int, float, long, etc. Python
> supports String, List, Tuple, etc.
[More about data types.](https://www.tutorialspoint.com/functional_programming/functional_programming_data_types.htm)

### Integer

In some languages you can specify the size of the integer transformed into a
short or Long data types

### Long

64 bits min and max value [-2<sup>63</sup> to 2<sup>63</sup>]
[ −9,223,372,036,854,775,808 to +9,223,372,036,854,775,807 ]

language    | type  |
-----------:|------:|
`C#`        | long  |
`Java`      | long  |
`Go`        | int64 |
`Rust`      | i64   |

### Short

16 bits  min and max value +- 2<sup>15</sup>  [ −32,767 to  32,767 ]

language    | type  |
-----------:|------:|
`C#`        | short |
`Java`      | short |
`Go`        | int16 |
`Rust`      | i16   |

In other languages has a system of Arbitrary-precision  all integers are
represented as a big num and these are limited only by the available memory
of the host system.

language    | type          |
-----------:|--------------:|
`Python`    | int           |
`Php`       | Math::BigInt  |
`Ruby`      | Bignum        |
`Go`        | big.Int       |

### Decimal numbers

### Single precision are the 32bit decimals

 language   | type          |
-----------:|--------------:|
`C#`        | float         |
`Java`      | float         |
`Go`        | float32       |
`Rust`      | f32           |
`Python`    | N/A           |
`Ruby`      | N/A           |
`php`       | N/A           |
`Js`        | N/A           |

### Double precision are the 64bit decimals

 language   | type          |
-----------:|--------------:|
`C#`        | Double        |
`Java`      | Double        |
`Go`        | float64       |
`Rust`      | f64           |
`Python`    | float         |
`Ruby`      | float         |
`php`       | float         |
`Js`        | Number        |

According to the tables we can see that 64-bit decimals are more used, some
languages do not have a data type for 32-bit decimals and use 64-bit decimals
directly.

### String

Data type for text

 language   | type          |
-----------:|--------------:|
`C#`        | string        |
`Java`      | string        |
`Go`        | string        |
`Rust`      | string        |
`Python`    | str           |
`Ruby`      | string        |
`php`       | string        |
`Js`        | string        |

### Character

Used to store single characters (letters, digits, symbols, etc...).

 language   | type              |
-----------:|------------------:|
`C#`        | char              |
`Java`      | char              |
`Go`        | N/A               |
`Rust`      | char              |
`Python`    | N/A               |
`Ruby`      | N/A               |
`php`       | N/A               |
`Js`        | N/A               |

### Boolean

 The Boolean data type is a data type that has one of two possible values
 (usually denoted true and false) which is intended to represent the two truth
 values of logic and Boolean algebra.

  language   | type              |
-----------:|------------------:|
`C#`        | bool (true / false)       |
`Java`      | boolean (true / false)    |
`Go`        | bool (true / false)       |
`Rust`      | bool (true / false)       |
`Python`    | bool (True / False) |
`Ruby`      | [TrueClass and FalseClass](https://www.rubyguides.com/2019/02/ruby-booleans/)               |
`php`       | bool (true, TRUE, True / false, FALSE, False)  |
`Js`        | boolean (true / false)                |

### Void

The void data type has no values and no operations. It's a data type that
represents the lack of a data type. Many programming languages need a data
type to define the lack of return value to indicate that nothing is being
returned.

  language   | type              |
-----------:|------------------:|
`C#`        | void              |
`Java`      | void              |
`Go`        | N/A               |
`Rust`      | N/A               |
`Python`    | N/A               |
`Ruby`      | N/A               |
`php`       | N/A               |
`Js`        | void              |

### Nothing

Represents that the variable is empty, this helps a lot to perform query validations.

```Python
if user.get_by_filers() not None:
    ## Do something

```

 language   | type              |
-----------:|------------------:|
`C#`        | null              |
`Java`      | null              |
`Go`        | nil               |
`Rust`      | None              |
`Python`    | None              |
`Ruby`      | nil               |
`php`       | null              |
`Js`        | null / undefined  |

### Date

 Typically stores a date in the YYYY-MM-DD format (ISO 8601 syntax).Programmers
 can include individual dates, ranges or differences in their code. Some
 examples might be:

- 2009-09-15
- 1998-11-30 09:45:87
- SYSDATETIME ()

 Language   | Module / Package / Class          |
-----------:|------------------:|
`C#`        | [DateTime](https://www.c-sharpcorner.com/article/datetime-in-c-sharp/)             |
`Java`      | [java.time](https://docs.oracle.com/javase/8/docs/api/java/time/package-summary.html)              |
`Go`        | [DateTime](https://pkg.go.dev/google.golang.org/genproto/googleapis/type/datetime)              |
`Rust`      | [DateTime](https://docs.rs/chrono/0.4.0/chrono/struct.DateTime.html)              |
`Python`    | [datetime](https://docs.python.org/3/library/datetime.html)              |
`Ruby`      | [DateTime](https://ruby-doc.org/stdlib-2.6.1/libdoc/date/rdoc/DateTime.html)               |
`php`       | [DateTime](https://www.php.net/manual/en/class.datetime.php)              |
`Js`        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) |

### Timestamp

 Typically represented in Unix time.
 The unix time stamp is a way to track time as a running total of seconds.
 This count starts at the Unix Epoch on January 1st, 1970 at UTC. Therefore,
 the unix time stamp is merely the number of seconds between a particular date
 and the Unix Epoch.
 The purpose of Unix Time is that it takes a lot less space to store a single
 number representing seconds than it does to store separate values for the year,
 month, hour, etc.

### Pointers

Some authors consider pointers as a data type, however we will consider that it
is not, because it is more a memory space than a data type.

> **_NOTE:_**  this opinion is our opinion and if you think otherwise you
> can give your opinion.

## Key Values data types

### Dictionary

A dictionary consists of a collection of key-value pairs. Each key-value pair maps the key to its associated value

<table>
<tr><td> Language </td><td> Declaration </td><td> Examples </td></tr><tr>
<tr>
<td> C# </td>
<td>

```C#
IDictionary<int, string> numberNames = new Dictionary<int, string>();
```

</td>
<td> 

[URL](https://www.tutorialsteacher.com/csharp/csharp-dictionary).

</td>
</tr>

<tr>
<td> Java </td>
<td>

```Java
Hashtable<String, String> my_dict = new Hashtable<String, String>();
```

</td>
<td> 

[URL](https://www.educative.io/edpresso/how-to-create-a-dictionary-in-java).

</td>
</tr>

<tr>
<td> Rust </td>
<td>

```Rust
pub struct HashMap<K, V, S = RandomState> { /* private fields */ }
```

</td>
<td> 

[URL](https://doc.rust-lang.org/std/collections/struct.HashMap.html).

</td>
</tr>

<tr>
<td> python </td>
<td>

```Python
MLB_team = {
...     'Colorado' : 'Rockies',
...     'Boston'   : 'Red Sox',
...     'Minnesota': 'Twins',
...     'Milwaukee': 'Brewers',
...     'Seattle'  : 'Mariners'
... }
```

</td>
<td> 

[URL](https://realpython.com/python-dicts/).

</td>
</tr>
<tr><td> Js </td>
<td>

```
const person = {
firstName: "John",
lastName: "Doe",
age: 50,
status: "marketing contact"
};
```
</td>
<td>

[URL](https://blog.hubspot.com/website/javascript-dictionary)

</td>
</tr>

</table>

### Hash Map and Hash Table

- [Hash Table](https://www.tutorialspoint.com/data_structures_algorithms/hash_data_structure.htm) is a data structure which stores data in an associative manner. In a hash table, data is stored in an array format, where each data value has its own unique index value.
- Can be implemented as a linear or non-linear data structure. Often, they are implemented as a linear data structure.
- Insertion and search operations are very fast irrespective of the size of the data.
- In a hash table, a new index is processed using the keys. And, the element corresponding to that key is stored in the index. This process is called [hashing](https://www.programiz.com/dsa/hash-table).

- [HashMap](https://www.geeksforgeeks.org/java-util-hashmap-in-java-with-examples/) is similar to HashTable, but it is unsynchronized. It allows to store the null keys as well, but there should be only one null key object and there can be any number of null values.

[More about Hash Table](https://www.geeksforgeeks.org/hashing-data-structure/)

Hash Table operations:

- Search: Searches an element in a hash table.
- Insert: inserts an element in a hash table.
- Delete: Deletes an element from a hash table.

Complexity of different operations in a hash table:

| Queue Operations | BEST CASE Complexity |
| ------ | ------ |
| Search | O(1)|
| Insert | O(1) |
| Delete | O(1)|
| Space Complexity | O(n) |

[More about complexity of Hash Table](https://iq.opengenus.org/time-and-space-complexity-of-queue/): This article covers Time and Space Complexity of Hash Table operations for different operations like search, insert and delete for two variants of Hash Table that is Open and Closed Addressing.

 language   |               |
-----------:|------------------:|
`C#`        | [Example](https://www.tutorialsteacher.com/csharp/csharp-hashtable) |
`Java`      | [Example](https://www.geeksforgeeks.org/hashtable-in-java/) |
`Go`        | [Example](https://fodor.org/blog/go-hash-table/) |
`Python`    | [Example](https://www.bogotobogo.com/python/python_hash_tables_hashing_dictionary_associated_arrays.php) |
`Js`        | [Example](https://www.educative.io/blog/data-strucutres-hash-table-javascript)

### Enum (Enumerated)

An enum is a word that represents a number.

<table>
<tr><td> Language </td><td> Declaration </td><td> Examples </td></tr><tr>
<tr>
<td> C# </td>
<td>

```C#
enum name{ item1 = value, item2 = value, ... }
```

</td>
<td>

[URL](https://www.w3schools.com/cs/cs_enums.php).

</td>
</tr>

<tr>
<td> Java </td>
<td>

```Java
enum name { item1, item2, ... }
```

</td>
<td>

[URL](https://www.w3schools.com/java/java_enums.asp).

</td>
</tr>

<tr>
<td> Go </td>
<td>

```Go
const ( 
    item1 = iota 
    item2 
    ... 
)
```

</td>
<td>

[URL](https://www.sohamkamani.com/golang/enums/).

</td>
</tr>

<tr>
<td> Rust </td>
<td>

```Rust
enum name { item1 = value, item2 = value, ... }
```

</td>
<td>

[URL](https://www.koderhq.com/tutorial/rust/enum/).

</td>
</tr>

<tr>
<td> python </td>
<td>

```Python
from enum import Enum
class Name(Enum):
    item1 = value
    item2 = value
```

</td>
<td>

[URL](https://www.geeksforgeeks.org/enum-in-python/).

</td>
</tr>

<tr><td> Ruby </td><td> N/A </td><td> N/A </td></tr>
<tr><td> php </td><td> N/A </td><td> N/A </td></tr>
<tr><td> Js </td><td> N/A </td><td> N/A </td></tr>

</table>
