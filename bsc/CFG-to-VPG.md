# CFG-to-VPG

Visibly Pushdown Grammars (VPG) are a secret level of the [Chomsky hierarchy](https://youtu.be/_Wq_bt_2pe4) of languages, hiding between the class of regular languages, corresponding to the regular expressions we all know and love (and sometimes [abuse](http://www.ex-parrot.com/~pdw/Mail-RFC822-Address.html)), and the omnipresent context-free grammars (CFG, used in tools like [ANTLR](https://www.antlr.org/) or [bison](https://tomassetti.me/why-you-should-not-use-flex-yacc-and-bison/). Essentially, they correspond to a class of automata which look like pushdown automata of the CFG world, but you can only push and pop "brackets" and not just any value on the stack. Visibly Pushdown Grammars are known to be able to parse a [Dyck language](https://en.wikipedia.org/wiki/Dyck_language) of balanced brackets, which is pretty much enough to parse real languages like XML.

In a [recent paper](https://doi.org/10.1145/3591472) the authors were analysing their own generator of parsers from VPGs and they used [ANTLR's grammars](https://github.com/antlr/grammars-v4) repository. Out of 239 grammars there, they were able to convert 136 automatically to VPGs. This conversion obviously boosted the parsers' performance tremendously! However, the authors did not have enough time and strength left to investigate if this is still possible to convert the other grammars. For instance, 34 of the grammars which could not be converted, just contained left recursion, but there are known methods to eliminate that automatically.

Can we build a tool that takes any ANTLR grammar and converts it automatically to an equivalent VPG? How far can we push it? Is it even possible? We don't know until we try — that's what the _research_ is all about!

To have a look at previous unrelated BSc TCS M12 pojects concerning VPGs, see the [Automate the Automaton](https://github.com/grammarware/project/blob/main/done/Automate_the_Automaton.md) project.

Get in touch with your [potential future supervisor](mailto:v.zaytsev@utwente.nl) to discuss details!
