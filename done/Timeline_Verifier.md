# Timeline Verifier

The movie industry has script supervisors, continuity supervisors and similar jobs — and had them for quite a while already. These are people who make sure that if it is shown on screen that a character chugs a drink and throws away the bottle, then in the subsequent scenes the bottle will not be on the table, even if those scenes were filmed earlier. They also make sure that all characters wear the same outfits when they depart from A to B as when they arrive at B, even though the actual filming happened months apart and took place in different countries. Similar occupations or at least similar tasks are performed routinely in other areas, such as game design or world building. Writers, quest designers, comic artists and whatnot — all of them want their fans to engage in long and deep discussions about the minute details of their settings with pleasure, and for that to happen, those details must make sense and be consistent.

This project is about automating a part of this process, namely developing a format for expressing timelines and placing characters on them, together with predicates that bind them in some sort of relationships ("is a teacher of", "is friends with", "has met", "is killed by"), and writing a small piece of software that verifies that that timeline is, indeed, consistent: if someone is a teacher, they are old enough and alive enough to function in that capacity; if two characters have met, their lifetimes should overlap, and if someone is killed on a particular year, they should not meet or teach others, unless they become a ghost.

If this turns out to be too easy (we never know, it's a research project after all!), some extra challenge can be provided by designing and implementing an algorithm for generating consistent timelines.

The project was done by **Aron Davids** aka [**@ArcaneLean**](https://github.com/ArcaneLean):
- Title: _[Identifying Plot Holes in Narrative Stories by Simulating Events](http://purl.utwente.nl/essays/91967)_
- Presented at [37th Twente Student Conference on IT](https://sites.google.com/utwente.nl/37th-twente-student-conference/) on 8 July 2023
- Paper: https://drive.google.com/file/d/1bvpkzsJgs-AVBQ82jlYXC9rRdYfHcxwC/view
