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

# September 14th - Regular Expressions
NFA vs DFA midterm question (convert nfa to dfa_
there are some things that are easier in dfas than nfas (intersect)

## Review 
Regular languages
- decided by dfa
- equal computation power as nfa
- can convert from nfa to dfa
- closed over
  - union, intersection, set difference, complement --> dfa
  - concatenation, repetition, kleen star, reverse --> nfa

## today
DFA Minimization <-- midterm stuff
- when we procedurally produce dfas, whether from nfas or by combining multiple dfas together, duplicated states can be produced

regular expresions

## DFA minimizaiton
what language does this dfa accept? &sigma; = {0,1}
A. if we have 3 1's, it goes into a sink state which is not acceptable --> not it
B. only rsn we're hesitant, is because 1111 does have one 1, we want "exactly" one 1
C. If we do 01, thats an odd number of zeros --> not it
D. If we do 001, its accepted --> not it

Why minimize at all?
- minimization reduces computational need, helps us understand what machine is actually doing
...

How do we know if a given DFA is minimal? (is there an equivalent dfa with fewer states?)
- search for states to combine
  - which can we combine? final and non-final
  
  real classic exam problem: description of language, produce the nfa, convert to dfa, minimize dfa
  - how to describe language?
  
  ## Regular expressions
  Give the regular express for language of binary strings tht can be broken into two, the first has an odd number of ones and the second has an odd number of 0's
  
  
