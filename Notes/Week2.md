Missed class Wed, and Last Fri

# Sep 7th - Automata

# Review
**Automata**
- machines which decide languages
- some input
- internal memory

**Finite state machine (DFA)**
- reads input one char at a time, left to right
- only memory is current state of machine

## DFA
- DFA is 5 tuple consisting of following elements...
  - Q: states
  - Summation (alphabet)
  - Sigma
  - q0: start state
  - F: final states
- Type for each of these:
- Transition function: every (state, character) pair maps to exactly one state

- what is the alphabet? M = ab (can verify by looking at any state and what edges come out of it)
- what is F? (What are the final states?) the set {q1,q4}
- every sequence of states is one longer than the string...
- arrow indicates start state
- double circles indicates final states
- what is the formal def of this DFA? ...

## Problem
Consider DFA for vending machine tht accepts nickels, dimes, quarters, doesnt give change and items only cost .25.

Language that reps this problem:
- input: Nickel Dime Quarter
- output: since we expect output to be .25, we don't expect nickel dime to be in the language (has to exceed or be equal to .25)
- number of states: start state with value 0
  - possible states: 5, 10, 25 (final state)
  - transitions: nickel, dime, quarter
- What is |sigma|?
  - 15
  - **18**
  - 21
  - 24

= size of |Q| |Summation|

|Summation| = 3, |Q| = 6
|Summation| = {N, D, Q}
|Q| = {0,5,10,15,20,25+}
6 states we need to keep track of and 3 possible transitions for all of them

Sigma: Q*Summation --> Q

# Languages
What sorts of languages can we decide with a DFA?
- regular (can be decided by a DFA)

Which of the following CANT be decided by a DFA?
- binary strings w equal numbers of 10s and 01s
- **decimal strings w equal numbers of 10s and 01s** 
- binary strings that start w 100 and end in 001
- decimal strings that dont contain 456

How to prove a language is regular:
- provide the DFA

How to prove a language is irregular:
- upsidedownA <sub>DFA</sub> (M Cannot solve L)

What sorts of languages are regular:
- finite languages -> yes
  - i.e. L = {0,01,010} --> E={0,1}
- null? -> yes



