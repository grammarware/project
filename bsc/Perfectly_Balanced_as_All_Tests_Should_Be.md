# Perfectly Balanced, as All Tests Should Be

Test cases can be generated automatically. Fundamentally, these tests try some inputs and wait what happens next.

A test generation algorithm can be written as intuitively as "From finitely many possible inputs, choose each equally likely." To bring this into formal terms, a generative grammar could be:

```
test_input
: [1/n] 'input_1' 
| [1/n] 'input_2' 
...
| [1/n] 'input_n' 
;
```

Each test input is chosen with equal likelihood, which is how many commercial testing tools work in practice. However, this need not be the case! These probabilities can be tweaked: One input might occur more frequently than others, or certain behaviour should be tested more thoroughly compared to the rest. This can be learned from past user experience or log files.

In this case [Zeller et al.](https://doi.org/10.1109/TSE.2020.3013716) show how tweaking probabilities *just* right, can reproduce real user behaviour. However, fixing these probabilities at the beginning can also be a hindrance. So why not overcome this hurdle and change them on-the-fly during test case generation? 

This can be done with innovative Weighted Attribute Grammars (WAG) -- an amalgamation of weighted grammars and attribute grammars.

Sounds interestig? Get in touch with your [potential future supervisors](mailto:v.zaytsev@utwente.nl,m.gerhold@utwente.nl) to discuss details!
