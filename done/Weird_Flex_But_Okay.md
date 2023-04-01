# Weird Flex But Okay

It is a known problem in software analytics that a single commit in a repository actually can cover multiple issues (e.g., fix a bug and rename some related methods). To untangle such commits into separate concerns, in 2020 several British scientists have developed a technique called [Delta Name Flow Graph](https://dl.acm.org/doi/10.1145/3368089.3409693) (𝛿-NFG for short) and implemented it in a tool called [Flexeme](https://dl.acm.org/do/10.5281/zenodo.3894559/full/), freely available as open source. Their tool is written in Python and works on C# code — and this project is about doing the same for another language like Java.

The project was done by **Cato de Kruif** aka [**@catoostrophe**](https://github.com/catoostrophe):
- Title: _[Using 𝛿-NFGs to Identify and Eliminate Dead Code in C# Programs](http://purl.utwente.nl/essays/91890)_
- Presented at [37th Twente Student Conference on IT](https://sites.google.com/utwente.nl/37th-twente-student-conference/) on 8 July 2023
- Code: https://github.com/catoostrophe/Flexeme
- Paper: https://drive.google.com/file/d/1dyPxjbfCZkfhCd5zxiW5fb_qdc2Q7lof/view
