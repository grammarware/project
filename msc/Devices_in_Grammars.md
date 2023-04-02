**Weighted Attribute Grammars** [1] combine the power of attributes and weights: attributes are ”local variables“ defined per nonterminal and assigned different values in each node of a parse tree; and weights are special properties of a production rule, guiding the generation (or parsing). The combined power allows us to use grammars to build adaptable systems that change their behaviour during execution. In particular, they can be used to build conversational artificial intelligence systems [2,3] like the following:

```
start <- setup activity* stop.
setup <- greet? getname.
greet <- 'hello'.
greet <- 'good morning'.
greet -> 'greetings, human!' 'what is your name?'.
getname <- 'I am' Word <$name:=$Word1>.
getname -> 'nice to meet you,' $name.
activity <- time | ... .
time <- 'what time is it?'.
time -> 'it is' [[DateTime.Now]] ',' !name <w:=5>.
time -> [w] 'it is' [[DateTime.Now.Hour]] 'o’clock' <w:=w-1>.
stop <- 'stop' | 'off' | 'stand by'.
```

When reading the example, note the following:
- some production rules are generative (`->`) and they produce messages intented for human consumption, others are analytic (`<-`) and those parse user input instead; having both in one grammar is a natural way to define a conversation;
- optionals (`?`), Kleene stars (`*`), terminals (`'x'`) work as they usually do in regular expressions or context-free grammars;
- attributes can be inherited (`!name`) or synthesised (`$name`): inherited ones are computed at one node, and propagated downwards through the tree, synthesised are computed and propagated upwards; attributes with the same name are implicitly connected by the tooling, even if they occur at different nonterminals;
- assignments are denoted with fish brackets and can be read as semantic actions (`<w:=5>`);
- weights are denoted by square brackets (`[w]`); absent weights are explicitly 1;
- attributes hold zero values until reassigned;
- zero-weight production rules are never chosen for derivation.

In addition, this grammar has two code blocks such as `[[DateTime.Now]]` which, in this particular case, just get flattened to strings are on the grammar side look nothing more complicated than plan terminals. However, it is an open question how to connect any smart internet-of-things device (such as a sensor — generating data, — or an actuator — accepting commands) to such a conversation. What does it mean on the device side, what kind of interface does one need to implement in order to allow conversing with that device? What does it mean on the grammar side, what kind of protocols and conventions must be followed? What kind of limitations in general would such a device-enriched grammarware system have? These are the most obvious research questions on this project, and more can be thought of.

Get in touch with your [potential future supervisor](mailto:v.zaytsev@utwente.nl) to discuss details!

References:
- [1] M. Gerhold, V. Zaytsev (2023). An Introduction to Weighted Attribute Grammars. Available upon request.
- [2] V. Zaytsev (2022). Speak Well or Be Still: Solving Conversational AI with Weighted Attribute Grammars. Proceedings of the International Workshop on MDE for Smart IoT Systems (MeSS), CEUR Vol. 3250, pp. 72–74. http://ceur-ws.org/Vol-3250/messpaper5.pdf
- [3] V. Zaytsev (2023). Building Conversational AI Systems with Weighted Attribute Grammars. Available upon request.
