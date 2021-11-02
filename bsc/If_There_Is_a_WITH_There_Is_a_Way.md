# If There Is a `with`, There is a Way

There are many different constructs in existing programming languages: conditional (`if`, `cond`, `evaluate`, `switch`, `case`, etc), iterative (`for`, `foreach`, `do`, `while`, `perform`, etc), and many others. However, there is always space to add another one. In this case, consider a `with` construct that can do the following (assuming Java as the base language):

| Pseudocode with `with`   | Pure Java |
|--------------------------|-----------|
| `with (A) { f(); g(); }` | `A.f(); g();` |
| `with (A in B) { f(); }` | `for (T A : B) { A.f(); }` |
| `with (A<B<C) { f(B); }` | `for (int B = A+1; B++; B<C) { f(B); }` |
| `with (A as B) { f(A); }` | `if (A instanceof B) { f( (B)A ); }` |
| `with (A as B, C in A, C as D) { f(C); }` | `if (A instanceof B) for (D C : (B)A) { f(C); }` |

In other words, it is up to the compiler (or preprocessor) to figure out the types of involved elements, add required casts, expand the context, add conditional and iterative statements of the base language, and in general combine the given constraints in the correct way.

In this project, you implement this construct in some way on top of a language of your choice.

Get in touch with your [potential future supervisor](mailto:v.zaytsev@utwente.nl) to discuss details!