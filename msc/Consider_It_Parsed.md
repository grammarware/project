# Consider It Parsed

The world of parsing techniques is huge and full of various techniques — if you don't believe me, have a look at “[Parsing Techniques](http://slebok.github.io/dyol/books/PT-GJ.html)” and bask in its 700 page glory. As a matter of fact, even since the second edition of this lovely book came out in 2008, there have been several significant advances in this area, with important new results published almost yearly.
One of these recent results was published at PLDI 2020 as “[Faster General Parsing through Context-Free Memoization](https://doi.org/10.1145/3385412.3386032)”. It is a nicely readable 14-page proposal of a new approach which seems to:
- be easier to understand than some other techniques
- map more straightforwardly to actions at parse time, making parser debugging a sensible activity
- theoretically, have the same/comparable complexity as competitors (other parsing techniques)
- experimentally, outperform competitors (other parser generators) by speed factors of 3–30 depending on which task is needed exactly.
These are all nice features. What's even nicer is that the authors put up their proof of concept implementation [on GitLab](https://gitlab.com/alt-lang/relational-parsing/csharp), free for public use. Let's perform a [replication](https://doi.org/10.1007/978-3-642-25231-0_2) of this study. Concretely, this means:
- read the paper/documentation
- get a basic understanding of how their algorithm works
- familiarise yourself with the code linked above
- find inconsistencies between the two and report on them (e.g., the paper advertises a C++ implementation, while the repository has C#)
- rerun the original experiment (on [elastic/elasticsearch](https://github.com/elastic/elasticsearch))
- rerun the experiment on a larger data set (Elastic Search has ~9k Java files, it is easy to get much, much more by grabbing [Qualitas Corpus](http://qualitascorpus.com/) or just the [Top 50 Repositories](https://medium.com/issuehunt/50-top-java-projects-on-github-adbfe9f67dbc), or even literally crawling the entire GitHub with GHTorrent or [GitHub REST API](https://docs.github.com/en/free-pro-team@latest/rest));
- propose optimisations or list ideas on optimisations based on the findings.
The code is relatively fresh and seems operational (compiles and runs on [.NET Core](https://dotnet.microsoft.com/download/dotnet-core) on a Mac laptop, both in Rider and Visual Studio). If you don't know [C#](http://docs.microsoft.com/en-us/dotnet/csharp/), that's not a problem: it looks and reads like Java, just designed better.
