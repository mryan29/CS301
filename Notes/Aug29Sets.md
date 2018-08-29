# Aug 29th - Sets

# Review
Languages and Automata

- Decision Problems
  - Functions that return t or f
- Models of computation
  - Depending on the computational power of the automata, some languages are computable and some aren't
- Classifying "computability"
  - Classify different types of languages/decision problems by how easy they are to compute

Theory needs proofs to make claims
- Formalization of a language
- Review from discrete
- Course building blocks

# Sets
**Unordered** collection of objects

Can be **heterogeneous** or contain other sets
- contain different types of objects

Should not include duplicates but can

I.e.
- A = {1,2,3}
- B = {'a','b','c'}
- C = {{1,2},3,4}

Objects are called **elements** or **members**

Most important operation: membership

&nbsp;&nbsp; 2 ⋲ C ? = "Is 2 in C"

## Notation
- **Roster Notation**: enumeration of elements
&nbsp;&nbsp; D = {1,3,4,7,9}
- **Set Builder Notation**: Describes properties of set elements
&nbsp;&nbsp; E = { x | x ⋲ D and x is divisible by 3 }

Roster notation for E: E = {3,9}

Set builder notation for D: D = { 2x + 1 | x ⋲ N and 0 <= x <= 4 }

## Subset
A set A is considered a **subset** of B (A ⊆ B) if Each element that exists in A exists in B

A set A is considered a **proper subset** of B (A ⊂ B) if
- each element that exists in A exists in B AND
- there exists an element B that doesn't exist in A

A, B are considered equal if A ⊆ B and B ⊆ A

Does this hold if A ⊂ B and B ⊂ A?

&nbsp;&nbsp; No, two sets can't be proper subsets of eachother

## Equality
D = { 1, 4, 9, 16}

E = {1, 9, 4, 9, 16}

D = E?

&nbsp;&nbsp; No, because for this class N includes 0

&nbsp;&nbsp; Although normally, yes, they are equal

&nbsp;&nbsp; Sets don't account for duplicates. They either exist in the set or they don't

Formalism: ∀x (x ⋲ D &rarr; x ⋲ E)

## Formalism
Formal definition of subset: ∀x (x ⋲ D &rarr; x ⋲ E)

Formal definition of proper subset: ∀x (x ⋲ D &rarr; x ⋲ E) and ∃y (y ⋲ D ^ y ∌ E)

Why not: ∃x (x ⋲ D &rarr; x ∌ E)? <-- theres some error on the slides/notes here

&nbsp;&nbsp; This states D and E are **disjoint** (intersection is empty, share no elements)

## Cardinality
Cardinality of a set is its size
- For finite sets: number of elements in it
- cardinality of set A is | A |
- cardinality of empty set {} or ∅ is 0

Let A = {1,1,{1}}, B = {{1,2,3}} and C = {∅}

|A|=2, |B|=1, |C|=1

## Power set
Power set of set S denoted P(S) is a set containing all subsets of S
- P(S) = {s | s ⊆ S}

What is the power set of {A,B,C}?

&nbsp;&nbsp; {{∅},{A},{B},{C},{A,B},{A,C},{B,C},{A,B,C}}

For finite set S, what is |P(S)|?

&nbsp;&nbsp; 2 ^ |S|

&nbsp;&nbsp; For each element in S, it is in half of the subsets

⊂⊆⋲∅∌∀∃∨
