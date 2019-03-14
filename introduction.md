# Crowbar 
- Crowbar is a library for testing code, combining QuickCheck-style property based testing and has magical big-finding powers.
- Based on using combinators. Combinatory logic is a notion to eliminate the need of quantified variables in mathematical logic.

## QuickCheck
- In QuickCheck the programmer writes assertions about the logical properties that a function should fulfill. Then QuickCheck attempts to generate test case that falsifies. Once the test case is found, QuickCheck tries to reduce it to minimal subset
by removing or simplifying the input data that doesnot make the test case fail. 
- QuickCheck not only help us in testing our regular program but also help us in specifyinf what a function must be doing.
- It can be also used for checking ompiler implementations.
- We can write tests as properties that must hold universally rather than just in specific instances.

## A simple example
- We need to decide which property we want to check.
- We need to also decide on the input we would like Crowbar to work on and vary.
- When we have these we invoke something like "Crowbar.check" 

```ocaml
let identity x = Crowbar.check_eq x x
```
## Crowbar tests:
- Has two modes
 - a simple quickcheck-like mode for testing propositions against totally random input.
 - a mode using afl to get good performance.
