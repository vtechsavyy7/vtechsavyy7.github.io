## Random Experiment

A random experiment is an experiment in which the outcome varies in an unpredictable manner whenever it is repeated under the same conditions.

It is specified by: 
- An experimental procedure that can be repeated,
- A set of one or more possible outcomes

Examples of random experiments are: 
- 


## Samples - L1

An outcome or sample point of an experiment is a result that cannot be decomposed into simpler components. 
For example, in a coin toss, the outcome can be either heads or tails. In a dice roll, the outcome can be any of the numbers 1 through 6.

The set of all possible outcomes of a random experiment is called the *Sample Space*. It is usually denoted by the symbol S.

A sample space can either be finite, countably infinite, or uncountably infinite.

## Events - L2

An event is defined as a subset of the sample space. 
It is a collection of one or more outcomes of a random experiment. 
For example, in a dice roll, the event "rolling an even number" consists of the outcomes {2, 4, 6}.

TODO: Certain event and null event.

## Event classes - L3
 An event class is a collection of events that share certain properties or characteristics. Essentially, it is a "set of sets"! 
 Q: What are the events to which a probability can be assigned and satisfy the axioms of probability?
 A: The events to which a probability can be assigned and satisfy the axioms of probability are called *measurable events*. These events form a σ-algebra (sigma-algebra) over the sample space, which is a collection of subsets of the sample space that includes the sample space itself, is closed under complementation, and is closed under countable unions.
 Todo: 
  - Need to understand more about σ-algebra and measurable events.
  - Need to understand the Banach-Tarski paradox and how it motivates the study of measure theory.

## Axioms of Probability: 

Given a sample space S and a σ-algebra of events F, a probability measure P is a function that assigns a probability to each event in F, satisfying the following axioms:

Axiom #1: Non-negativity: For any event A, the probability of A is greater than or equal to 0. P(A) ≥ 0.

Axiom #2: Normalization: The probability of the sample space S is 1. P(S) = 1.

Axiom #3: Additivity: For any countable sequence of mutually exclusive events A1, A2, A3, ..., the probability of their union is equal to the sum of their individual probabilities. P(A1 ∪ A2 ∪ A3 ∪ ...) = P(A1) + P(A2) + P(A3) + ...

## Conditional Probability