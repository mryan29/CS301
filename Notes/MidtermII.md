# Midterm II Review
November 9th, 2018

Not cumulative, post-midterm on (exception may be definitions)

cfl only thru last fridays lecture

## Topics
1. Context-Free Languages
  - ggenerating cfg
  - creating pda
  - converting cfl to pda
  - cnf
  - non context free proofs
  - (non) determinism
2. Turing Machines
- state diagrams
- implementation-level descriptions
- robustness
  - given a change, how does this affect expressability
  - if we change some hardware, 2 tapes, L,R,S
- turing-decidability
  - halts
- reductions
  - given that a is decidable, 
  - empty dfa problem = acceptance dfa problem ...
- halting problem
  - recognizable (v. decidable)
  - don't need to do reductions to halting, will be to decidable
3. General
- proofs
  - regular languages
- closure
- definitions (including from first midterm)

## On appendix
- every language shown decidable
- cf pumping lemma
- discrete math info - no primes
- cnf ordering
- operations we have shown to be closed or not

## Format
1. 10 MC
2. 4 short answer
3. not creating a cfg. possibly: create pda, determine what language pda or cfg accepts, chomsky normal form (likely)
4. not reduction to a decidable language. possibly: determining what language a TM accepts (Halt, state diagram), implementation-level TM (HW4 Q2), TM state diagram
5. choice of two
  - one will be non-context free proof
  - other will be some other proof
  - options: closure, ~~decidability (implementation, reduction)~~, robustness, equivalence

## PDAS
- clearly define stack alphabet
- end of stack char $
- build from cfg
- non-determinism
- using stack as counter and using special chars

## Turing Machines
- marking the input string
- make sure machine must halt
- consider edge cases
- define tape alphabet clearly
- non-determinism
- DTM = NDIM
- TM = Q...


# Study Content
Finite < Regular (DFA) < Context-Free (PDA) < Turing-Decidable (TM)


## Context-Free Languages
  - ggenerating cfg
  - creating pda
  - converting cfl to pda
  - cnf
  - non context free proofs
  - (non) determinism
 
 defining binary palindromes
 
 base case: ε - empty string palindrome
 
 ### Context-Free Grammars
 rules R, terminals Σ, non-terminals (variables) V, start variable S∈V
 
 
 ## CNF
 
 
 parse trees: there are two for the same language
 
 **ambiguous**: there are 2 parse trees for the same string
 
 __**Is there an equivalent CFG for each regular language? <<<???????**__
 
 Many possible approaches:
 1. DFA/NFA
 2. Regex
 
 #### DFA &rarr; CFG
 - Let each state have its own rule and let start state be the start symbol
 - for each transition  δ(q</sub>i</sub>,y) in the DFA, add a rule q<sub>i</sub> &rarr; yq<sub>i</sub>
 - if multiple rules for each symbol, combine into union
 - for each q<sub>f</sub> in F, add the rule q<sub>f</sub> &rarr; ε
 
 #### Regex &rarr; CFG
use structural induction:
- show CFG for base cases ('a',∅,ε)
- Show that if you have two CFG R and S, we can perform the three operations:
  - union: C &rarr; R | S
  - concatenation: C &rarr; RS
  - kleene star: C &rarr; RC | ε
  
  We can generate CFGs from regular languages and their automata
  
  **REGULAR  ⊆ CONTEXT-FREE** (but CF != Regular)
  
  #### Right linear
  If all rules follow one of the two following forms:
  1. X &rarr;zY
  2. X &rarr; w
  
  where X,Y ∈ V (and can be the same) and w,z ∈ Σ
  
  **if a grammar is left/right linear, then it is a regular grammar**
  
  we can restrict grammar to mimic constraints of dfa
  
  A string w is in th elanguage described by a CFG S if it can be produced by applying finite number of rules in S
  
  ## CFL
  **Iff a language can be described by a CFG &rarr; CFL**

  
Grammar is a **single step** iff every rule falls into one of the following forms:
1. X &rarr; zY
2. X &rarr; ε

where {X,Y} ∈ V (and can be the same) and z ∈ Σ ∪ {ε}

**If a grammar is regular &rarr; it can be converted to a right-linear single step and it can be converted to an NFA**
**However, even if the grammar is not regular, it can still produce a regular language**

A grammar is **context-free** if it falls into the following form:
X &rarr; z 

where X ∈ V and z ∈ (V ∪ Σ)*

left side must always be a single non-terminal symbol

### Producing CFG
- break into pieces
- find regular segments
- identify balanced pairs, middle pts
- how strings are produced

### parse trees
- root = start symbol
- recursively follow productions/rules
- all leaves = terminals
- if multiple trees can exist: ambiguous


Regular languages:
(aaa)*

## CNF
A CFG G is in CNF if all rules in G are in one of the following forms:
1. S &rarr; ε
2. A &rarr; BC
3. A &rarr; a
where S is the start symbol, ABC are nonterminals, a is a terminal, and B,C != S

**all CFGs can be represented in CNF**


 
 


