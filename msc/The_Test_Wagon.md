**Weighted Attribute Grammars** [1] combine the power of attributes and weights: attributes are ”local variables“ defined per nonterminal and assigned different values in each node of a parse tree; and weights are special properties of a production rule, guiding the generation (or parsing). The combined power allows us to use grammars to build adaptable systems that change their behaviour during execution. However, since they have only been discovered very recently, there is no general theory and even no practices or guidelines in how to test them.

Luckily, there are many advanced techniques for testing context-free grammars, concerning coverage criteria [2,3], grammar-based test generation [4,5,6] and even automated grammar repair [7]. Additionally, there are many existing testing techniques applicable here, such as input space partitioning, boundary value analysis, mutation testing, etc. Some of them will work with drastically different effectiveness on a range of different grammars, including those with recursive, ambiguous, and/or nonterminal cycles. After diving sufficiently into the adjacent yet up till now separated topics of testing attribute grammars and testing probabilistic grammars, you can port these methods to WAG.

Get in touch with your [potential future supervisor](mailto:v.zaytsev@utwente.nl) to discuss details!

References:
- [1] Marcus Gerhold, Vadim Zaytsev (2023). An Introduction to Weighted Attribute Grammars. Available upon request.
- [2] Ralf Lämmel (2001). Grammar Testing. FASE: 201-216. https://doi.org/10.1007/3-540-45314-8_15
- [3] Ralf Lämmel, Wolfram Schulte (2006). Controllable Combinatorial Coverage in Grammar-Based Testing. TestCom: 19-38. https://doi.org/10.1007/11754008_2
- [4] Bernd Fischer, Ralf Lämmel, Vadim Zaytsev (2011). Comparison of Context-Free Grammars Based on Parsing Generated Test Data. SLE: 324-343. https://doi.org/10.1007/978-3-642-28830-2_18
- [5] Christoff Rossouw, Bernd Fischer (2020). Test Case Generation from Context-Free Grammars using Generalized Traversal of LR-automata. SLE: 133-139. https://doi.org/10.1145/3426425.3426938
- [6] Christoff Rossouw, Bernd Fischer (2021). Vision: Bias in Systematic Grammar-Based Test Suite Construction Algorithms. SLE: 143-149. https://doi.org/10.1145/3486608.3486902
- [7] Moeketsi Raselimo, Bernd Fischer (2021). Automatic Grammar Repair. SLE: 126-142. https://doi.org/10.1145/3486608.3486910
