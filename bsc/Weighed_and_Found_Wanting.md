# Weighed and Found Wanting (to Generate Tests)

A very simplified excerpt from a [Java grammar](https://github.com/antlr/grammars-v4/blob/master/java/java9/Java9Parser.g4#L792) could look like this:

```
statement
	:	'if' '(' expression ')' statement ('else' statement)?
	|	'while' '(' expression ')' statement
	|	'for' '(' forInit? ';' expression? ';' forUpdate? ')' statement
	;
```

As you see, there are three possible branches, and some contain optional elements, and we do get a bit of an idea of what a `statement` could be in that language, but there is no information about the use of different constructs there. Wouldn't it be better to have something like the following?

```
statement
	:	[42%] 'if' '(' expression ')' statement ([32%] 'else' statement | [68%] ε)
	|	[23%] 'while' '(' expression ')' statement
	|	[35%] 'for' '(' ([91%] forInit | [9%] ε) ';' ([88%] expression | [12%] ε) ';' ([77%] forUpdate | [23%] ε) ')' statement
	;
```

In the second example we have the usage statistics, which can help humans when they are learning the language (to explain what are the normal and often used constructs and which ones are weird and exotic), and also can direct test generation (by following the observed distribution we generate realistic test cases; by following the inverse of the chances we generate unexpected ones).

There can be variations of this project:
- take [one of the Java grammars](https://github.com/antlr/grammars-v4/tree/master/java) and grab as much `*.java` files from GitHub as you can, and infer the weights for all constructs; draw conclusions from observed data
- take a [Python 2&3](https://github.com/nvavrova/thesis/blob/master/main/grammar/Python.g4) grammar and grab as much `*.py` files from GitHub as you can, and infer the weights for all constructs; draw conclusions from observed data
- take the [ANTLR grammar of ANTLR](https://github.com/antlr/grammars-v4/tree/master/antlr/antlr4) and assign weights to it by analysing all other ANTLR grammars from the same repository (or from the [Grammar Zoo](http://slebok.github.io/zoo/)); draw conclusions from observed data
- take any grammar of the language you like, and enough source code in that language, infer the weights, draw conclusions…

Get in touch with your [potential future supervisors](mailto:v.zaytsev@utwente.nl,m.gerhold@utwente.nl) to discuss details!
