# Ambiguous Regular Expressions

Regular expressions are omnipresent in software which needs to process some structured or semi-structured data, and always have been, since their introduction in 1951 by Stephen Kleene. Yet, the research on them is still ongoing: developers want more features without the loss of performance, they want advanced tools to help them debug regular expressions, and to generate code from them.

In this project, you take a [recently published paper](https://doi.org/10.1007/s00236-020-00366-7) explaining how to generate deterministic parsers from regular expressions even when they are ambiguous. The code produced by the same authors, [is also available](https://github.com/FLC-project/BSP/blob/master/reBSP.zip), and seem to contain a mix of Java and C++. Dive into it, get it working, get acquainted with the algorithm and its implementation, in order to ask and answer some research questions.

* For instance, can you reimplement the same algorithm in modern nice language, such as Kotlin or C#?
* Can you inventorise which PCRE features are and are not supported by this algorithm? Can the supported subset be increased?
* The experimental comparison in the original paper is very limited, can you do better?
* The performance of the Berry–Sethi parser is still worse that the RE2 implementation, can you find ways to improve it?

You can also define your own research questions during the investigation phase or after it.

Get in touch with your [potential future supervisor](mailto:v.zaytsev@utwente.nl) to discuss details!