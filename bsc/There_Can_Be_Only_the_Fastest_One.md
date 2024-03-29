# There Can Be Only (the Fastest) One

There are many data structures known to humankind, some more popular than others. It can be said that each data structure has two sides: the external side with visible commitments (like a list that promises to keep the order in which the elements are stored and retrieved, but a set does not save the order but promises each element uniqueness instead), and the internal side with the implementation details (something behaving like a set can be implemented based on an array, a list, a bit map, etc). For example, if we focus on the external side of collections, we can think of at least the following ones:

|                                | **order matters** | **order does not matter**|
|--------------------------------|-------------------|--------------------------|
| **duplicate elements allowed** | list, array       | bag, multiset, counter   |
| **all elements unique**        | uniq              | set, hashset             |
| **key-value mapping**          | sorted dictionary | map, hashmap, dictionary |
| **LIFO access**                | stack             | —                        |
| **FIFO access**                | queue, channel    | —                        |

(with `uniq` we denote the unnamed data structure that the Linux tool [uniq](https://man7.org/linux/man-pages/man1/uniq.1.html), which prints input lines in order but skips duplicate ones)

Each of these basic eight groups of data structures supports its own range of operations which makes sense for it: for instance, a stack should support at least `push` and `pop`, but a reasomable implementation should show good performance also for `peek`, `drop`, `dup` and `rot`.

The idea behind this project is to do the following:

* For each of these 8 data types,
  * identify the main set of operations expected to be supported (mostly by reading books on algorithms and data structures)
  * find the corresponding data types in some popular portable framework (such as JVM or .NET Core), reimplement those
  * find state of the art implementation variants that did not make it yet to the mainstream platforms, implement those
  * find state of the art benchmarks used to compare data structure implementations in practice
* That's it. Visualise results, and give advice in which cases which implementation is the most practical (i.e., efficient for all operations, some operations, having the best performance-effort ratio, etc).

**NB:** There is a strong preference for using a platform **not** necessarily geared towards performance (such as .NET Core or JVM) instead of, say, bare C/C++, because (1) implementations of complex data structures are considerably harder in a low-level non-garbage-collected language and (2) most such questions have already been answered with concrete libraries. This project aims more at answering a mainstream developer's questions like "is using `Stack<...>` enough, or do I need to code up my own linked list implementation for my program to be fast?"

**NB2:** This project has been successfully completed a couple of times, each of them investigated a different dimension:
* **Marten Voorberg** in *[Performance Analysis of Membership Data Structures for Integers in Java](http://purl.utwente.nl/essays/87064)* focused on membership data structures which support only one query: determining whether a certain element is contained in the data structure;
* **Mark van Wijk** in *[The Quest for the Best Thread-Safe Java List](http://purl.utwente.nl/essays/91694)* focused on lists and how thread (un)safety of their implementations affects their performance;
* **Leonardo Pasquarelli** in *[Extending Java Collections for List and Set Data Structures](http://purl.utwente.nl/essays/91726)* focused on what additional data structures can/should be added to Java Collections by porting them from classic algorithms and alternative libraries;
* **Kristian Nedelchev** in *[Performance evaluation of Map implementations in Java, Python and C#](http://purl.utwente.nl/essays/94391)* focused on the performance of map/dictionary implementations on different platforms: JVM, .NET and in Python.
If you want to do a related project, it is up to you to define another unique point to investigate.
