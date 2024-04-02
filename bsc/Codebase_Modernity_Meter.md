# Codebase Modernity Meter

The concept of “modernity” has been a topic of discussion in many fields, including philosophy, sociology and technology. In
the software engineering context, modernity can be defined as the extent to which the source code of a software system utilises
new features and capabilities of the programming language it is written in. In software evolution, we define modernity as a scale of measuring the age of a codebase, expressed as language levels/versions. For instance, your Python code can have a modernity of 3.11, if it runs fine with Python 3.11 but fails with an error with Python 3.10.

To investigate it in more detail, we introduce _modernity signatures_ as vectors of values, each representing one language version: the higher the corresponding value, the more of language features from that version are used in the code. This has previously been done for [PHP](http://purl.utwente.nl/essays/91794), [Python](http://purl.utwente.nl/essays/94375) and [Rust](http://purl.utwente.nl/essays/98262), as well as for [Java](http://purl.utwente.nl/essays/91735) (technically, the project for Java only computed weighted abstract syntax trees, but converting them to modernity signatures is just a matter of traversal). A long internationally peer-reviewed paper was published about this at a highly ranked scientific journal recently: https://doi.org/10.1016/j.jss.2024.111973

There are two ways to take this project:
- using existing implementations as inspiration, apply the method to another language and observe the differences (there were some differences between PHP and Python, so most probably if you take a completely different language like Kotlin, Rascal, Haskell or CSS, the differences will be substantial and interesting to investigate and explain);
- consider existing implementations, generalising their design choices, and propose conceptual improvements on visualisation, interpretation, summarisation, pattern detection, etc; then run experiments to show what the effect is (if any) of choosing one way or the other.

As an example of the first way, you can read the [Chris Bleeker](http://purl.utwente.nl/essays/98262)'s thesis; as an example of the second way, [Cris Zubcu](http://purl.utwente.nl/essays/96034)'s.

Get in touch with your [potential future supervisors](mailto:v.zaytsev@utwente.nl,m.gerhold@utwente.nl) to discuss details!
