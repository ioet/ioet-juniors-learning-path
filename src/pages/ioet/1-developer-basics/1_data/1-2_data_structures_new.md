---
layout: "../../../../layouts/BlogPost.astro"
title: "Data Structures"
---

## Authors

- Daniela García @dsgarcia8
- Jefferson Oña @jeffqev

> Data structure is a storage that is used to store and organize data.
Basically, data structures are divided into two categories: Linear data structure
and Non-linear data structure [More info](https://www.programiz.com/dsa/data-structure-types)

In a linear data structure, data elements are arranged in a linear order where each and every element is attached to its previous and next adjacent.

In a non-linear data structure, data elements are attached in hierarchically manner.

![Data structure](https://media.geeksforgeeks.org/wp-content/uploads/20191010170332/Untitled-Diagram-183.png)

### Topics

- [Authors](#authors)
  - [Topics](#topics)
  - [Linear Data Structure](#linear-data-structure)
    - [Array](#array)
    - [Linked-list](#linked-list)
- [Single](#single)
- [Doubly](#doubly)
  - [Stack](#stack)
  - [Queue](#queue)
    - [Hashing data structure](#hashing-data-structure)
  - [Non-linear data structure](#non-linear-data-structure)
    - [Trees](#trees)
    - [Graphs](#graphs)
    - [Libraries](#libraries)

### Linear Data Structure

#### Array

![Array](https://cdn.programiz.com/cdn/farfuture/CvSYKIrQaK-KlCU2PC0qZULI9kZa33XK3-HH1uipQIE/mtime:1623152231/sites/tutorial2program/files/array_.png)

- An array is a data structure for storing multiple data items that have a similar data type.
- Use the index for processing the values of array elements
- In most languages, an array is created by specifying an identifier, data type, and elements to include
- Arrays are best for processing a large number of values, and for quick sorting and searching

Complexity of different operations in an array ([more about complexity of array and big O notation](https://iq.opengenus.org/time-complexity-of-array/)):

| Array Operation | Time Complexity |
| ------ | ------ |
| Access i-th element | O(1)|
| Traverse all elements | O(N) |
| Override element at i-th index | O(1)|
| Insert element E | O(N) |
| Delete element E | O(N) |

Example in different languages:
<table>
<tr><td> Language </td><td> Example </td><td> Documentation </td></tr><tr>
<tr>
<td> C# </td>
<td>

```C#
int[] numbers = { 1, 2, 3, 4, 5 };
```

</td>
<td>

[Array in C#](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/arrays/)

</td>
</tr>

<tr>
<td> Java </td>
<td>

```Java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
```

</td>
<td>

[Array in Java](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays)

</td>
</tr>

<tr>
<td> Go </td>
<td>

```Go
var a [10]int
```

</td>
<td>

[Array in Go](https://gobyexample.com/arrays)

</td>
</tr>

<tr>
<td> Rust </td>
<td>

```Rust
let array: [i32; 3] = [1, 2, 3]; 
```

</td>
<td>

[Array in Rust](https://doc.rust-lang.org/reference/types/array.html)

</td>
</tr>

<tr>
<td> python </td>
<td>

```Python
import array as arr

a = arr.array('i', [1, 2, 3])
```

</td>
<td>

[Array in Python](https://docs.python.org/3/library/array.html)

</td>
</tr>

<tr>
<td> Ruby </td>
<td>

```Ruby
names = Array.new(20)
```

</td>
<td>

[Array in Ruby](https://ruby-doc.org/core-2.7.0/Array.html)

</td>
</tr>
<tr><td> php </td>
<td>

```php
$array = [
    "foo" => "bar",
    "bar" => "foo",
];
```

</td>
<td>

[Array in php](https://www.php.net/manual/en/language.types.array.php)
 </td>
 </tr>
<tr>
<td> Js </td>
<td>

```javascript
const cars = ["Saab", "Volvo", "BMW"];
```

</td>
<td>

[Array in js](https://javascript.info/array)
</td></tr>

</table>

#### Linked-list

[Linked list](https://www.programiz.com/dsa/linked-list) has a sequence of continuous nodes.

## Single

a single node is just the object which contains things like, "data" and a "next" pointer which points to the next node

![single-linked-list](https://cdn.programiz.com/sites/tutorial2program/files/linked-list-concept.png)

## Doubly

in a doubly-linked We add a pointer to the previous node

![doubly-linked-list](https://cdn.programiz.com/sites/tutorial2program/files/doubly-linked-list-concept.png)

Linked list [operations](https://www.programiz.com/dsa/linked-list-operations):

- Traversal - access each element of the linked list
- Insertion - adds a new element to the linked list
- Deletion - removes the existing elements
- Search - find a node in the linked list
- Sort - sort the nodes of the linked list

Complexity of different operations in linked list ([more about complexity of linked list and big O notation](https://iq.opengenus.org/time-complexity-of-stack/)):

| Stack Operations | Time Complexity |
| ------ | ------ |
| Search | O(1)|
| Insert  | O(1) |
| Deletion | O(1)|

### Stack

[Stack](https://geeksforgeeks.org/stack-data-structure/) is an ordered data structure that follows the Last-In-First-Out (LIFO). Forward and backward navigation is one of the most common uses of batteries.

![stack](https://cdn.programiz.com/sites/tutorial2program/files/stack.png)

Stack operations:

- Push: Adds an item in the stack. If the stack is full.
- Pop: Removes an item from the stack.
- Peek or Top: Returns the top element of the stack.
- isEmpty: Returns true if the stack is empty, else false.

Stack can be implemented using Arrays and LinkedLists

 language   |               |
-----------:|------------------:|
`C#`        | [Example](https://www.geeksforgeeks.org/stack-data-structure-introduction-program/) |
`Java`      | [Example](https://www.geeksforgeeks.org/stack-data-structure-introduction-program/) |
`Go`        | [Example](https://www.educative.io/edpresso/how-to-implement-a-stack-in-golang) |
`Rust`      | [Example](https://www.kirillvasiltsov.com/writing/how-to-write-a-stack-in-rust/) |
`Python`    | [Example](https://www.geeksforgeeks.org/stack-in-python/) |
`Ruby`      | [Example](https://gist.github.com/vderyagin/1372655) |
`php`       | [Example](https://www.geeksforgeeks.org/stack-data-structure-introduction-program/) |
`Js`        | [Example](https://www.alphacodingskills.com/php/pages/stack-in-php.php) |

Complexity of different operations in stacks ([more about complexity of stack and big O notation](https://iq.opengenus.org/time-complexity-of-stack/)):

| Stack Operations | Time Complexity |
| ------ | ------ |
| Push | O(1)|
| Pop  | O(1) |
| Peek | O(1)|

### Queue

It follows the First In First Out (FIFO) rule - the item that goes in first is the item that comes out first.

[Queue](https://www.geeksforgeeks.org/applications-of-queue-data-structure/) is used when things don’t have to be processed immediately, but have to be processed in First In First Out order. This property of Queue makes it also useful in following kind of scenarios.

1) When a resource is shared among multiple consumers. Examples include CPU scheduling, Disk Scheduling.
2) When data is transferred asynchronously (data not necessarily received at same rate as sent) between two processes. Examples include IO Buffers, pipes, file IO, etc.
3) In Operating systems: Semaphores, Spooling in printers, Buffer for devices like keyboard
4) In Networks: Queues in routers/ switches, Mail Queues

![queue](https://cdn.programiz.com/sites/tutorial2program/files/queue-implementation.png)

Complexity of different operations in a queue ([more about complexity of queue and big O notation](https://iq.opengenus.org/time-and-space-complexity-of-queue/)):

| Queue Operations | Time Complexity |
| ------ | ------ |
| Enque | O(1)|
| Deque | O(1) |
| Get front | O(1)|
| Get rear | O(1) |

Example in different languages:
<table>
<tr><td> Language </td><td> Example </td><td> Documentation </td></tr><tr>
<tr>
<td> C# </td>
<td>

```C#
Queue<int> callerIds = new Queue<int>();
```

</td>
<td>

[Queue in C#](https://www.tutorialsteacher.com/csharp/csharp-queue)

</td>
</tr>

<tr>
<td> Java </td>
<td>

```Java
Queue<String> queue = new LinkedList<>();
```

</td>
<td>

[Queue in Java](https://jenkov.com/tutorials/java-collections/queue.html)

</td>
</tr>

<tr>
<td> Rust </td>
<td>

```Rust
let mut demo: Queue<> = queue![];
```

</td>
<td>

[Queue in Rust](https://docs.rs/queues/latest/queues/)

</td>
</tr>

<tr>
<td> python </td>
<td>

```Python
q = queue.Queue()
```

</td>
<td>

[Queue in Python](https://docs.python.org/3/library/queue.html)

</td>
</tr>

<tr>
<td> Ruby </td>
<td>

```Ruby
queue = Queue.new
```

</td>
<td>

[Queue in Ruby](https://ruby-doc.org/core-2.5.0/Queue.html)

</td>

</table>

#### Hashing data structure

Hashing is a technique or process of mapping keys, values into the hash table by using a hash function. It is done for faster access to elements. The efficiency of mapping depends on the efficiency of the hash function used.

Hash Map and Hash Table

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

Dictionary

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

``` javascript
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

### Non-linear data structure

#### Trees

A [tree](https://www.programiz.com/dsa/trees) is a nonlinear hierarchical data structure that consists of nodes connected by edges tree data structures allow quicker and easier access to the data

 ![tree](https://cdn.programiz.com/sites/tutorial2program/files/nodes-edges_0.png)

One reason to use trees might be because you want to store information that naturally forms a hierarchy. For example, the file system on a computer
<!-- markdownlint-disable MD046 -->
---
        /   <-- root 
      /      \
    ...        home
          /          \
      ugrad        course
        /          /    |    \
      ...        cs101 cs112 cs113
---
<!-- markdownlint-enable MD046 -->
[Practical Applications](https://www.geeksforgeeks.org/applications-of-tree-data-structure/) of Trees data structures in Real Life:

 language   |  Examples     | Library        |
-----------:|---------------|---------------:|
`C#`        | [Example](https://debug.to/3253/tree-in-data-structure-using-c) | [TreeCollections](https://github.com/davidwest/TreeCollections) |
`Java`      | [Example](https://www.developer.com/design/understanding-java-tree-apis/) | [DefaultTreeModel](https://docs.oracle.com/javase/7/docs/api/javax/swing/tree/DefaultTreeModel.html) |
`Go`        | [Example](https://www.golangprograms.com/golang-program-to-implement-binary-tree.html) | [rtreego](https://github.com/dhconnelly/rtreego)
`Rust`      | [Example](https://dev.to/deciduously/no-more-tears-no-more-knots-arena-allocated-trees-in-rust-44k6) | [indextree](https://github.com/saschagrunert/indextree) |
`Python`    | [Example](https://www.educative.io/edpresso/binary-trees-in-python) | [treelib](https://treelib.readthedocs.io/en/latest/) |
`Ruby`      | [Example](https://medium.com/analytics-vidhya/implement-a-binary-search-tree-in-ruby-c3fa9192410b) | [RubyTree](https://github.com/evolve75/RubyTree) |
`php`       | [Example](https://medium.com/the-andela-way/binary-tree-implementation-in-php-e12df09d046f) | [Tree](https://github.com/BlueM/Tree) |
`Js`        | [Example](https://adrianmejia.com/data-structures-for-beginners-trees-binary-search-tree-tutorial/) | [functional-red-black-tree](https://github.com/mikolalysenko/functional-red-black-tree) |

Complexity of different operations in tree ([more about complexity of trees and big O notation](https://www.geeksforgeeks.org/complexity-different-operations-binary-tree-binary-search-tree-avl-tree/)):

#### Graphs

A [Graph](https://www.programiz.com/dsa/graph) consists of a finite set of vertices(or nodes) and set of Edges which connect a pair of nodes.
Graph data structures are said to contain graph data, often stored in graph databases. Graph data tends towards intricate connections with high-value relationships.

![Graphs](https://www.geeksforgeeks.org/wp-content/uploads/undirectedgraph.png)

[Practical Applications](https://leapgraph.com/graph-data-structures-applications/) of Graph Data Structures in Real Life:

1. Facebook's Graph API
2. Google's Knowledge Graph
3. Yelp's Local Graph
4. Google Maps Platform (Maps, Routes APIs)

[Graphs algorithms](https://yourbasic.org/algorithms/graph/) complexity
![Graphs algorithms complexity](https://media.codenza.app/2018/05/Graph-Algorithms.png)

Implementation of graphs on different languages
| Language| Graph representation |
| ------ | ------ |
| Python | A graph can be easily presented using the python dictionary data types. [Graphs in Python](https://www.tutorialspoint.com/python_data_structure/python_graphs.htm)|
| C# | This tutorial teaches how to represent graphs in two ways in C#. [How to Represent a Graph in C#](https://dev.to/russianguycoding/how-to-represent-a-graph-in-c-4cmo)|
| Java | The following program shows the implementation of a graph in Java. [Java Graph Tutorial – How To Implement Graph Data Structure](https://www.softwaretestinghelp.com/java-graph-tutorial/) |
| Javascript | In this post the author covered some of the most fundamental graphs algorithms, such as Breadth-First Search (BFS) and Depth-First Search (DFS). [Graph Data Structures in JavaScript for Beginners](https://adrianmejia.com/data-structures-for-beginners-graphs-time-complexity-tutorial/#Summary)|

#### Libraries

- Python: [networkx](https://networkx.org), use example: [Graphs in Python](https://unipython.com/grafos-en-python/)
- Java: [JGraphT](https://jgrapht.org)
