**[Whitespace](https://en.wikipedia.org/wiki/Whitespace_(programming_language))** is a programming language that has an interpreter which ignores all non-whitespace characters and preserves all the rest (while it is more common for mainstream languages to do otherwise). Underneath such an app(e)al(l)ing frontend there is a stack-based language with **`push`** (`\ \ `), **`dup`** (`\ \n\ `), **`over`** (`\ \t\ `), **`swap`** (`\ \n\t`), **`drop`** (`\ \n\n`), **`slide`** (`\ \t\n`), etc.

Implement several automated refactorings for this language — i.e., transformations that take a valid Whitespace program and output another Whitespace program that is still valid, produces the same results in all situations, and is somehow structurally different. Any valid refactoring can be implemented, up to the student who dares to pick up this project. Inspiration can be found in [the book](https://martinfowler.com/books/refactoring.html) or any [website](https://refactoring.guru/refactoring) on the topic.

https://github.com/wspace/corpus contains a lot of implementations of Whitespace in different languages, as well as sample programs that can be used for testing.

The project was done by **Rutger Witmans** aka [**@rwitmans**](https://github.com/rwitmans):
- Title: _[Improving nothingness: Refactorings on Whitespace](http://purl.utwente.nl/essays/94374)_
- Presented at [38th Twente Student Conference on IT](https://sites.google.com/utwente.nl/38tscit/) on 3 February 2023
- Code: https://github.com/rwitmans/whiteref
- Paper: https://drive.google.com/file/d/1P1STztsK40syJxeX45tJ1EIGdXK9xLH-/view
