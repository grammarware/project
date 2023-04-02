**Weighted Attribute Grammars** combine the power of attributes and weights: attributes are ”local variables“ defined per nonterminal and assigned different values in each node of a parse tree; and weights are special properties of a production rule, guiding the generation (or parsing). The combined power allows us to use grammars to build adaptable systems that change their behaviour during execution.

Leaving attributes aside for a moment, traditinally, there are following well-studied classes of grammars:
- probabilistic generative grammars, which assign probabilities to each production rule in such a way that all the probabilities of all production rules of one nonterminals will always result in 1;
- weighted generative grammars, which assign arbitrary weights to each production rule.

Then, unlike context-free grammars that can accommodate only questions like “is the given sentence grammatical?” (known as recognition) or “how to represent the structure of this sentence?” (known as parsing), WAG can also accommodate the following questions:
- given an input and a grammar, what probability does this grammar assign to this input?
- given an input and a grammar, what is its grammatical representation with the highest probability?
- given an input and a grammar, what is its grammatical representation with the lowest total weight?
- given a grammar in a generative context, does it always terminate when attempting to derive a sentence?

Additionally, there can be deterministic non-generalised parsing algorithms (e.g., those that always choose the production rule with the highest probability or the lowest weight if several rules are applicable), as well as stochastic ones (e.g., those that make a random choice, depending on the given weights/probabilities). In other words, there is a lot to investigate around the use of weights, probabilities and distributions, are the specifics of the project can be determined during the Research Topics phase together.

Get in touch with your [potential future supervisor](mailto:v.zaytsev@utwente.nl) to discuss details!
