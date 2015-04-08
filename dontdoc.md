Three reasons why code documentation is a bad idea
==================================================

1. Maintainability
2. Trust
3. Responsibility

# Maintainability

With docs, you need to maintain both the code and the documentation == more expensive maintenance == lower maintainability.

# Trust

You can't trust the doc.

- if you misunderstand the doc then you have to read the code anyway
- the person who wrote it maybee didn't understand the code fully
- or he maybe simply expressed himself in a unfortunate way
- or he maybe didn't explain why the code does what it does, but only how it does it

# Responsibility

Docs doesn't force us to write readable code. Everything that isn't understandable and simple can be excused with *"the docs explains it"*. People therefore think that it's somehow okey to write complex/incomprehensible code.

The argument that *"docs makes it easier to understand the code"* is fundamentally flawed. If the code is hard to read, then maybe you should fix the code itself?

# Summary

Eliminate the need of documentation by writing code that is intuitive to understand. Easier said than done, you say? Well writing documentation certainly isn't a viable solution in my experience.

