# Automate the Automaton

In the [Chomsky hierarchy](https://youtu.be/_Wq_bt_2pe4) of languages we have a class of regular languages, corresponding to the regular expressions we all know and love (and sometimes [abuse](http://www.ex-parrot.com/~pdw/Mail-RFC822-Address.html)), these are parsable with a simple finite state machine which only have states and transitions (and no memory); and right above it a class of context-free languages, for which you need to add a stack or some other memory to such an automaton, and you can describe it with a context-free grammar (and use a tool like [ANTLR](https://www.antlr.org/) or [bison](https://tomassetti.me/why-you-should-not-use-flex-yacc-and-bison/) to generate the parser code out of it).

Grammars are complex and hard to write, so the creators of grammar toolkits, language workbenches and parser generators tend to expose only the most necessary features and assume the rest themselves. On the other hand, regular expressions are naturally simple but often their expressive power is simply not enough. What could be a solution? Writing a parsing algorithm yourself, of course! A parsing automaton is a simple implementation of a deeply nested `if`/`switch` construct with at least one variable (e.g., `state`) guiding the process together with the input that is being consumed.

The goal of this project is to write a generator for such automata. The syntax of the input for this generator is negotiable and will be designed as a part of this project. The choice of the implementation language is up for the student. If there is time left in the project, your generator can be compared (feature-wise or experimentally) with some existing parser generator for a comparable language class (e.g., [**owl**](https://github.com/ianh/owl)).

The project was "done" three times, focusing on:
- testing the existing implementation => Luc Timmerman
- focusing on translation and performance => Michael Janssen
- focusing on handling ambiguous definitions => Bas Marcelis

The project was done by **Luc Timmerman** aka [**@Luctia**](https://github.com/Luctia):
- Title: _[Performance Testing Owl, Parser Generator for Visibly Pushdown Grammars](http://purl.utwente.nl/essays/91958)_
- Presented at [37th Twente Student Conference on IT](https://sites.google.com/utwente.nl/37th-twente-student-conference/) on 8 July 2023
- Code: https://github.com/Luctia/owl_perftest
- Paper: https://drive.google.com/file/d/1TlSYbI7MWJGNEdEALBknY5v4jtR3Q_OJ/view

The project was done by **Michael Janssen** aka [**@Michael-Janssen-dev**](https://github.com/Michael-Janssen-dev):
- Title: _[A Parser Generator for Visibly Pushdown Languages: Translating between VPLs](http://purl.utwente.nl/essays/94363)_
- Presented at [38th Twente Student Conference on IT](https://sites.google.com/utwente.nl/38tscit/) on 3 February 2023
- Code: https://github.com/Michael-Janssen-dev/vpl-parser-generator
- Paper: https://drive.google.com/file/d/1Z14uncPvCCvDEfcKWCFLu3mCNfUK-G3G/view

The project was done by **Bas Marcelis** aka [**@basmarcelis**](https://github.com/basmarcelis):
- Title: _[A Derivative-based, Colored-edged Parser Generator for Nested Words](http://purl.utwente.nl/essays/94400)_
- Presented at [38th Twente Student Conference on IT](https://sites.google.com/utwente.nl/38tscit/) on 3 February 2023
- Code: https://github.com/basmarcelis/Derivative-based-Colored-edged-Parser-Generator-for-Nested-Words
- Paper: https://drive.google.com/file/d/1PrZjC7lvjzmmSQUB3Ua8djA54lfW40bO/view
- [Best Paper Award](https://lh6.googleusercontent.com/GCAx6FPBnaikw0bbXTyZdsDM_rtr_Qp_bWjJmtElGXfpKB962kvLsa9POKMsibMOg4oB1i-DYlJmI9GPBZDbyNk6ibVQtgW92WO4SK5lN5G170BTxHVr7NgKxksQwuIrBA=w1280)
