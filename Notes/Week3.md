# Sep. 10th - DFA/NFA

# Review
Regular languages
- any language that can be decided by DFA
- can be infinite in size
- constructed from set and string ops

Closure 
- an operation is closed over a set if the input and output are from the same set
- if we can show the ops are closed over the regular language, we can build languages from these operations without having to prove that they're regular

## Review Q
What language does the following DFA Accept?
- **b.**
because it's a binary string, it must start with a 0
...

# Closure
Suppose A and B are regular languages. Prove A U B is regular.
By Def exist DFA Ma, Mb which recognize it, which means it have those 5 MFA properties which define it.
...

# Sep 12th - N-Regular Languages
Any language that can be decided by an NFA

## Review
Closure
- union intersection and set difference are closed over the regular languages
- still missing concatenation, kleene star and repetition

Nondeterministic finite automata
- relaxed transition constraints of DFAs
- multiple paths each string can follow
- easier construction

Which strings are not accepted by this NFA? ...
a and c

> Fave EC question is "prove this property is true" when it isn't true

What language does this accept? ...
- must end in ab or c (true) --> no, because would accept abcab 
- *none of the above* 

## NFA v DFA
How would we show that concatenation is closed over the n-regular languages?

..



